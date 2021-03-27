---
title: Método ID3DX11Effect GetVariableBySemantic (D3dx11effect. h)
description: Obtiene una variable por semántica.
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- Método GetVariableBySemantic Direct3D 11
- Método GetVariableBySemantic Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetVariableBySemantic
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280450"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a><span data-ttu-id="10f19-106">ID3DX11Effect:: GetVariableBySemantic (método)</span><span class="sxs-lookup"><span data-stu-id="10f19-106">ID3DX11Effect::GetVariableBySemantic method</span></span>

<span data-ttu-id="10f19-107">Obtiene una variable por semántica.</span><span class="sxs-lookup"><span data-stu-id="10f19-107">Get a variable by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="10f19-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10f19-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="10f19-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10f19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10f19-110">*Semántica*</span><span class="sxs-lookup"><span data-stu-id="10f19-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="10f19-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="10f19-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="10f19-112">Nombre semántico.</span><span class="sxs-lookup"><span data-stu-id="10f19-112">The semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10f19-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10f19-113">Return value</span></span>

<span data-ttu-id="10f19-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="10f19-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="10f19-115">Puntero a la variable de efecto indicada por la semántica.</span><span class="sxs-lookup"><span data-stu-id="10f19-115">A pointer to the effect variable indicated by the Semantic.</span></span> <span data-ttu-id="10f19-116">Vea [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="10f19-116">See [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="10f19-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10f19-117">Remarks</span></span>

<span data-ttu-id="10f19-118">Cada variable de efecto puede tener una semántica adjunta, que es una cadena de metadatos definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="10f19-118">Each effect variable can have a semantic attached, which is a user defined metadata string.</span></span> <span data-ttu-id="10f19-119">Algunas [semánticas de valores del sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) son palabras reservadas que desencadenan la funcionalidad integrada por fases de canalización.</span><span class="sxs-lookup"><span data-stu-id="10f19-119">Some [system-value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) are reserved words that trigger built in functionality by pipeline stages.</span></span>

<span data-ttu-id="10f19-120">El método devuelve un puntero a una [**interfaz de variable de efecto**](id3dx11effectvariable.md) si no se encuentra una variable; puede llamar a [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) para comprobar si la semántica existe o no.</span><span class="sxs-lookup"><span data-stu-id="10f19-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the semantic exists.</span></span>

> [!Note]  
> <span data-ttu-id="10f19-121">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="10f19-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="10f19-122">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="10f19-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="10f19-123">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="10f19-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="10f19-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10f19-124">Requirements</span></span>



| <span data-ttu-id="10f19-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="10f19-125">Requirement</span></span> | <span data-ttu-id="10f19-126">Value</span><span class="sxs-lookup"><span data-stu-id="10f19-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f19-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10f19-127">Header</span></span><br/>  | <dl> <span data-ttu-id="10f19-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="10f19-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="10f19-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="10f19-129">Library</span></span><br/> | <dl> <span data-ttu-id="10f19-130"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="10f19-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10f19-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="10f19-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f19-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="10f19-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

