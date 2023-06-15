---
title: Policy Management
description: .
ms.date: 06/14/2023
ms.topic: overview
ms.localizationpriority: medium
---

# Policy Management

The following Windows Package Manager policies are configurable on a Windows device using Group Policy, CSPs or through updating the associated registry keys.

| Policy Name                                                               | Description                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable App Installer                                                      | This policy controls whether the Windows Package Manager can be used by users.                                                                                                                                         |
| Enable App Installer Settings                                             | This policy controls whether users can change their settings.                                                                                                                                                          |
| Enable App Installer Experimental Features                                | This policy controls whether users can enable experimental features in the Windows Package Manager.                                                                                                                    |
| Enable App Installer Local Manifest Files                                 | This policy controls whether users can install packages with local manifest files.                                                                                                                                     |
| Enable App Installer Microsoft Store Source Certificate Validation Bypass | This policy controls whether the Windows Package Manager will validate the Microsoft Store certificate hash matches to a known Microsoft Store certificate when initiating a connection to the Microsoft Store Source. |
| Enable App Installer Hash Override                                        | This policy controls whether or not the Windows Package Manager can be configured to enable the ability override the SHA256 security validation in settings.                                                           |
| Enable App Installer Local Archive Malware Scan Override                  | This policy controls the ability to override malware vulnerability scans when installing an archive file using a local manifest using the command line arguments.                                                      |
| Enable App Installer Default Source                                       | This policy controls the default source included with the Windows Package Manager.                                                                                                                                     |
| Enable App Installer Microsoft Store Source                               | This policy controls the Microsoft Store source included with the Windows Package Manager.                                                                                                                             |
| Set App Installer Source Auto Update Interval in Minutes                  | This policy controls the auto update interval for package-based sources.                                                                                                                                               |
| Enable App Installer Additional Sources                                   | This policy controls additional sources provided by the enterprise IT administrator.                                                                                                                                   |
| Enable App Installer Allowed Sources                                      | This policy controls additional sources allowed by the enterprise IT administrator.                                                                                                                                    |
| Enable App Installer ms-appinstaller Protocol                             | This policy controls whether users can install packages from a website that is using the ms-appinstaller protocol.                                                                                                     |


## Enable App Installer
This policy controls whether the Windows Package Manager can be used by users. If you enable or do not configure this setting, users will be able to use the Windows Package Manager. If you disable this setting, users will not be able to use the Windows Package Manager.

| Registry Key                                     | Registry Value     | Enabled     | Disabled    |
|--------------------------------------------------|--------------------|-------------|-------------|
| Software\Policies\Microsoft\Windows\AppInstaller | EnableAppInstaller | Decimal (1) | Decimal (0) |


## Enable App Installer Settings
This policy controls whether users can change their settings. If you enable or do not configure this setting, users will be able to change settings for the Windows Package Manager. If you disable this setting, users will not be able to change settings for the Windows Package Manager.

| Registry Key                                     | Registry Value | Enabled     | Disabled    |
|--------------------------------------------------|----------------|-------------|-------------|
| Software\Policies\Microsoft\Windows\AppInstaller | EnableSettings | Decimal (1) | Decimal (0) |

## Enable App Installer Experimental Features
This policy controls whether users can enable experimental features in the Windows Package Manager. If you enable or do not configure this setting, users will be able to enable experimental features for the Windows Package Manager. If you disable this setting, users will not be able to enable experimental features for the Windows Package Manager.

| Registry Key                                     | Registry Value             | Enabled     | Disabled    |
|--------------------------------------------------|----------------------------|-------------|-------------|
| Software\Policies\Microsoft\Windows\AppInstaller | EnableExperimentalFeatures | Decimal (1) | Decimal (0) |

## Enable App Installer Local Manifest Files
This policy controls whether users can install packages with local manifest files. If you enable or do not configure this setting, users will be able to install packages with local manifests using the Windows Package Manager. If you disable this setting, users will not be able to install packages with local manifests using the Windows Package Manager.

| Registry Key                                     | Registry Value           | Enabled     | Disabled    |
|--------------------------------------------------|--------------------------|-------------|-------------|
| Software\Policies\Microsoft\Windows\AppInstaller | EnableLocalManifestFiles | Decimal (1) | Decimal (0) |

## Enable App Installer Microsoft Store Source Certificate Validation Bypass
This policy controls whether the Windows Package Manager will validate the Microsoft Store certificate hash matches to a known Microsoft Store certificate when initiating a connection to the Microsoft Store Source. If you enable this policy, the Windows Package Manager will bypass the Microsoft Store certificate validation. If you disable this policy, the Windows Package Manager will validate the Microsoft Store certificate used is valid and belongs to the Microsoft Store before communicating with the Microsoft Store source. If you do not configure this policy, the Windows Package Manager administrator settings will be adhered to.

| Registry Key                                     | Registry Value                                  | Enabled     | Disabled    |
|--------------------------------------------------|-------------------------------------------------|-------------|-------------|
| Software\Policies\Microsoft\Windows\AppInstaller | EnableBypassCertificatePinningForMicrosoftStore | Decimal (1) | Decimal (0) |

