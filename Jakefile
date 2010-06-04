PROJECT_DIR = File.expand_path(File.dirname(__FILE__))
LIB_DIR     = File.join(PROJECT_DIR, 'test/lib')

jake_helper :license do
  File.read('LICENSE')
end

jake_hook :build_complete do |build|
  FileUtils.rm_rf(LIB_DIR) if File.exists?(LIB_DIR)
  FileUtils.cp_r(build.build_directory, LIB_DIR)
end
