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
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665575"
---
# <a name="systemmonitor-events"></a>Eventos SystemMonitor

La clase [**SystemMonitor**](systemmonitor.md) tiene los siguientes eventos:

-   [**OnCounterAdded**](systemmonitor-oncounteradded.md)
-   [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
-   [**OnCounterSelected**](-systemmonitor-oncounterselected.md)
-   [**OnDblClick**](-systemmonitor-ondblclick.md)
-   [**OnSampleCollected**](-systemmonitor-onsamplecollected.md)

> [!Note]  
> Debe volver del controlador de eventos antes de que expire el [**intervalo de actualización**](systemmonitor-updateinterval.md) ; de lo contrario, SYSMON muestra un cuadro de mensaje que indica al usuario que no pudo muestrear los valores del contador para el intervalo de actualización anterior.

 

 

 




