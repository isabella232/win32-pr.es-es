---
description: Location API define los siguientes tipos de enumeración.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Estructuras y tipos de enumeración (API de ubicación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8cfea31e8822147cc33710239b31dcd4b982ca3b523dfb6f118d1969af703c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129815"
---
# <a name="structures-and-enumeration-types-location-api"></a>Estructuras y tipos de enumeración (API de ubicación)

\[La API de ubicación de Win32 está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [**el Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API. \]

Location API define los siguientes tipos de enumeración.



| Enumeración                                                                       | Descripción                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**PRECISIÓN \_ DESEADA DE LA \_ UBICACIÓN**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))                  | Define los posibles tipos de precisión deseados.                         |
| [**ESTADO DEL \_ INFORME \_ DE UBICACIÓN**](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | Define el posible estado de los nuevos informes de un tipo de informe determinado. |



 

## <a name="location-constants-from-the-sensor-api"></a>Constantes de ubicación de Sensor API

Sensor API también define constantes y claves de propiedad relacionadas con la ubicación. Las claves de propiedad definidas en sensors.h se pueden usar para recuperar datos de ubicación de un informe mediante una llamada a [**ILocationReport::GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).

 

 