## Enable App Installer Hash Override
This policy controls whether or not the Windows Package Manager can be configured to enable the ability override the SHA256 security validation in settings. If you enable or do not configure this policy, users will be able to enable the ability override the SHA256 security validation in the Windows Package Manager settings. If you disable this policy, users will not be able to enable the ability override the SHA256 security validation in the Windows Package Manager settings.

| Registry Key                                     | Registry Value     | Enabled     | Disabled    |
|--------------------------------------------------|--------------------|-------------|-------------|
| Software\Policies\Microsoft\Windows\AppInstaller | EnableHashOverride | Decimal (1) | Decimal (0) |

## Enable App Installer Local Archive Malware Scan Override
This policy controls the ability to override malware vulnerability scans when installing an archive file using a local manifest using the command line arguments. If you enable this policy, users can override the malware scan when performing a local manifest install of an archive file. If you disable this policy, users will be unable to override the malware scan of an archive file when installing using a local manifest. If you do not configure this policy, the Windows Package Manager administrator settings will be adhered to.

| Registry Key                                     | Registry Value                        | Enabled     | Disabled    |
|--------------------------------------------------|---------------------------------------|-------------|-------------|
| Software\Policies\Microsoft\Windows\AppInstaller | EnableLocalArchiveMalwareScanOverride | Decimal (1) | Decimal (0) |

## Enable App Installer Default Source
This policy controls the default source included with the Windows Package Manager. If you do not configure this setting, the default source for the Windows Package Manager will be available and can be removed. If you enable this setting, the default source for the Windows Package Manager will be available and cannot be removed. If you disable this setting the default source for the Windows Package Manager will not be available.

| Registry Key                                     | Registry Value      | Enabled     | Disabled    |
|--------------------------------------------------|---------------------|-------------|-------------|
| Software\Policies\Microsoft\Windows\AppInstaller | EnableDefaultSource | Decimal (1) | Decimal (0) |

## Enable App Installer Microsoft Store Source
This policy controls the Microsoft Store source included with the Windows Package Manager. If you do not configure this setting, the Microsoft Store source for the Windows Package manager will be available and can be removed. If you enable this setting, the Microsoft Store source for the Windows Package Manager will be available and cannot be removed. If you disable this setting the Microsoft Store source for the Windows Package Manager will not be available.

| Registry Key                                     | Registry Value             | Enabled     | Disabled    |
|--------------------------------------------------|----------------------------|-------------|-------------|
| Software\Policies\Microsoft\Windows\AppInstaller | EnableMicrosoftStoreSource | Decimal (1) | Decimal (0) |

## Set App Installer Source Auto Update Interval in Minutes
This policy controls the auto update interval for package-based sources. If you disable or do not configure this setting, the default interval or the value specified in settings will be used by the Windows Package Manager. If you enable this setting, the number of minutes specified will be used by the Windows Package Manager.

| Registry Key                                     | Registry Value           | Max Value       |
|--------------------------------------------------|--------------------------|-----------------|
| Software\Policies\Microsoft\Windows\AppInstaller | SourceAutoUpdateInterval | Decimal (43200) |

## Enable App Installer Additional Sources
This policy controls additional sources provided by the enterprise IT administrator. If you do not configure this policy, no additional sources will be configured for the Windows Package Manager. If you enable this policy, the additional sources will be added to the Windows Package Manager and cannot be removed. The representation for each additional source can be obtained from installed sources using 'winget source export'. If you disable this policy, no additional sources can be configured for the Windows Package Manager.

| Registry Key                                                       | Registry Value                     | Enabled     | Disabled       |
|--------------------------------------------------------------------|------------------------------------|-------------|----------------|
| Software\Policies\Microsoft\Windows\AppInstaller                   | EnableAdditionalSources            | Decimal (1) | Decimal (0)    |
| Software\Policies\Microsoft\Windows\AppInstaller\AdditionalSources | Incremental counter (1, 2, 3, ...) | String (Source URL)     | String ($null) |

## Enable App Installer Allowed Sources
This policy controls additional sources allowed by the enterprise IT administrator. If you do not configure this policy, users will be able to add or remove additional sources other than those configured by policy. If you enable this policy, only the sources specified can be added or removed from the Windows Package Manager. The representation for each allowed source can be obtained from installed sources using 'winget source export'. If you disable this policy, no additional sources can be configured for the Windows Package Manager.

| Registry Key                                                    | Registry Value                     | Enabled             | Disabled       |
|-----------------------------------------------------------------|------------------------------------|---------------------|----------------|
| Software\Policies\Microsoft\Windows\AppInstaller                | EnableAllowedSources               | Decimal (1)         | Decimal (0)    |
| Software\Policies\Microsoft\Windows\AppInstaller\AllowedSources | Incremental counter (1, 2, 3, ...) | String (Source URL) | String ($null) |

## Enable App Installer ms-appinstaller Protocol
This policy controls whether users can install packages from a website that is using the ms-appinstaller protocol. If you enable this setting, users will be able to install packages from websites that use this protocol. If you disable or do not configure this setting, users will not be able to install packages from websites that use this protocol.

| Registry Key                                     | Registry Value               | Enabled     | Disabled    |
|--------------------------------------------------|------------------------------|-------------|-------------|
| Software\Policies\Microsoft\Windows\AppInstaller | EnableMSAppInstallerProtocol | Decimal (1) | Decimal (0) |
