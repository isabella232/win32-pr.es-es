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
# <a name="span-idvspixengineofflineanalysisstagespanofflineanalysisstage-enumeration"></a><span data-ttu-id="013fd-103"><span id="vspixengine.offlineanalysisstage"></span>Enumeración OFFLINEANALYSISSTAGE</span><span class="sxs-lookup"><span data-stu-id="013fd-103"><span id="vspixengine.offlineanalysisstage"></span>OFFLINEANALYSISSTAGE enumeration</span></span>

<span data-ttu-id="013fd-104">Una enumeración que se usa para indicar las fases de progreso en el análisis de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="013fd-104">An enum used to indicate stages of progress in frame analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="013fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="013fd-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="013fd-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="013fd-106">Constants</span></span>

<span data-ttu-id="013fd-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage \_ NotStarted**</span><span class="sxs-lookup"><span data-stu-id="013fd-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage\_NotStarted**</span></span>  
<span data-ttu-id="013fd-108">No se ha iniciado aún el análisis de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="013fd-108">Frame analysis not yet started.</span></span>

<span data-ttu-id="013fd-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**\_Inicialización de OfflineAnalysisStage**</span><span class="sxs-lookup"><span data-stu-id="013fd-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**OfflineAnalysisStage\_Initializing**</span></span>  
<span data-ttu-id="013fd-110">Inicialización de análisis de fotogramas (solicitud emitida).</span><span class="sxs-lookup"><span data-stu-id="013fd-110">Frame analysis initializing (request issued).</span></span>

<span data-ttu-id="013fd-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage \_ inicializando \_ LinkOk**</span><span class="sxs-lookup"><span data-stu-id="013fd-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage\_Initializing\_LinkOk**</span></span>  
<span data-ttu-id="013fd-112">Inicialización de análisis de fotogramas (vínculo establecido).</span><span class="sxs-lookup"><span data-stu-id="013fd-112">Frame analysis initializing (link established).</span></span>

<span data-ttu-id="013fd-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage \_ inicializando \_ ManifestOk**</span><span class="sxs-lookup"><span data-stu-id="013fd-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage\_Initializing\_ManifestOk**</span></span>  
<span data-ttu-id="013fd-114">Inicialización del análisis de fotogramas (el manifiesto se analizó correctamente).</span><span class="sxs-lookup"><span data-stu-id="013fd-114">Frame analysis initializing (manifest parsed successfully).</span></span>

<span data-ttu-id="013fd-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage \_ inicializando \_ ToolOk**</span><span class="sxs-lookup"><span data-stu-id="013fd-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage\_Initializing\_ToolOk**</span></span>  
<span data-ttu-id="013fd-116">Inicialización de análisis de fotogramas (carga de analizador).</span><span class="sxs-lookup"><span data-stu-id="013fd-116">Frame analysis initializing (analyzer loading).</span></span>

<span data-ttu-id="013fd-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**OfflineAnalysisStage \_ analizar**</span><span class="sxs-lookup"><span data-stu-id="013fd-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**OfflineAnalysisStage\_Analyzing**</span></span>  
<span data-ttu-id="013fd-118">El análisis de fotogramas se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="013fd-118">Frame analysis is running.</span></span>

<span data-ttu-id="013fd-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage \_ AnalysisCompleted**</span><span class="sxs-lookup"><span data-stu-id="013fd-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage\_AnalysisCompleted**</span></span>  
<span data-ttu-id="013fd-120">Análisis de fotogramas completado (evento ' complete ' enviado).</span><span class="sxs-lookup"><span data-stu-id="013fd-120">Frame analysis completed ('complete' event sent).</span></span>

<span data-ttu-id="013fd-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage \_ AnalysisCompleted se \_ completó correctamente**</span><span class="sxs-lookup"><span data-stu-id="013fd-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage\_AnalysisCompleted\_Successful**</span></span>  
<span data-ttu-id="013fd-122">El análisis de fotogramas se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="013fd-122">Frame analysis completed successfully.</span></span>

<span data-ttu-id="013fd-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage \_ AnalysisCompleted \_ OutputFileExists**</span><span class="sxs-lookup"><span data-stu-id="013fd-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage\_AnalysisCompleted\_OutputFileExists**</span></span>  
<span data-ttu-id="013fd-124">Se completó el análisis de fotogramas y el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="013fd-124">Frame analysis completed and output file exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="013fd-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="013fd-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="013fd-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="013fd-126">Header</span></span></p></td><td><span data-ttu-id="013fd-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="013fd-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



