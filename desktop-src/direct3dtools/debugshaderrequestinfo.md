---
description: Representa información sobre una solicitud del depurador de sombreador.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura DebugShaderRequestInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a59bfb84bb7d4e8644c0cfadc4475be7d7da4a54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537342"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span data-ttu-id="d6d08-103"><span id="vspixengine.debugshaderrequestinfo"></span>Estructura DebugShaderRequestInfo</span><span class="sxs-lookup"><span data-stu-id="d6d08-103"><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo structure</span></span>

<span data-ttu-id="d6d08-104">Representa información sobre una solicitud del depurador de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d6d08-104">Represents information about a shader debugger request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d08-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6d08-105">Syntax</span></span>


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a><span data-ttu-id="d6d08-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d6d08-106">Members</span></span>

<span data-ttu-id="d6d08-107">**media**</span><span class="sxs-lookup"><span data-stu-id="d6d08-107">**stage**</span></span>  
<span data-ttu-id="d6d08-108">Fase de canalización que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="d6d08-108">The pipeline stage to debug.</span></span>

<span data-ttu-id="d6d08-109">**eventID**</span><span class="sxs-lookup"><span data-stu-id="d6d08-109">**eventID**</span></span>  
<span data-ttu-id="d6d08-110">IDENTIFICADOR del evento de gráficos que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="d6d08-110">The ID of the graphics event to debug.</span></span>

<span data-ttu-id="d6d08-111">**Númeromarco**</span><span class="sxs-lookup"><span data-stu-id="d6d08-111">**frameNumber**</span></span>  
<span data-ttu-id="d6d08-112">Marco que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="d6d08-112">The frame to debug.</span></span>

<span data-ttu-id="d6d08-113">**vértice**</span><span class="sxs-lookup"><span data-stu-id="d6d08-113">**vertex**</span></span>  
<span data-ttu-id="d6d08-114">El vértice que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="d6d08-114">The vertex to debug.</span></span>

<span data-ttu-id="d6d08-115">**píxel**</span><span class="sxs-lookup"><span data-stu-id="d6d08-115">**pixel**</span></span>  
<span data-ttu-id="d6d08-116">Píxel que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="d6d08-116">The pixel to debug.</span></span>

<span data-ttu-id="d6d08-117">**groupCoordinates**</span><span class="sxs-lookup"><span data-stu-id="d6d08-117">**groupCoordinates**</span></span>  
<span data-ttu-id="d6d08-118">Coordenadas del grupo que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="d6d08-118">The coordinates of the group to debug.</span></span>

<span data-ttu-id="d6d08-119">**threadCoordinates**</span><span class="sxs-lookup"><span data-stu-id="d6d08-119">**threadCoordinates**</span></span>  
<span data-ttu-id="d6d08-120">Coordenadas del subproceso que se va a depurar</span><span class="sxs-lookup"><span data-stu-id="d6d08-120">The coordinates of the thread to debug</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d08-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6d08-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d6d08-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6d08-122">Header</span></span></p></td><td><span data-ttu-id="d6d08-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d6d08-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



