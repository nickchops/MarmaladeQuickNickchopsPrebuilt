
This project is example files showin ghow you would include all of the
extensions in my github. It includes:

- MarmaladeQuickNickchopsPrebuilt.mkf - This shows what you would put in
  <sdk>/quick/quickuser.mkf in order to build all C++ code from wrappers into
  the Quick binaries. You can include it there to pull them all in. These
  put lightweight C++ code into the binaries to expose APIs. It's sensible
  to build *all* wrappers you have in here as it adds little bloat to
  binaries or your final packages.
  
- quickuser_tolua.pkg - This shows what you would put in
  <sdk>/quick/quickuser_tolua.pkg to make the binaries provide Lua APIs
  for the C++ stuff included above. Again, this adds minimal size to binaries
  so just include all the ones you have.
  
- DeployIncludes.mkf - This shows what you would put in your app project
  so that you can actually use wrapped extensions. This makes platform libs
  that contain most of the code and assets actually go into your project.
  You should only include the ones your project needs to avoid bloat.
  
- s3e-default.mkf - This shows an exmaple ofhow you would tell Marmalade
  where to find your extensions/wrappers. It lives in <sdk>/s3e.
  In my case I'm using C:/Users/Nick/projects which is where all my
  git stuff lives.
