---
description: Representa la información del desencadenador del experimento.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura ExperimentTrigger
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906564"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span data-ttu-id="8a302-103"><span id="vspixengine.experimenttrigger"></span>Estructura ExperimentTrigger</span><span class="sxs-lookup"><span data-stu-id="8a302-103"><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger structure</span></span>

<span data-ttu-id="8a302-104">Representa la información del desencadenador del experimento.</span><span class="sxs-lookup"><span data-stu-id="8a302-104">Represents experiment trigger information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a302-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a302-105">Syntax</span></span>


```C++
} ExperimentTrigger;
```

## <a name="members"></a><span data-ttu-id="8a302-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a302-106">Members</span></span>

<span data-ttu-id="8a302-107">**type**</span><span class="sxs-lookup"><span data-stu-id="8a302-107">**type**</span></span>  
<span data-ttu-id="8a302-108">El tipo de experimento (captura) desencadenado.</span><span class="sxs-lookup"><span data-stu-id="8a302-108">The kind of experiment (capture) triggered.</span></span>

<span data-ttu-id="8a302-109">**key**</span><span class="sxs-lookup"><span data-stu-id="8a302-109">**key**</span></span>  
<span data-ttu-id="8a302-110">Cuando el tipo es igual a EXPERIMENTTRIGGERTYPE:: KEY, la clave utilizada para desencadenar la captura.</span><span class="sxs-lookup"><span data-stu-id="8a302-110">When type is equal to EXPERIMENTTRIGGERTYPE::KEY, the key used to trigger capture.</span></span>

<span data-ttu-id="8a302-111">**Númeromarco**</span><span class="sxs-lookup"><span data-stu-id="8a302-111">**frameNumber**</span></span>  
<span data-ttu-id="8a302-112">Cuando el tipo es igual a EXPERIMENTTRIGGERTYPE:: NÚMEROMARCO, el número de marco que desencadenará la captura.</span><span class="sxs-lookup"><span data-stu-id="8a302-112">When type is equal to EXPERIMENTTRIGGERTYPE::FRAMENUMBER, the frame number that will trigger capture.</span></span>

<span data-ttu-id="8a302-113">**captureCount**</span><span class="sxs-lookup"><span data-stu-id="8a302-113">**captureCount**</span></span>  
<span data-ttu-id="8a302-114">Número de fotogramas secuenciales que se van a capturar.</span><span class="sxs-lookup"><span data-stu-id="8a302-114">The number of sequential frames to capture.</span></span>

<span data-ttu-id="8a302-115">**actionIID**</span><span class="sxs-lookup"><span data-stu-id="8a302-115">**actionIID**</span></span>  
<span data-ttu-id="8a302-116">IDENTIFICADOR del evento de acción (captura de pantalla, captura de fotogramas, etc.).</span><span class="sxs-lookup"><span data-stu-id="8a302-116">The ID of the action event (screenshot, frame capture, etc).</span></span>

<span data-ttu-id="8a302-117">**actionPlayload**</span><span class="sxs-lookup"><span data-stu-id="8a302-117">**actionPlayload**</span></span>  
<span data-ttu-id="8a302-118">Puntero a la carga del evento de acción.</span><span class="sxs-lookup"><span data-stu-id="8a302-118">A pointer to the action event payload.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a302-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a302-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8a302-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a302-120">Header</span></span></p></td><td><span data-ttu-id="8a302-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8a302-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



