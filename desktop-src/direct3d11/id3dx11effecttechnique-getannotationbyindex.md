---
title: Método ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect. h)
description: Obtiene una anotación por índice. | Método ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: 703663b0-ee00-4686-a038-6c99ce61266b
keywords:
- Método GetAnnotationByIndex Direct3D 11
- Método GetAnnotationByIndex Direct3D 11, interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11, método GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e30712ba38f1360a992a8e409c249a746cca036
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998706"
---
# <a name="id3dx11effecttechniquegetannotationbyindex-method"></a><span data-ttu-id="bb8c5-107">ID3DX11EffectTechnique:: GetAnnotationByIndex (método)</span><span class="sxs-lookup"><span data-stu-id="bb8c5-107">ID3DX11EffectTechnique::GetAnnotationByIndex method</span></span>

<span data-ttu-id="bb8c5-108">Obtiene una anotación por índice.</span><span class="sxs-lookup"><span data-stu-id="bb8c5-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb8c5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb8c5-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="bb8c5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb8c5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb8c5-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="bb8c5-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="bb8c5-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bb8c5-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bb8c5-113">Índice de base cero del puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="bb8c5-113">The zero-based index of the interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb8c5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb8c5-114">Return value</span></span>

<span data-ttu-id="bb8c5-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb8c5-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="bb8c5-116">Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="bb8c5-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bb8c5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb8c5-117">Remarks</span></span>

<span data-ttu-id="bb8c5-118">Use una anotación para adjuntar un fragmento de metadatos a una técnica.</span><span class="sxs-lookup"><span data-stu-id="bb8c5-118">Use an annotation to attach a piece of metadata to a technique.</span></span>

> [!Note]  
> <span data-ttu-id="bb8c5-119">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="bb8c5-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bb8c5-120">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="bb8c5-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bb8c5-121">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bb8c5-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bb8c5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb8c5-122">Requirements</span></span>



| <span data-ttu-id="bb8c5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb8c5-123">Requirement</span></span> | <span data-ttu-id="bb8c5-124">Value</span><span class="sxs-lookup"><span data-stu-id="bb8c5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb8c5-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb8c5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bb8c5-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb8c5-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bb8c5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb8c5-127">Library</span></span><br/> | <dl> <span data-ttu-id="bb8c5-128"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="bb8c5-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb8c5-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb8c5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb8c5-130">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="bb8c5-130">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

