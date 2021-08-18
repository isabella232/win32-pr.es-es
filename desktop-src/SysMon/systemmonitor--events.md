---
title: Eventos SystemMonitor
description: La clase SystemMonitor tiene los siguientes eventos
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3584eed86abcaef019f0fc8f8bd794a80abca1143286317189889231bbc2cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882951"
---
# <a name="systemmonitor-events"></a>Eventos SystemMonitor

La [**clase SystemMonitor**](systemmonitor.md) tiene los siguientes eventos:

-   [**OnCounter Agregado**](systemmonitor-oncounteradded.md)
-   [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
-   [**OnCounterSelected**](-systemmonitor-oncounterselected.md)
-   [**OnDblClick**](-systemmonitor-ondblclick.md)
-   [**OnSampleCollected**](-systemmonitor-onsamplecollected.md)

> [!Note]  
> Debe volver del controlador de eventos antes de que [**expire el intervalo de**](systemmonitor-updateinterval.md) actualización. de lo contrario, SYSMON muestra un cuadro de mensaje que indica al usuario que no pudo muestrear los valores de contador del intervalo de actualización anterior.

 

 

 




