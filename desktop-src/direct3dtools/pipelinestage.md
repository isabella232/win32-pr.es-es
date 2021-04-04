---
description: Representa una fase de canalización, incluidos los detalles del sombreador utilizado.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PipeLineStage
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997799"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span data-ttu-id="435dc-103"><span id="vspixengine.pipelinestage"></span>Estructura PipeLineStage</span><span class="sxs-lookup"><span data-stu-id="435dc-103"><span id="vspixengine.pipelinestage"></span>PipeLineStage structure</span></span>

<span data-ttu-id="435dc-104">Representa una fase de canalización, incluidos los detalles del sombreador utilizado.</span><span class="sxs-lookup"><span data-stu-id="435dc-104">Represents a pipeline stage, including details of the shader used.</span></span>

## <a name="syntax"></a><span data-ttu-id="435dc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="435dc-105">Syntax</span></span>


```C++
} PipeLineStage;
```

## <a name="members"></a><span data-ttu-id="435dc-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="435dc-106">Members</span></span>

<span data-ttu-id="435dc-107">**StageId**</span><span class="sxs-lookup"><span data-stu-id="435dc-107">**StageId**</span></span>  
<span data-ttu-id="435dc-108">IDENTIFICADOR de la fase de canalización.</span><span class="sxs-lookup"><span data-stu-id="435dc-108">The ID of the pipeline stage.</span></span>

<span data-ttu-id="435dc-109">**Depurable**</span><span class="sxs-lookup"><span data-stu-id="435dc-109">**Debuggable**</span></span>  
<span data-ttu-id="435dc-110">True si la fase de canalización admite la depuración; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="435dc-110">true if the pipeline stage supports debugging; otherwise, false.</span></span>

<span data-ttu-id="435dc-111">**StageName**</span><span class="sxs-lookup"><span data-stu-id="435dc-111">**StageName**</span></span>  
<span data-ttu-id="435dc-112">Cadena COM que contiene el nombre de la fase de canalización.</span><span class="sxs-lookup"><span data-stu-id="435dc-112">A COM string containing the name of the pipeline stage.</span></span>

<span data-ttu-id="435dc-113">**GuaranteedOutput**</span><span class="sxs-lookup"><span data-stu-id="435dc-113">**GuaranteedOutput**</span></span>  
<span data-ttu-id="435dc-114">True si la fase de canalización siempre tiene una salida de canalización; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="435dc-114">true if the pipeline stage always has pipeline output; otherwise, false.</span></span>

<span data-ttu-id="435dc-115">**DebugEntryPoint**</span><span class="sxs-lookup"><span data-stu-id="435dc-115">**DebugEntryPoint**</span></span>  
<span data-ttu-id="435dc-116">Cadena COM que contiene el nombre del punto de entrada del sombreador, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="435dc-116">A COM string containing the name of the shader entry point, if there is one.</span></span>

<span data-ttu-id="435dc-117">**ShaderFile**</span><span class="sxs-lookup"><span data-stu-id="435dc-117">**ShaderFile**</span></span>  
<span data-ttu-id="435dc-118">Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador.</span><span class="sxs-lookup"><span data-stu-id="435dc-118">A COM string containing the filepath of the shader source file.</span></span>

<span data-ttu-id="435dc-119">**ShaderByteStreamPtr**</span><span class="sxs-lookup"><span data-stu-id="435dc-119">**ShaderByteStreamPtr**</span></span>  
<span data-ttu-id="435dc-120">Un FILEPTR para la secuencia de bytes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="435dc-120">A FILEPTR for the shader byte stream.</span></span> <span data-ttu-id="435dc-121">Esto se devuelve para depurar.</span><span class="sxs-lookup"><span data-stu-id="435dc-121">This is passed back in order to debug.</span></span>

## <a name="requirements"></a><span data-ttu-id="435dc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="435dc-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="435dc-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="435dc-123">Header</span></span></p></td><td><span data-ttu-id="435dc-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="435dc-124">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



