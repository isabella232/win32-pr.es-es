---
title: Función D3DX12GetBaseSubobjectType (D3dx12. h)
description: Devuelve el tipo de subobjeto que corresponde a la clase base del tipo de subobjeto pasado.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- D3DX12GetBaseSubobjectType función)
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707755"
---
# <a name="d3dx12getbasesubobjecttype-function"></a><span data-ttu-id="ad923-104">D3DX12GetBaseSubobjectType función)</span><span class="sxs-lookup"><span data-stu-id="ad923-104">D3DX12GetBaseSubobjectType function</span></span>

<span data-ttu-id="ad923-105">Devuelve el tipo de subobjeto que corresponde a la clase base del tipo de subobjeto pasado.</span><span class="sxs-lookup"><span data-stu-id="ad923-105">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad923-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad923-106">Syntax</span></span>


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a><span data-ttu-id="ad923-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad923-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad923-108">*SubobjectType*</span><span class="sxs-lookup"><span data-stu-id="ad923-108">*SubobjectType*</span></span> 
</dt> <dd>

<span data-ttu-id="ad923-109">Tipo: **\_ \_ \_ \_ tipo de subobjeto de estado de canalización D3D12**</span><span class="sxs-lookup"><span data-stu-id="ad923-109">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="ad923-110">Un valor de enumeración que especifica el tipo de subobjeto que le interesa.</span><span class="sxs-lookup"><span data-stu-id="ad923-110">An enumeration value that specifies the subobject type that you're interested in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad923-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad923-111">Return value</span></span>

<span data-ttu-id="ad923-112">Tipo: **\_ \_ \_ \_ tipo de subobjeto de estado de canalización D3D12**</span><span class="sxs-lookup"><span data-stu-id="ad923-112">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="ad923-113">Si *SubobjectType* corresponde a un tipo de datos de subobjeto que se deriva de otro tipo de datos de subobjeto, se devuelve el tipo de subobjeto del tipo de datos base de subobjeto; de lo contrario, se devuelve el tipo de subobjeto pasado.</span><span class="sxs-lookup"><span data-stu-id="ad923-113">If *SubobjectType* corresponds to a subobject data type that is derived from another subobject data type, the subobject type of the base subobject data type is returned; otherwise, the passed-in subobject type is returned.</span></span> <span data-ttu-id="ad923-114">Por ejemplo, si se pasa el **\_ tipo de subobjeto de estado de canalización D3D12 \_ \_ \_ \_ Depth \_ STENCIL1** , se devuelve **D3D12 el \_ \_ \_ \_ tipo \_ \_ de subobjeto de estado de canalización** .</span><span class="sxs-lookup"><span data-stu-id="ad923-114">For example, if **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** is passed in, then **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad923-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad923-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ad923-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad923-116">Requirements</span></span>



| <span data-ttu-id="ad923-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad923-117">Requirement</span></span> | <span data-ttu-id="ad923-118">Value</span><span class="sxs-lookup"><span data-stu-id="ad923-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ad923-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad923-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ad923-120"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad923-120"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="ad923-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad923-121">Library</span></span><br/> | <dl> <span data-ttu-id="ad923-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad923-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="ad923-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ad923-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ad923-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad923-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad923-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad923-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad923-126">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="ad923-126">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





