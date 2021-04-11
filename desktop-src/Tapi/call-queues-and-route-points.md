---
description: Una cola de llamadas o un punto de ruta es una dirección especial dentro del conmutador en la que las llamadas se mantienen temporalmente como acciones pendientes.
ms.assetid: 1c801401-be05-4b5f-bc4f-628dde0f3cf7
title: Colas de llamadas y puntos de ruta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66895101b72ca8e16810d3766edf897efcfedddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276678"
---
# <a name="call-queues-and-route-points"></a>Colas de llamadas y puntos de ruta

Una cola de llamadas o un punto de ruta es una dirección especial dentro del conmutador en la que las llamadas se mantienen temporalmente como acciones pendientes. Esta característica se representa mediante la cola de bits LINEADDRCAPFLAGS \_ y LINEADDRCAPFLAGS \_ ROUTEPOINT en el miembro **dwAddrCapFlags** en [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). Todas las llamadas que aparecen en dicha dirección esperan la acción de la aplicación y puede haber acciones predeterminadas que tienen lugar (por ejemplo, transferir a un agente o tronco) si la aplicación no realiza ninguna acción dentro de un período de tiempo definido. El administrador del sistema debe configurar la aplicación para que sepa qué acciones debe realizar en lo que respecta a las llamadas que aparecen en cada dirección de punto de ruta o cola, y la cantidad de tiempo disponible para decidir la acción que se debe llevar a cabo.

Las aplicaciones pueden determinar el número de llamadas pendientes en una cola o un punto de ruta mediante [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus). La función [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) se puede utilizar para obtener información como el identificador de llamada, el identificador, el origen entrante o saliente, etc., y que la aplicación usa para tomar decisiones sobre el control de llamadas. las llamadas se pueden redirigir, invidentes, descartar, etc., o bien se les permite pasar automáticamente de la cola a un destino. Una llamada va a LINECALLSTATE \_ DESconectada si se abandona. Las llamadas van *inactivas* cuando salen de la cola; **lineGetCallInfo** se puede usar para leer el identificador de redirección para determinar dónde se transfirieron.

Algunos modificadores permiten llamadas en una cola o en espera para recibir un tratamiento concreto como el silencio, el timbre, la señal de ocupación, la música o la escucha de un anuncio grabado. La función [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) permite que la aplicación controle el tratamiento. La estructura delimitada por los miembros **dwCallTreatmentListSize** y **dwCallTreatmentListOffset** de [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) permite a las aplicaciones determinar los tratamientos admitidos. El miembro **dwCallTreatment** de [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) indica el tratamiento actual y un mensaje de [**línea \_ CALLINFO**](line-callinfo.md) con el tratamiento de LINECALLINFOSTATE \_ indica cuándo cambia. El \_ bit LINECALLFEATURE SETTREATMENT en el miembro **DwCallFeatures** de [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) indica cuándo se permite a la aplicación cambiar el tratamiento. El \_ conjunto LINECALLTREATMENT de constantes define un conjunto limitado de tratamientos de llamadas predefinidos; los proveedores de servicios pueden definir muchos más.

 

 



