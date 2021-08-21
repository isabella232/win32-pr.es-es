---
description: Una cola de llamadas o un punto de ruta es una dirección especial dentro del conmutador donde las llamadas se mantienen temporalmente pendientes de acción.
ms.assetid: 1c801401-be05-4b5f-bc4f-628dde0f3cf7
title: Colas de llamadas y puntos de ruta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd9c4c137b9304fda405201fb16a6637c5fa193e3853f1d570fa288cf9a1edc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117947693"
---
# <a name="call-queues-and-route-points"></a>Colas de llamadas y puntos de ruta

Una cola de llamadas o un punto de ruta es una dirección especial dentro del conmutador donde las llamadas se mantienen temporalmente pendientes de acción. Esta característica se representa mediante los bits LINEADDRCAPFLAGS QUEUE y \_ LINEADDRCAPFLAGS ROUTEPOINT en el \_ **miembro dwAddrCapFlags** de [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). Todas las llamadas que aparecen en dicha dirección están esperando la acción de la aplicación y pueden tener lugar acciones predeterminadas (por ejemplo, transferir a un agente o tronco) si la aplicación no realiza ninguna acción dentro de un período de tiempo definido. El administrador del sistema debe configurar la aplicación para que sepa qué acciones debe realizar con respecto a las llamadas que aparecen en cada dirección de cola o punto de ruta, así como la cantidad de tiempo disponible para decidir la acción que se debe realizar.

Las aplicaciones pueden determinar el número de llamadas pendientes en una cola o un punto de ruta [**mediante lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus). La función [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) se puede usar para obtener información como el identificador de llamada, el identificador llamado, el origen entrante o saliente, y así sucesivamente, y la aplicación puede usar para tomar decisiones sobre el control de llamadas. Las llamadas se pueden redirigir, transferir a la vista, eliminar, y así sucesivamente, o simplemente se pueden pasar automáticamente de la cola a un destino. Una llamada a LINECALLSTATE \_ DISCONNECTED si se abandona. Las llamadas dejan *de* estar inactivas cuando salen de la cola. **lineGetCallInfo** se puede usar para leer el identificador de redireccionamiento para determinar dónde se han transferido.

Algunos modificadores permiten que las llamadas en una cola o en espera reciban un tratamiento determinado, como silencio, anillo, señal ocupada, música o escuchar un anuncio grabado. La [**función lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) permite a la aplicación controlar el tratamiento. La estructura delimitada por los miembros **dwCallTreatmentListSize** y **dwCallTreatmentListOffset** en [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) permite a las aplicaciones determinar los tratamientos admitidos. El **miembro dwCallTreatment** de [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) indica el tratamiento actual y un mensaje [**LINE \_ CALLINFO**](line-callinfo.md) con LINECALLINFOSTATE TREATMENT indica cuándo \_ cambia. El bit LINECALLFEATURE SETTREATMENT del miembro \_ **dwCallFeatures** de [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) indica cuándo se permite a la aplicación cambiar el tratamiento. El conjunto de constantes LINECALLTREATMENT define un conjunto limitado de tratamientos de llamadas predefinidos; los proveedores de \_ servicios pueden definir muchos más.

 

 



