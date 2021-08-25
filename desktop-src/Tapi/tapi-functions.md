---
description: Las secciones siguientes contienen una lista alfabética de funciones agrupadas por área. La información de cada función incluye una lista de los estados de llamada válidos en la entrada de la función y las transiciones de estado de llamada típicas cuando se completa la solicitud.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: Funciones TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27ec2383f826efe5620ea44d3a643e46a90b08c7820548733238290bff26512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872915"
---
# <a name="tapi-functions"></a>Funciones TAPI

Las secciones siguientes contienen una lista alfabética de funciones agrupadas por área. La información de cada función incluye una lista de los estados de llamada válidos en la entrada de la función y las transiciones de estado de llamada típicas cuando se completa la solicitud.

-   [Funciones de telefonía asistida](assisted-telephony-functions.md)
-   [Funciones del centro de llamadas](call-center-functions.md)
-   [Funciones de dispositivo de línea](line-device-functions.md)
-   [Teléfono Funciones de dispositivo](phone-device-functions.md)

Para ver las funciones TAPI clasificadas por nivel de servicio y tarea, consulte [Referencia de funciones rápidas de TAPI.](tapi-quick-function-reference.md)

Tenga en cuenta que pueden existir limitaciones del proveedor de servicios con respecto a los estados reales en los que se puede realizar una función. Las aplicaciones deben comprobar el **miembro dwCallFeatures** en la estructura [**LINECALLSTATUS,**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) el **miembro dwAddressFeatures** en la estructura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) y el **miembro dwLineFeatures** de la estructura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) para determinar si se permite o no una función dentro del estado de llamada actual.

 

 



