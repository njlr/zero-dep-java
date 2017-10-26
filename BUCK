java_library(
  name = 'hello',
  srcs = [
    'Program.java',
  ],
)

java_binary(
  name = 'hello-app',
  main_class = 'Program',
  deps = [
    ':hello',
  ],
)

genrule(
  name = 'hello-app-native',
  out = 'out',
  cmd = 'javapackager -deploy -native -outdir $OUT -outfile app -srcfiles $(location :hello-app) -appclass Program ',
)
