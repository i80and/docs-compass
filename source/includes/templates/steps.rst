.. register-template:: steps
   :yaml:

   {{ for step in steps }}
   .. only:: not (html or dirhtml or singlehtml)

      Step {{ i inc }}: {{ step.title }}
      {{ step.heading }}

      {{step.body}}

   .. only:: html or dirhtml or singlehtml

      .. raw:: html

         <div class="sequence-block">
           <div class="bullet-block">
             <div class="sequence-step">{{ i inc }}</div></div>

      {{step.title}}
      {{step.heading}}

      {{step.body}}

      .. raw:: html

         </div>
   {{ end }}
