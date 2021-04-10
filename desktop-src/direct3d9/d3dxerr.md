---
description: Los errores se representan con valores negativos y no se pueden combinar.
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: Enumeración D3DXERR (D3dx9. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXERR
api_type:
- HeaderDef
api_location:
- d3dx9.h
ms.openlocfilehash: 0d4ef0fddf70effd63a0fcdc42b46889a879c13a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280323"
---
# <a name="d3dxerr-enumeration"></a><span data-ttu-id="a4f63-103">Enumeración D3DXERR</span><span class="sxs-lookup"><span data-stu-id="a4f63-103">D3DXERR enumeration</span></span>

<span data-ttu-id="a4f63-104">Los errores se representan con valores negativos y no se pueden combinar.</span><span class="sxs-lookup"><span data-stu-id="a4f63-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="a4f63-105">A continuación se muestra una lista de los valores que pueden ser devueltos por los métodos incluidos en la biblioteca de utilidades de D3DX.</span><span class="sxs-lookup"><span data-stu-id="a4f63-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="a4f63-106">Vea las descripciones individuales de cada método para ver las listas de los valores que puede devolver.</span><span class="sxs-lookup"><span data-stu-id="a4f63-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="a4f63-107">Estas listas no son necesariamente completas.</span><span class="sxs-lookup"><span data-stu-id="a4f63-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f63-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4f63-108">Syntax</span></span>


```C++
enum _D3DXERR {
  D3DXERR_CANNOTMODIFYINDEXBUFFER, 
  D3DXERR_INVALIDMESH, 
  D3DXERR_CANNOTATTRSORT, 
  D3DXERR_SKINNINGNOTSUPPORTED, 
  D3DXERR_TOOMANYINFLUENCES, 
  D3DXERR_INVALIDDATA, 
  D3DXERR_LOADEDMESHASNODATA, 
  D3DXERR_DUPLICATENAMEDFRAGMENT, 
  D3DXERR_CANNOTREMOVELASTITEM 

};
```



## <a name="constants"></a><span data-ttu-id="a4f63-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="a4f63-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a4f63-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ CANNOTMODIFYINDEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="a4f63-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR\_CANNOTMODIFYINDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="a4f63-111">No se puede modificar el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="a4f63-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="a4f63-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ INVALIDMESH**</span><span class="sxs-lookup"><span data-stu-id="a4f63-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR\_INVALIDMESH**</span></span>
</dt> <dd>

<span data-ttu-id="a4f63-113">La malla no es válida.</span><span class="sxs-lookup"><span data-stu-id="a4f63-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a4f63-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ CANNOTATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="a4f63-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR\_CANNOTATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="a4f63-115">La ordenación de atributos (D3DXMESHOPT \_ ATTRSORT) no se admite como técnica de optimización.</span><span class="sxs-lookup"><span data-stu-id="a4f63-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="a4f63-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ SKINNINGNOTSUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="a4f63-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR\_SKINNINGNOTSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="a4f63-117">No se admite la recubrimiento.</span><span class="sxs-lookup"><span data-stu-id="a4f63-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a4f63-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR \_ TOOMANYINFLUENCES**</span><span class="sxs-lookup"><span data-stu-id="a4f63-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR\_TOOMANYINFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="a4f63-119">Se han especificado demasiadas influencias.</span><span class="sxs-lookup"><span data-stu-id="a4f63-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="a4f63-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ INVALIDDATA**</span><span class="sxs-lookup"><span data-stu-id="a4f63-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR\_INVALIDDATA**</span></span>
</dt> <dd>

<span data-ttu-id="a4f63-121">Los datos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a4f63-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a4f63-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ LOADEDMESHASNODATA**</span><span class="sxs-lookup"><span data-stu-id="a4f63-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR\_LOADEDMESHASNODATA**</span></span>
</dt> <dd>

<span data-ttu-id="a4f63-123">La malla no tiene datos.</span><span class="sxs-lookup"><span data-stu-id="a4f63-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="a4f63-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ DUPLICATENAMEDFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="a4f63-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR\_DUPLICATENAMEDFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="a4f63-125">Ya existe un fragmento con ese nombre.</span><span class="sxs-lookup"><span data-stu-id="a4f63-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a4f63-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ CANNOTREMOVELASTITEM**</span><span class="sxs-lookup"><span data-stu-id="a4f63-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR\_CANNOTREMOVELASTITEM**</span></span>
</dt> <dd>

<span data-ttu-id="a4f63-127">No se puede eliminar el último elemento.</span><span class="sxs-lookup"><span data-stu-id="a4f63-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4f63-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4f63-128">Remarks</span></span>

<span data-ttu-id="a4f63-129">El código de instalación \_ FACDD se utiliza para generar códigos de error, como en las siguientes macros.</span><span class="sxs-lookup"><span data-stu-id="a4f63-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="a4f63-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4f63-130">Requirements</span></span>



| <span data-ttu-id="a4f63-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4f63-131">Requirement</span></span> | <span data-ttu-id="a4f63-132">Value</span><span class="sxs-lookup"><span data-stu-id="a4f63-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f63-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4f63-133">Header</span></span><br/> | <dl> <span data-ttu-id="a4f63-134"><dt>D3dx9. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f63-134"><dt>D3dx9.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f63-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4f63-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f63-136">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="a4f63-136">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




