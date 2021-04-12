---
description: Estira el patrón punteado a lo largo de la dirección de la línea.
ms.assetid: 411464db-d721-4252-bff3-bec57252273e
title: 'ID3DXLine:: SetPatternScale (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44c040a2e8899784bcea9b93bf0781afb39c2464
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280517"
---
# <a name="id3dxlinesetpatternscale-method"></a><span data-ttu-id="3ab64-103">ID3DXLine:: SetPatternScale (método)</span><span class="sxs-lookup"><span data-stu-id="3ab64-103">ID3DXLine::SetPatternScale method</span></span>

<span data-ttu-id="3ab64-104">Estira el patrón punteado a lo largo de la dirección de la línea.</span><span class="sxs-lookup"><span data-stu-id="3ab64-104">Stretches the stipple pattern along the line direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab64-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ab64-105">Syntax</span></span>


```C++
HRESULT SetPatternScale(
  [in] FLOAT fPatternScale
);
```



## <a name="parameters"></a><span data-ttu-id="3ab64-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ab64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ab64-107">*fPatternScale* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ab64-107">*fPatternScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ab64-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ab64-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ab64-109">Valor de escala del patrón punteado.</span><span class="sxs-lookup"><span data-stu-id="3ab64-109">Stipple pattern scaling value.</span></span> <span data-ttu-id="3ab64-110">1.0 f es el valor predeterminado y no representa ningún ajuste de escala.</span><span class="sxs-lookup"><span data-stu-id="3ab64-110">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="3ab64-111">Un valor menor que 1,0 f reduce el modelo y un valor mayor que 1,0 expande el patrón.</span><span class="sxs-lookup"><span data-stu-id="3ab64-111">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ab64-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ab64-112">Return value</span></span>

<span data-ttu-id="3ab64-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3ab64-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3ab64-114">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3ab64-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3ab64-115">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="3ab64-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ab64-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ab64-116">Requirements</span></span>



| <span data-ttu-id="3ab64-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ab64-117">Requirement</span></span> | <span data-ttu-id="3ab64-118">Value</span><span class="sxs-lookup"><span data-stu-id="3ab64-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab64-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ab64-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3ab64-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ab64-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3ab64-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ab64-121">Library</span></span><br/> | <dl> <span data-ttu-id="3ab64-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ab64-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3ab64-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ab64-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ab64-124">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="3ab64-124">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
