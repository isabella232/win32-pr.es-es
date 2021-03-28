---
title: Método ID3DX11EffectVectorVariable SetFloatVector (D3dx11effect. h)
description: Establezca un vector de cuatro componentes que contenga datos de punto flotante.
ms.assetid: fb646df6-b9f9-4d71-93c3-38833076b781
keywords:
- Método SetFloatVector Direct3D 11
- Método SetFloatVector Direct3D 11, interfaz ID3DX11EffectVectorVariable
- Interfaz ID3DX11EffectVectorVariable Direct3D 11, método SetFloatVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5541f2773e992c4c52bf748bceb832d67b28825
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424468"
---
# <a name="id3dx11effectvectorvariablesetfloatvector-method"></a><span data-ttu-id="d0041-106">ID3DX11EffectVectorVariable:: SetFloatVector (método)</span><span class="sxs-lookup"><span data-stu-id="d0041-106">ID3DX11EffectVectorVariable::SetFloatVector method</span></span>

<span data-ttu-id="d0041-107">Establezca un vector de cuatro componentes que contenga datos de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="d0041-107">Set a four-component vector that contains floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0041-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0041-108">Syntax</span></span>


```C++
HRESULT SetFloatVector(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="d0041-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0041-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0041-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="d0041-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="d0041-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="d0041-111">Type: **float\***</span></span>

<span data-ttu-id="d0041-112">Puntero al primer componente.</span><span class="sxs-lookup"><span data-stu-id="d0041-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0041-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0041-113">Return value</span></span>

<span data-ttu-id="d0041-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0041-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0041-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d0041-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0041-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0041-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d0041-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="d0041-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d0041-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="d0041-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d0041-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d0041-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0041-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0041-120">Requirements</span></span>



| <span data-ttu-id="d0041-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0041-121">Requirement</span></span> | <span data-ttu-id="d0041-122">Value</span><span class="sxs-lookup"><span data-stu-id="d0041-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0041-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0041-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d0041-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0041-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d0041-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0041-125">Library</span></span><br/> | <dl> <span data-ttu-id="d0041-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="d0041-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0041-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0041-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0041-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="d0041-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

 





