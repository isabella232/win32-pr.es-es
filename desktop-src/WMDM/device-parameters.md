---
title: Parámetros del dispositivo
description: Parámetros del dispositivo
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows Parámetros Administrador de dispositivos medios, parámetros de dispositivo
- Administrador de dispositivos,parámetros de dispositivo
- guía de programación, parámetros de dispositivo
- proveedores de servicios, parámetros de dispositivo
- crear proveedores de servicios, parámetros de dispositivo
- parámetros de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef097940670148551042c22fd8efc6aa51c641960bf0f821361aaf3c29c731d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585354"
---
# <a name="device-parameters"></a>Parámetros del dispositivo

Windows Los Administrador de dispositivos usan parámetros de dispositivo para controlar el comportamiento de un dispositivo. Estos parámetros se agregan al Registro como se especifica en el archivo de instalación del dispositivo (archivo INF). En la tabla siguiente se enumeran los parámetros del dispositivo Windows consultas Administrador de dispositivos multimedia.



| Nombre del parámetro de dispositivo | Tipo de datos del Registro | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *WMDMSPCLSID*         | **REG \_ SZ**        | Valor que especifica el CLSID del proveedor de servicios que controla este dispositivo. Este parámetro es obligatorio para la compatibilidad con PnP.<br/> El valor del parámetro debe ser el CLSID, no el ProgID del proveedor de servicios. Este parámetro es obligatorio para admitir Plug and Play (PnP) en Windows Media Administrador de dispositivos. Para obtener más información, vea Enabling PnP for Devices ( [Habilitación de PnP para dispositivos).](enabling-pnp-for-devices.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *OptimalTransferSize* | **REG \_ DWORD**     | Valor opcional que especifica el tamaño de transferencia preferido que Windows media Administrador de dispositivos durante las operaciones de lectura y escritura. Si no se proporciona, se usa un tamaño de transferencia predeterminado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *UseMetadataViews*    | **REG \_ DWORD**     | Parámetro opcional que especifica si Windows multimedia Administrador de dispositivos el contenido por metadatos al presentar el contenido del dispositivo a las aplicaciones. Si no se especifica ningún valor, se utiliza el valor predeterminado 0.<br/> Cuando las aplicaciones enumeran el contenido en los almacenamientos de un reproductor de audio portátil, Windows Media Administrador de dispositivos puede presentar el contenido organizado por metadatos. Esto es especialmente útil para dispositivos con una gran capacidad de almacenamiento.<br/> Las aplicaciones y los dispositivos tienen la capacidad de controlar este comportamiento. Los dispositivos indican su preferencia a través del *parámetro de dispositivo UseMetadataViews*.<br/> Se admiten los dos valores enteros siguientes:<br/> Solicita que el contenido se presente a las aplicaciones exactamente como se organiza en el sistema de archivos del dispositivo.<br/> Solicita que el contenido se presente a las aplicaciones organizadas por metadatos.<br/> |
| *ShowInShell*         | **REG \_ DWORD**     | Parámetro opcional que especifica si el dispositivo debe aparecer en Windows Explorer. El valor 1 indica que el dispositivo debe aparecer en Windows Explorer. Para obtener más información, vea [Requisitos para que los reproductores de audio portátiles aparezcan en Windows Explorer](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *UseExtendedWmdm*     | **REG \_ DWORD**     | Parámetro opcional que Windows a Media Administrador de dispositivos que el proveedor de servicios admite **IMDSPDevice3,** **IMDSPObject2** e **IMDSPStorage4**. Sin esta marca, Windows Media Administrador de dispositivos llamará nunca a estas interfaces. El valor 1 indica que se admiten estas interfaces.<br/> Esta marca es necesaria para los proveedores de servicios que se sincronizan con Reproductor de Windows Media. (Consulte [Habilitación de la sincronización Reproductor de Windows Media](enabling-synchronization-with-windows-media-player.md)).<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

**Codificación del archivo INF**

El código de ejemplo siguiente del archivo INF de un dispositivo muestra cómo establecer algunos parámetros de dispositivo durante la instalación del dispositivo.


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

[**IWMDMDevice (interfaz)**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





