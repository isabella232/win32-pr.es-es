---
title: Método ID3DX11EffectScalarVariable GetFloat (D3dx11effect. h)
description: Obtiene una variable de punto flotante.
ms.assetid: 0416db40-5e70-44e4-905f-86f49a9b58b8
keywords:
- Método GetFloat Direct3D 11
- Método GetFloat Direct3D 11, interfaz ID3DX11EffectScalarVariable
- Interfaz ID3DX11EffectScalarVariable Direct3D 11, método GetFloat
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1d8f7ae63bc8312c2432e50f5b6dcfeccdf525
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362748"
---
# <a name="id3dx11effectscalarvariablegetfloat-method"></a><span data-ttu-id="e8c71-106">ID3DX11EffectScalarVariable:: GetFloat (método)</span><span class="sxs-lookup"><span data-stu-id="e8c71-106">ID3DX11EffectScalarVariable::GetFloat method</span></span>

<span data-ttu-id="e8c71-107">Obtiene una variable de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="e8c71-107">Get a floating-point variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c71-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8c71-108">Syntax</span></span>


```C++
HRESULT GetFloat(
   float *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e8c71-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8c71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c71-110">*pValue*</span><span class="sxs-lookup"><span data-stu-id="e8c71-110">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="e8c71-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="e8c71-111">Type: **float\***</span></span>

<span data-ttu-id="e8c71-112">Puntero a la variable.</span><span class="sxs-lookup"><span data-stu-id="e8c71-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8c71-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8c71-113">Return value</span></span>

<span data-ttu-id="e8c71-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8c71-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8c71-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e8c71-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8c71-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8c71-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8c71-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="e8c71-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e8c71-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e8c71-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e8c71-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e8c71-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8c71-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8c71-120">Requirements</span></span>



| <span data-ttu-id="e8c71-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8c71-121">Requirement</span></span> | <span data-ttu-id="e8c71-122">Value</span><span class="sxs-lookup"><span data-stu-id="e8c71-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c71-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8c71-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e8c71-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8c71-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e8c71-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8c71-125">Library</span></span><br/> | <dl> <span data-ttu-id="e8c71-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="e8c71-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8c71-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8c71-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c71-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="e8c71-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

 





