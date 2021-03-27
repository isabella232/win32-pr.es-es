---
title: Método ID3DX11EffectScalarVariable SetIntArray (D3dx11effect. h)
description: Establezca una matriz de variables de tipo entero.
ms.assetid: 27efb643-0762-4cd7-84ad-f82b2bb1584a
keywords:
- Método SetIntArray Direct3D 11
- Método SetIntArray Direct3D 11, interfaz ID3DX11EffectScalarVariable
- Interfaz ID3DX11EffectScalarVariable Direct3D 11, método SetIntArray
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetIntArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142a1686b9dde8f6a2c8f41d521ac085bd403ec0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986827"
---
# <a name="id3dx11effectscalarvariablesetintarray-method"></a><span data-ttu-id="c47d7-106">ID3DX11EffectScalarVariable:: SetIntArray (método)</span><span class="sxs-lookup"><span data-stu-id="c47d7-106">ID3DX11EffectScalarVariable::SetIntArray method</span></span>

<span data-ttu-id="c47d7-107">Establezca una matriz de variables de tipo entero.</span><span class="sxs-lookup"><span data-stu-id="c47d7-107">Set an array of integer variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="c47d7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c47d7-108">Syntax</span></span>


```C++
HRESULT SetIntArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="c47d7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c47d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c47d7-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="c47d7-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="c47d7-111">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="c47d7-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="c47d7-112">Puntero al principio de los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="c47d7-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="c47d7-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="c47d7-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="c47d7-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c47d7-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c47d7-115">Debe establecerse en 0; está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c47d7-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="c47d7-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="c47d7-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="c47d7-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c47d7-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c47d7-118">Número de elementos de matriz que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="c47d7-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c47d7-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c47d7-119">Return value</span></span>

<span data-ttu-id="c47d7-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c47d7-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c47d7-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c47d7-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c47d7-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c47d7-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c47d7-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="c47d7-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c47d7-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c47d7-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c47d7-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c47d7-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c47d7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c47d7-126">Requirements</span></span>



| <span data-ttu-id="c47d7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c47d7-127">Requirement</span></span> | <span data-ttu-id="c47d7-128">Value</span><span class="sxs-lookup"><span data-stu-id="c47d7-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c47d7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c47d7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c47d7-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c47d7-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c47d7-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c47d7-131">Library</span></span><br/> | <dl> <span data-ttu-id="c47d7-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="c47d7-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c47d7-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c47d7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c47d7-134">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="c47d7-134">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

