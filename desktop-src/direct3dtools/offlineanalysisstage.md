---
description: Una enumeración que se usa para indicar las fases de progreso en el análisis de fotogramas.
MS-HAID: vspixengine.OFFLINEANALYSISSTAGE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración OFFLINEANALYSISSTAGE
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85D0288C-113A-4ABE-8EDB-ABB8F009956A
api_name:
- OFFLINEANALYSISSTAGE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf12b70acf70a654fe74b23d4bd3a196467797fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537180"
---
# <a name="span-idvspixengineofflineanalysisstagespanofflineanalysisstage-enumeration"></a><span id="vspixengine.offlineanalysisstage"></span>Enumeración OFFLINEANALYSISSTAGE

Una enumeración que se usa para indicar las fases de progreso en el análisis de fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage \_ NotStarted**  
No se ha iniciado aún el análisis de fotogramas.

<span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**\_Inicialización de OfflineAnalysisStage**  
Inicialización de análisis de fotogramas (solicitud emitida).

<span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage \_ inicializando \_ LinkOk**  
Inicialización de análisis de fotogramas (vínculo establecido).

<span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage \_ inicializando \_ ManifestOk**  
Inicialización del análisis de fotogramas (el manifiesto se analizó correctamente).

<span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage \_ inicializando \_ ToolOk**  
Inicialización de análisis de fotogramas (carga de analizador).

<span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**OfflineAnalysisStage \_ analizar**  
El análisis de fotogramas se está ejecutando.

<span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage \_ AnalysisCompleted**  
Análisis de fotogramas completado (evento ' complete ' enviado).

<span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage \_ AnalysisCompleted se \_ completó correctamente**  
El análisis de fotogramas se completó correctamente.

<span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage \_ AnalysisCompleted \_ OutputFileExists**  
Se completó el análisis de fotogramas y el archivo de salida.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



