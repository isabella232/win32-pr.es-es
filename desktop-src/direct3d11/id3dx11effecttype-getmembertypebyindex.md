---
title: Método ID3DX11EffectType GetMemberTypeByIndex (D3dx11effect. h)
description: Obtiene un tipo de miembro por índice.
ms.assetid: 6421f08f-0236-4d8f-b3c2-ef7ec5ffe2a1
keywords:
- Método GetMemberTypeByIndex Direct3D 11
- Método GetMemberTypeByIndex Direct3D 11, interfaz ID3DX11EffectType
- Interfaz ID3DX11EffectType Direct3D 11, método GetMemberTypeByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5023e064539f57af9998c788385f2a1316433f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547982"
---
# <a name="id3dx11effecttypegetmembertypebyindex-method"></a><span data-ttu-id="f140e-106">ID3DX11EffectType:: GetMemberTypeByIndex (método)</span><span class="sxs-lookup"><span data-stu-id="f140e-106">ID3DX11EffectType::GetMemberTypeByIndex method</span></span>

<span data-ttu-id="f140e-107">Obtiene un tipo de miembro por índice.</span><span class="sxs-lookup"><span data-stu-id="f140e-107">Get a member type by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f140e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f140e-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="f140e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f140e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f140e-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="f140e-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="f140e-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f140e-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f140e-112">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="f140e-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f140e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f140e-113">Return value</span></span>

<span data-ttu-id="f140e-114">Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="f140e-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="f140e-115">Un puntero a un [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="f140e-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f140e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f140e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f140e-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="f140e-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f140e-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f140e-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f140e-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f140e-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f140e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f140e-120">Requirements</span></span>



| <span data-ttu-id="f140e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f140e-121">Requirement</span></span> | <span data-ttu-id="f140e-122">Value</span><span class="sxs-lookup"><span data-stu-id="f140e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f140e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f140e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f140e-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f140e-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f140e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f140e-125">Library</span></span><br/> | <dl> <span data-ttu-id="f140e-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="f140e-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f140e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f140e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f140e-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="f140e-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

