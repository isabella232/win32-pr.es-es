---
description: Un servidor de distribución automática de llamadas (ACD) es una combinación de hardware y software que clasifica, pone en cola y distribuye las llamadas entrantes a los agentes o las llamadas salientes a las líneas.
ms.assetid: 29fb0bd7-0ca9-4490-82d2-39550f00a97b
title: ACD Proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7af989994a19612612dcba52b72f84946ca886a3a4b775dd2b1c23b53f83a648
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949245"
---
# <a name="acd-proxy"></a>ACD Proxy

Un servidor de distribución automática de llamadas (ACD) es una combinación de hardware y software que clasifica, pone en cola y distribuye las llamadas entrantes a los agentes o las llamadas salientes a las líneas.

La aplicación Server ACD es una aplicación de proxy TAPI, que para obtener la máxima eficacia debe ejecutarse en el mismo servidor que el proveedor de servicios de telefonía (TSP). Con un conmutador ACD tradicional, la aplicación de proxy se interfazría con el ACD interno del conmutador y expondría su funcionamiento. Una aplicación de proxy ACD basada en software o "virtual" sería totalmente responsable del seguimiento de llamadas, colas, grupos y agentes, y usaría las interfaces TAPI estándar para controlar el hardware de conmutación. Las aplicaciones cliente del agente normalmente se ejecutarán en las estaciones de trabajo del agente individual y usarán el proveedor de servicios remotos TAPI para comunicarse con TAPISRV en el equipo del servidor y, por tanto, la aplicación proxy.

La clasificación de las llamadas entrantes está diseñada para obtener una llamada a un agente que podrá controlarla de forma eficaz. La clasificación puede basarse en el número marcado, un sistema de reconocimiento de voz interactivo (IVR) u otros criterios. TAPI usa el concepto de un [grupo ACD para](about-call-center-controls.md) representar esta operación.

Las colas son una manera correcta y esperada de que los centros de llamadas se desasociarán con períodos de carga pesados. Normalmente, una cola está asociada a un grupo de ACD, pero se puede crear para controlar las líneas salientes o las llamadas entrantes que esperan una aplicación IVR. Consulte [Colas para](about-call-center-controls.md) obtener más información.

La distribución de llamadas a agentes o grupos de agentes puede ser uniforme, pero normalmente se basa en datos como la información de llamadas, la disponibilidad del agente y la capacidad. El controlador de agentes [de](about-call-center-controls.md) TAPI proporciona acceso a información como la disponibilidad del agente y las direcciones para la transferencia de llamadas a agentes.

Además de la distribución básica de llamadas, un sistema ACD proporciona para administrar e informar sobre el rendimiento del sistema. Las estadísticas recopiladas en colas de llamadas, grupos y agentes se usan para refinar y mejorar el rendimiento del sistema y normalmente se usan como base para la limpieza del agente.

 

 



