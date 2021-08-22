---
description: La supervisión y el control del estado del agente ACD en estaciones se admiten a través de estas funciones lineGetAgentCaps lineGetAgentStatus lineGetAgentGroupList lineGetAgentActivityList lineSetAgentGroup lineSetAgentState y lineSetAgentActivity.
ms.assetid: 2851fe54-f807-4cef-b6ca-2dcc7e1ae6fb
title: Supervisión y control del agente de ACD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8986fc31e8b30e8b32c4b347a26abfa46adbd426c20c506553ae2f41ea879a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872662"
---
# <a name="acd-agent-monitoring-and-control"></a>Supervisión y control del agente de ACD

La supervisión y el control del estado del agente ACD en las estaciones se admiten mediante estas funciones: [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa), [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa), [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista), [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista), [**lineSetAgentGroup,**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup) [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)y [**lineSetAgentActivity.**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)

El [**mensaje LINE \_ AGENTSTATUS**](line-agentstatus.md) se usa para indicar cuándo ha cambiado la información del agente.

Estos controles están asociados a una dirección en lugar de a una línea porque muchos sistemas ACD se implementan con diferentes colas de ACD asociadas a botones en el terminal del teléfono (y apariencias de llamadas independientes). Además, los teléfonos del agente de ACD a menudo pueden tener apariencias de llamadas independientes para las llamadas personales.

En la arquitectura, la funcionalidad de ACD debe implementarse en una aplicación basada en servidor. Las funciones de cliente mencionadas anteriormente, en lugar de asignarse al proveedor de servicios de telefonía, se transmiten a una aplicación de servidor que se ha registrado (mediante una opción [**de lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)) como controlador para dichas funciones. El [**mensaje \_ LINE PROXYREQUEST**](line-proxyrequest.md) se usa para señalar a la aplicación de controlador cuando se ha realizado una solicitud; llama a la función [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para devolver resultados y datos. Las aplicaciones de controlador también pueden llamar [**a lineProxyMessage para**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) generar mensajes \_ LINE AGENTSTATUS cuando sea necesario. En el caso de una instancia heredada de SWITCH o un ACD independiente que implemente la propia funcionalidad de ACD, el proveedor de servicios de telefonía para el conmutador debe incluir una aplicación de servidor proxy que acepte las solicitudes y las enruta (posiblemente mediante funciones [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) o una interfaz privada) al proveedor de servicios, que las enruta al conmutador.

 

 



