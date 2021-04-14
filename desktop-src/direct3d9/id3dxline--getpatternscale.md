---
description: Obtiene el valor de escala del patrón punteado.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'ID3DXLine:: GetPatternScale (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424531"
---
# <a name="id3dxlinegetpatternscale-method"></a><span data-ttu-id="e65ce-103">ID3DXLine:: GetPatternScale (método)</span><span class="sxs-lookup"><span data-stu-id="e65ce-103">ID3DXLine::GetPatternScale method</span></span>

<span data-ttu-id="e65ce-104">Obtiene el valor de escala del patrón punteado.</span><span class="sxs-lookup"><span data-stu-id="e65ce-104">Gets the stipple-pattern scale value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e65ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e65ce-105">Syntax</span></span>


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a><span data-ttu-id="e65ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e65ce-106">Parameters</span></span>

<span data-ttu-id="e65ce-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e65ce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e65ce-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e65ce-108">Return value</span></span>

<span data-ttu-id="e65ce-109">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e65ce-109">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e65ce-110">Devuelve el valor usado para escalar el patrón punteado.</span><span class="sxs-lookup"><span data-stu-id="e65ce-110">Returns the value used to scale the stipple-pattern.</span></span> <span data-ttu-id="e65ce-111">1.0 f es el valor predeterminado y no representa ningún ajuste de escala.</span><span class="sxs-lookup"><span data-stu-id="e65ce-111">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="e65ce-112">Un valor menor que 1,0 f reduce el modelo y un valor mayor que 1,0 expande el patrón.</span><span class="sxs-lookup"><span data-stu-id="e65ce-112">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

## <a name="requirements"></a><span data-ttu-id="e65ce-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e65ce-113">Requirements</span></span>



| <span data-ttu-id="e65ce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e65ce-114">Requirement</span></span> | <span data-ttu-id="e65ce-115">Value</span><span class="sxs-lookup"><span data-stu-id="e65ce-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e65ce-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e65ce-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e65ce-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e65ce-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e65ce-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e65ce-118">Library</span></span><br/> | <dl> <span data-ttu-id="e65ce-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e65ce-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e65ce-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e65ce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e65ce-121">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="e65ce-121">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="e65ce-122">**ID3DXLine::SetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="e65ce-122">**ID3DXLine::SetPatternScale**</span></span>](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
