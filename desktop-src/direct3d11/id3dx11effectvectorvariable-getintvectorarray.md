---
title: Método ID3DX11EffectVectorVariable GetIntVectorArray (D3dx11effect. h)
description: Obtiene una matriz de vectores de cuatro componentes que contienen datos enteros.
ms.assetid: cabc3bb1-8b65-455a-af84-f96219f7cfb5
keywords:
- Método GetIntVectorArray Direct3D 11
- Método GetIntVectorArray Direct3D 11, interfaz ID3DX11EffectVectorVariable
- Interfaz ID3DX11EffectVectorVariable Direct3D 11, método GetIntVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetIntVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 024db61b559d74c6453c6838795d5785ca7a0eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362694"
---
# <a name="id3dx11effectvectorvariablegetintvectorarray-method"></a><span data-ttu-id="3a763-106">ID3DX11EffectVectorVariable:: GetIntVectorArray (método)</span><span class="sxs-lookup"><span data-stu-id="3a763-106">ID3DX11EffectVectorVariable::GetIntVectorArray method</span></span>

<span data-ttu-id="3a763-107">Obtiene una matriz de vectores de cuatro componentes que contienen datos enteros.</span><span class="sxs-lookup"><span data-stu-id="3a763-107">Get an array of four-component vectors that contain integer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a763-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a763-108">Syntax</span></span>


```C++
HRESULT GetIntVectorArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="3a763-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a763-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a763-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="3a763-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="3a763-111">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="3a763-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3a763-112">Puntero al principio de los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="3a763-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="3a763-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="3a763-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="3a763-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3a763-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3a763-115">Debe establecerse en 0; está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3a763-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="3a763-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="3a763-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="3a763-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3a763-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3a763-118">Número de elementos de matriz que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="3a763-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a763-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a763-119">Return value</span></span>

<span data-ttu-id="3a763-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a763-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a763-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3a763-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a763-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a763-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3a763-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="3a763-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3a763-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3a763-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3a763-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3a763-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3a763-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a763-126">Requirements</span></span>



| <span data-ttu-id="3a763-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a763-127">Requirement</span></span> | <span data-ttu-id="3a763-128">Value</span><span class="sxs-lookup"><span data-stu-id="3a763-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a763-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a763-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3a763-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a763-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3a763-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a763-131">Library</span></span><br/> | <dl> <span data-ttu-id="3a763-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="3a763-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a763-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a763-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a763-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="3a763-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

