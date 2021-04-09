---
description: Especifica qué partes de los datos de la malla se van a descartar del dispositivo. Se usa con ID3DX10Mesh::D iscard.
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: Enumeración D3DX10_MESH_DISCARD_FLAGS (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH_DISCARD_FLAGS
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 6640834cf81bfa5e4b6263d3b3cfbb1181bb16c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003924"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a><span data-ttu-id="0ed50-104">D3DX10 \_ \_ enumeración de marcas de descartado de malla \_</span><span class="sxs-lookup"><span data-stu-id="0ed50-104">D3DX10\_MESH\_DISCARD\_FLAGS enumeration</span></span>

<span data-ttu-id="0ed50-105">Especifica qué partes de los datos de la malla se van a descartar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ed50-105">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="0ed50-106">Se usa con [**ID3DX10Mesh::D iscard**](id3dx10mesh-discard.md).</span><span class="sxs-lookup"><span data-stu-id="0ed50-106">Used with [**ID3DX10Mesh::Discard**](id3dx10mesh-discard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed50-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ed50-107">Syntax</span></span>


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="0ed50-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="0ed50-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0ed50-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3DX10 \_ \_ búfer de atributo de descartar malla \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0ed50-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="0ed50-110">Descarte el búfer de atributo.</span><span class="sxs-lookup"><span data-stu-id="0ed50-110">Discard the attribute buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0ed50-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**\_Tabla de \_ atributos de descartar malla D3DX10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0ed50-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_TABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0ed50-112">Descartar la tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="0ed50-112">Discard the attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="0ed50-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 \_ malla \_ descartar \_ POINTREPS**</span><span class="sxs-lookup"><span data-stu-id="0ed50-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10\_MESH\_DISCARD\_POINTREPS**</span></span>
</dt> <dd>

<span data-ttu-id="0ed50-114">Descartar el búfer de representantes de puntero.</span><span class="sxs-lookup"><span data-stu-id="0ed50-114">Discard the pointer reps buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0ed50-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 \_ de \_ descartar la proximidad de la malla \_**</span><span class="sxs-lookup"><span data-stu-id="0ed50-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10\_MESH\_DISCARD\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="0ed50-116">Descarte el búfer de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="0ed50-116">Discard the adjacency buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0ed50-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**\_ \_ \_ Búferes de dispositivo de descartar malla D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="0ed50-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10\_MESH\_DISCARD\_DEVICE\_BUFFERS**</span></span>
</dt> <dd>

<span data-ttu-id="0ed50-118">Descartar los búferes confirmados en el dispositivo (con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).</span><span class="sxs-lookup"><span data-stu-id="0ed50-118">Discard the buffers committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ed50-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ed50-119">Requirements</span></span>



| <span data-ttu-id="0ed50-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ed50-120">Requirement</span></span> | <span data-ttu-id="0ed50-121">Value</span><span class="sxs-lookup"><span data-stu-id="0ed50-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed50-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ed50-122">Header</span></span><br/> | <dl> <span data-ttu-id="0ed50-123"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ed50-123"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ed50-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ed50-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed50-125">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="0ed50-125">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




