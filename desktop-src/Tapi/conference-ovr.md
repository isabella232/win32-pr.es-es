---
description: Las conferencias avanzadas que usan redes basadas en IP se describen en la Conferencia de telefonía IP de 3s Rendezvous de TAPI. El material siguiente se relaciona con las conferencias básicas.
ms.assetid: f685097b-1b54-412b-999f-d9bdb3120ab9
title: Ferenc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace4cb45bf74335298a3d4d262d064eb85c547f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677487"
---
# <a name="conference"></a>Ferenc

Las conferencias avanzadas que usan redes basadas en IP se describen en [conferencias de telefonía IP de encuentro](rendezvous-ip-telephony-conferencing.md)de TAPI 3. El material siguiente se relaciona con las conferencias básicas.

Las sesiones de conferencia son sesiones que incluyen más de dos partes simultáneamente. Se pueden configurar mediante un puente externo basado en servidor o un puente de conferencia basado en conmutadores.

En las sesiones de conferencia basadas en servidor, todas las partes participantes marcan el servidor, que combina los flujos multimedia y envía la mezcla a cada participante. No puede haber ninguna noción de partes individuales en la llamada de conferencia, solo la de una llamada única entre la aplicación y el servidor de puente. En TAPI, este tipo de llamada de conferencia parece ser una conexión de uno a uno normal.

Las conferencias basadas en conmutadores continúan en fases, algunas de las cuales se pueden combinar si el proveedor de servicios lo admite:

1.  Inicie una sesión de comunicaciones ordinaria.
2.  Cree una sesión de conferencia con su primer miembro de la entidad que inició la Conferencia.
3.  Cree una sesión de consulta de conferencias con la entidad en el otro extremo de la conexión actual.
4.  Agregue la sesión de consulta a la Conferencia.

Una vez que una sesión se convierte en miembro de una conferencia, el estado del miembro se revierte a la Conferencia. El estado de la sesión de conferencia suele estar *conectado*. Los identificadores de sesión de la Conferencia y todas las entidades agregadas siguen siendo válidos. Se pueden recibir eventos de estado acerca de todas las llamadas. Por ejemplo, si uno de los miembros se desconecta al colgar, un mensaje de estado adecuado puede informar a la aplicación de este hecho.

**TAPI 2. x:** Las aplicaciones pueden usar la característica "no incluir conferencia" de PBX mediante la \_ opción NOHOLDCONFERENCE de LINECALLPARAMFLAGS; esta característica permite adjuntar de forma silenciosa otro dispositivo, como un supervisor o un dispositivo de registro, a la línea.

Al cancelar la sesión de consulta a terceros para una conferencia o al quitar el tercero de una conferencia establecida previamente, el proveedor de servicios puede liberar la Conferencia y volver a revertir la sesión a una conexión de dos entidades normal. En este caso, la sesión de conferencia pasará al estado *inactivo* y la única sesión participante restante pasará de la Conferencia al estado *conectado* .

No todos los proveedores de servicios admiten conferencias.

**TAPI 2. x:** La función [**lineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference) toma la llamada de dos entidades original como entrada, asigna una llamada de conferencia, conecta la llamada original a la Conferencia y asigna una llamada de consulta cuyo identificador se devuelve a la aplicación.

Si la aplicación va a agregar otro miembro a la Conferencia, se puede realizar una operación de marcado en la llamada de consulta. El identificador de llamada de conferencia y la conexión de llamada de consulta se usan en la función [**lineAddToConference**](/windows/win32/api/tapi/nf-tapi-lineaddtoconference) . También se pueden agregar miembros de Conferencia mediante la función [**linePrepareAddToConference**](/windows/win32/api/tapi/nf-tapi-lineprepareaddtoconference) , si el proveedor de servicios lo admite.

Los miembros de la Conferencia se quitan mediante la función [**lineRemoveFromConference**](/windows/win32/api/tapi/nf-tapi-lineremovefromconference) , si el proveedor de servicios lo admite.

Como alternativa, se puede crear una conferencia mediante la función [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer) , que devuelve un identificador de llamada de consulta y la función [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer) con la opción Conference (en lugar de la opción [Transfer](transfer-ovr.md) ).

**TAPI 3. x:** El método [**ITBasicCallControl:: Conference**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-conference) toma la sesión existente como entrada y crea un [objeto CallHub](callhub-object.md) si todavía no existe uno. El método [**ITBasicCallControl:: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) agrega la llamada de consulta a CallHub. Las sesiones de consulta adicionales se pueden crear mediante [**ITAddress:: CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)y se agregan mediante los métodos **Conference** y **Finish** .

> [!Note]  
> Las capacidades del dispositivo de línea de dirección pueden limitar el número de entidades que se celebran en una sola llamada y si una conferencia comienza o no con una llamada normal de dos partes.

 

 

 
