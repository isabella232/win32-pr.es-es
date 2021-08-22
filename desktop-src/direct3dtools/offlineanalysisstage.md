---
description: Enumeración que se usa para indicar las fases de progreso en el análisis de fotogramas.
MS-HAID: vspixengine.OFFLINEANALYSISSTAGE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: OFFLINEANALYSISSTAGE (enumeración)
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
ms.openlocfilehash: a431de8d45666bb03f6841da895ceaebecb6ebfa1b8f5ac1b4daa5a11893e11f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119239685"
---
# <a name="span-idvspixengineofflineanalysisstagespanofflineanalysisstage-enumeration"></a><span id="vspixengine.offlineanalysisstage"></span>OFFLINEANALYSISSTAGE (enumeración)

Enumeración que se usa para indicar las fases de progreso en el análisis de fotogramas.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage \_ NotStarted**  
El análisis de fotogramas aún no se ha iniciado.

<span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**OfflineAnalysisStage \_ Initializing**  
Inicialización del análisis de fotogramas (solicitud emitida).

<span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage \_ Initializing \_ LinkOk**  
Inicialización del análisis de fotogramas (vínculo establecido).

<span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage \_ Initializing \_ ManifestOk**  
Inicialización del análisis de fotogramas (manifiesto analizado correctamente).

<span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage \_ Initializing \_ ToolOk**  
Inicialización del análisis de fotogramas (carga del analizador).

<span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**Análisis de \_ OfflineAnalysisStage**  
Se está ejecutando el análisis de fotogramas.

<span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage \_ AnalysisCompleted**  
Se completó el análisis de fotogramas (se envió el evento "complete").

<span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage \_ AnalysisCompleted \_ Successful**  
El análisis de fotogramas se completó correctamente.

<span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage \_ AnalysisCompleted \_ OutputFileExists**  
Se completó el análisis de fotogramas y existe el archivo de salida.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



