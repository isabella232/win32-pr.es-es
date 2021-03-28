---
title: Método ID3DX11Effect GetConstantBufferByName (D3dx11effect. h)
description: Obtiene un búfer de constantes por nombre.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- Método GetConstantBufferByName Direct3D 11
- Método GetConstantBufferByName Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetConstantBufferByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa01d20bfeebfa3f689a58aae5c5face8b879e3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914790"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a><span data-ttu-id="6c3b9-106">ID3DX11Effect:: GetConstantBufferByName (método)</span><span class="sxs-lookup"><span data-stu-id="6c3b9-106">ID3DX11Effect::GetConstantBufferByName method</span></span>

<span data-ttu-id="6c3b9-107">Obtiene un búfer de constantes por nombre.</span><span class="sxs-lookup"><span data-stu-id="6c3b9-107">Get a constant buffer by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c3b9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c3b9-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="6c3b9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c3b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c3b9-110">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="6c3b9-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="6c3b9-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6c3b9-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6c3b9-112">Nombre del búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="6c3b9-112">The constant-buffer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c3b9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c3b9-113">Return value</span></span>

<span data-ttu-id="6c3b9-114">Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c3b9-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="6c3b9-115">Puntero al búfer de constantes indicado por el nombre.</span><span class="sxs-lookup"><span data-stu-id="6c3b9-115">A pointer to the constant buffer indicated by the Name.</span></span> <span data-ttu-id="6c3b9-116">Vea [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="6c3b9-116">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6c3b9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c3b9-117">Remarks</span></span>

<span data-ttu-id="6c3b9-118">Un efecto que contiene una variable que una aplicación va a leer o escribir requiere al menos un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="6c3b9-118">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="6c3b9-119">Para obtener el mejor rendimiento, un efecto debe organizar las variables en uno o varios búferes de constantes según su frecuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="6c3b9-119">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="6c3b9-120">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="6c3b9-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6c3b9-121">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6c3b9-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6c3b9-122">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6c3b9-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c3b9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c3b9-123">Requirements</span></span>



| <span data-ttu-id="6c3b9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c3b9-124">Requirement</span></span> | <span data-ttu-id="6c3b9-125">Value</span><span class="sxs-lookup"><span data-stu-id="6c3b9-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3b9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c3b9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6c3b9-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c3b9-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6c3b9-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c3b9-128">Library</span></span><br/> | <dl> <span data-ttu-id="6c3b9-129"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="6c3b9-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c3b9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c3b9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3b9-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="6c3b9-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

