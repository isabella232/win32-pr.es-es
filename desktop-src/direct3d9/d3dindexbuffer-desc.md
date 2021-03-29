---
description: Describe un búfer de índice.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: D3DINDEXBUFFER_DESC estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003846"
---
# <a name="d3dindexbuffer_desc-structure"></a><span data-ttu-id="be9ab-103">D3DINDEXBUFFER \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="be9ab-103">D3DINDEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="be9ab-104">Describe un búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="be9ab-104">Describes an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be9ab-105">Syntax</span></span>


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="be9ab-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="be9ab-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="be9ab-107">**Format**</span><span class="sxs-lookup"><span data-stu-id="be9ab-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="be9ab-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="be9ab-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be9ab-109">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de superficie de los datos del búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="be9ab-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the index buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="be9ab-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="be9ab-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="be9ab-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="be9ab-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be9ab-112">Miembro del tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) que identifica este recurso como un búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="be9ab-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as an index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="be9ab-113">**Uso**</span><span class="sxs-lookup"><span data-stu-id="be9ab-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="be9ab-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be9ab-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be9ab-115">Combinación de una o varias de las marcas siguientes, especificando el uso de este recurso.</span><span class="sxs-lookup"><span data-stu-id="be9ab-115">Combination of one or more of the following flags, specifying the usage for this resource.</span></span>



