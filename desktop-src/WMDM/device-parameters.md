---
title: Parámetros del dispositivo
description: Parámetros del dispositivo
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Administrador de dispositivos de Windows Media, parámetros de dispositivo
- Administrador de dispositivos, parámetros de dispositivo
- Guía de programación, parámetros de dispositivo
- proveedores de servicios, parámetros de dispositivo
- crear proveedores de servicios, parámetros de dispositivo
- parámetros del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3ad1a1bfc6a24736fdad8385e6cc03e0b20be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356967"
---
# <a name="device-parameters"></a>Parámetros del dispositivo

Windows Media Administrador de dispositivos usa parámetros de dispositivo para controlar el comportamiento de un dispositivo. Estos parámetros se agregan al registro como se especifica en el archivo de instalación del dispositivo (archivo INF). En la tabla siguiente se enumeran los parámetros de dispositivo que Windows Media Administrador de dispositivos consulta.



| Nombre del parámetro de dispositivo | Tipo de datos del registro | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *WMDMSPCLSID*         | **Registro \_ SZ**        | Valor que especifica el CLSID del proveedor de servicios que controla este dispositivo. Este parámetro es obligatorio para la compatibilidad con PnP.<br/> El valor del parámetro debe ser el CLSID, no el ProgID del proveedor de servicios. Este parámetro es obligatorio para admitir Plug and Play (PnP) en Windows Media Administrador de dispositivos. Para obtener más información, consulte [habilitación de PNP para dispositivos](enabling-pnp-for-devices.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *OptimalTransferSize* | **\_valor DWORD reg**     | Valor opcional que especifica el tamaño de transferencia preferido que usa Windows Media Administrador de dispositivos durante las operaciones de lectura y escritura. Si no se proporciona, se usa un tamaño de transferencia predeterminado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *UseMetadataViews*    | **\_valor DWORD reg**     | Parámetro opcional que especifica si Windows Media Administrador de dispositivos organiza el contenido por metadatos mientras presenta el contenido del dispositivo en las aplicaciones. Si no se especifica ningún valor, se utiliza el valor predeterminado 0.<br/> Cuando las aplicaciones enumeran el contenido de los almacenamientos de un reproductor de audio portátil, Windows Media Administrador de dispositivos puede presentar el contenido organizado por metadatos. Esto es especialmente útil para dispositivos con gran capacidad de almacenamiento.<br/> Las aplicaciones y los dispositivos tienen la capacidad de controlar este comportamiento. Los dispositivos indican sus preferencias a través del parámetro de dispositivo *UseMetadataViews*.<br/> Se admiten los siguientes dos valores enteros:<br/> Solicita que el contenido se presente a las aplicaciones exactamente como se organiza en el sistema de archivos del dispositivo.<br/> Solicita que el contenido se presente a las aplicaciones organizadas por metadatos.<br/> |
| *ShowInShell*         | **\_valor DWORD reg**     | Parámetro opcional que especifica si el dispositivo debe aparecer en el explorador de Windows. El valor 1 indica que el dispositivo debe aparecer en el explorador de Windows. Para obtener más información, consulte [requisitos de los reproductores de audio portátiles para que aparezcan en el explorador de Windows](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *UseExtendedWmdm*     | **\_valor DWORD reg**     | Parámetro opcional que alerta a Windows Media Administrador de dispositivos que el proveedor de servicios admite **IMDSPDevice3**, **IMDSPObject2** y **IMDSPStorage4**. Sin esta marca, Windows Media Administrador de dispositivos nunca llamará a estas interfaces. El valor 1 indica que se admiten estas interfaces.<br/> Esta marca es necesaria para los proveedores de servicios que se sincronizan con Media Player de Windows. (Consulte [habilitación de la sincronización con Windows Media Player](enabling-synchronization-with-windows-media-player.md)).<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

**Codificar el archivo INF**

En el siguiente código de ejemplo del archivo INF de un dispositivo se muestra la configuración de algunos parámetros de dispositivo durante la instalación del dispositivo.


```C++
; Set parameters on Windows 95 and Windows 98 operating systems.
[DriverInstall.hw]
AddReg=DriverHwPropReg

; Set parameters on Windows NT-based operating systems.
[DriverInstall.NT.hw]
AddReg=DriverHwPropReg

; Related section that specifies the device parameters.
[DriverHwPropReg]
; Add your own CLSID here.
HKR,,WMDMSPCLSID,,"{00000000-0000-0000-0000-000000000000}"
HKR,,OptimalTransferSize,0x10001,0x10000
HKR,,UseMetadataViews,0x10001,0x1
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> <dt>

[**Interfaz IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)
</dt> <dt>

[**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[**Interfaz IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





