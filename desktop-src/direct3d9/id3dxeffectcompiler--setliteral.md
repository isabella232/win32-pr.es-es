---
description: Alterna el estado literal de un parámetro. Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'ID3DXEffectCompiler:: SetLiteral (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5a64426381876458b601b741050a01e5f35d084c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362470"
---
# <a name="id3dxeffectcompilersetliteral-method"></a><span data-ttu-id="5bb28-104">ID3DXEffectCompiler:: SetLiteral (método)</span><span class="sxs-lookup"><span data-stu-id="5bb28-104">ID3DXEffectCompiler::SetLiteral method</span></span>

<span data-ttu-id="5bb28-105">Alterna el estado literal de un parámetro.</span><span class="sxs-lookup"><span data-stu-id="5bb28-105">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="5bb28-106">Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.</span><span class="sxs-lookup"><span data-stu-id="5bb28-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb28-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bb28-107">Syntax</span></span>


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a><span data-ttu-id="5bb28-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bb28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bb28-109">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5bb28-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb28-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5bb28-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5bb28-111">Identificador único de un parámetro.</span><span class="sxs-lookup"><span data-stu-id="5bb28-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="5bb28-112">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5bb28-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bb28-113">*Literal* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5bb28-113">*Literal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb28-114">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5bb28-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5bb28-115">Establézcalo en **true** para que el parámetro sea un literal y **false** si el parámetro puede cambiar el valor durante la vigencia del sombreador.</span><span class="sxs-lookup"><span data-stu-id="5bb28-115">Set to **TRUE** to make the parameter a literal, and **FALSE** if the parameter can change value during the shader lifetime.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bb28-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bb28-116">Return value</span></span>

<span data-ttu-id="5bb28-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5bb28-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5bb28-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5bb28-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5bb28-119">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5bb28-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bb28-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bb28-120">Remarks</span></span>

<span data-ttu-id="5bb28-121">Este método solo cambia si el parámetro es un literal o no.</span><span class="sxs-lookup"><span data-stu-id="5bb28-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="5bb28-122">Para cambiar el valor de un parámetro, use un método como [**ID3DXBaseEffect:: SetBool**](id3dxbaseeffect--setbool.md) o [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="5bb28-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

<span data-ttu-id="5bb28-123">Se debe llamar a esta función antes de que se compile el efecto.</span><span class="sxs-lookup"><span data-stu-id="5bb28-123">This function must be called before the effect is compiled.</span></span> <span data-ttu-id="5bb28-124">Este es un ejemplo de cómo puede usarse esta función:</span><span class="sxs-lookup"><span data-stu-id="5bb28-124">Here is an example of how one might use this function:</span></span>


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a><span data-ttu-id="5bb28-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bb28-125">Requirements</span></span>



| <span data-ttu-id="5bb28-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bb28-126">Requirement</span></span> | <span data-ttu-id="5bb28-127">Value</span><span class="sxs-lookup"><span data-stu-id="5bb28-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb28-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bb28-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5bb28-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bb28-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5bb28-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5bb28-130">Library</span></span><br/> | <dl> <span data-ttu-id="5bb28-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bb28-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5bb28-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bb28-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb28-133">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="5bb28-133">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="5bb28-134">Usos y literales (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5bb28-134">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="5bb28-135">**ID3DXEffectCompiler::GetLiteral**</span><span class="sxs-lookup"><span data-stu-id="5bb28-135">**ID3DXEffectCompiler::GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
