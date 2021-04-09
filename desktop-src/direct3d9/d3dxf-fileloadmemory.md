---
description: Identifica los datos de memoria.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: D3DXF_FILELOADMEMORY estructura (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003818"
---
# <a name="d3dxf_fileloadmemory-structure"></a><span data-ttu-id="8143f-103">D3DXF \_ estructura FILELOADMEMORY</span><span class="sxs-lookup"><span data-stu-id="8143f-103">D3DXF\_FILELOADMEMORY structure</span></span>

<span data-ttu-id="8143f-104">Identifica los datos de memoria.</span><span class="sxs-lookup"><span data-stu-id="8143f-104">Identifies memory data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8143f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8143f-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="8143f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8143f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8143f-107">**lpMemory**</span><span class="sxs-lookup"><span data-stu-id="8143f-107">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="8143f-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8143f-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8143f-109">Puntero a un bloque de memoria que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="8143f-109">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="8143f-110">**dSize**</span><span class="sxs-lookup"><span data-stu-id="8143f-110">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="8143f-111">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8143f-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8143f-112">Tamaño del bloque de memoria que se va a cargar, en bytes.</span><span class="sxs-lookup"><span data-stu-id="8143f-112">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8143f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8143f-113">Remarks</span></span>

<span data-ttu-id="8143f-114">Esta estructura identifica los datos que se van a cargar desde la memoria cuando una aplicación usa el método [**CreateEnumObject**](id3dxfile--createenumobject.md) y especifica la \_ marca D3DXF FILELOAD \_ FROMMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8143f-114">This structure identifies data to be loaded from memory when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the D3DXF\_FILELOAD\_FROMMEMORY flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="8143f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8143f-115">Requirements</span></span>



| <span data-ttu-id="8143f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8143f-116">Requirement</span></span> | <span data-ttu-id="8143f-117">Value</span><span class="sxs-lookup"><span data-stu-id="8143f-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8143f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8143f-118">Header</span></span><br/> | <dl> <span data-ttu-id="8143f-119"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="8143f-119"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8143f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="8143f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8143f-121">Estructuras de archivos de D3DX X</span><span class="sxs-lookup"><span data-stu-id="8143f-121">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
