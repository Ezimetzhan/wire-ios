source 'https://github.com/CocoaPods/Specs.git'

def ios_pods
    pod 'GoogleAPIClient/YouTube', '1.0.4', :inhibit_warnings => true
    pod 'CocoaSecurity', '1.2.4', :inhibit_warnings => true

    pod 'Localytics', '4.0.0', :inhibit_warnings => true
    pod 'NSObject-ObjectMap', :git => 'https://github.com/wireapp/NSObject-ObjectMap', :tag => 'v2.3.1'
    pod 'AFNetworking', :git => 'https://github.com/wireapp/AFNetworking', :tag => '2.6.3'
    pod 'PureLayout', :git => 'https://github.com/wireapp/PureLayout', :tag => 'v3.0.0'
    pod 'VIMNetworking', :git => 'https://github.com/wireapp/VIMNetworking', :tag => '6.0.0'
    pod 'RBBAnimation', :git => 'https://github.com/wireapp/RBBAnimation', :commit => '7dd8d9a3cf610be5f7c1e4459692d555d70704c7'
    pod 'ARCollectionViewMasonryLayout', :git => 'https://github.com/wireapp/ARCollectionViewMasonryLayout', :tag => '2.3.0'
    pod 'SCSiriWaveformView', :git => 'https://github.com/wireapp/SCSiriWaveformView', :tag => 'v1.0.3'
    pod 'FLAnimatedImage', :git => 'https://github.com/wireapp/FLAnimatedImage', :tag => '1.0.12'
    pod 'MTAnimation', :git => 'https://github.com/wireapp/MTAnimation', :tag => '1.2.2-wire'
end

target 'Wire-iOS' do

    platform :ios, '8.0'

    ios_pods

    post_install do |installer_representation|
		installer_representation.pods_project.targets.each do |target|
            target.build_configurations.each do |config|
                config.build_settings['APPLICATION_EXTENSION_API_ONLY'] = 'NO'
            end
	    end
    end
end

target 'WireExtensionComponents' do

    platform :ios, '8.0'
    pod 'PureLayout', :git => 'https://github.com/wireapp/PureLayout', :tag => 'v3.0.0'
end

target 'Wire-iOS-Tests' do
    platform :ios, '8.0'

    ios_pods
end
