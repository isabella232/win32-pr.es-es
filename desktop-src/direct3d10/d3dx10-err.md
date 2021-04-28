---
description: 'D3DX10_ERR enumeración: los errores se representan mediante valores negativos y no se pueden combinar.'
ms.assetid: 4149ce6d-e87a-4003-b123-5555c6b3b086
title: D3DX10_ERR enumeración (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ERR
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 520abae0409dd4214106363d7ffde0cfb5c81ff1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094363"
---
# <a name="d3dx10_err-enumeration"></a><span data-ttu-id="28ff3-103">Enumeración ERR D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="28ff3-103">D3DX10\_ERR enumeration</span></span>

<span data-ttu-id="28ff3-104">Los errores se representan mediante valores negativos y no se pueden combinar.</span><span class="sxs-lookup"><span data-stu-id="28ff3-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="28ff3-105">A continuación se muestra una lista de valores que pueden devolver los métodos incluidos con la biblioteca de utilidades D3DX.</span><span class="sxs-lookup"><span data-stu-id="28ff3-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="28ff3-106">Consulte las descripciones de métodos individuales para obtener listas de los valores que cada uno puede devolver.</span><span class="sxs-lookup"><span data-stu-id="28ff3-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="28ff3-107">Estas listas no son necesariamente completas.</span><span class="sxs-lookup"><span data-stu-id="28ff3-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ff3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="28ff3-108">Syntax</span></span>


```C++
typedef enum D3DX10_ERR { 
  D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX10_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX10_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX10_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX10_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX10_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX10_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX10_ERR, *LPD3DX10_ERR;
```



## <a name="constants"></a><span data-ttu-id="28ff3-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="28ff3-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="28ff3-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**ERROR DE D3DX10 \_ NO SE PUEDE MODIFICAR EL BÚFER DE \_ \_ \_ \_ ÍNDICE**</span><span class="sxs-lookup"><span data-stu-id="28ff3-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="28ff3-111">No se puede modificar el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="28ff3-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="28ff3-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**MALLA NO VÁLIDA DE ERROR D3DX10 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28ff3-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="28ff3-113">La malla no es válida.</span><span class="sxs-lookup"><span data-stu-id="28ff3-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="28ff3-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**ERROR D3DX10 \_ NO SE PUEDE ORDENAR \_ \_ ATTR \_**</span><span class="sxs-lookup"><span data-stu-id="28ff3-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="28ff3-115">La ordenación de atributos (D3DXMESHOPT \_ ATTRSORT) no se admite como una técnica de optimización.</span><span class="sxs-lookup"><span data-stu-id="28ff3-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="28ff3-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10 \_ ERR \_ SKINNING \_ NOT \_ SUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="28ff3-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="28ff3-117">No se admite el desnasado.</span><span class="sxs-lookup"><span data-stu-id="28ff3-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="28ff3-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10 \_ ERR \_ TOO \_ MANY \_ INFLUENCES**</span><span class="sxs-lookup"><span data-stu-id="28ff3-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="28ff3-119">Demasiadas influencias especificadas.</span><span class="sxs-lookup"><span data-stu-id="28ff3-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="28ff3-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10 \_ ERR DATOS NO \_ \_ VÁLIDOS**</span><span class="sxs-lookup"><span data-stu-id="28ff3-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="28ff3-121">Los datos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="28ff3-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="28ff3-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3DX10 \_ ERR LOADED MESH NO TIENE \_ \_ \_ \_ \_ DATOS**</span><span class="sxs-lookup"><span data-stu-id="28ff3-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3DX10\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="28ff3-123">La malla no tiene datos.</span><span class="sxs-lookup"><span data-stu-id="28ff3-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="28ff3-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**FRAGMENTO CON NOMBRE DUPLICADO DE ERROR D3DX10 \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28ff3-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="28ff3-125">Ya existe un fragmento con ese nombre.</span><span class="sxs-lookup"><span data-stu-id="28ff3-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="28ff3-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10 \_ ERR NO PUEDE QUITAR EL ÚLTIMO \_ \_ \_ \_ ELEMENTO**</span><span class="sxs-lookup"><span data-stu-id="28ff3-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="28ff3-127">No se puede eliminar el último elemento.</span><span class="sxs-lookup"><span data-stu-id="28ff3-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28ff3-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28ff3-128">Remarks</span></span>

<span data-ttu-id="28ff3-129">El código de instalación \_ FACDD se usa para generar códigos de error, como en las macros siguientes.</span><span class="sxs-lookup"><span data-stu-id="28ff3-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="28ff3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28ff3-130">Requirements</span></span>



| <span data-ttu-id="28ff3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="28ff3-131">Requirement</span></span> | <span data-ttu-id="28ff3-132">Value</span><span class="sxs-lookup"><span data-stu-id="28ff3-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="28ff3-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28ff3-133">Header</span></span><br/> | <dl> <span data-ttu-id="28ff3-134"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="28ff3-134"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28ff3-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="28ff3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ff3-136">Enumeraciones D3DX</span><span class="sxs-lookup"><span data-stu-id="28ff3-136">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




