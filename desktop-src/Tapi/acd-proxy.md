---
description: Un servidor de distribución automática de llamadas (ACD) es una combinación de hardware y software que clasifica, pone en cola y distribuye llamadas entrantes a agentes o llamadas salientes a líneas.
ms.assetid: 29fb0bd7-0ca9-4490-82d2-39550f00a97b
title: Proxy ACD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c345fbcac3ac3471098e964336a0c3135fd1f582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002453"
---
# <a name="acd-proxy"></a>Proxy ACD

Un servidor de distribución automática de llamadas (ACD) es una combinación de hardware y software que clasifica, pone en cola y distribuye llamadas entrantes a agentes o llamadas salientes a líneas.

La aplicación ACD de servidor es una aplicación de proxy TAPI que, para obtener la máxima eficacia, debe ejecutarse en el mismo servidor que el proveedor de servicios de telefonía (TSP). Con un modificador ACD tradicional, la aplicación de proxy tendría que interactuar con el ACD interno del conmutador y exponer su funcionamiento. Una aplicación proxy ACD basada en software o "virtual" sería totalmente responsable del seguimiento de llamadas, colas, grupos y agentes y usaría las interfaces TAPI estándar para controlar el hardware de conmutación. Las aplicaciones cliente del agente normalmente se ejecutan en las estaciones de trabajo del agente individual y usan el proveedor de servicios remotos TAPI para comunicarse con el TAPISRV en el equipo servidor y, por tanto, la aplicación proxy.

La clasificación de las llamadas entrantes está diseñada para recibir una llamada a un agente que podrá controlarla de forma eficaz. La clasificación puede basarse en el número marcado, un sistema de reconocimiento de voz interactivo (IVR) u otros criterios. TAPI usa el concepto de [Grupo ACD](about-call-center-controls.md) para representar esta operación.

Las colas son una manera correcta y esperada de que los centros de llamadas traten los períodos de carga intensos. Normalmente, una cola está asociada a un grupo ACD, pero se puede crear para controlar las líneas de salida o las llamadas entrantes en espera para una aplicación IVR. Consulte [colas](about-call-center-controls.md) para obtener más información.

La distribución de llamadas a agentes o grupos de agentes puede ser uniforme pero normalmente se basa en datos como la información de llamadas, la disponibilidad del agente y la capacidad. El [controlador de agente](about-call-center-controls.md) de TAPI proporciona acceso a información como la disponibilidad y las direcciones del agente para la transferencia de llamadas a los agentes.

Además de la distribución de llamadas básica, un sistema ACD permite administrar e informar sobre el rendimiento del sistema. Las estadísticas recopiladas en las colas de llamadas, los grupos y los agentes se utilizan para refinar y mejorar el rendimiento del sistema y se suelen usar como base para la remuneración del agente.

 

 



