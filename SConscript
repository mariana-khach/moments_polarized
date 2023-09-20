
import os
import sbms

# get env object and clone it
Import('*')

# Verify AMPTOOLS environment variable is set
if os.getenv('AMPTOOLS', 'nada')!='nada' and os.getenv('AMPPLOTTER', 'nada')!='nada':

   env = env.Clone()

   AMPTOOLS_LIBS = "AMPTOOLS_AMPS AMPTOOLS_DATAIO AMPTOOLS_MCGEN"
   env.AppendUnique(LIBS = AMPTOOLS_LIBS.split())

   sbms.AddHDDM(env)
   sbms.AddAmpTools(env)
   sbms.AddAmpPlotter(env)
   sbms.AddROOT(env)
   ROOT_LIBS = "MathMore"
   env.AppendUnique(LIBS = ROOT_LIBS.split())

   sbms.executable(env)
