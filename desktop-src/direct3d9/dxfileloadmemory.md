---
description: Identifica los datos de memoria. En desuso.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: Estructura DXFILELOADMEMORY (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707974"
---
# <a name="dxfileloadmemory-structure"></a><span data-ttu-id="72afa-104">Estructura DXFILELOADMEMORY</span><span class="sxs-lookup"><span data-stu-id="72afa-104">DXFILELOADMEMORY structure</span></span>

<span data-ttu-id="72afa-105">Identifica los datos de memoria.</span><span class="sxs-lookup"><span data-stu-id="72afa-105">Identifies memory data.</span></span> <span data-ttu-id="72afa-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="72afa-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="72afa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72afa-107">Syntax</span></span>


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="72afa-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="72afa-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="72afa-109">**lpMemory**</span><span class="sxs-lookup"><span data-stu-id="72afa-109">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="72afa-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72afa-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="72afa-111">Puntero a un bloque de memoria que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="72afa-111">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="72afa-112">**dSize**</span><span class="sxs-lookup"><span data-stu-id="72afa-112">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="72afa-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72afa-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="72afa-114">Tamaño del bloque de memoria que se va a cargar, en bytes.</span><span class="sxs-lookup"><span data-stu-id="72afa-114">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72afa-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72afa-115">Remarks</span></span>

<span data-ttu-id="72afa-116">Esta estructura identifica un recurso que se va a cargar cuando una aplicación usa el método [**CreateEnumObject**](idirectxfile--createenumobject.md) y especifica DXFILELOAD \_ FROMMEMORY.</span><span class="sxs-lookup"><span data-stu-id="72afa-116">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="72afa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72afa-117">Requirements</span></span>



| <span data-ttu-id="72afa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="72afa-118">Requirement</span></span> | <span data-ttu-id="72afa-119">Value</span><span class="sxs-lookup"><span data-stu-id="72afa-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="72afa-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72afa-120">Header</span></span><br/> | <dl> <span data-ttu-id="72afa-121"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="72afa-121"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72afa-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="72afa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72afa-123">Estructuras de archivos X</span><span class="sxs-lookup"><span data-stu-id="72afa-123">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="72afa-124">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="72afa-124">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="72afa-125">Constantes de DXFILE</span><span class="sxs-lookup"><span data-stu-id="72afa-125">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
