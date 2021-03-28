---
title: Método ID3DX11EffectTechnique GetPassByName (D3dx11effect. h)
description: Obtiene un paso por nombre.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- Método GetPassByName Direct3D 11
- Método GetPassByName Direct3D 11, interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11, método GetPassByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84bbe9b954efff12e458ee6172665118a7b8ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998485"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a><span data-ttu-id="a1541-106">ID3DX11EffectTechnique:: GetPassByName (método)</span><span class="sxs-lookup"><span data-stu-id="a1541-106">ID3DX11EffectTechnique::GetPassByName method</span></span>

<span data-ttu-id="a1541-107">Obtiene un paso por nombre.</span><span class="sxs-lookup"><span data-stu-id="a1541-107">Get a pass by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1541-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1541-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="a1541-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1541-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1541-110">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="a1541-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="a1541-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a1541-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a1541-112">Nombre del paso.</span><span class="sxs-lookup"><span data-stu-id="a1541-112">The name of the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1541-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1541-113">Return value</span></span>

<span data-ttu-id="a1541-114">Tipo: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1541-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="a1541-115">Un puntero a un [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="a1541-115">A pointer to an [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1541-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1541-116">Remarks</span></span>

<span data-ttu-id="a1541-117">Una técnica contiene uno o más pasos; obtener un paso mediante un nombre o un índice.</span><span class="sxs-lookup"><span data-stu-id="a1541-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="a1541-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="a1541-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a1541-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a1541-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a1541-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a1541-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1541-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1541-121">Requirements</span></span>



| <span data-ttu-id="a1541-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1541-122">Requirement</span></span> | <span data-ttu-id="a1541-123">Value</span><span class="sxs-lookup"><span data-stu-id="a1541-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1541-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1541-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a1541-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1541-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a1541-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1541-126">Library</span></span><br/> | <dl> <span data-ttu-id="a1541-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="a1541-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1541-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1541-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1541-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="a1541-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

