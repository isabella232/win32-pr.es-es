---
title: Método ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
description: Obtiene una técnica por índice. | Método ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: ee9c0cc3-0ca1-42e8-bd37-5878fd56cff1
keywords:
- Método GetTechniqueByIndex Direct3D 11
- Método GetTechniqueByIndex Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81d3be5ec403fb25ab3a49792ed77fd4d96bf571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003920"
---
# <a name="id3dx11effectgettechniquebyindex-method"></a><span data-ttu-id="4a8bb-107">ID3DX11Effect:: GetTechniqueByIndex (método)</span><span class="sxs-lookup"><span data-stu-id="4a8bb-107">ID3DX11Effect::GetTechniqueByIndex method</span></span>

<span data-ttu-id="4a8bb-108">Obtiene una técnica por índice.</span><span class="sxs-lookup"><span data-stu-id="4a8bb-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a8bb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a8bb-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="4a8bb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a8bb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a8bb-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="4a8bb-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="4a8bb-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4a8bb-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4a8bb-113">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="4a8bb-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a8bb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a8bb-114">Return value</span></span>

<span data-ttu-id="4a8bb-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a8bb-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="4a8bb-116">Un puntero a un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="4a8bb-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a8bb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a8bb-117">Remarks</span></span>

<span data-ttu-id="4a8bb-118">Un efecto contiene una o más técnicas; cada técnica contiene una o varias fases.</span><span class="sxs-lookup"><span data-stu-id="4a8bb-118">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="4a8bb-119">Puede tener acceso a una técnica mediante su nombre o con un índice.</span><span class="sxs-lookup"><span data-stu-id="4a8bb-119">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="4a8bb-120">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="4a8bb-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4a8bb-121">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="4a8bb-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4a8bb-122">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4a8bb-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a8bb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a8bb-123">Requirements</span></span>



| <span data-ttu-id="4a8bb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a8bb-124">Requirement</span></span> | <span data-ttu-id="4a8bb-125">Value</span><span class="sxs-lookup"><span data-stu-id="4a8bb-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8bb-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a8bb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4a8bb-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a8bb-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4a8bb-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a8bb-128">Library</span></span><br/> | <dl> <span data-ttu-id="4a8bb-129"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="4a8bb-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a8bb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a8bb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a8bb-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="4a8bb-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

