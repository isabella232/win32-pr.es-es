---
title: Método ID3DX11EffectInterfaceVariable SetClassInstance (D3dx11effect. h)
description: Establece una instancia de clase.
ms.assetid: fc71a0d2-054a-48ed-86a5-54cf0017062a
keywords:
- Método SetClassInstance Direct3D 11
- Método SetClassInstance Direct3D 11, interfaz ID3DX11EffectInterfaceVariable
- Interfaz ID3DX11EffectInterfaceVariable Direct3D 11, método SetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.SetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03d319d55b073393ff511b2e072aa07c244e5a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986947"
---
# <a name="id3dx11effectinterfacevariablesetclassinstance-method"></a><span data-ttu-id="4c79e-106">ID3DX11EffectInterfaceVariable:: SetClassInstance (método)</span><span class="sxs-lookup"><span data-stu-id="4c79e-106">ID3DX11EffectInterfaceVariable::SetClassInstance method</span></span>

<span data-ttu-id="4c79e-107">Establece una instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="4c79e-107">Sets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c79e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c79e-108">Syntax</span></span>


```C++
HRESULT SetClassInstance(
   ID3DX11EffectClassInstanceVariable *pEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="4c79e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c79e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c79e-110">*pEffectClassInstance*</span><span class="sxs-lookup"><span data-stu-id="4c79e-110">*pEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="4c79e-111">Tipo: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c79e-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span></span>

<span data-ttu-id="4c79e-112">Puntero a una interfaz [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) .</span><span class="sxs-lookup"><span data-stu-id="4c79e-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c79e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c79e-113">Return value</span></span>

<span data-ttu-id="4c79e-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c79e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c79e-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4c79e-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c79e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c79e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c79e-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="4c79e-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4c79e-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="4c79e-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4c79e-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4c79e-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c79e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c79e-120">Requirements</span></span>



| <span data-ttu-id="4c79e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c79e-121">Requirement</span></span> | <span data-ttu-id="4c79e-122">Value</span><span class="sxs-lookup"><span data-stu-id="4c79e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c79e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c79e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4c79e-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c79e-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4c79e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c79e-125">Library</span></span><br/> | <dl> <span data-ttu-id="4c79e-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="4c79e-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c79e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c79e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c79e-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="4c79e-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