| <span data-ttu-id="be9ab-116">Value</span><span class="sxs-lookup"><span data-stu-id="be9ab-116">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="be9ab-117">Significado</span><span class="sxs-lookup"><span data-stu-id="be9ab-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <span data-ttu-id="be9ab-118"><dt>**D3DUSAGE \_ DONOTCLIP**</dt></span><span class="sxs-lookup"><span data-stu-id="be9ab-118"><dt>**D3DUSAGE\_DONOTCLIP**</dt></span></span> </dl>                            | <span data-ttu-id="be9ab-119">Se establece para indicar que el contenido del búfer de índice nunca requerirá un recorte.</span><span class="sxs-lookup"><span data-stu-id="be9ab-119">Set to indicate that the index buffer content will never require clipping.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <span data-ttu-id="be9ab-120"><dt>**D3DUSAGE \_ dinámico**</dt></span><span class="sxs-lookup"><span data-stu-id="be9ab-120"><dt>**D3DUSAGE\_DYNAMIC**</dt></span></span> </dl>                                  | <span data-ttu-id="be9ab-121">Se establece para indicar que el búfer de índice requiere el uso de memoria dinámica.</span><span class="sxs-lookup"><span data-stu-id="be9ab-121">Set to indicate that the index buffer requires dynamic memory use.</span></span> <span data-ttu-id="be9ab-122">Esto resulta útil para los controladores porque les permite decidir dónde colocar el búfer.</span><span class="sxs-lookup"><span data-stu-id="be9ab-122">This is useful for drivers because it enables them to decide where to place the buffer.</span></span> <span data-ttu-id="be9ab-123">En general, los búferes de índice estáticos se colocan en la memoria de vídeo y los búferes de índice dinámicos se colocan en la memoria AGP.</span><span class="sxs-lookup"><span data-stu-id="be9ab-123">In general, static index buffers are placed in video memory and dynamic index buffers are placed in AGP memory.</span></span> <span data-ttu-id="be9ab-124">Tenga en cuenta que no hay ningún uso estático independiente; Si no especifica D3DUSAGE Dynamic, \_ el búfer de índice se convierte en estático.</span><span class="sxs-lookup"><span data-stu-id="be9ab-124">Note that there is no separate static usage; if you do not specify D3DUSAGE\_DYNAMIC the index buffer is made static.</span></span> <span data-ttu-id="be9ab-125">D3DUSAGE \_ Dynamic se aplica estrictamente a través de las \_ marcas de bloqueo D3DLOCK discard y D3DLOCK \_ NOOVERWRITE.</span><span class="sxs-lookup"><span data-stu-id="be9ab-125">D3DUSAGE\_DYNAMIC is strictly enforced through the D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE locking flags.</span></span> <span data-ttu-id="be9ab-126">Como resultado, D3DLOCK \_ discard y D3DLOCK \_ NOOVERWRITE solo son válidos en los búferes de índice creados con D3DUSAGE \_ Dynamic; no son marcas válidas en los búferes de vértices estáticos.</span><span class="sxs-lookup"><span data-stu-id="be9ab-126">As a result, D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE are only valid on index buffers created with D3DUSAGE\_DYNAMIC; they are not valid flags on static vertex buffers.</span></span><br/> <span data-ttu-id="be9ab-127">Para obtener más información sobre el uso de búferes de índice dinámicos, vea [usar búferes dinámicos y de índice](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="be9ab-127">For more information about using dynamic index buffers, see [Using Dynamic Vertex and Index Buffers](performance-optimizations.md).</span></span><br/> <span data-ttu-id="be9ab-128">Tenga en cuenta que \_ no se puede especificar D3DUSAGE Dynamic en búferes de índice administrados.</span><span class="sxs-lookup"><span data-stu-id="be9ab-128">Note that D3DUSAGE\_DYNAMIC cannot be specified on managed index buffers.</span></span> <span data-ttu-id="be9ab-129">Para obtener más información, vea [administrar recursos (Direct3D 9)](managing-resources.md).</span><span class="sxs-lookup"><span data-stu-id="be9ab-129">For more information, see [Managing Resources (Direct3D 9)](managing-resources.md).</span></span><br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <span data-ttu-id="be9ab-130"><dt>**D3DUSAGE \_ RTPATCHES**</dt></span><span class="sxs-lookup"><span data-stu-id="be9ab-130"><dt>**D3DUSAGE\_RTPATCHES**</dt></span></span> </dl>                            | <span data-ttu-id="be9ab-131">Se establece para indicar si el búfer de índice se va a utilizar para dibujar primitivas de orden superior.</span><span class="sxs-lookup"><span data-stu-id="be9ab-131">Set to indicate when the index buffer is to be used for drawing high-order primitives.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <span data-ttu-id="be9ab-132"><dt>**D3DUSAGE \_ NPATCHES**</dt></span><span class="sxs-lookup"><span data-stu-id="be9ab-132"><dt>**D3DUSAGE\_NPATCHES**</dt></span></span> </dl>                               | <span data-ttu-id="be9ab-133">Se establece para indicar si el búfer de índice se va a utilizar para dibujar N revisiones.</span><span class="sxs-lookup"><span data-stu-id="be9ab-133">Set to indicate when the index buffer is to be used for drawing N patches.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <span data-ttu-id="be9ab-134"><dt>**\_Puntos D3DUSAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="be9ab-134"><dt>**D3DUSAGE\_POINTS**</dt></span></span> </dl>                                     | <span data-ttu-id="be9ab-135">Se establece para indicar cuándo se va a utilizar el búfer de índice para los sprites de punto de dibujo o listas de puntos indizados.</span><span class="sxs-lookup"><span data-stu-id="be9ab-135">Set to indicate when the index buffer is to be used for drawing point sprites or indexed point lists.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <span data-ttu-id="be9ab-136"><dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt></span><span class="sxs-lookup"><span data-stu-id="be9ab-136"><dt>**D3DUSAGE\_SOFTWAREPROCESSING**</dt></span></span> </dl> | <span data-ttu-id="be9ab-137">Se establece para indicar que el búfer se va a utilizar con el procesamiento de software.</span><span class="sxs-lookup"><span data-stu-id="be9ab-137">Set to indicate that the buffer is to be used with software processing.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <span data-ttu-id="be9ab-138"><dt>**D3DUSAGE \_ WRITEONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="be9ab-138"><dt>**D3DUSAGE\_WRITEONLY**</dt></span></span> </dl>                            | <span data-ttu-id="be9ab-139">Informa al sistema de que la aplicación solo escribe en el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="be9ab-139">Informs the system that the application writes only to the index buffer.</span></span> <span data-ttu-id="be9ab-140">El uso de esta marca permite al controlador elegir la mejor ubicación de memoria para operaciones de escritura y representación eficientes.</span><span class="sxs-lookup"><span data-stu-id="be9ab-140">Using this flag enables the driver to choose the best memory location for efficient write operations and rendering.</span></span> <span data-ttu-id="be9ab-141">Los intentos de leer desde un búfer de índice creado con esta capacidad pueden dar lugar a un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="be9ab-141">Attempts to read from an index buffer that is created with this capability can result in degraded performance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="be9ab-142">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="be9ab-142">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="be9ab-143">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="be9ab-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be9ab-144">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que especifica la clase de memoria asignada para este búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="be9ab-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="be9ab-145">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="be9ab-145">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="be9ab-146">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be9ab-146">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be9ab-147">Tamaño del búfer de índice, en bytes.</span><span class="sxs-lookup"><span data-stu-id="be9ab-147">Size of the index buffer, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be9ab-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be9ab-148">Requirements</span></span>



| <span data-ttu-id="be9ab-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="be9ab-149">Requirement</span></span> | <span data-ttu-id="be9ab-150">Value</span><span class="sxs-lookup"><span data-stu-id="be9ab-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be9ab-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be9ab-151">Header</span></span><br/> | <dl> <span data-ttu-id="be9ab-152"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="be9ab-152"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9ab-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="be9ab-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9ab-154">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="be9ab-154">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="be9ab-155">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="be9ab-155">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="be9ab-156">Búferes de índice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="be9ab-156">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
</dt> </dl>

 

 
