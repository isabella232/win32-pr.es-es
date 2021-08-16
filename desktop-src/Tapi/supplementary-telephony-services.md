---
description: Los servicios complementarios de telefonía son la colección de todos los servicios definidos por la API distintos de los incluidos en el subconjunto de telefonía básica.
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: Servicios complementarios de telefonía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9762b2d9ca74d0212170e1e87662242d3983663db024ce52018d108cc37fb883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760757"
---
# <a name="supplementary-telephony-services"></a>Servicios complementarios de telefonía

Los servicios complementarios de telefonía son la colección de todos los servicios definidos por la API distintos de los incluidos en el subconjunto de telefonía básica. Incluye todas las llamadas características adicionales que se encuentran en los PBX modernos, como la retención, la transferencia, la conferencia, el aparcamiento, y así sucesivamente. Todas las características adicionales se consideran opcionales; es decir, el proveedor de servicios decide cuál de estos servicios proporciona o no.

Una aplicación puede consultar un dispositivo de línea o teléfono para el conjunto de servicios adicionales que proporciona mediante funciones como [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) [**o lineGetAddressCaps.**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) Un único servicio complementario puede constar de varias llamadas de función y mensajes. La API de telefonía, y no el desarrollador del proveedor de servicios, define el comportamiento de cada una de estas características adicionales. Un proveedor de servicios debe proporcionar un servicio de telefonía complementaria solo si puede implementar el significado exacto según lo definido por la API. Si no es así, la característica debe proporcionarse como un servicio de telefonía extendida.

Como se mencionó en Servicios básicos de telefonía, los servicios de dispositivos telefónicos se consideran opcionales. Por lo tanto, todos los servicios de dispositivos telefónicos forman parte de la telefonía complementaria. Para obtener una lista de las funciones de telefonía complementaria, vea Referencia de [funciones rápidas de TAPI.](./tapi-quick-function-reference.md)

 

 
