---
title: Método ID3DX11EffectType GetMemberTypeByName (D3dx11effect. h)
description: Obtiene un tipo de miembro por nombre.
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- Método GetMemberTypeByName Direct3D 11
- Método GetMemberTypeByName Direct3D 11, interfaz ID3DX11EffectType
- Interfaz ID3DX11EffectType Direct3D 11, método GetMemberTypeByName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e573bcdc2dc4470e87539a307cdc38b71a6320ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998365"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a><span data-ttu-id="d5200-106">ID3DX11EffectType:: GetMemberTypeByName (método)</span><span class="sxs-lookup"><span data-stu-id="d5200-106">ID3DX11EffectType::GetMemberTypeByName method</span></span>

<span data-ttu-id="d5200-107">Obtiene un tipo de miembro por nombre.</span><span class="sxs-lookup"><span data-stu-id="d5200-107">Get an member type by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5200-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5200-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="d5200-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5200-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5200-110">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="d5200-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="d5200-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d5200-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d5200-112">Nombre de un miembro.</span><span class="sxs-lookup"><span data-stu-id="d5200-112">A member's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5200-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5200-113">Return value</span></span>

<span data-ttu-id="d5200-114">Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="d5200-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="d5200-115">Un puntero a un [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="d5200-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5200-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5200-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5200-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="d5200-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d5200-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="d5200-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d5200-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d5200-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d5200-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5200-120">Requirements</span></span>



| <span data-ttu-id="d5200-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5200-121">Requirement</span></span> | <span data-ttu-id="d5200-122">Value</span><span class="sxs-lookup"><span data-stu-id="d5200-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5200-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5200-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d5200-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5200-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d5200-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5200-125">Library</span></span><br/> | <dl> <span data-ttu-id="d5200-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="d5200-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5200-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5200-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5200-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="d5200-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

