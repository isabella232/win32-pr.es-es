---
description: Requisitos generales para el desarrollo de aplicaciones
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Requisitos generales para el desarrollo de aplicaciones (API de WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277610"
---
# <a name="general-requirements-for-application-development-wpd-api"></a>Requisitos generales para el desarrollo de aplicaciones (API de WPD)

Para crear una aplicación de dispositivos portátiles de Windows, debe tener instalado en el equipo el [Kit de desarrollo de software (SDK) de Windows](https://developer.microsoft.com/windows/downloads) . Los encabezados y las bibliotecas necesarios aparecen en la lista siguiente.

-   PortableDeviceGuids. lib
-   PortableDevice. h
-   PortableDeviceTypes. h
-   PortableDeviceApi. h
-   Cualquier otra biblioteca y encabezado necesarios que necesite la aplicación para consumir o representar archivos multimedia.

Si la aplicación admite las nuevas interfaces de servicios de dispositivo, también incluirá uno o varios de los siguientes archivos de encabezado.

-   AnchorSyncDeviceService. h
-   BridgeDeviceService. h
-   CalendarDeviceService. h
-   ContactDeviceService. h
-   DeviceServices. h
-   FullEnumSyncDeviceService. h
-   HintsDeviceService. h
-   MessageDeviceService. h
-   MetadataDeviceService. h
-   NotesDeviceService. h
-   RingtoneDeviceService. h
-   StatusDeviceService. h
-   SyncDeviceService. h
-   TaskDeviceService. h

De los archivos de la lista anterior, se necesitan BridgeDeviceService. h y DeviceService. h para casi cualquier aplicación que admita servicios de dispositivo. los otros archivos definen diferentes tipos de servicios de dispositivo y se incluirán según corresponda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Dispositivos portátiles de Windows**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
