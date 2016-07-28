use_frameworks!

abstract_target 'CocoaPods' do
  pod 'RSTWebViewController', :git => 'https://github.com/rileytestut/RSTWebViewController-Legacy.git'
  pod "AFNetworking", "~> 2.4"
  pod "PSPDFTextView", :git => 'https://github.com/steipete/PSPDFTextView.git'
  pod "Dropbox-iOS-SDK", "~> 1.3.0"
  pod "Crashlytics"
  
  target 'GBA4iOS' do
  end
end

post_install do |installer|
  puts "Add embed swift standard libraries option to targets"
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['ALWAYS_EMBED_SWIFT_STANDARD_LIBRARIES'] = 'NO'
    end
  end
end