---
description: Obtiene el valor de un parámetro o anotación arbitrarios, incluidos los tipos simples, Structs, matrices, cadenas, sombreadores y texturas. Este método se puede usar en lugar de casi todas las llamadas a GetXXX en ID3DXBaseEffect.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'ID3DXBaseEffect:: GetValue (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 166635b22875692da0396f1c7c2145f13ca08df3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707727"
---
# <a name="id3dxbaseeffectgetvalue-method"></a><span data-ttu-id="7a69b-104">ID3DXBaseEffect:: GetValue (método)</span><span class="sxs-lookup"><span data-stu-id="7a69b-104">ID3DXBaseEffect::GetValue method</span></span>

<span data-ttu-id="7a69b-105">Obtiene el valor de un parámetro o anotación arbitrarios, incluidos los tipos simples, Structs, matrices, cadenas, sombreadores y texturas.</span><span class="sxs-lookup"><span data-stu-id="7a69b-105">Get the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span> <span data-ttu-id="7a69b-106">Este método se puede usar en lugar de casi todas las llamadas a GetXXX en [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="7a69b-106">This method can be used in place of nearly all the Getxxx calls in [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a69b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a69b-107">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="7a69b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a69b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a69b-109">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7a69b-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a69b-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7a69b-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7a69b-111">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="7a69b-111">Unique identifier.</span></span> <span data-ttu-id="7a69b-112">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="7a69b-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a69b-113">*pdata* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7a69b-113">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a69b-114">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a69b-114">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a69b-115">Devuelve un búfer que contiene el valor.</span><span class="sxs-lookup"><span data-stu-id="7a69b-115">Returns a buffer containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="7a69b-116">*Bytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7a69b-116">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a69b-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a69b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a69b-118">\[en \] número de bytes en el búfer.</span><span class="sxs-lookup"><span data-stu-id="7a69b-118">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="7a69b-119">Pase \_ el valor predeterminado de D3DX si sabe que el búfer es lo suficientemente grande como para contener todo el parámetro y desea omitir la validación de tamaño.</span><span class="sxs-lookup"><span data-stu-id="7a69b-119">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a69b-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a69b-120">Return value</span></span>

<span data-ttu-id="7a69b-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7a69b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7a69b-122">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7a69b-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7a69b-123">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7a69b-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a69b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a69b-124">Requirements</span></span>



| <span data-ttu-id="7a69b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a69b-125">Requirement</span></span> | <span data-ttu-id="7a69b-126">Value</span><span class="sxs-lookup"><span data-stu-id="7a69b-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a69b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a69b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7a69b-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a69b-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7a69b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7a69b-129">Library</span></span><br/> | <dl> <span data-ttu-id="7a69b-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a69b-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7a69b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a69b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a69b-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="7a69b-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="7a69b-133">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="7a69b-133">**SetValue**</span></span>](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
