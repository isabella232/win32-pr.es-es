---
description: Las secciones siguientes contienen una lista alfabética de funciones agrupadas por área. La información de cada función incluye una lista de los Estados de llamada válidos en la entrada de la función y las transiciones de estado de llamada típicas cuando se completa la solicitud.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: Funciones de TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545643"
---
# <a name="tapi-functions"></a>Funciones de TAPI

Las secciones siguientes contienen una lista alfabética de funciones agrupadas por área. La información de cada función incluye una lista de los Estados de llamada válidos en la entrada de la función y las transiciones de estado de llamada típicas cuando se completa la solicitud.

-   [Funciones de telefonía asistida](assisted-telephony-functions.md)
-   [Funciones del centro de llamadas](call-center-functions.md)
-   [Funciones de dispositivo de línea](line-device-functions.md)
-   [Funciones de dispositivo de teléfono](phone-device-functions.md)

Para las funciones TAPI clasificadas por nivel de servicio y tarea, consulte [referencia rápida de funciones de TAPI](tapi-quick-function-reference.md).

Tenga en cuenta que pueden existir limitaciones en el proveedor de servicios en relación con los Estados reales en los que se puede realizar una función. Las aplicaciones deben comprobar el miembro **dwCallFeatures** de la estructura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , el miembro **dwAddressFeatures** de la estructura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) y el miembro **dwLineFeatures** de la estructura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) para determinar si se permite una función dentro del estado de la llamada actual.

 

 



