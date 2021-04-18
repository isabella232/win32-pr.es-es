---
description: Identifica los datos de recursos. En desuso.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: Estructura DXFILELOADRESOURCE (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 233fe6acb13a6ae654a714028a316d7d6f6871ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649427"
---
# <a name="dxfileloadresource-structure"></a><span data-ttu-id="a8261-104">Estructura DXFILELOADRESOURCE</span><span class="sxs-lookup"><span data-stu-id="a8261-104">DXFILELOADRESOURCE structure</span></span>

<span data-ttu-id="a8261-105">Identifica los datos de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8261-105">Identifies resource data.</span></span> <span data-ttu-id="a8261-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="a8261-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8261-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8261-107">Syntax</span></span>


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="a8261-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8261-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8261-109">**hModule**</span><span class="sxs-lookup"><span data-stu-id="a8261-109">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="a8261-110">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8261-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a8261-111">Identificador del módulo que contiene el recurso que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="a8261-111">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="a8261-112">Si este miembro es **null**, el recurso se debe adjuntar al archivo ejecutable que lo usará.</span><span class="sxs-lookup"><span data-stu-id="a8261-112">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="a8261-113">**lpName**</span><span class="sxs-lookup"><span data-stu-id="a8261-113">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="a8261-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8261-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a8261-115">Puntero a una cadena que especifica el nombre del recurso que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="a8261-115">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="a8261-116">Por ejemplo, si el recurso es una malla, este miembro debe especificar el nombre del archivo de malla.</span><span class="sxs-lookup"><span data-stu-id="a8261-116">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="a8261-117">**lpType**</span><span class="sxs-lookup"><span data-stu-id="a8261-117">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="a8261-118">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8261-118">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a8261-119">Puntero a una cadena que especifica el tipo definido por el usuario que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="a8261-119">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8261-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8261-120">Remarks</span></span>

<span data-ttu-id="a8261-121">Esta estructura identifica un recurso que se va a cargar cuando una aplicación usa el método [**CreateEnumObject**](idirectxfile--createenumobject.md) y especifica DXFILELOAD \_ FROMRESOURCE.</span><span class="sxs-lookup"><span data-stu-id="a8261-121">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMRESOURCE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8261-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8261-122">Requirements</span></span>



| <span data-ttu-id="a8261-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8261-123">Requirement</span></span> | <span data-ttu-id="a8261-124">Value</span><span class="sxs-lookup"><span data-stu-id="a8261-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a8261-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8261-125">Header</span></span><br/> | <dl> <span data-ttu-id="a8261-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8261-126"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8261-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8261-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8261-128">Estructuras de archivos X</span><span class="sxs-lookup"><span data-stu-id="a8261-128">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="a8261-129">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="a8261-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="a8261-130">Constantes de DXFILE</span><span class="sxs-lookup"><span data-stu-id="a8261-130">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
