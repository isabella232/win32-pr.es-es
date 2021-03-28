---
title: Método ID3DX11EffectType GetMemberName (D3dx11effect. h)
description: Obtiene el nombre de un miembro.
ms.assetid: cd231741-09e1-4e69-9384-5cdfbf83fc8b
keywords:
- Método GetMemberName Direct3D 11
- Método GetMemberName Direct3D 11, interfaz ID3DX11EffectType
- Interfaz ID3DX11EffectType Direct3D 11, método GetMemberName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4aa9a24067d8ef19680ca58e41659da850659b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362633"
---
# <a name="id3dx11effecttypegetmembername-method"></a><span data-ttu-id="5ec85-106">ID3DX11EffectType:: GetMemberName (método)</span><span class="sxs-lookup"><span data-stu-id="5ec85-106">ID3DX11EffectType::GetMemberName method</span></span>

<span data-ttu-id="5ec85-107">Obtiene el nombre de un miembro.</span><span class="sxs-lookup"><span data-stu-id="5ec85-107">Get the name of a member.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec85-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ec85-108">Syntax</span></span>


```C++
LPCSTR GetMemberName(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="5ec85-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ec85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ec85-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="5ec85-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="5ec85-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5ec85-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5ec85-112">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="5ec85-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ec85-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ec85-113">Return value</span></span>

<span data-ttu-id="5ec85-114">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5ec85-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5ec85-115">Nombre del miembro.</span><span class="sxs-lookup"><span data-stu-id="5ec85-115">The name of the member.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ec85-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ec85-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ec85-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="5ec85-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5ec85-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5ec85-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5ec85-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5ec85-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ec85-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ec85-120">Requirements</span></span>



| <span data-ttu-id="5ec85-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ec85-121">Requirement</span></span> | <span data-ttu-id="5ec85-122">Value</span><span class="sxs-lookup"><span data-stu-id="5ec85-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec85-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ec85-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5ec85-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ec85-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5ec85-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ec85-125">Library</span></span><br/> | <dl> <span data-ttu-id="5ec85-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="5ec85-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec85-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ec85-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec85-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="5ec85-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

