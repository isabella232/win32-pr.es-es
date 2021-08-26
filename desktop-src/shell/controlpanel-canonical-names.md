---
description: A Windows Vista, Panel de control elementos incluidos con Windows reciben un nombre canónico que se puede usar en una llamada API o una instrucción de línea de comandos para iniciar ese elemento mediante programación.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Nombres canónicos de Panel de control elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebf831bfb1cb86c41a8f97c2bfa041dad836e4b77f8fd233cb94d4a3951c38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943475"
---
# <a name="canonical-names-of-control-panel-items"></a>Nombres canónicos de Panel de control elementos

A Windows Vista, Panel de control elementos incluidos con Windows reciben un nombre canónico que se puede usar en una llamada [API](executing-control-panel-items.md) o una instrucción de línea de comandos para iniciar ese elemento mediante programación. A partir Windows 7 y Windows Server 2008 R2, los nombres canónicos se pueden usar en una directiva de grupo para ocultar elementos Panel de control específicos. En este tema se proporcionan detalles para cada elemento Panel de control: nombre canónico, GUID, nombre del módulo y las versiones del sistema operativo que reconocen el nombre canónico.

> [!Note]  
> Los nombres canónicos Panel de control los elementos no se admiten antes de Windows Vista.

 

-   [Panel de control canónicos](#control-panel-canonical-names)
-   [Nombres canónicos Panel de control en desuso](#deprecated-control-panel-canonical-names)
-   [Uso de nombres canónicos en directiva de grupo](#using-canonical-names-in-local-group-policy)
-   [Comentarios:](#remarks)

## <a name="control-panel-canonical-names"></a>Panel de control canónicos

Puntos que debe recordar al trabajar con estos valores:

-   Por definición, los nombres canónicos no cambian en función del lenguaje del sistema; siempre están en inglés, incluso si el idioma del sistema no es .
-   No todos los Panel de control están presentes en todas las variedades de Windows.
-   Algunos Panel de control solo aparecen si se detecta el hardware correcto en el sistema.
-   Los terceros también pueden agregar Panel de control elementos. Los nombres canónicos enumerados aquí son solo para Panel de control elementos que se incluyen con Windows.

Estos son los elementos Panel de control disponibles en Windows 8.1:

-   [Centro de actividades](#action-center)
-   [Herramientas administrativas](#administrative-tools)
-   [Autoplay](#autoplay)
-   [Dispositivos biométricos](#biometric-devices)
-   [Cifrado de unidad BitLocker](#bitlocker-drive-encryption)
-   [Administración del color](#color-management)
-   [Administrador de credenciales](#credential-manager)
-   [Fecha y hora](#date-and-time)
-   [Programas predeterminados](#default-programs)
-   [Administrador de dispositivos](#device-manager)
-   [Dispositivos e impresoras](#devices-and-printers)
-   [Pantalla](#display)
-   [Centro de accesibilidad](#ease-of-access-center)
-   [Protección infantil](#family-safety)
-   [Historial de archivos](#file-history)
-   [Opciones de carpeta](#folder-options)
-   [Fuentes](#fonts)
-   [Grupo Hogar](#homegroup)
-   [Opciones de indexación](#indexing-options)
-   [Infrarrojos](#infrared)
-   [Opciones de Internet](#internet-options)
-   [Iniciador iSCSI](#iscsi-initiator)
-   [Servidor iSNS](#isns-server)
-   [Teclado](#keyboard)
-   [Ubicación Configuración](#location-settings)
-   [Mouse](#mouse)
-   [MPIOConfiguration](#mpioconfiguration)
-   [Centro de redes y recursos compartidos](#network-and-sharing-center)
-   [Iconos del área de notificación](#notification-area-icons)
-   [Lápiz y táctil](#pen-and-touch)
-   [Personalización](#personalization)
-   [Teléfono y módem](#phone-and-modem)
-   [Opciones de energía](#power-options)
-   [Programas y características](#programs-and-features)
-   [Recuperación](#recovery)
-   [Región](#region)
-   [Conexión de RemoteApp y Escritorio](#remoteapp-and-desktop-connections)
-   [Sonido](#sound)
-   [Reconocimiento de voz](#speech-recognition)
-   [Espacios de almacenamiento](#storage-spaces)
-   [Centro de sincronización](#sync-center)
-   [Sistema](#system)
-   [Tablet PC Configuración](#tablet-pc-settings)
-   [Barra de tareas y navegación](#taskbar-and-navigation)
-   [Solución de problemas](#troubleshooting)
-   [TSAppInstall](#tsappinstall)
-   [Cuentas de usuario](#user-accounts)
-   [Windows Anytime Upgrade](#windows-anytime-upgrade)
-   [Windows Defender](#windows-defender)
-   [Firewall de Windows](#windows-firewall)
-   [Centro de movilidad de Windows](#windows-mobility-center)
-   [Windows To Go](#windows-to-go)
-   [Windows Update](#windows-update)
-   [Carpetas de trabajo](#work-folders)

### <a name="action-center"></a>Centro de actividades

-   **Nombre canónico:** Microsoft.ActionCenter
-   **GUID:**{BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\ActionCenterCPL.dll,-1
-   **Páginas**

    | Nombre de página           | Aperturas                      |
    |---------------------|----------------------------|
    | MaintenanceSettings | Mantenimiento automático      |
    | pageProblems        | Informes de problemas            |
    | pageReliabilityView | Monitor de confiabilidad        |
    | pageResponseArchive | Mensajes archivados          |
    | pageSettings        | Informe de problemas Configuración |

    

     

### <a name="administrative-tools"></a>Herramientas administrativas

-   **Nombre canónico:** Microsoft.AdministrativeTools
-   **GUID:**{D20EA4E1-3957-11d2-A40B-0C5020524153}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ system32 \\shell32.dll,-22982

### <a name="autoplay"></a>Reproducción automática

-   **Nombre canónico:** Microsoft.AutoPlay
-   **GUID:**{9C60DE1E-E5FC-40f4-A487-460851A8D915}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\autoplay.dll,-1

### <a name="biometric-devices"></a>Dispositivos biométricos

-   **Nombre canónico:** Microsoft.BiometricDevices
-   **GUID:**{0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\biocpl.dll,-1

### <a name="bitlocker-drive-encryption"></a>Cifrado BitLocker de unidades

-   **Nombre canónico:** Microsoft.BitLockerDriveEncryption
-   **GUID:**{D9EF8727-CAC2-4e60-809E-86F80A666C91}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\fvecpl.dll,-1

### <a name="color-management"></a>Administración del color

-   **Nombre canónico:** Microsoft.ColorManagement
-   **GUID:**{B2C761C6-29BC-4f19-9251-E6195265BAF1}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%systemroot% \\ system32 \\colorcpl.exe,-6

### <a name="credential-manager"></a>Administrador de credenciales

-   **Nombre canónico:** Microsoft.CredentialManager
-   **GUID:**{1206F5F1-0569-412C-8FEC-3204630DFB70}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ system32 \\Vault.dll,-1
-   **Páginas**

    | Nombre de página                   | Aperturas               |
    |-----------------------------|---------------------|
    | ? SelectedVault=CredmanVault | Windows Credenciales |

    

     

### <a name="date-and-time"></a>Fecha y hora

-   **Nombre canónico:** Microsoft.DateAndTime
-   **GUID:**{E2E7934B-DCE5-43C4-9576-7FE4F75E7480}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\timedate.cpl,-51
-   **Páginas**

    | Nombre de página | Aperturas             |
    |-----------|-------------------|
    | 1         | Relojes adicionales |

    

     

### <a name="default-programs"></a>Programas predeterminados

-   **Nombre canónico:** Microsoft.DefaultPrograms
-   **GUID:**{17cd9488-1228-4b2f-88ce-4298e93e0966}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\sud.dll,-1
-   **Páginas**

    | Nombre de página          | Aperturas                |
    |--------------------|----------------------|
    | pageDefaultProgram | Establecer programas predeterminados |
    | pageFileAssoc      | Establecer asociaciones     |

    

     

### <a name="device-manager"></a>Administrador de dispositivos

-   **Nombre canónico:** Microsoft.DeviceManager
-   **GUID:**{74246bfc-4c96-11d0-cef-0020af6b0b7a}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\devmgr.dll,-4

### <a name="devices-and-printers"></a>Dispositivos e impresoras

-   **Nombre canónico:** Microsoft.DevicesAndPrinters
-   **GUID:**{A8A91A66-3A7D-4424-8D24-04E180695C7A}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%systemroot% \\ system32 \\DeviceCenter.dll,-1000

### <a name="display"></a>Mostrar

-   **Nombre canónico:** Microsoft.Display
-   **GUID:**{C555438B-3C23-4769-A71F-B6D3D9B6053A}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\Display.dll,-1
-   **Páginas**

    | Nombre de página | Aperturas             |
    |-----------|-------------------|
    | Configuración  | Resolución de pantalla |

    

     

### <a name="ease-of-access-center"></a>Centro de accesibilidad

-   **Nombre canónico:** Microsoft.EaseOfAccessCenter
-   **GUID:**{D555645E-D4F8-4c29-A827-D93C859C4F2A}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\accessibilitycpl.dll,-10
-   **Páginas**

    | Nombre de página               | Aperturas                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | pageEasierToClick       | Facilitar el uso del mouse                                        |
    | pageEasierToSee         | Facilitar la visualización en el equipo                                     |
    | pageEasierWithSounds    | Uso de alternativas visuales o de texto para sonidos                          |
    | pageFilterKeysSettings  | Configuración de claves de filtro                                                  |
    | pageKeyboardEasierToUse | Facilitar el uso del teclado                                     |
    | pageNoMouseOrKeyboard   | Usar el equipo sin un mouse o teclado                        |
    | pageNoVisual            | Usar el equipo sin pantalla                                  |
    | pageQuestionsCognitive  | Obtener recomendaciones para facilitar el uso del equipo (cognitive) |
    | pageQuestionsEyesight   | Obtener recomendaciones para que el equipo sea más fácil de usar (vista)  |

    

     

### <a name="family-safety"></a>Protección infantil

-   **Nombre canónico:** Microsoft.ParentalControls
-   **GUID:**{96AE8D84-A250-4520-95A5-A47A7E3C548B}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\wpccpl.dll,-100
-   **Páginas**

    | Nombre de página   | Aperturas                                  |
    |-------------|----------------------------------------|
    | pageUserHub | Elección de un usuario y configuración de la seguridad de la familia |

    

     

### <a name="file-history"></a>Historial de archivos

-   **Nombre canónico:** Microsoft.FileHistory
-   **GUID:**{F6B6E965-E9B2-444B-9286-10C9152EDBC5}
-   **Sistema operativo compatible:** Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\fhcpl.dll,-52
-   Historial de archivos incluye una versión más reciente del elemento Copia de seguridad y restauración, pero el nombre canónico de ese elemento anterior no se reasigna a Historial de archivos.

### <a name="folder-options"></a>Opciones de carpeta

-   **Nombre canónico:** Microsoft.FolderOptions
-   **GUID:**{6DFD7C5C-2451-11d3-A299-00C04F8EF6AF}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ system32 \\shell32.dll,-22985

### <a name="fonts"></a>Fuentes

-   **Nombre canónico:** Microsoft.Fonts
-   **GUID:**{93412589-74D4-4E4E-AD0E-E0CB621440FD}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\FontExt.dll,-8007

### <a name="homegroup"></a>Grupo Hogar

-   **Nombre canónico:** Microsoft.HomeGroup
-   **GUID:**{67CA7650-96E6-4FDD-BB43-A8E774F73A57}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\hgcpl.dll,-1

### <a name="indexing-options"></a>Opciones de indización

-   **Nombre canónico:** Microsoft.IndexingOptions
-   **GUID:**{87D66A43-7B11-4A28-9811-C86EE395ACF7}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\srchadmin.dll,-601

### <a name="infrared"></a>Infrarrojos

-   **Nombre canónico:** Microsoft.Desarroba
-   **GUID:**{A0275511-0E86-4ECA-97C2-ECD8F1221D08}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\irprops.cpl,-1

### <a name="internet-options"></a>Opciones de Internet

-   **Nombre canónico:** Microsoft.InternetOptions
-   **GUID:**{A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @C: \\ Windows \\ System32 \\inetcpl.cpl,-4312
-   **Páginas**

    | Nombre de página | Aperturas       |
    |-----------|-------------|
    | 1         | Seguridad    |
    | 2         | Privacidad     |
    | 3         | Content     |
    | 4         | Conexiones |
    | 5         | Programas    |
    | 6         | Avanzado    |

    

     

### <a name="iscsi-initiator"></a>Iniciador iSCSI

-   **Nombre canónico:** Microsoft.iSCSIInitiator
-   **GUID:**{A304259D-52B8-4526-8B1A-A1D6CECC8243}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\iscsicpl.dll,-5001

### <a name="isns-server"></a>Servidor iSNS

-   **Nombre canónico:** Microsoft.iSNSServer
-   **GUID:**{0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\isnssrv.dll,-5005
-   Este Panel de control elemento solo se verá en las versiones de servidor de Windows.

### <a name="keyboard"></a>Keyboard

-   **Nombre canónico:** Microsoft.Keyboard
-   **GUID:**{725BE8F7-668E-4C7B-8F90-46BDB0936430}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\main.cpl,-102

### <a name="location-settings"></a>Ubicación Configuración

-   **Nombre canónico:** Microsoft.LocationSettings
-   **GUID:**{E9950154-C418-419e-A90A-20C5287AE24B}
-   **Sistema operativo compatible:** Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\SensorsCpl.dll,-1

### <a name="mouse"></a>Mouse

-   **Nombre canónico:** Microsoft.Mouse
-   **GUID:**{6C8EEC18-8D75-41B2-A177-8831D59D2D50}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\main.cpl,-100
-   **Páginas**

    | Nombre de página | Aperturas           |
    |-----------|-----------------|
    | 1         | Punteros        |
    | 2         | Opciones de puntero |
    | 3         | Rueda           |
    | 4         | Hardware        |

    

     

### <a name="mpioconfiguration"></a>MPIOConfiguration

-   **Nombre canónico:** Microsoft.MPIOConfiguration
-   **GUID:**{AB3BE6AA-7561-4838-AB77-ACF8427DF426}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\mpiocpl.dll,-1000
-   Este Panel de control elemento solo se verá en las versiones de servidor de Windows.

### <a name="network-and-sharing-center"></a>Centro de redes y recursos compartidos

-   **Nombre canónico:** Microsoft.NetworkAndSharingCenter
-   **GUID:**{8E908FC9-BECC-40f6-915B-F4CA0E70D03D}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\netcenter.dll,-1
-   **Páginas**

    | Nombre de página  | Aperturas                     |
    |------------|---------------------------|
    | Avanzado   | Configuración avanzada de uso compartido |
    | ShareMedia | Opciones de streaming multimedia   |

    

     

### <a name="notification-area-icons"></a>Iconos del área de notificación

-   **Nombre canónico:** Microsoft.NotificationAreaIcons
-   **GUID:**{05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\taskbarcpl.dll,-1

### <a name="pen-and-touch"></a>Lápiz y táctil

-   **Nombre canónico:** Microsoft.PenAndTouch
-   **GUID:**{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\tabletpc.cpl,-10103
-   **Páginas**

    | Nombre de página | Aperturas       |
    |-----------|-------------|
    | 1         | Películas      |
    | 2         | Escritura a mano |

    

     

### <a name="personalization"></a>Personalization

-   **Nombre canónico:** Microsoft.Personalization
-   **GUID:**{ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\themecpl.dll,-1
-   **Páginas**

    | Nombre de página        | Aperturas                |
    |------------------|----------------------|
    | pageColorization | Color y apariencia |
    | pageWallpaper    | Fondo de escritorio   |

    

     

### <a name="phone-and-modem"></a>Teléfono y módem

-   **Nombre canónico:** Microsoft.PhoneAndModem
-   **GUID:**{40419485-C444-4567-851A-2DD7BFA1684D}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\telephon.cpl,-1
-   La ventana que se inicia este valor se titulada "Información de ubicación" en las versiones de Windows antes de Windows 8. La interfaz de usuario del elemento cambia considerablemente a Windows 8.

### <a name="power-options"></a>Opciones de energía

-   **Nombre canónico:** Microsoft.PowerOptions
-   **GUID:**{025A5937-A6BE-4686-A844-36FE4BEC8B6D}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\powercpl.dll,-1
-   **Páginas**

    | Nombre de página          | Aperturas              |
    |--------------------|--------------------|
    | pageGlobalSettings | Configuración del sistema    |
    | pagePlanSettings   | Editar plan Configuración |

    

     

### <a name="programs-and-features"></a>Programas y características

-   **Nombre canónico:** Microsoft.ProgramsAndFeatures
-   **GUID:**{7b81be6a-ce2b-4676-a29e-eb907a5126c5}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%systemroot% \\ system32 \\appwiz.cpl,-159
-   **Páginas**

    | Nombre de página                                | Aperturas             |
    |------------------------------------------|-------------------|
    | ::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD} | Actualizaciones instaladas |

    

     

### <a name="recovery"></a>Recuperación

-   **Nombre canónico:** Microsoft.Recovery
-   **GUID:**{9FE63AFD-59CF-4419-9775-ABCC3849F861}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\recovery.dll,-101

### <a name="region"></a>Region

-   **Nombre canónico:** Microsoft.RegionAndLanguage
-   **GUID:**{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\intl.cpl,-1
-   El elemento Región e idioma que se encuentra en Windows 7 se dividió a partir de Windows 8. Microsoft.RegionAndLanguage ahora inicia el elemento Región. Para iniciar el elemento Language, use [Microsoft.Language](#location-settings).
-   **Páginas**

    | Nombre de página | Aperturas          |
    |-----------|----------------|
    | 1         | Ubicación       |
    | 2         | Administrativo |

    

     

### <a name="remoteapp-and-desktop-connections"></a>Conexión de RemoteApp y Escritorio

-   **Nombre canónico:** Microsoft.RemoteAppAndDesktopConnections
-   **GUID:**{241D7C96-F8BF-4F85-B01F-E2B043341A4B}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\tsworkspace.dll,-15300

### <a name="sound"></a>Sonido

-   **Nombre canónico:** Microsoft.Sound
-   **GUID:**{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\mmsys.cpl,-300

### <a name="speech-recognition"></a>Reconocimiento de voz

-   **Nombre canónico:** Microsoft.SpeechRecognition
-   **GUID:**{58E3C745-D971-4081-9034-86E34B30836A}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del módulo:**@%SystemRoot% \\ System32 \\ \\ SpeechUx \\speechuxcpl.dll,-1

### <a name="storage-spaces"></a>Espacios de almacenamiento

-   **Nombre canónico:** Microsoft.StorageSpaces
-   **GUID:**{F942C606-0914-47AB-BE56-1321B8035096}
-   **Sistema operativo compatible:** Windows 8, Windows 8.1
-   **Nombre del** módulo: @C: \\ Windows \\ System32 \\SpaceControl.dll,-1

### <a name="sync-center"></a>Centro de sincronización

-   **Nombre canónico:** Microsoft.SyncCenter
-   **GUID:**{9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\SyncCenter.dll,-3000

### <a name="system"></a>Sistema

-   **Nombre canónico:** Microsoft.System
-   **GUID:**{BB06C0E4-D293-4f75-8A90-CB05B6477EEE}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\systemcpl.dll,-1

### <a name="tablet-pc-settings"></a>Tablet PC Configuración

-   **Nombre canónico:** Microsoft.TabletPCSettings
-   **GUID:**{80F3F1D5-FECA-45F3-BC32-752C152E456E}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\tabletpc.cpl,-10100

### <a name="taskbar-and-navigation"></a>Barra de tareas y navegación

-   **Nombre canónico:** Microsoft.Taskbar
-   **GUID:**{0DF44EAA-FF21-4412-828E-260A8728E7F1}
-   **Sistema operativo compatible:** Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ system32 \\shell32.dll,-32517

### <a name="troubleshooting"></a>Solución de problemas

-   **Nombre canónico:** Microsoft.Troubleshooting
-   **GUID:**{C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\DiagCpl.dll,-1
-   **Páginas**

    | Nombre de página   | Aperturas   |
    |-------------|---------|
    | HistoryPage | Historial |

    

     

### <a name="tsappinstall"></a>TSAppInstall

-   **Nombre canónico:** Microsoft.TSAppInstall
-   **GUID:**{BAA884F4-3432-48b8-AA72-9BF20EEF31D5}
-   **Sistema operativo compatible:** Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%systemroot% \\ system32 \\tsappinstall.exe,-2001

### <a name="user-accounts"></a>Cuentas de usuario

-   **Nombre canónico:** Microsoft.UserAccounts
-   **GUID:**{60632754-c523-4b62-b45c-4172da012619}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\usercpl.dll,-1

### <a name="windows-anytime-upgrade"></a>Windows Anytime Upgrade

-   **Nombre canónico:** Microsoft.WindowsAnytimeUpgrade
-   **GUID:**{BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @$(resourceString. \_ SYS \_ MOD \_ PATH),-1

### <a name="windows-defender"></a>Windows Defender

-   **Nombre canónico:** Microsoft.WindowsDefender
-   **GUID:**{D8559EB9-20C0-410E-BEDA-7ED416AECC2A}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%ProgramFiles% \\ Windows Defender \\MsMpRes.dll,-104

### <a name="windows-firewall"></a>Firewall de Windows

-   **Nombre canónico:** Microsoft.WindowsFirewall
-   **GUID:**{4026492F-2F69-46B8-B9BF-5654FC07E423}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @C: \\ Windows \\ system32 \\FirewallControlPanel.dll,-12122
-   **Páginas**

    | Nombre de página         | Aperturas        |
    |-------------------|--------------|
    | pageConfigureApps | Aplicaciones permitidas |

    

     

### <a name="windows-mobility-center"></a>Centro de movilidad de Windows

-   **Nombre canónico:** Microsoft.MobilityCenter
-   **GUID:**{5ea4f148-308c-46d7-98a9-49041b1dd468}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ system32 \\mblctr.exe,-1002

### <a name="windows-to-go"></a>Windows To Go

-   **Nombre canónico:** Microsoft.PortableWorkspaceCreator
-   **GUID:**{8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}
-   **Sistema operativo compatible:** Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ System32 \\pwcreator.exe,-151

### <a name="windows-update"></a>Windows Update

-   **Nombre canónico:** Microsoft.WindowsUpdate
-   **GUID:**{36eef7db-88ad-4e81-ad49-0e313f0c35f8}
-   **Sistema operativo compatible:** Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nombre del** módulo: @%SystemRoot% \\ system32 \\wucltux.dll,-1
-   **Páginas**

    | Nombre de página         | Aperturas               |
    |-------------------|---------------------|
    | pageSettings      | Cambio de configuración     |
    | pageUpdateHistory | Visualización del historial de actualizaciones |

    

     

### <a name="work-folders"></a>Carpetas de trabajo

-   **Nombre canónico:** Microsoft.WorkFolders
-   **GUID:**{ECDB0924-4208-451E-8EE0-373C0956DE16}
-   **Sistema operativo compatible:** Windows 8.1
-   **Nombre del** módulo: @C: \\ Windows \\ System32 \\WorkfoldersControl.dll,-1

## <a name="deprecated-control-panel-canonical-names"></a>Nombres canónicos Panel de control en desuso

Los siguientes son nombres canónicos que ya no se usan a Windows 8.1 o posterior. Algunos se han quitado por completo. Otros se han rematado en estas situaciones:

-   Se cambia Panel de control nombre de un elemento. Al elemento cuyo nombre se ha cambiado se le da un nuevo nombre canónico, pero mantiene el mismo GUID. En este caso, el nombre canónico anterior inicia el nombre Panel de control elemento. Tenga en cuenta que es posible que el elemento que se inicia no use la misma interfaz de usuario que la versión anterior de ese elemento.
-   La funcionalidad de uno o varios elementos Panel de control se mueve o se consolida en un nuevo elemento. En este caso, el nombre canónico anterior se asigna al nuevo elemento Panel de control más adecuado.

> [!Note]  
> Existen remappings para la compatibilidad con versiones anteriores. No debe usar valores en desuso en el código nuevo.

 



| Nombre canónico en desuso                                   | Control Panel Item                | GUID                                   | Notas                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft.AddHardware                                       | Agregar hardware                      | {7A979262-40CE-46ff-AEEE-7884AC3B6136} | Mapas a [Microsoft.DevicesAndPrinters a](#devices-and-printers) partir Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft.AudioDevicesAnd SoundThemes                        | Sonido                             | {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D} | Mapas a [Microsoft.Sound](#sound) a partir de Windows 7.                                                                                                                                                                                                                                                                                                        |
| Microsoft.BackupAndRestoreCenter/Microsoft.BackupAndRestore | Centro de copias de seguridad y restauración         | {B98A2BEA-7D42-4558-8BD1-832F41BAC6FD} | Microsoft.BackupAndRestoreCenter se asigna a Microsoft.BackupAndRestore en Windows 7. Ambos se quitan a Windows 8; use [Microsoft.FileHistory en](#file-history) su lugar.                                                                                                                                                                                   |
| Microsoft.CardSpace                                         | Windows CardSpace                 | {78CB147A-98EA-4AA6-B0DF-C8681F69341C} | Se ha quitado a Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft.DesktopGadgets                                    | Desktop Gadgets                   | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Se ha quitado a Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft.GetProgramsOnline                                 | Azure Marketplace               | {3e7efb4c-faf1-453d-89eb-56026875ef90} | Se ha quitado a partir Windows 7.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft.OptionOptions                                   | Infrarrojos                          | {A0275511-0E86-4ECA-97C2-ECD8F1221D08} | Mapas a [Microsoft.Locución](#infrared) a partir de Windows 7.                                                                                                                                                                                                                                                                                                  |
| Microsoft.Language                                          | Lenguaje                          | {BF782CC9-5A52-4A17-806C-2A894FFEEAC5} | Se ha quitado a Windows 10, versión 1803                                                                                                                                                                                                                                                                                                                    |
| Microsoft.LocationAndOtherSensors                           | Ubicación y otros sensores        | {E9950154-C418-419e-A90A-20C5287AE24B} | Mapas a [Microsoft.LocationSettings](#infrared) a Windows 8.                                                                                                                                                                                                                                                                                          |
| Microsoft.PenAndInputDevices                                | Lápiz y dispositivos de entrada             | {F82DF8F7-8B9F-442E-A48C-818EA735FF9B} | Mapas a [Microsoft.PenAndTouch](#pen-and-touch) a partir de Windows 7.                                                                                                                                                                                                                                                                                          |
| Microsoft.PeopleNearMe                                      | People Near Me (Gente que esté cerca)                    | {5224F545-A443-4859-BA23-7B5A95BDC8EF} | Se ha quitado a Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft.PerformanceInformationAndTools                    | Información y herramientas de rendimiento | {78F3955E-3B90-4184-BD14-5397C15F1EFC} | Se ha quitado a Windows 8.1.                                                                                                                                                                                                                                                                                                                                |
| Microsoft.PhoneAndModemOptions                              | Teléfono y módem                   | {40419485-C444-4567-851A-2DD7BFA1684D} | Mapas a [Microsoft.PhoneAndModem](#phone-and-modem) a partir Windows 7.                                                                                                                                                                                                                                                                                      |
| Microsoft.Printers                                          | Impresoras                          | {2227A280-3AEA-1069-A2DE-08002B30309D} | Mapas a [Microsoft.DevicesAndPrinters a](#devices-and-printers) partir Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft.ProblemReportsAndSolutions                        | Informes de problemas y soluciones     | {FCFEECAE-EE1B-4849-AE50-685DCF7717EC} | Mapas a [Microsoft.ActionCenter](#action-center) a partir de Windows 7.                                                                                                                                                                                                                                                                                         |
| Microsoft.RegionalAndLanguageOptions                        | Configuración regional y de idioma     | {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0} | Mapas a [Microsoft.RegionAndLanguage](#region) a partir Windows 7. Tenga en cuenta que a Windows 8, región e idioma tenían cada uno su propio Panel de control elemento. Microsoft.RegionalAndLanguageOptions y Microsoft.RegionAndLanguage abren actualmente el elemento Región. Debe usar [Microsoft.Language para acceder](#location-settings) al elemento Language. |
| Microsoft.SecurityCenter                                    | Centro de seguridad de Windows           | {087DA31B-0DD3-4537-8E23-64A18591F88B} | Mapas a [Microsoft.ActionCenter](#action-center) a partir de Windows 7.                                                                                                                                                                                                                                                                                         |
| Microsoft.SpeechRecognitionOptions                          | Opciones de reconocimiento de voz        | {58E3C745-D971-4081-9034-86E34B30836A} | Mapas a [Microsoft.SpeechRecognition](#speech-recognition) a partir Windows 7.                                                                                                                                                                                                                                                                               |
| Microsoft.TaskbarAndStartMenu                               | Barra de tareas y menú Inicio            | {0DF44EAA-FF21-4412-828E-260A8728E7F1} | Mapas a [Microsoft.Taskbar](#speech-recognition) a Windows 8.                                                                                                                                                                                                                                                                                         |
| Microsoft.WelcomeCenter                                     | Centro de bienvenida                    | {CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1} | Mapas a Microsoft.GettingStarted en Windows 7. Inicia la página Panel de control página principal a Windows 8.                                                                                                                                                                                                                                                      |
| Microsoft.WindowsSidebarProperties                          | Windows Propiedades de la barra lateral        | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Mapas a Microsoft.DesktopGadgets en Windows 7. Se ha quitado a Windows 8.                                                                                                                                                                                                                                                                                   |
| Microsoft.WindowsSideShow                                   | Windows SideShow                  | {E95A4861-D57A-4be1-AD0F-35267E261739} | Característica en desuso Windows 8, quitada a Windows 8.1.                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a>Uso de nombres canónicos en el directiva de grupo

A partir Windows 7, puede usar nombres canónicos para restringir el acceso a elementos de Panel de control a través de la directiva de grupo. Este mismo procedimiento se puede usar en Windows Vista, pero debe usar el nombre del módulo en lugar del nombre canónico.

### <a name="hiding-individual-control-panel-items"></a>Ocultar elementos de Panel de control individuales

Use este método si desea mostrar más elementos Panel de control que desea ocultar.

1.  Ejecute el archivo Gpedit.msc para iniciar el Editor de directivas de grupo local. También puede escribir "directiva de grupo" en el Windows 8.1 pantalla Inicio seleccione Editar directiva de **grupo** en los resultados de la búsqueda.
2.  Seleccione **Configuración de** usuario  >  **Plantillas administrativas**  >  **Panel de control**.
3.  Seleccione **Ocultar elementos Panel de control especificados.**
4.  En la **ventana Ocultar elementos Panel de control especificados** que se abre, haga clic en **Habilitado.**
5.  Haga clic **en el** botón Mostrar del panel Opciones para mostrar la lista de elementos Panel de control no permitidos.
6.  En la **ventana Mostrar** contenido que se abre, escriba un nombre canónico en la **columna** Valor. Repita este paso las veces que sea necesario.
7.  Haga clic en **Aceptar**.

### <a name="showing-individual-control-panel-items"></a>Mostrar elementos de Panel de control individuales

Use este método si desea ocultar más elementos Panel de control que desea mostrar.

1.  Ejecute el archivo Gpedit.msc para iniciar el Editor de directivas de grupo local. También puede escribir "directiva de grupo" en el Windows 8.1 pantalla Inicio seleccione Editar directiva de **grupo** en los resultados de la búsqueda.
2.  Seleccione **Configuración de** usuario  >  **Plantillas administrativas**  >  **Panel de control**.
3.  Seleccione **Mostrar solo los elementos Panel de control especificados.**
4.  En la **ventana Mostrar solo elementos Panel de control especificados** que se abre, haga clic en **Habilitado.** Esto oculta todo el Panel de control.
5.  Haga clic **en el botón** Mostrar del panel Opciones para mostrar la lista de elementos Panel de control permitidos.
6.  En la **ventana Mostrar** contenido que se abre, escriba un nombre canónico en la **columna** Valor. Repita este paso las veces que sea necesario.
7.  Haga clic en **Aceptar**.

Si desea quitar todas las entradas que ha agregado a una lista Mostrar u ocultar elementos de Panel de control, vuelva  a la pantalla del paso 4 y seleccione No configurado para borrar la lista. Si desea conservar las entradas pero suspender las restricciones, seleccione **Deshabilitado.**

## <a name="remarks"></a>Comentarios

Es posible que vea elementos en la Panel de control que no aparecen aquí. Esos elementos no forman parte de Windows, sino que se agregan durante la instalación de diversos software y hardware, como Microsoft Office o una tarjeta de vídeo. Los elementos que no Windows Panel de control pueden tener o no un nombre canónico. Para buscar el nombre canónico de un elemento Panel de control no aparece aquí, busque en el Registro en estas rutas de acceso:

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

Para obtener más información que pueda ayudarle a detectar los CLSID necesarios, vea [Cómo](how-to-register-an-executable-control-panel-item-registration-.md) registrar elementos ejecutables Panel de control y Cómo registrar [dll Panel de control elementos](how-to-register-dll-control-panel-item-registration-.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejecutar elementos Panel de control datos](executing-control-panel-items.md)
</dt> <dt>

[**IOpenControlPanel**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



