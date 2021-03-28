---
title: Método ID3DX11Effect GetGroupByName (D3dx11effect. h)
description: Obtiene un grupo de efectos por nombre.
ms.assetid: 14b4b484-848a-409c-9a99-207ab25b7566
keywords:
- Método GetGroupByName Direct3D 11
- Método GetGroupByName Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetGroupByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1c2132dedb34fe71db30bf82b1c6d336f110a8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998628"
---
# <a name="id3dx11effectgetgroupbyname-method"></a><span data-ttu-id="11de1-106">ID3DX11Effect:: GetGroupByName (método)</span><span class="sxs-lookup"><span data-stu-id="11de1-106">ID3DX11Effect::GetGroupByName method</span></span>

<span data-ttu-id="11de1-107">Obtiene un grupo de efectos por nombre.</span><span class="sxs-lookup"><span data-stu-id="11de1-107">Gets an effect group by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="11de1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11de1-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="11de1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11de1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11de1-110">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="11de1-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="11de1-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="11de1-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="11de1-112">Nombre del grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="11de1-112">Name of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11de1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11de1-113">Return value</span></span>

<span data-ttu-id="11de1-114">Tipo: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="11de1-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="11de1-115">Puntero a una interfaz [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="11de1-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="11de1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11de1-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="11de1-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="11de1-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="11de1-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="11de1-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="11de1-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="11de1-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11de1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11de1-120">Requirements</span></span>



| <span data-ttu-id="11de1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="11de1-121">Requirement</span></span> | <span data-ttu-id="11de1-122">Value</span><span class="sxs-lookup"><span data-stu-id="11de1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11de1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11de1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="11de1-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="11de1-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="11de1-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11de1-125">Library</span></span><br/> | <dl> <span data-ttu-id="11de1-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="11de1-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11de1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="11de1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11de1-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="11de1-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

