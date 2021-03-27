---
title: Método ID3DX11Effect GetDevice (D3dx11effect. h)
description: Obtiene el dispositivo que creó el efecto.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- Método GetDevice Direct3D 11
- Método GetDevice Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetDevice
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25317740cade8a937aeeeac29f5a608bb4a43931
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280452"
---
# <a name="id3dx11effectgetdevice-method"></a><span data-ttu-id="62d60-106">ID3DX11Effect:: GetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="62d60-106">ID3DX11Effect::GetDevice method</span></span>

<span data-ttu-id="62d60-107">Obtiene el dispositivo que creó el efecto.</span><span class="sxs-lookup"><span data-stu-id="62d60-107">Get the device that created the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="62d60-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62d60-108">Syntax</span></span>


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="62d60-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62d60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62d60-110">*ppDevice*</span><span class="sxs-lookup"><span data-stu-id="62d60-110">*ppDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="62d60-111">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span><span class="sxs-lookup"><span data-stu-id="62d60-111">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span></span>

<span data-ttu-id="62d60-112">Un puntero a un [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span><span class="sxs-lookup"><span data-stu-id="62d60-112">A pointer to an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62d60-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62d60-113">Return value</span></span>

<span data-ttu-id="62d60-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62d60-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62d60-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="62d60-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62d60-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62d60-116">Remarks</span></span>

<span data-ttu-id="62d60-117">Se crea un efecto para un dispositivo específico mediante una llamada a una función como [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="62d60-117">An effect is created for a specific device, by calling a function such as [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

> [!Note]  
> <span data-ttu-id="62d60-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="62d60-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="62d60-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="62d60-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="62d60-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="62d60-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62d60-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62d60-121">Requirements</span></span>



| <span data-ttu-id="62d60-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="62d60-122">Requirement</span></span> | <span data-ttu-id="62d60-123">Value</span><span class="sxs-lookup"><span data-stu-id="62d60-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62d60-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62d60-124">Header</span></span><br/>  | <dl> <span data-ttu-id="62d60-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="62d60-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="62d60-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62d60-126">Library</span></span><br/> | <dl> <span data-ttu-id="62d60-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="62d60-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62d60-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="62d60-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62d60-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="62d60-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





