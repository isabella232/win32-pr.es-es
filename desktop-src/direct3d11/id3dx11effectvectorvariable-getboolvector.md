---
title: Método ID3DX11EffectVectorVariable GetBoolVector (D3dx11effect. h)
description: Obtiene un vector de cuatro componentes que contiene datos booleanos.
ms.assetid: ecaf5705-d13b-4d61-9766-d2ff183af789
keywords:
- Método GetBoolVector Direct3D 11
- Método GetBoolVector Direct3D 11, interfaz ID3DX11EffectVectorVariable
- Interfaz ID3DX11EffectVectorVariable Direct3D 11, método GetBoolVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetBoolVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a24563bd7c685579115e3b10309fb0a1c158c2e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987078"
---
# <a name="id3dx11effectvectorvariablegetboolvector-method"></a><span data-ttu-id="8aaab-106">ID3DX11EffectVectorVariable:: GetBoolVector (método)</span><span class="sxs-lookup"><span data-stu-id="8aaab-106">ID3DX11EffectVectorVariable::GetBoolVector method</span></span>

<span data-ttu-id="8aaab-107">Obtiene un vector de cuatro componentes que contiene datos booleanos.</span><span class="sxs-lookup"><span data-stu-id="8aaab-107">Get a four-component vector that contains boolean data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aaab-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8aaab-108">Syntax</span></span>


```C++
HRESULT GetBoolVector(
   BOOL *pData
);
```



## <a name="parameters"></a><span data-ttu-id="8aaab-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8aaab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aaab-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="8aaab-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="8aaab-111">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="8aaab-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="8aaab-112">Puntero al primer componente.</span><span class="sxs-lookup"><span data-stu-id="8aaab-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8aaab-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8aaab-113">Return value</span></span>

<span data-ttu-id="8aaab-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8aaab-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8aaab-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8aaab-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8aaab-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8aaab-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8aaab-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="8aaab-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8aaab-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="8aaab-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8aaab-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8aaab-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8aaab-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aaab-120">Requirements</span></span>



| <span data-ttu-id="8aaab-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aaab-121">Requirement</span></span> | <span data-ttu-id="8aaab-122">Value</span><span class="sxs-lookup"><span data-stu-id="8aaab-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aaab-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8aaab-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8aaab-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aaab-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8aaab-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8aaab-125">Library</span></span><br/> | <dl> <span data-ttu-id="8aaab-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="8aaab-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aaab-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8aaab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aaab-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="8aaab-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

