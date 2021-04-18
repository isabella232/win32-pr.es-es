---
description: Identifica los datos de recursos.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: D3DXF_FILELOADRESOURCE estructura (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698249"
---
# <a name="d3dxf_fileloadresource-structure"></a><span data-ttu-id="627cb-103">D3DXF \_ estructura FILELOADRESOURCE</span><span class="sxs-lookup"><span data-stu-id="627cb-103">D3DXF\_FILELOADRESOURCE structure</span></span>

<span data-ttu-id="627cb-104">Identifica los datos de recursos.</span><span class="sxs-lookup"><span data-stu-id="627cb-104">Identifies resource data.</span></span>

## <a name="syntax"></a><span data-ttu-id="627cb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="627cb-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="627cb-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="627cb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="627cb-107">**hModule**</span><span class="sxs-lookup"><span data-stu-id="627cb-107">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="627cb-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="627cb-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="627cb-109">Identificador del módulo que contiene el recurso que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="627cb-109">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="627cb-110">Si este miembro es **null**, el recurso se debe adjuntar al archivo ejecutable que lo usará.</span><span class="sxs-lookup"><span data-stu-id="627cb-110">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="627cb-111">**lpName**</span><span class="sxs-lookup"><span data-stu-id="627cb-111">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="627cb-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="627cb-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="627cb-113">Puntero a una cadena que especifica el nombre del recurso que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="627cb-113">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="627cb-114">Por ejemplo, si el recurso es una malla, este miembro debe especificar el nombre del archivo de malla.</span><span class="sxs-lookup"><span data-stu-id="627cb-114">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="627cb-115">**lpType**</span><span class="sxs-lookup"><span data-stu-id="627cb-115">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="627cb-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="627cb-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="627cb-117">Puntero a una cadena que especifica el tipo definido por el usuario que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="627cb-117">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="627cb-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="627cb-118">Remarks</span></span>

<span data-ttu-id="627cb-119">Esta estructura identifica un recurso que se va a cargar cuando una aplicación usa el método [**CreateEnumObject**](id3dxfile--createenumobject.md) y especifica la marca [D3DXF \_ FILELOAD \_ FROMRESOURCE](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="627cb-119">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the [D3DXF\_FILELOAD\_FROMRESOURCE](d3dxf.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="627cb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="627cb-120">Requirements</span></span>



| <span data-ttu-id="627cb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="627cb-121">Requirement</span></span> | <span data-ttu-id="627cb-122">Value</span><span class="sxs-lookup"><span data-stu-id="627cb-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="627cb-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="627cb-123">Header</span></span><br/> | <dl> <span data-ttu-id="627cb-124"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="627cb-124"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="627cb-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="627cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="627cb-126">Estructuras de archivos de D3DX X</span><span class="sxs-lookup"><span data-stu-id="627cb-126">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
