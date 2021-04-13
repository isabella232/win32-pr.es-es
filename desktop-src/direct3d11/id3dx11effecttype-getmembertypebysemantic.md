---
title: Método ID3DX11EffectType GetMemberTypeBySemantic (D3dx11effect. h)
description: Obtiene un tipo de miembro por semántica.
ms.assetid: d5fea2d9-8d08-4e02-a9c6-dbcfaaf4a7d1
keywords:
- Método GetMemberTypeBySemantic Direct3D 11
- Método GetMemberTypeBySemantic Direct3D 11, interfaz ID3DX11EffectType
- Interfaz ID3DX11EffectType Direct3D 11, método GetMemberTypeBySemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5f0894c83ff2d0885ae3b951e0e324343fae8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998682"
---
# <a name="id3dx11effecttypegetmembertypebysemantic-method"></a><span data-ttu-id="56d2b-106">ID3DX11EffectType:: GetMemberTypeBySemantic (método)</span><span class="sxs-lookup"><span data-stu-id="56d2b-106">ID3DX11EffectType::GetMemberTypeBySemantic method</span></span>

<span data-ttu-id="56d2b-107">Obtiene un tipo de miembro por semántica.</span><span class="sxs-lookup"><span data-stu-id="56d2b-107">Get a member type by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d2b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56d2b-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="56d2b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56d2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56d2b-110">*Semántica*</span><span class="sxs-lookup"><span data-stu-id="56d2b-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="56d2b-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="56d2b-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="56d2b-112">Una semántica.</span><span class="sxs-lookup"><span data-stu-id="56d2b-112">A semantic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56d2b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56d2b-113">Return value</span></span>

<span data-ttu-id="56d2b-114">Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="56d2b-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="56d2b-115">Un puntero a un [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="56d2b-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="56d2b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56d2b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="56d2b-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="56d2b-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="56d2b-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="56d2b-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="56d2b-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="56d2b-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56d2b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56d2b-120">Requirements</span></span>



| <span data-ttu-id="56d2b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="56d2b-121">Requirement</span></span> | <span data-ttu-id="56d2b-122">Value</span><span class="sxs-lookup"><span data-stu-id="56d2b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56d2b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56d2b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="56d2b-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="56d2b-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="56d2b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56d2b-125">Library</span></span><br/> | <dl> <span data-ttu-id="56d2b-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="56d2b-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56d2b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="56d2b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d2b-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="56d2b-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

