---
title: Método ID3DX11Effect GetClassLinkage (D3dx11effect. h)
description: Obtiene una interfaz de vinculación de clases.
ms.assetid: 006c900d-3464-4666-9fe9-d62ba8cb2b7f
keywords:
- Método GetClassLinkage Direct3D 11
- Método GetClassLinkage Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetClassLinkage
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetClassLinkage
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b19f14794186f85d0a51f21bc6b2759e512998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003785"
---
# <a name="id3dx11effectgetclasslinkage-method"></a><span data-ttu-id="a65a4-106">ID3DX11Effect:: GetClassLinkage (método)</span><span class="sxs-lookup"><span data-stu-id="a65a4-106">ID3DX11Effect::GetClassLinkage method</span></span>

<span data-ttu-id="a65a4-107">Obtiene una interfaz de vinculación de clases.</span><span class="sxs-lookup"><span data-stu-id="a65a4-107">Gets a class linkage interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65a4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a65a4-108">Syntax</span></span>


```C++
ID3D11ClassLinkage* GetClassLinkage();
```



## <a name="parameters"></a><span data-ttu-id="a65a4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a65a4-109">Parameters</span></span>

<span data-ttu-id="a65a4-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a65a4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a65a4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a65a4-111">Return value</span></span>

<span data-ttu-id="a65a4-112">Tipo: **[ **ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span><span class="sxs-lookup"><span data-stu-id="a65a4-112">Type: **[**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span></span>

<span data-ttu-id="a65a4-113">Devuelve un puntero a una interfaz [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) .</span><span class="sxs-lookup"><span data-stu-id="a65a4-113">Returns a pointer to an [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="a65a4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a65a4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a65a4-115">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="a65a4-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a65a4-116">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a65a4-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a65a4-117">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a65a4-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a65a4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a65a4-118">Requirements</span></span>



| <span data-ttu-id="a65a4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a65a4-119">Requirement</span></span> | <span data-ttu-id="a65a4-120">Value</span><span class="sxs-lookup"><span data-stu-id="a65a4-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65a4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a65a4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a65a4-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a65a4-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a65a4-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a65a4-123">Library</span></span><br/> | <dl> <span data-ttu-id="a65a4-124"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="a65a4-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a65a4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a65a4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a65a4-126">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="a65a4-126">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





