---
description: Requisitos generales para el desarrollo de aplicaciones
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Requisitos generales para el desarrollo de aplicaciones (API de WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359896"
---
# <a name="general-requirements-for-application-development-wpd-api"></a>Requisitos generales para el desarrollo de aplicaciones (API de WPD)

Para crear una Windows dispositivos portátiles, debe tener instalado Windows [Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) en el equipo. Los encabezados y bibliotecas necesarios aparecen en la lista siguiente.

-   PortableDeviceGuids.lib
-   PortableDevice.h
-   PortableDeviceTypes.h
-   PortableDeviceApi.h
-   Cualquier otra biblioteca y encabezado necesarios que requiera la aplicación para consumir o representar archivos multimedia.

Si la aplicación admite las nuevas interfaces de Device Services, también incluirá uno o varios de los siguientes archivos de encabezado.

-   AnchorSyncDeviceService.h
-   BridgeDeviceService.h
-   CalendarDeviceService.h
-   ContactDeviceService.h
-   DeviceServices.h
-   FullEnumSyncDeviceService.h
-   HintsDeviceService.h
-   MessageDeviceService.h
-   MetadataDeviceService.h
-   NotesDeviceService.h
-   DeviceService.h
-   StatusDeviceService.h
-   SyncDeviceService.h
-   TaskDeviceService.h

De los archivos de la lista anterior, BridgeDeviceService.h y DeviceService.h son necesarios para casi cualquier aplicación que admita Device Services; los demás archivos definen diferentes tipos de servicios de dispositivo y se incluirían según corresponda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Windows Dispositivos portátiles**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
