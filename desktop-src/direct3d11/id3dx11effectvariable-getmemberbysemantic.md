---
title: Método ID3DX11EffectVariable GetMemberBySemantic (D3dx11effect. h)
description: Obtiene un miembro de estructura por semántica.
ms.assetid: e4ae1f6a-43d2-45df-9dba-833d4f767818
keywords:
- Método GetMemberBySemantic Direct3D 11
- Método GetMemberBySemantic Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método GetMemberBySemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af8b628247dcc89f8df99c6ffebb04d500e76a1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998701"
---
# <a name="id3dx11effectvariablegetmemberbysemantic-method"></a><span data-ttu-id="33a53-106">ID3DX11EffectVariable:: GetMemberBySemantic (método)</span><span class="sxs-lookup"><span data-stu-id="33a53-106">ID3DX11EffectVariable::GetMemberBySemantic method</span></span>

<span data-ttu-id="33a53-107">Obtiene un miembro de estructura por semántica.</span><span class="sxs-lookup"><span data-stu-id="33a53-107">Get a structure member by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a53-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33a53-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="33a53-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33a53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33a53-110">*Semántica*</span><span class="sxs-lookup"><span data-stu-id="33a53-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="33a53-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="33a53-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="33a53-112">La semántica.</span><span class="sxs-lookup"><span data-stu-id="33a53-112">The semantic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33a53-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33a53-113">Return value</span></span>

<span data-ttu-id="33a53-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="33a53-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="33a53-115">Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="33a53-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="33a53-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33a53-116">Remarks</span></span>

<span data-ttu-id="33a53-117">Si la variable de efecto es una estructura, use este método para buscar un miembro por semántica adjunta.</span><span class="sxs-lookup"><span data-stu-id="33a53-117">If the effect variable is an structure, use this method to look up a member by attached semantic.</span></span>

> [!Note]  
> <span data-ttu-id="33a53-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="33a53-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="33a53-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="33a53-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="33a53-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="33a53-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="33a53-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33a53-121">Requirements</span></span>



| <span data-ttu-id="33a53-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="33a53-122">Requirement</span></span> | <span data-ttu-id="33a53-123">Value</span><span class="sxs-lookup"><span data-stu-id="33a53-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a53-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33a53-124">Header</span></span><br/>  | <dl> <span data-ttu-id="33a53-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="33a53-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="33a53-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33a53-126">Library</span></span><br/> | <dl> <span data-ttu-id="33a53-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="33a53-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33a53-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="33a53-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a53-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="33a53-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

