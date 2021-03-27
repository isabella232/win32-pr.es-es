---
title: Método ID3DX11EffectGroup GetAnnotationByIndex (D3dx11effect. h)
description: Obtiene una anotación por índice. | Método ID3DX11EffectGroup GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: 9d3a54b1-384b-4ed4-96a3-09d6bacafda1
keywords:
- Método GetAnnotationByIndex Direct3D 11
- Método GetAnnotationByIndex Direct3D 11, interfaz ID3DX11EffectGroup
- Interfaz ID3DX11EffectGroup Direct3D 11, método GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663dc8d487552dba521c8e47f9a1eecf6db38122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280408"
---
# <a name="id3dx11effectgroupgetannotationbyindex-method"></a><span data-ttu-id="3c1f4-107">ID3DX11EffectGroup:: GetAnnotationByIndex (método)</span><span class="sxs-lookup"><span data-stu-id="3c1f4-107">ID3DX11EffectGroup::GetAnnotationByIndex method</span></span>

<span data-ttu-id="3c1f4-108">Obtiene una anotación por índice.</span><span class="sxs-lookup"><span data-stu-id="3c1f4-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c1f4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c1f4-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="3c1f4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c1f4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c1f4-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="3c1f4-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="3c1f4-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c1f4-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c1f4-113">Índice de la anotación.</span><span class="sxs-lookup"><span data-stu-id="3c1f4-113">Index of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c1f4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c1f4-114">Return value</span></span>

<span data-ttu-id="3c1f4-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c1f4-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="3c1f4-116">Puntero a una interfaz [**ID3DX11EffectVariable**](id3dx11effectvariable.md) .</span><span class="sxs-lookup"><span data-stu-id="3c1f4-116">Pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c1f4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c1f4-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3c1f4-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="3c1f4-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3c1f4-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3c1f4-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3c1f4-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3c1f4-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c1f4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c1f4-121">Requirements</span></span>



| <span data-ttu-id="3c1f4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c1f4-122">Requirement</span></span> | <span data-ttu-id="3c1f4-123">Value</span><span class="sxs-lookup"><span data-stu-id="3c1f4-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c1f4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c1f4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3c1f4-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c1f4-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3c1f4-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c1f4-126">Library</span></span><br/> | <dl> <span data-ttu-id="3c1f4-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="3c1f4-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c1f4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c1f4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c1f4-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="3c1f4-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

