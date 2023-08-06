source 'https://github.com/CocoaPods/Specs.git'

platform :ios, '14.0'

use_frameworks!

inhibit_all_warnings!

def shared_pods
  pod 'ExpoFpFplan', '4.2.4'
  pod 'ExpoFpCrowdConnected', '4.2.4'
  pod 'ExpoFpIndoorAtlas', '4.2.4'
  pod 'ExpoFpGpsProvider', '4.2.4'
end

target 'FplanUiKit' do
  shared_pods
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '14.0'
    end
  end
end