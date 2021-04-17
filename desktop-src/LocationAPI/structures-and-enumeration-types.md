---
description: La API de ubicación define los siguientes tipos de enumeración.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Estructuras y tipos de enumeración (API de ubicación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678149"
---
# <a name="structures-and-enumeration-types-location-api"></a>Estructuras y tipos de enumeración (API de ubicación)

\[La API de ubicación de Win32 está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) . \]

La API de ubicación define los siguientes tipos de enumeración.



| Enumeración                                                                       | Descripción                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_precisión deseada de la ubicación \_**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))                  | Define los posibles tipos de precisión deseados.                         |
| [**\_Estado del informe de ubicación \_**](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | Define el estado posible para los nuevos informes de un tipo de informe determinado. |



 

## <a name="location-constants-from-the-sensor-api"></a>Constantes de ubicación de la API de sensor

La API del sensor también define las constantes y las claves de propiedad relacionadas con la ubicación. Las claves de propiedad definidas en Sensors. h se pueden usar para recuperar datos de ubicación de un informe mediante una llamada a [**ILocationReport:: GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).

 

 
