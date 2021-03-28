---
title: Método ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect. h)
description: Obtiene una anotación por nombre. | Método ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect. h)
ms.assetid: 3a9e1fa7-4586-42d6-a723-3140f29a01b4
keywords:
- Método GetAnnotationByName Direct3D 11
- Método GetAnnotationByName Direct3D 11, interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11, método GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae5a7c24d392bd034dfcd69fb67723c9492f982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362624"
---
# <a name="id3dx11effecttechniquegetannotationbyname-method"></a><span data-ttu-id="9a588-107">ID3DX11EffectTechnique:: GetAnnotationByName (método)</span><span class="sxs-lookup"><span data-stu-id="9a588-107">ID3DX11EffectTechnique::GetAnnotationByName method</span></span>

<span data-ttu-id="9a588-108">Obtiene una anotación por nombre.</span><span class="sxs-lookup"><span data-stu-id="9a588-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a588-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a588-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="9a588-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a588-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a588-111">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="9a588-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="9a588-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a588-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a588-113">Nombre de la anotación.</span><span class="sxs-lookup"><span data-stu-id="9a588-113">Name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a588-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a588-114">Return value</span></span>

<span data-ttu-id="9a588-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a588-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="9a588-116">Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="9a588-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a588-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a588-117">Remarks</span></span>

<span data-ttu-id="9a588-118">Use una anotación para adjuntar un fragmento de metadatos a una técnica.</span><span class="sxs-lookup"><span data-stu-id="9a588-118">Use an annotation to attach a piece of metadata to a technique.</span></span>

> [!Note]  
> <span data-ttu-id="9a588-119">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="9a588-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9a588-120">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="9a588-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9a588-121">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9a588-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a588-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a588-122">Requirements</span></span>



| <span data-ttu-id="9a588-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a588-123">Requirement</span></span> | <span data-ttu-id="9a588-124">Value</span><span class="sxs-lookup"><span data-stu-id="9a588-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a588-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a588-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9a588-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a588-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9a588-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a588-127">Library</span></span><br/> | <dl> <span data-ttu-id="9a588-128"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="9a588-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a588-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a588-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a588-130">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="9a588-130">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

