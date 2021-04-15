---
title: Extensiones de dispositivo de Windows Media Administrador de dispositivos para la transferencia de metadatos
description: Extensiones de dispositivo de Windows Media Administrador de dispositivos para la transferencia de metadatos
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player, extensiones de dispositivo
- Windows Media Player, extensiones
- Media Player de Windows, metadatos
- Windows Media Player, transferencia acelerada de metadatos
- Windows Media Player, transferencia acelerada de metadatos
- metadatos, extensiones de dispositivo
- metadatos, extensiones
- extensiones de dispositivo, transferencia de metadatos
- extensiones, transferencia de metadatos
- transferencia acelerada de metadatos
- metadatos, transferencia acelerada
- extensiones de dispositivo, transferencia acelerada de metadatos
- extensiones, transferencia de metadatos acelerada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486882"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a>Extensiones de dispositivo de Windows Media Administrador de dispositivos para la transferencia de metadatos

Para habilitar la transferencia de metadatos acelerada, los fabricantes de dispositivos que no admiten MTP deben hacer lo siguiente en el código fuente:

-   Definir **la \_ \_ \_ compatibilidad con dispositivos de WMP WMDM**.
-   Incluya wmpdevices. h, que se instala como parte del SDK de Windows Media Player.

Wmpdevices. h define las siguientes estructuras.



| Estructura                                                                                 | Descripción                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ciclo de ida y \_ vuelta de metadatos de WMP WMDM \_ \_ \_ \_ PC2DEVICE](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | Estructura utilizada por Windows Media Player para solicitar información de sincronización de metadatos acelerada de dispositivos portátiles que no son compatibles con MTP. |
| [Ciclo de ida y \_ vuelta de metadatos de WMP WMDM \_ \_ \_ \_ DEVICE2PC](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | Estructura utilizada por Windows Media Player para recibir información de sincronización de metadatos acelerada de dispositivos portátiles que no son compatibles con MTP. |



 

Para solicitar información del dispositivo sobre los metadatos que han cambiado, Windows Media Player 10 o posterior llama al método de Administrador de dispositivos de Windows Media **IWMDMDevice3::D eviceiocontrol**. Al realizar esta llamada, el reproductor sigue los pasos específicos, como se indica a continuación:

-   El primer parámetro, *dwIoControlCode*, contiene la constante **ioctl \_ WMP \_ Metadata \_ Round \_ Trip**. Esta constante se define en wmpdevices. h.
-   El segundo parámetro, *lpInBuffer*, apunta a una estructura de PC2DEVICE de ida y **\_ \_ \_ \_ \_ vuelta de metadatos de WMP WMDM** .
-   El tercer parámetro, *nInBufferSize*, contiene el tamaño del búfer de entrada.
-   El cuarto parámetro, *lpOutBuffer*, apunta a una estructura de DEVICE2PC de ida y **\_ \_ \_ \_ \_ vuelta de metadatos de WMP WMDM** . El dispositivo debe rellenar esta estructura con información sobre los cambios.
-   El quinto parámetro, *pnOutBufferSize*, recibe el tamaño del búfer de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensiones de dispositivo para la transferencia de metadatos acelerada**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




