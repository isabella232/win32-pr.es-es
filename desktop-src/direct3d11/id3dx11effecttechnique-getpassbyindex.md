---
title: Método ID3DX11EffectTechnique GetPassByIndex (D3dx11effect. h)
description: Obtiene un paso por índice.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- Método GetPassByIndex Direct3D 11
- Método GetPassByIndex Direct3D 11, interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11, método GetPassByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6af222298cc3d00ad87e5037f9de20139e4fc40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003933"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a><span data-ttu-id="673f5-106">ID3DX11EffectTechnique:: GetPassByIndex (método)</span><span class="sxs-lookup"><span data-stu-id="673f5-106">ID3DX11EffectTechnique::GetPassByIndex method</span></span>

<span data-ttu-id="673f5-107">Obtiene un paso por índice.</span><span class="sxs-lookup"><span data-stu-id="673f5-107">Get a pass by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="673f5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="673f5-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="673f5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="673f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="673f5-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="673f5-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="673f5-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="673f5-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="673f5-112">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="673f5-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="673f5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="673f5-113">Return value</span></span>

<span data-ttu-id="673f5-114">Tipo: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="673f5-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="673f5-115">Un puntero a un [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="673f5-115">A pointer to a [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="673f5-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="673f5-116">Remarks</span></span>

<span data-ttu-id="673f5-117">Una técnica contiene uno o más pasos; obtener un paso mediante un nombre o un índice.</span><span class="sxs-lookup"><span data-stu-id="673f5-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="673f5-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="673f5-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="673f5-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="673f5-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="673f5-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="673f5-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="673f5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="673f5-121">Requirements</span></span>



| <span data-ttu-id="673f5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="673f5-122">Requirement</span></span> | <span data-ttu-id="673f5-123">Value</span><span class="sxs-lookup"><span data-stu-id="673f5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="673f5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="673f5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="673f5-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="673f5-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="673f5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="673f5-126">Library</span></span><br/> | <dl> <span data-ttu-id="673f5-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="673f5-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="673f5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="673f5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673f5-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="673f5-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

