---
description: La supervisión y el control del estado del agente ACD en las estaciones se admiten a través de estas funciones lineGetAgentCaps lineGetAgentStatus lineGetAgentGroupList lineGetAgentActivityList lineSetAgentGroup lineSetAgentState y lineSetAgentActivity.
ms.assetid: 2851fe54-f807-4cef-b6ca-2dcc7e1ae6fb
title: Supervisión y control del agente ACD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52d3cf9387819bada069920099b19da65e6a1e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083077"
---
# <a name="acd-agent-monitoring-and-control"></a>Supervisión y control del agente ACD

La supervisión y el control del estado del agente ACD en las estaciones se admiten a través de estas funciones: [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa), [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa), [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista), [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista), [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup), [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)y [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).

El mensaje [**line \_ AGENTSTATUS**](line-agentstatus.md) se usa para indicar cuándo ha cambiado la información del agente.

Estos controles se asocian con una dirección en lugar de una línea porque muchos sistemas ACD se implementan con diferentes colas de ACD asociadas a botones en el terminal telefónico (y aspectos de la llamada independientes). Además, los teléfonos del agente ACD pueden tener a menudo aspectos de llamadas independientes para llamadas personales.

Arquitectónicamente, la funcionalidad ACD debe implementarse en una aplicación basada en servidor. Las funciones de cliente mencionadas anteriormente, en lugar de asignarse al proveedor de servicios de telefonía, se transmiten a una aplicación de servidor que ha registrado (mediante una opción de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)) como un controlador para estas funciones. El mensaje [**line \_ PROXYREQUEST**](line-proxyrequest.md) se usa para indicar a la aplicación de controlador cuando se ha realizado una solicitud; llama a la función [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para devolver los resultados y los datos. Las aplicaciones de controlador también pueden llamar a [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) para generar mensajes de línea \_ AGENTSTATUS cuando sea necesario. En el caso de una PBX heredada o un ACD independiente que implementa la funcionalidad de ACD, el proveedor de servicios de telefonía para el conmutador debe incluir una aplicación de servidor proxy que acepte las solicitudes y las enrute (posiblemente mediante funciones [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) o una interfaz privada) al proveedor de servicios, que las enruta al conmutador.

 

 



