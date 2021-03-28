---
title: Enumeración D3DX11_ERR (D3DX11. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Los errores se representan con valores negativos y no se pueden combinar.
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- Enumeración de D3DX11_ERR Direct3D 11
- LPD3DX11_ERR puntero de enumeración Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_ERR
api_location:
- D3DX11.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0607bd495bad4bdeacf66ae593670dbe3ad0d2e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998689"
---
# <a name="d3dx11_err-enumeration"></a><span data-ttu-id="faba8-106">\_Enumeración de D3DX11 Err</span><span class="sxs-lookup"><span data-stu-id="faba8-106">D3DX11\_ERR enumeration</span></span>

> [!Note]  
> <span data-ttu-id="faba8-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="faba8-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="faba8-108">Los errores se representan con valores negativos y no se pueden combinar.</span><span class="sxs-lookup"><span data-stu-id="faba8-108">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="faba8-109">A continuación se muestra una lista de los valores que pueden ser devueltos por los métodos incluidos en la biblioteca de utilidades de D3DX.</span><span class="sxs-lookup"><span data-stu-id="faba8-109">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="faba8-110">Vea las descripciones individuales de cada método para ver las listas de los valores que puede devolver.</span><span class="sxs-lookup"><span data-stu-id="faba8-110">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="faba8-111">Estas listas no son necesariamente completas.</span><span class="sxs-lookup"><span data-stu-id="faba8-111">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="faba8-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="faba8-112">Syntax</span></span>


```C++
typedef enum D3DX11_ERR { 
  D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX11_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX11_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX11_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX11_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX11_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX11_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX11_ERR, *LPD3DX11_ERR;
```



## <a name="constants"></a><span data-ttu-id="faba8-113">Constantes</span><span class="sxs-lookup"><span data-stu-id="faba8-113">Constants</span></span>

<dl> <dt>

<span data-ttu-id="faba8-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ Err \_ no puede \_ modificar el \_ búfer de índice \_**</span><span class="sxs-lookup"><span data-stu-id="faba8-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="faba8-115">No se puede modificar el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="faba8-115">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="faba8-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ Err \_ no válida \_ Mesh**</span><span class="sxs-lookup"><span data-stu-id="faba8-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="faba8-117">La malla no es válida.</span><span class="sxs-lookup"><span data-stu-id="faba8-117">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="faba8-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ Err \_ no se puede \_ ordenar el atributo \_**</span><span class="sxs-lookup"><span data-stu-id="faba8-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="faba8-119">La ordenación de atributos (D3DXMESHOPT \_ ATTRSORT) no se admite como técnica de optimización.</span><span class="sxs-lookup"><span data-stu-id="faba8-119">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="faba8-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**\_No se \_ \_ \_ admiten los aspectos de D3DX11 Err**</span><span class="sxs-lookup"><span data-stu-id="faba8-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="faba8-121">No se admite la recubrimiento.</span><span class="sxs-lookup"><span data-stu-id="faba8-121">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="faba8-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 \_ Err \_ demasiadas \_ \_ influencias**</span><span class="sxs-lookup"><span data-stu-id="faba8-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="faba8-123">Se han especificado demasiadas influencias.</span><span class="sxs-lookup"><span data-stu-id="faba8-123">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="faba8-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11 \_ Err \_ invalid \_ Data**</span><span class="sxs-lookup"><span data-stu-id="faba8-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="faba8-125">Los datos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="faba8-125">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="faba8-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11 el error de la \_ \_ \_ malla cargada \_ \_ no tiene \_ datos**</span><span class="sxs-lookup"><span data-stu-id="faba8-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="faba8-127">La malla no tiene datos.</span><span class="sxs-lookup"><span data-stu-id="faba8-127">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="faba8-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11 \_ Err \_ Duplicate \_ nombre \_ FRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="faba8-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="faba8-129">Ya existe un fragmento con ese nombre.</span><span class="sxs-lookup"><span data-stu-id="faba8-129">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="faba8-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ Err \_ no puede \_ quitar el \_ último \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="faba8-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="faba8-131">No se puede eliminar el último elemento.</span><span class="sxs-lookup"><span data-stu-id="faba8-131">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="faba8-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="faba8-132">Remarks</span></span>

<span data-ttu-id="faba8-133">El código de instalación \_ FACDD se utiliza para generar códigos de error, como en las siguientes macros.</span><span class="sxs-lookup"><span data-stu-id="faba8-133">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="faba8-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faba8-134">Requirements</span></span>



| <span data-ttu-id="faba8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="faba8-135">Requirement</span></span> | <span data-ttu-id="faba8-136">Value</span><span class="sxs-lookup"><span data-stu-id="faba8-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="faba8-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="faba8-137">Header</span></span><br/> | <dl> <span data-ttu-id="faba8-138"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="faba8-138"><dt>D3DX11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faba8-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="faba8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faba8-140">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="faba8-140">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





