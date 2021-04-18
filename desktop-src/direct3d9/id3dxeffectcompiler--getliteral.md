---
description: Obtiene un estado literal de un parámetro. Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: 'ID3DXEffectCompiler:: GetLiteral (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c16e3798ab66a34e12812a3560572c45b9206b30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707789"
---
# <a name="id3dxeffectcompilergetliteral-method"></a><span data-ttu-id="f51dd-104">ID3DXEffectCompiler:: GetLiteral (método)</span><span class="sxs-lookup"><span data-stu-id="f51dd-104">ID3DXEffectCompiler::GetLiteral method</span></span>

<span data-ttu-id="f51dd-105">Obtiene un estado literal de un parámetro.</span><span class="sxs-lookup"><span data-stu-id="f51dd-105">Gets a literal status of a parameter.</span></span> <span data-ttu-id="f51dd-106">Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.</span><span class="sxs-lookup"><span data-stu-id="f51dd-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="f51dd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f51dd-107">Syntax</span></span>


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="f51dd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f51dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f51dd-109">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f51dd-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f51dd-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f51dd-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f51dd-111">Identificador único de un parámetro.</span><span class="sxs-lookup"><span data-stu-id="f51dd-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="f51dd-112">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f51dd-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f51dd-113">*pLiteral* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f51dd-113">*pLiteral* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f51dd-114">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f51dd-114">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f51dd-115">Devuelve true si el parámetro es un literal y false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f51dd-115">Returns True if the parameter is a literal, and False otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f51dd-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f51dd-116">Return value</span></span>

<span data-ttu-id="f51dd-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f51dd-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f51dd-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f51dd-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f51dd-119">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f51dd-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f51dd-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f51dd-120">Remarks</span></span>

<span data-ttu-id="f51dd-121">Este método solo cambia si el parámetro es un literal o no.</span><span class="sxs-lookup"><span data-stu-id="f51dd-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="f51dd-122">Para cambiar el valor de un parámetro, use un método como [**ID3DXBaseEffect:: SetBool**](id3dxbaseeffect--setbool.md) o [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="f51dd-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f51dd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f51dd-123">Requirements</span></span>



| <span data-ttu-id="f51dd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f51dd-124">Requirement</span></span> | <span data-ttu-id="f51dd-125">Value</span><span class="sxs-lookup"><span data-stu-id="f51dd-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51dd-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f51dd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f51dd-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f51dd-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f51dd-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f51dd-128">Library</span></span><br/> | <dl> <span data-ttu-id="f51dd-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f51dd-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f51dd-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f51dd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f51dd-131">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="f51dd-131">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="f51dd-132">Usos y literales (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f51dd-132">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="f51dd-133">**ID3DXEffectCompiler::SetLiteral**</span><span class="sxs-lookup"><span data-stu-id="f51dd-133">**ID3DXEffectCompiler::SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
