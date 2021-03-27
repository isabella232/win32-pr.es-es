---
title: Método ID3DX11EffectInterfaceVariable GetClassInstance (D3dx11effect. h)
description: Obtiene una instancia de clase.
ms.assetid: a965f4e7-1761-45f1-a72e-7ad0ed1ad671
keywords:
- Método GetClassInstance Direct3D 11
- Método GetClassInstance Direct3D 11, interfaz ID3DX11EffectInterfaceVariable
- Interfaz ID3DX11EffectInterfaceVariable Direct3D 11, método GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f729da6ee84d76dd37a40a7946438e367c1a4cbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003881"
---
# <a name="id3dx11effectinterfacevariablegetclassinstance-method"></a><span data-ttu-id="79539-106">ID3DX11EffectInterfaceVariable:: GetClassInstance (método)</span><span class="sxs-lookup"><span data-stu-id="79539-106">ID3DX11EffectInterfaceVariable::GetClassInstance method</span></span>

<span data-ttu-id="79539-107">Obtiene una instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="79539-107">Get a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="79539-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79539-108">Syntax</span></span>


```C++
HRESULT GetClassInstance(
   ID3DX11EffectClassInstanceVariable **ppEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="79539-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79539-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79539-110">*ppEffectClassInstance*</span><span class="sxs-lookup"><span data-stu-id="79539-110">*ppEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="79539-111">Tipo: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="79539-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span></span>

<span data-ttu-id="79539-112">Puntero a un puntero [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) que se establecerá en la instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="79539-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) pointer that will be set to the class instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79539-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79539-113">Return value</span></span>

<span data-ttu-id="79539-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79539-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79539-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="79539-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="79539-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79539-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="79539-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="79539-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="79539-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="79539-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="79539-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="79539-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79539-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79539-120">Requirements</span></span>



| <span data-ttu-id="79539-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="79539-121">Requirement</span></span> | <span data-ttu-id="79539-122">Value</span><span class="sxs-lookup"><span data-stu-id="79539-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79539-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79539-123">Header</span></span><br/>  | <dl> <span data-ttu-id="79539-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="79539-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="79539-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79539-125">Library</span></span><br/> | <dl> <span data-ttu-id="79539-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="79539-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79539-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="79539-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79539-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="79539-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





