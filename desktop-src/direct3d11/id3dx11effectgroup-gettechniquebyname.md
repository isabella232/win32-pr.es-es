---
title: Método ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
description: Obtener una técnica por nombre. | Método ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- Método GetTechniqueByName Direct3D 11
- Método GetTechniqueByName Direct3D 11, interfaz ID3DX11EffectGroup
- Interfaz ID3DX11EffectGroup Direct3D 11, método GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5121f67345ba863d773d8e7a73a5d6fa8b69895
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986965"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a><span data-ttu-id="e418e-107">ID3DX11EffectGroup:: GetTechniqueByName (método)</span><span class="sxs-lookup"><span data-stu-id="e418e-107">ID3DX11EffectGroup::GetTechniqueByName method</span></span>

<span data-ttu-id="e418e-108">Obtener una técnica por nombre.</span><span class="sxs-lookup"><span data-stu-id="e418e-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e418e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e418e-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="e418e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e418e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e418e-111">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="e418e-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="e418e-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e418e-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e418e-113">El nombre de la técnica.</span><span class="sxs-lookup"><span data-stu-id="e418e-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e418e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e418e-114">Return value</span></span>

<span data-ttu-id="e418e-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="e418e-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="e418e-116">Un puntero a un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md), o **null** si no se encuentra la técnica.</span><span class="sxs-lookup"><span data-stu-id="e418e-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md), or **NULL** if the technique is not found.</span></span>

## <a name="remarks"></a><span data-ttu-id="e418e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e418e-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e418e-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="e418e-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e418e-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e418e-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e418e-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e418e-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e418e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e418e-121">Requirements</span></span>



| <span data-ttu-id="e418e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e418e-122">Requirement</span></span> | <span data-ttu-id="e418e-123">Value</span><span class="sxs-lookup"><span data-stu-id="e418e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e418e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e418e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e418e-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e418e-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e418e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e418e-126">Library</span></span><br/> | <dl> <span data-ttu-id="e418e-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="e418e-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e418e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e418e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e418e-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="e418e-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

