---
title: Método ID3DX11EffectVectorVariable SetIntVector (D3dx11effect. h)
description: Establezca un vector de cuatro componentes que contenga datos enteros.
ms.assetid: d0546da4-c3b4-4e97-9aa9-d3b7022e22c5
keywords:
- Método SetIntVector Direct3D 11
- Método SetIntVector Direct3D 11, interfaz ID3DX11EffectVectorVariable
- Interfaz ID3DX11EffectVectorVariable Direct3D 11, método SetIntVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetIntVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6141185459dbe7aad494312210b4517fe4f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280333"
---
# <a name="id3dx11effectvectorvariablesetintvector-method"></a><span data-ttu-id="9f05f-106">ID3DX11EffectVectorVariable:: SetIntVector (método)</span><span class="sxs-lookup"><span data-stu-id="9f05f-106">ID3DX11EffectVectorVariable::SetIntVector method</span></span>

<span data-ttu-id="9f05f-107">Establezca un vector de cuatro componentes que contenga datos enteros.</span><span class="sxs-lookup"><span data-stu-id="9f05f-107">Set a four-component vector that contains integer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f05f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f05f-108">Syntax</span></span>


```C++
HRESULT SetIntVector(
   int *pData
);
```



## <a name="parameters"></a><span data-ttu-id="9f05f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f05f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f05f-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="9f05f-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="9f05f-111">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="9f05f-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="9f05f-112">Puntero al primer componente.</span><span class="sxs-lookup"><span data-stu-id="9f05f-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f05f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f05f-113">Return value</span></span>

<span data-ttu-id="9f05f-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f05f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f05f-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9f05f-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f05f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f05f-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9f05f-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="9f05f-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9f05f-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="9f05f-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9f05f-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9f05f-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f05f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f05f-120">Requirements</span></span>



| <span data-ttu-id="9f05f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f05f-121">Requirement</span></span> | <span data-ttu-id="9f05f-122">Value</span><span class="sxs-lookup"><span data-stu-id="9f05f-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f05f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f05f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9f05f-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f05f-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9f05f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f05f-125">Library</span></span><br/> | <dl> <span data-ttu-id="9f05f-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="9f05f-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f05f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f05f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f05f-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="9f05f-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

