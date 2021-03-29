---
title: Método ID3DX11EffectType GetMemberSemantic (D3dx11effect. h)
description: Obtiene la semántica asociada a un miembro.
ms.assetid: e0666d4e-7510-4496-849e-a0531238b5f8
keywords:
- Método GetMemberSemantic Direct3D 11
- Método GetMemberSemantic Direct3D 11, interfaz ID3DX11EffectType
- Interfaz ID3DX11EffectType Direct3D 11, método GetMemberSemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberSemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6255860dc9f7dc5cf12742e6f40b7e5148a3f27c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998383"
---
# <a name="id3dx11effecttypegetmembersemantic-method"></a><span data-ttu-id="d8aa7-106">ID3DX11EffectType:: GetMemberSemantic (método)</span><span class="sxs-lookup"><span data-stu-id="d8aa7-106">ID3DX11EffectType::GetMemberSemantic method</span></span>

<span data-ttu-id="d8aa7-107">Obtiene la semántica asociada a un miembro.</span><span class="sxs-lookup"><span data-stu-id="d8aa7-107">Get the semantic attached to a member.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8aa7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8aa7-108">Syntax</span></span>


```C++
LPCSTR GetMemberSemantic(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="d8aa7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8aa7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8aa7-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="d8aa7-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="d8aa7-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8aa7-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8aa7-112">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="d8aa7-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8aa7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8aa7-113">Return value</span></span>

<span data-ttu-id="d8aa7-114">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8aa7-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8aa7-115">Cadena que contiene la semántica.</span><span class="sxs-lookup"><span data-stu-id="d8aa7-115">A string that contains the semantic.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8aa7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8aa7-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d8aa7-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="d8aa7-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d8aa7-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="d8aa7-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d8aa7-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d8aa7-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d8aa7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8aa7-120">Requirements</span></span>



| <span data-ttu-id="d8aa7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8aa7-121">Requirement</span></span> | <span data-ttu-id="d8aa7-122">Value</span><span class="sxs-lookup"><span data-stu-id="d8aa7-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8aa7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8aa7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d8aa7-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8aa7-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d8aa7-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8aa7-125">Library</span></span><br/> | <dl> <span data-ttu-id="d8aa7-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="d8aa7-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8aa7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8aa7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8aa7-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="d8aa7-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

