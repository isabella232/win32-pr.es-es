---
title: Método ID3DX11Effect GetConstantBufferByIndex (D3dx11effect. h)
description: Obtiene un búfer de constantes por índice.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Método GetConstantBufferByIndex Direct3D 11
- Método GetConstantBufferByIndex Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetConstantBufferByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbc44b2d9ceea1bcfbf854a8d3c6998d03e3eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987097"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a><span data-ttu-id="5c291-106">ID3DX11Effect:: GetConstantBufferByIndex (método)</span><span class="sxs-lookup"><span data-stu-id="5c291-106">ID3DX11Effect::GetConstantBufferByIndex method</span></span>

<span data-ttu-id="5c291-107">Obtiene un búfer de constantes por índice.</span><span class="sxs-lookup"><span data-stu-id="5c291-107">Get a constant buffer by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c291-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c291-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="5c291-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c291-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c291-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="5c291-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="5c291-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c291-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5c291-112">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="5c291-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c291-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c291-113">Return value</span></span>

<span data-ttu-id="5c291-114">Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5c291-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="5c291-115">Un puntero a un [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="5c291-115">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c291-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c291-116">Remarks</span></span>

<span data-ttu-id="5c291-117">Un efecto que contiene una variable que una aplicación va a leer o escribir requiere al menos un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="5c291-117">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="5c291-118">Para obtener el mejor rendimiento, un efecto debe organizar las variables en uno o varios búferes de constantes según su frecuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="5c291-118">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="5c291-119">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="5c291-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5c291-120">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5c291-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5c291-121">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5c291-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c291-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c291-122">Requirements</span></span>



| <span data-ttu-id="5c291-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c291-123">Requirement</span></span> | <span data-ttu-id="5c291-124">Value</span><span class="sxs-lookup"><span data-stu-id="5c291-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c291-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c291-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5c291-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c291-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5c291-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c291-127">Library</span></span><br/> | <dl> <span data-ttu-id="5c291-128"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="5c291-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c291-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c291-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c291-130">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="5c291-130">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

