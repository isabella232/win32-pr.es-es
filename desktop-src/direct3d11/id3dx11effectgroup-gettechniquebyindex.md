---
title: Método ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
description: Obtiene una técnica por índice. | Método ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: b0962957-20d1-4ec6-9f8e-acc7a62c5f4e
keywords:
- Método GetTechniqueByIndex Direct3D 11
- Método GetTechniqueByIndex Direct3D 11, interfaz ID3DX11EffectGroup
- Interfaz ID3DX11EffectGroup Direct3D 11, método GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe42d71886ae93bdaff7ac956554ff9a97fc9f8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003884"
---
# <a name="id3dx11effectgroupgettechniquebyindex-method"></a><span data-ttu-id="321fc-107">ID3DX11EffectGroup:: GetTechniqueByIndex (método)</span><span class="sxs-lookup"><span data-stu-id="321fc-107">ID3DX11EffectGroup::GetTechniqueByIndex method</span></span>

<span data-ttu-id="321fc-108">Obtiene una técnica por índice.</span><span class="sxs-lookup"><span data-stu-id="321fc-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="321fc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="321fc-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="321fc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="321fc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="321fc-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="321fc-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="321fc-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="321fc-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="321fc-113">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="321fc-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="321fc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="321fc-114">Return value</span></span>

<span data-ttu-id="321fc-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="321fc-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="321fc-116">Un puntero a un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="321fc-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="321fc-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="321fc-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="321fc-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="321fc-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="321fc-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="321fc-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="321fc-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="321fc-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="321fc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="321fc-121">Requirements</span></span>



| <span data-ttu-id="321fc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="321fc-122">Requirement</span></span> | <span data-ttu-id="321fc-123">Value</span><span class="sxs-lookup"><span data-stu-id="321fc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321fc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="321fc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="321fc-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="321fc-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="321fc-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="321fc-126">Library</span></span><br/> | <dl> <span data-ttu-id="321fc-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="321fc-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="321fc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="321fc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321fc-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="321fc-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

