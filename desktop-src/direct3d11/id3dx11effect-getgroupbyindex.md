---
title: Método ID3DX11Effect GetGroupByIndex (D3dx11effect. h)
description: Obtiene un grupo de efectos por índice.
ms.assetid: b38ecdbf-0920-48ff-a599-9629a3581d75
keywords:
- Método GetGroupByIndex Direct3D 11
- Método GetGroupByIndex Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetGroupByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd0f629a60255ed28aa5cc426b99198867e0b23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003921"
---
# <a name="id3dx11effectgetgroupbyindex-method"></a><span data-ttu-id="87734-106">ID3DX11Effect:: GetGroupByIndex (método)</span><span class="sxs-lookup"><span data-stu-id="87734-106">ID3DX11Effect::GetGroupByIndex method</span></span>

<span data-ttu-id="87734-107">Obtiene un grupo de efectos por índice.</span><span class="sxs-lookup"><span data-stu-id="87734-107">Gets an effect group by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="87734-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87734-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="87734-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87734-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87734-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="87734-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="87734-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="87734-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="87734-112">Índice del grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="87734-112">Index of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87734-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87734-113">Return value</span></span>

<span data-ttu-id="87734-114">Tipo: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="87734-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="87734-115">Puntero a una interfaz [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="87734-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="87734-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87734-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87734-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="87734-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="87734-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="87734-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="87734-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="87734-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87734-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87734-120">Requirements</span></span>



| <span data-ttu-id="87734-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="87734-121">Requirement</span></span> | <span data-ttu-id="87734-122">Value</span><span class="sxs-lookup"><span data-stu-id="87734-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87734-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87734-123">Header</span></span><br/>  | <dl> <span data-ttu-id="87734-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="87734-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="87734-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87734-125">Library</span></span><br/> | <dl> <span data-ttu-id="87734-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="87734-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87734-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="87734-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87734-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="87734-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

