---
title: Windows Extensiones de Administrador de dispositivos multimedia para la transferencia de metadatos
description: Windows Extensiones de Administrador de dispositivos multimedia para la transferencia de metadatos
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Reproductor de Windows Media,extensiones de dispositivo
- Reproductor de Windows Media,extensions
- Reproductor de Windows Media,metadata
- Reproductor de Windows Media, transferencia acelerada de metadatos
- Reproductor de Windows Media, transferencia acelerada de metadatos
- metadata,device extensions
- metadata,extensions
- extensiones de dispositivo, transferencia de metadatos
- extensiones, transferencia de metadatos
- transferencia acelerada de metadatos
- metadatos, transferencia acelerada
- extensiones de dispositivo, transferencia acelerada de metadatos
- extensiones, transferencia acelerada de metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9b37271fc9714bf3665dccf1475da1a5840c429d7df9136a50fe95789f7a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571645"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a>Windows Extensiones de Administrador de dispositivos multimedia para la transferencia de metadatos

Para habilitar la transferencia acelerada de metadatos, los fabricantes de dispositivos que no admiten MTP deben hacer lo siguiente en el código fuente:

-   Defina la **compatibilidad con \_ dispositivos WMDM \_ de \_ WMP.**
-   Incluya wmpdevices.h, que se instala como parte del SDK de Reproductor de Windows Media.

Wmpdevices.h define las estructuras siguientes.



| Estructura                                                                                 | Descripción                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMP \_ WMDM \_ METADATA \_ ROUND \_ TRIP \_ PC2DEVICE](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | Estructura usada por Reproductor de Windows Media para solicitar información de sincronización acelerada de metadatos desde dispositivos portátiles que no admiten MTP. |
| [WMP \_ WMDM \_ METADATA \_ ROUND \_ TRIP \_ DEVICE2PC](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | Estructura usada por Reproductor de Windows Media para recibir información de sincronización acelerada de metadatos de dispositivos portátiles que no admiten MTP. |



 

Para solicitar información del dispositivo sobre los metadatos que han cambiado, Reproductor de Windows Media 10 o posterior llama al método Windows Media Administrador de dispositivos **IWMDMDevice3::D eviceIoControl**. Al realizar esta llamada, el reproductor sigue pasos específicos, como se muestra a continuación:

-   El primer parámetro, *dwIoControlCode*, contiene la constante **IOCTL \_ WMP \_ METADATA ROUND \_ \_ TRIP**. Esta constante se define en wmpdevices.h.
-   El segundo parámetro, *lpInBuffer*, apunta a una estructura **\_ WMP WMDM \_ METADATA ROUND TRIP \_ \_ \_ PC2DEVICE.**
-   El tercer parámetro, *nInBufferSize*, contiene el tamaño del búfer de entrada.
-   El cuarto parámetro, *lpOutBuffer*, apunta a una estructura **\_ WMP WMDM \_ METADATA ROUND TRIP \_ \_ \_ DEVICE2PC.** El dispositivo debe rellenar esta estructura con información sobre los cambios.
-   El quinto parámetro, *pnOutBufferSize,* recibe el tamaño del búfer de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensiones de dispositivo para la transferencia acelerada de metadatos**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




