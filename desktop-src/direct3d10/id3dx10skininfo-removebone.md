---
description: Quitar un hueso.
ms.assetid: efb88108-5c76-47c8-b8ce-1ba29cb18ba4
title: 'ID3DX10SkinInfo:: RemoveBone (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemoveBone
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 49fd24c5661bbedb7fb839171fa4a835f07e446a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718224"
---
# <a name="id3dx10skininforemovebone-method"></a><span data-ttu-id="5c8d6-103">ID3DX10SkinInfo:: RemoveBone (método)</span><span class="sxs-lookup"><span data-stu-id="5c8d6-103">ID3DX10SkinInfo::RemoveBone method</span></span>

<span data-ttu-id="5c8d6-104">Quitar un hueso.</span><span class="sxs-lookup"><span data-stu-id="5c8d6-104">Remove a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c8d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c8d6-105">Syntax</span></span>


```C++
HRESULT RemoveBone(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="5c8d6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c8d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c8d6-107">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5c8d6-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c8d6-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c8d6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c8d6-109">Índice que especifica el hueso que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="5c8d6-109">An index that specifies which bone to remove.</span></span> <span data-ttu-id="5c8d6-110">Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="5c8d6-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c8d6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c8d6-111">Return value</span></span>

<span data-ttu-id="5c8d6-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c8d6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c8d6-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5c8d6-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5c8d6-114">Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="5c8d6-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c8d6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c8d6-115">Requirements</span></span>



| <span data-ttu-id="5c8d6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c8d6-116">Requirement</span></span> | <span data-ttu-id="5c8d6-117">Value</span><span class="sxs-lookup"><span data-stu-id="5c8d6-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8d6-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c8d6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5c8d6-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c8d6-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c8d6-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c8d6-120">Library</span></span><br/> | <dl> <span data-ttu-id="5c8d6-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c8d6-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c8d6-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c8d6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c8d6-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="5c8d6-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="5c8d6-124">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="5c8d6-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
