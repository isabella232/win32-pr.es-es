---
description: Establezca el valor de un parámetro o anotación arbitrario, incluidos los tipos simples, Structs, matrices, cadenas, sombreadores y texturas.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'ID3DXBaseEffect:: SetValue (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157216"
---
# <a name="id3dxbaseeffectsetvalue-method"></a><span data-ttu-id="db3e9-103">ID3DXBaseEffect:: SetValue (método)</span><span class="sxs-lookup"><span data-stu-id="db3e9-103">ID3DXBaseEffect::SetValue method</span></span>

<span data-ttu-id="db3e9-104">Establezca el valor de un parámetro o anotación arbitrario, incluidos los tipos simples, Structs, matrices, cadenas, sombreadores y texturas.</span><span class="sxs-lookup"><span data-stu-id="db3e9-104">Set the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="db3e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db3e9-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="db3e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db3e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db3e9-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="db3e9-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db3e9-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="db3e9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="db3e9-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="db3e9-109">Unique identifier.</span></span> <span data-ttu-id="db3e9-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="db3e9-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="db3e9-111">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="db3e9-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db3e9-112">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db3e9-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db3e9-113">Puntero a un búfer que contiene datos.</span><span class="sxs-lookup"><span data-stu-id="db3e9-113">Pointer to a buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="db3e9-114">*Bytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="db3e9-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db3e9-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db3e9-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db3e9-116">\[en \] número de bytes en el búfer.</span><span class="sxs-lookup"><span data-stu-id="db3e9-116">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="db3e9-117">Pase \_ el valor predeterminado de D3DX si sabe que el búfer es lo suficientemente grande como para contener todo el parámetro y desea omitir la validación de tamaño.</span><span class="sxs-lookup"><span data-stu-id="db3e9-117">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db3e9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db3e9-118">Return value</span></span>

<span data-ttu-id="db3e9-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db3e9-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db3e9-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db3e9-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="db3e9-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="db3e9-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="db3e9-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db3e9-122">Remarks</span></span>

<span data-ttu-id="db3e9-123">Este método se puede usar en lugar de casi todas las llamadas API de conjunto de efectos.</span><span class="sxs-lookup"><span data-stu-id="db3e9-123">This method can be used in place of nearly all the effect set API calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="db3e9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db3e9-124">Requirements</span></span>



| <span data-ttu-id="db3e9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="db3e9-125">Requirement</span></span> | <span data-ttu-id="db3e9-126">Value</span><span class="sxs-lookup"><span data-stu-id="db3e9-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db3e9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db3e9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="db3e9-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="db3e9-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="db3e9-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db3e9-129">Library</span></span><br/> | <dl> <span data-ttu-id="db3e9-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db3e9-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="db3e9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="db3e9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db3e9-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="db3e9-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="db3e9-133">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="db3e9-133">**GetValue**</span></span>](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
