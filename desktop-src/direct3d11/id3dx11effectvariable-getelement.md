---
title: Método GetElement de ID3DX11EffectVariable (D3dx11effect. h)
description: Obtiene un elemento de matriz.
ms.assetid: 3edf2084-570a-4423-8205-0b94a2a0cfde
keywords:
- GetElement (método) Direct3D 11
- GetElement (método) Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, GetElement (método)
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetElement
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b887bb9e4c1d40f4d3eb0d36b9a7b4d2698b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986809"
---
# <a name="id3dx11effectvariablegetelement-method"></a><span data-ttu-id="f4dbd-106">ID3DX11EffectVariable:: GetElement (método)</span><span class="sxs-lookup"><span data-stu-id="f4dbd-106">ID3DX11EffectVariable::GetElement method</span></span>

<span data-ttu-id="f4dbd-107">Obtiene un elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="f4dbd-107">Get an array element.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4dbd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4dbd-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetElement(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="f4dbd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4dbd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4dbd-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="f4dbd-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="f4dbd-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f4dbd-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f4dbd-112">Índice de base cero; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="f4dbd-112">A zero-based index; otherwise 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4dbd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4dbd-113">Return value</span></span>

<span data-ttu-id="f4dbd-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4dbd-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="f4dbd-115">Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="f4dbd-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4dbd-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4dbd-116">Remarks</span></span>

<span data-ttu-id="f4dbd-117">Si la variable de efecto es una matriz, use este método para devolver uno de los elementos.</span><span class="sxs-lookup"><span data-stu-id="f4dbd-117">If the effect variable is an array, use this method to return one of the elements.</span></span>

> [!Note]  
> <span data-ttu-id="f4dbd-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="f4dbd-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f4dbd-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f4dbd-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f4dbd-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f4dbd-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f4dbd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4dbd-121">Requirements</span></span>



| <span data-ttu-id="f4dbd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4dbd-122">Requirement</span></span> | <span data-ttu-id="f4dbd-123">Value</span><span class="sxs-lookup"><span data-stu-id="f4dbd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4dbd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4dbd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f4dbd-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4dbd-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f4dbd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4dbd-126">Library</span></span><br/> | <dl> <span data-ttu-id="f4dbd-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="f4dbd-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4dbd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4dbd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4dbd-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="f4dbd-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

