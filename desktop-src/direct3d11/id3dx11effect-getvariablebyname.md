---
title: Método ID3DX11Effect GetVariableByName (D3dx11effect. h)
description: Obtiene una variable por nombre.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Método GetVariableByName Direct3D 11
- Método GetVariableByName Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetVariableByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998610"
---
# <a name="id3dx11effectgetvariablebyname-method"></a><span data-ttu-id="2517b-106">ID3DX11Effect:: GetVariableByName (método)</span><span class="sxs-lookup"><span data-stu-id="2517b-106">ID3DX11Effect::GetVariableByName method</span></span>

<span data-ttu-id="2517b-107">Obtiene una variable por nombre.</span><span class="sxs-lookup"><span data-stu-id="2517b-107">Get a variable by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="2517b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2517b-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="2517b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2517b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2517b-110">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="2517b-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="2517b-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2517b-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2517b-112">El nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="2517b-112">The variable name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2517b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2517b-113">Return value</span></span>

<span data-ttu-id="2517b-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="2517b-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="2517b-115">Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="2517b-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="2517b-116">Devuelve una variable no válida si no se encuentra el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="2517b-116">Returns an invalid variable if the specified name cannot be found.</span></span>

## <a name="remarks"></a><span data-ttu-id="2517b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2517b-117">Remarks</span></span>

<span data-ttu-id="2517b-118">Un efecto puede contener una o más variables.</span><span class="sxs-lookup"><span data-stu-id="2517b-118">An effect may contain one or more variables.</span></span> <span data-ttu-id="2517b-119">Las variables fuera de una técnica se consideran globales para todos los efectos, las que se encuentran dentro de una técnica son locales para esa técnica.</span><span class="sxs-lookup"><span data-stu-id="2517b-119">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="2517b-120">Puede tener acceso a una variable de efecto mediante su nombre o con un índice.</span><span class="sxs-lookup"><span data-stu-id="2517b-120">You can access an effect variable using its name or with an index.</span></span>

<span data-ttu-id="2517b-121">El método devuelve un puntero a una [**interfaz de variable de efecto**](id3dx11effectvariable.md) tanto si se encuentra una variable como si no.</span><span class="sxs-lookup"><span data-stu-id="2517b-121">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) whether or not a variable is found.</span></span> <span data-ttu-id="2517b-122">Se debe llamar a [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) para comprobar si existe o no el nombre.</span><span class="sxs-lookup"><span data-stu-id="2517b-122">[**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) should be called to verify whether or not the name exists.</span></span>

> [!Note]  
> <span data-ttu-id="2517b-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="2517b-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2517b-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="2517b-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2517b-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2517b-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2517b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2517b-126">Requirements</span></span>



| <span data-ttu-id="2517b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2517b-127">Requirement</span></span> | <span data-ttu-id="2517b-128">Value</span><span class="sxs-lookup"><span data-stu-id="2517b-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2517b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2517b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2517b-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2517b-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2517b-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2517b-131">Library</span></span><br/> | <dl> <span data-ttu-id="2517b-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="2517b-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2517b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2517b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2517b-134">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="2517b-134">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

