---
description: Representa una descripción de un segmento de textura.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PixEngineTextureSliceDescriptor
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1A183AFB-0BEF-4474-A60C-DBCFA4B34604
api_name:
- PixEngineTextureSliceDescriptor
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b80a23a5ec3340b775c314f66651926743249ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152156"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span data-ttu-id="27d5a-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>Estructura PixEngineTextureSliceDescriptor</span><span class="sxs-lookup"><span data-stu-id="27d5a-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>PixEngineTextureSliceDescriptor structure</span></span>

<span data-ttu-id="27d5a-104">Representa una descripción de un segmento de textura.</span><span class="sxs-lookup"><span data-stu-id="27d5a-104">Represents a description of a texture slice.</span></span>

## <a name="syntax"></a><span data-ttu-id="27d5a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27d5a-105">Syntax</span></span>


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a><span data-ttu-id="27d5a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="27d5a-106">Members</span></span>

<span data-ttu-id="27d5a-107">**width**</span><span class="sxs-lookup"><span data-stu-id="27d5a-107">**width**</span></span>  
<span data-ttu-id="27d5a-108">El ancho (número de muestras en el eje X) del segmento.</span><span class="sxs-lookup"><span data-stu-id="27d5a-108">The width (number of samples in the X axis) of the slice.</span></span>

<span data-ttu-id="27d5a-109">**height**</span><span class="sxs-lookup"><span data-stu-id="27d5a-109">**height**</span></span>  
<span data-ttu-id="27d5a-110">Alto (número de muestras en el eje Y) del segmento.</span><span class="sxs-lookup"><span data-stu-id="27d5a-110">The height (number of samples in the Y axis) of the slice.</span></span>

<span data-ttu-id="27d5a-111">**blockRowBytes**</span><span class="sxs-lookup"><span data-stu-id="27d5a-111">**blockRowBytes**</span></span>  
<span data-ttu-id="27d5a-112">El número de bytes por fila en cada bloque.</span><span class="sxs-lookup"><span data-stu-id="27d5a-112">The number of bytes per row in each block.</span></span>

<span data-ttu-id="27d5a-113">**offset**</span><span class="sxs-lookup"><span data-stu-id="27d5a-113">**offset**</span></span>  
<span data-ttu-id="27d5a-114">Desplazamiento del segmento dentro de toda la textura.</span><span class="sxs-lookup"><span data-stu-id="27d5a-114">The offset of the slice within the whole texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="27d5a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27d5a-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="27d5a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27d5a-116">Header</span></span></p></td><td><span data-ttu-id="27d5a-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="27d5a-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



