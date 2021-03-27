---
title: Método ID3DX11EffectPass GetAnnotationByName (D3dx11effect. h)
description: Obtiene una anotación por nombre. | Método ID3DX11EffectPass GetAnnotationByName (D3dx11effect. h)
ms.assetid: b54a4fb0-62c7-4d96-af30-f9ae04ff7dab
keywords:
- Método GetAnnotationByName Direct3D 11
- Método GetAnnotationByName Direct3D 11, interfaz ID3DX11EffectPass
- Interfaz ID3DX11EffectPass Direct3D 11, método GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129f1548e7f63c47906ac736cbddb5f6b2548b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003902"
---
# <a name="id3dx11effectpassgetannotationbyname-method"></a><span data-ttu-id="23db3-107">ID3DX11EffectPass:: GetAnnotationByName (método)</span><span class="sxs-lookup"><span data-stu-id="23db3-107">ID3DX11EffectPass::GetAnnotationByName method</span></span>

<span data-ttu-id="23db3-108">Obtiene una anotación por nombre.</span><span class="sxs-lookup"><span data-stu-id="23db3-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="23db3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23db3-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="23db3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23db3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23db3-111">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="23db3-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="23db3-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="23db3-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="23db3-113">El nombre de la anotación.</span><span class="sxs-lookup"><span data-stu-id="23db3-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23db3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23db3-114">Return value</span></span>

<span data-ttu-id="23db3-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="23db3-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="23db3-116">Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="23db3-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23db3-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23db3-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23db3-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="23db3-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="23db3-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="23db3-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="23db3-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="23db3-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23db3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23db3-121">Requirements</span></span>



| <span data-ttu-id="23db3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="23db3-122">Requirement</span></span> | <span data-ttu-id="23db3-123">Value</span><span class="sxs-lookup"><span data-stu-id="23db3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23db3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23db3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="23db3-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="23db3-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="23db3-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23db3-126">Library</span></span><br/> | <dl> <span data-ttu-id="23db3-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="23db3-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23db3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="23db3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23db3-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="23db3-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

