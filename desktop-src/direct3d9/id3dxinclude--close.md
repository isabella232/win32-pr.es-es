---
description: Método implementado por el usuario para cerrar un archivo de inclusión de sombreador \# .
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'ID3DXInclude:: Close (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698395"
---
# <a name="id3dxincludeclose-method"></a><span data-ttu-id="31b45-103">ID3DXInclude:: Close (método)</span><span class="sxs-lookup"><span data-stu-id="31b45-103">ID3DXInclude::Close method</span></span>

<span data-ttu-id="31b45-104">Método implementado por el usuario para cerrar un archivo de inclusión de sombreador \# .</span><span class="sxs-lookup"><span data-stu-id="31b45-104">A user-implemented method for closing a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="31b45-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31b45-105">Syntax</span></span>


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a><span data-ttu-id="31b45-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31b45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b45-107">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31b45-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b45-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31b45-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31b45-109">Puntero al búfer devuelto que contiene las directivas Include.</span><span class="sxs-lookup"><span data-stu-id="31b45-109">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="31b45-110">Este es el puntero devuelto por la llamada a [**ID3DXInclude:: Open**](id3dxinclude--open.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="31b45-110">This is the pointer that was returned by the corresponding [**ID3DXInclude::Open**](id3dxinclude--open.md) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b45-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31b45-111">Return value</span></span>

<span data-ttu-id="31b45-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31b45-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31b45-113">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="31b45-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="31b45-114">Si se produce un error en la devolución de llamada al leer el \# archivo de inclusión, se producirá un error en la API que provocó la llamada de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="31b45-114">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="31b45-115">Es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="31b45-115">This is one of the following:</span></span>

-   <span data-ttu-id="31b45-116">El sombreador HLSL producirá un error en una de las funciones de D3DXCompileShader \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="31b45-116">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="31b45-117">El sombreador de ensamblado producirá un error en una de las funciones de D3DXAssembleShader \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="31b45-117">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="31b45-118">El efecto producirá un error en una de las \* \* \* funciones D3DXCreateEffect o D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="31b45-118">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="remarks"></a><span data-ttu-id="31b45-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31b45-119">Remarks</span></span>

<span data-ttu-id="31b45-120">Si [**ID3DXInclude:: Open**](id3dxinclude--open.md) se ejecutó correctamente, se garantiza que se llamará a **ID3DXInclude:: Close** antes de que la API que usa esta interfaz devuelva.</span><span class="sxs-lookup"><span data-stu-id="31b45-120">If [**ID3DXInclude::Open**](id3dxinclude--open.md) was successful, **ID3DXInclude::Close** is guaranteed to be called before the API using this interface returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="31b45-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31b45-121">Requirements</span></span>



| <span data-ttu-id="31b45-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="31b45-122">Requirement</span></span> | <span data-ttu-id="31b45-123">Value</span><span class="sxs-lookup"><span data-stu-id="31b45-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="31b45-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31b45-124">Header</span></span><br/>  | <dl> <span data-ttu-id="31b45-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="31b45-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="31b45-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31b45-126">Library</span></span><br/> | <dl> <span data-ttu-id="31b45-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31b45-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="31b45-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="31b45-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b45-129">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="31b45-129">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="31b45-130">**ID3DXInclude:: Open**</span><span class="sxs-lookup"><span data-stu-id="31b45-130">**ID3DXInclude::Open**</span></span>](id3dxinclude--open.md)
</dt> </dl>

 

 
