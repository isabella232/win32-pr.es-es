---
description: Representa el índice de un segmento de textura.
MS-HAID: vspixengine.PixEngineTextureSliceIndex
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PixEngineTextureSliceIndex
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 127765F7-4EBF-4B66-9491-A6FE9DC673C8
api_name:
- PixEngineTextureSliceIndex
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0fd954b5ba9d4dd20f35245350857352bc9b8ae3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705217"
---
# <a name="span-idvspixenginepixenginetexturesliceindexspanpixenginetexturesliceindex-structure"></a><span data-ttu-id="d69fd-103"><span id="vspixengine.pixenginetexturesliceindex"></span>Estructura PixEngineTextureSliceIndex</span><span class="sxs-lookup"><span data-stu-id="d69fd-103"><span id="vspixengine.pixenginetexturesliceindex"></span>PixEngineTextureSliceIndex structure</span></span>

<span data-ttu-id="d69fd-104">Representa el índice de un segmento de textura.</span><span class="sxs-lookup"><span data-stu-id="d69fd-104">Represents the index of a texture slice</span></span>

## <a name="syntax"></a><span data-ttu-id="d69fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d69fd-105">Syntax</span></span>


```C++
} PixEngineTextureSliceIndex;
```

## <a name="members"></a><span data-ttu-id="d69fd-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d69fd-106">Members</span></span>

<span data-ttu-id="d69fd-107">**arrayIndex**</span><span class="sxs-lookup"><span data-stu-id="d69fd-107">**arrayIndex**</span></span>  
<span data-ttu-id="d69fd-108">Cuando la textura es una matriz de textura, el índice de la matriz del segmento.</span><span class="sxs-lookup"><span data-stu-id="d69fd-108">When the texture is a texture array, the array index of the slice.</span></span>

<span data-ttu-id="d69fd-109">**mipmapLevel**</span><span class="sxs-lookup"><span data-stu-id="d69fd-109">**mipmapLevel**</span></span>  
<span data-ttu-id="d69fd-110">Nivel de mipmap del segmento.</span><span class="sxs-lookup"><span data-stu-id="d69fd-110">The mipmap level of the slice.</span></span>

<span data-ttu-id="d69fd-111">**sampleIndex**</span><span class="sxs-lookup"><span data-stu-id="d69fd-111">**sampleIndex**</span></span>  
<span data-ttu-id="d69fd-112">Índice de ejemplo del segmento.</span><span class="sxs-lookup"><span data-stu-id="d69fd-112">The sample index of the slice.</span></span>

<span data-ttu-id="d69fd-113">**zSlice**</span><span class="sxs-lookup"><span data-stu-id="d69fd-113">**zSlice**</span></span>  
<span data-ttu-id="d69fd-114">Profundidad (z) del segmento.</span><span class="sxs-lookup"><span data-stu-id="d69fd-114">The depth (z) of the slice.</span></span>

## <a name="requirements"></a><span data-ttu-id="d69fd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d69fd-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d69fd-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d69fd-116">Header</span></span></p></td><td><span data-ttu-id="d69fd-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d69fd-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



