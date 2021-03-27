---
title: Método ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
description: Obtener una técnica por nombre. | Método ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- Método GetTechniqueByName Direct3D 11
- Método GetTechniqueByName Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26b6067352d4ca898cc1fc970524040d407bda1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987091"
---
# <a name="id3dx11effectgettechniquebyname-method"></a><span data-ttu-id="e3b9e-107">ID3DX11Effect:: GetTechniqueByName (método)</span><span class="sxs-lookup"><span data-stu-id="e3b9e-107">ID3DX11Effect::GetTechniqueByName method</span></span>

<span data-ttu-id="e3b9e-108">Obtener una técnica por nombre.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b9e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3b9e-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="e3b9e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3b9e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b9e-111">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="e3b9e-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="e3b9e-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e3b9e-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e3b9e-113">El nombre de la técnica.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b9e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3b9e-114">Return value</span></span>

<span data-ttu-id="e3b9e-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3b9e-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="e3b9e-116">Un puntero a un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="e3b9e-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span> <span data-ttu-id="e3b9e-117">Si no se encuentra una técnica con el nombre adecuado, se devuelve una técnica no válida.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-117">If a technique with the appropriate name is not found an invalid technique is returned.</span></span> <span data-ttu-id="e3b9e-118">Se debe llamar a [**ID3DX11EffectTechnique:: IsValid**](id3dx11effecttechnique-isvalid.md) en la técnica devuelta para determinar si es válido.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-118">[**ID3DX11EffectTechnique::IsValid**](id3dx11effecttechnique-isvalid.md) should be called on the returned technique to determine whether it is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b9e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3b9e-119">Remarks</span></span>

<span data-ttu-id="e3b9e-120">Un efecto contiene una o más técnicas; cada técnica contiene una o varias fases.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-120">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="e3b9e-121">Puede tener acceso a una técnica mediante su nombre o con un índice.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-121">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="e3b9e-122">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-122">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e3b9e-123">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-123">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e3b9e-124">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e3b9e-124">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e3b9e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3b9e-125">Requirements</span></span>



| <span data-ttu-id="e3b9e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b9e-126">Requirement</span></span> | <span data-ttu-id="e3b9e-127">Value</span><span class="sxs-lookup"><span data-stu-id="e3b9e-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b9e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3b9e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e3b9e-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b9e-129"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e3b9e-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3b9e-130">Library</span></span><br/> | <dl> <span data-ttu-id="e3b9e-131"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="e3b9e-131"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b9e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3b9e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b9e-133">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="e3b9e-133">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

