---
description: Representa los campos de diseño de entrada de un búfer de vértice, uno por campo en el búfer de vértices.
MS-HAID: vspixengine.InputLayoutStruct
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura InputLayoutStruct
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC7AAC2F-FDB1-4AD8-9B87-A97EE557FEAC
api_name:
- InputLayoutStruct
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1369d80d202682b67eacbb184b215d9da1711874
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714695"
---
# <a name="span-idvspixengineinputlayoutstructspaninputlayoutstruct-structure"></a><span data-ttu-id="82bd9-103"><span id="vspixengine.inputlayoutstruct"></span>Estructura InputLayoutStruct</span><span class="sxs-lookup"><span data-stu-id="82bd9-103"><span id="vspixengine.inputlayoutstruct"></span>InputLayoutStruct structure</span></span>

<span data-ttu-id="82bd9-104">Representa los campos de diseño de entrada de un búfer de vértice, uno por campo en el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="82bd9-104">Represents the input layout fields of a vertex buffer, one per field in the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="82bd9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82bd9-105">Syntax</span></span>


```C++
} InputLayoutStruct;
```

## <a name="members"></a><span data-ttu-id="82bd9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="82bd9-106">Members</span></span>

<span data-ttu-id="82bd9-107">**SemanticName**</span><span class="sxs-lookup"><span data-stu-id="82bd9-107">**SemanticName**</span></span>  
<span data-ttu-id="82bd9-108">Cadena COM que contiene el nombre de la semántica asociada.</span><span class="sxs-lookup"><span data-stu-id="82bd9-108">A COM string containing the name of the associated semantic.</span></span>

<span data-ttu-id="82bd9-109">**SemanticIndex**</span><span class="sxs-lookup"><span data-stu-id="82bd9-109">**SemanticIndex**</span></span>  
<span data-ttu-id="82bd9-110">Índice de la semántica asociada.</span><span class="sxs-lookup"><span data-stu-id="82bd9-110">The index of the associated semantic.</span></span>

<span data-ttu-id="82bd9-111">**Format**</span><span class="sxs-lookup"><span data-stu-id="82bd9-111">**Format**</span></span>  
<span data-ttu-id="82bd9-112">Formato del campo.</span><span class="sxs-lookup"><span data-stu-id="82bd9-112">The format of the field.</span></span> <span data-ttu-id="82bd9-113">Para obtener más información, consulte la \_ enumeración de formato de DXGI.</span><span class="sxs-lookup"><span data-stu-id="82bd9-113">For more information see the DXGI\_FORMAT enumeration.</span></span>

<span data-ttu-id="82bd9-114">**InputSlot**</span><span class="sxs-lookup"><span data-stu-id="82bd9-114">**InputSlot**</span></span>  
<span data-ttu-id="82bd9-115">La ranura de entrada asociada.</span><span class="sxs-lookup"><span data-stu-id="82bd9-115">The associated input slot.</span></span>

<span data-ttu-id="82bd9-116">**AlignedByteOffset**</span><span class="sxs-lookup"><span data-stu-id="82bd9-116">**AlignedByteOffset**</span></span>  

<span data-ttu-id="82bd9-117">**InputSlotClass**</span><span class="sxs-lookup"><span data-stu-id="82bd9-117">**InputSlotClass**</span></span>  

<span data-ttu-id="82bd9-118">**InstanceDataStepRate**</span><span class="sxs-lookup"><span data-stu-id="82bd9-118">**InstanceDataStepRate**</span></span>  

## <a name="requirements"></a><span data-ttu-id="82bd9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82bd9-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="82bd9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82bd9-120">Header</span></span></p></td><td><span data-ttu-id="82bd9-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="82bd9-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



