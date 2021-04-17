---
description: Método implementado por el usuario para abrir y leer el contenido de un archivo de inclusión de sombreador \# .
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'ID3DXInclude:: Open (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698394"
---
# <a name="id3dxincludeopen-method"></a><span data-ttu-id="d08d3-103">ID3DXInclude:: Open (método)</span><span class="sxs-lookup"><span data-stu-id="d08d3-103">ID3DXInclude::Open method</span></span>

<span data-ttu-id="d08d3-104">Método implementado por el usuario para abrir y leer el contenido de un archivo de inclusión de sombreador \# .</span><span class="sxs-lookup"><span data-stu-id="d08d3-104">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08d3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d08d3-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a><span data-ttu-id="d08d3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d08d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d08d3-107">*IncludeType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d08d3-107">*IncludeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08d3-108">Tipo: **[ **D3DXINCLUDE \_ Type**](./d3dxinclude-type.md)**</span><span class="sxs-lookup"><span data-stu-id="d08d3-108">Type: **[**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md)**</span></span>

<span data-ttu-id="d08d3-109">Ubicación del archivo de \# inclusión.</span><span class="sxs-lookup"><span data-stu-id="d08d3-109">The location of the \#include file.</span></span> <span data-ttu-id="d08d3-110">Consulte [**\_ tipo de D3DXINCLUDE**](./d3dxinclude-type.md).</span><span class="sxs-lookup"><span data-stu-id="d08d3-110">See [**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="d08d3-111">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d08d3-111">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08d3-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d08d3-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d08d3-113">Nombre del \# archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="d08d3-113">Name of the \#include file.</span></span>

</dd> <dt>

<span data-ttu-id="d08d3-114">*pParentData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d08d3-114">*pParentData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08d3-115">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d08d3-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d08d3-116">Puntero al contenedor que incluye el \# archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="d08d3-116">Pointer to the container that includes the \#include file.</span></span> <span data-ttu-id="d08d3-117">El compilador podría pasar NULL en *pParentData*.</span><span class="sxs-lookup"><span data-stu-id="d08d3-117">The compiler might pass NULL in *pParentData*.</span></span> <span data-ttu-id="d08d3-118">Para obtener más información, vea la sección "buscar archivos de inclusión" en [compilar un efecto (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span><span class="sxs-lookup"><span data-stu-id="d08d3-118">For more information, see the "Searching for Include Files" section in [Compile an Effect (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d08d3-119">*ppData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d08d3-119">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d08d3-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d08d3-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d08d3-121">Puntero al búfer devuelto que contiene las directivas Include.</span><span class="sxs-lookup"><span data-stu-id="d08d3-121">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="d08d3-122">Este puntero sigue siendo válido hasta que se llama a [**ID3DXInclude:: Close**](id3dxinclude--close.md) .</span><span class="sxs-lookup"><span data-stu-id="d08d3-122">This pointer remains valid until [**ID3DXInclude::Close**](id3dxinclude--close.md) is called.</span></span>

</dd> <dt>

<span data-ttu-id="d08d3-123">*pBytes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d08d3-123">*pBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d08d3-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d08d3-124">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d08d3-125">Número de bytes devueltos en ppData.</span><span class="sxs-lookup"><span data-stu-id="d08d3-125">Number of bytes returned in ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d08d3-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d08d3-126">Return value</span></span>

<span data-ttu-id="d08d3-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d08d3-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d08d3-128">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="d08d3-128">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="d08d3-129">Si se produce un error en la devolución de llamada al leer el \# archivo de inclusión, se producirá un error en la API que provocó la llamada de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="d08d3-129">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="d08d3-130">Es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d08d3-130">This is one of the following:</span></span>

-   <span data-ttu-id="d08d3-131">El sombreador HLSL producirá un error en una de las funciones de D3DXCompileShader \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="d08d3-131">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="d08d3-132">El sombreador de ensamblado producirá un error en una de las funciones de D3DXAssembleShader \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="d08d3-132">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="d08d3-133">El efecto producirá un error en una de las \* \* \* funciones D3DXCreateEffect o D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="d08d3-133">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d08d3-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d08d3-134">Requirements</span></span>



| <span data-ttu-id="d08d3-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d08d3-135">Requirement</span></span> | <span data-ttu-id="d08d3-136">Value</span><span class="sxs-lookup"><span data-stu-id="d08d3-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d08d3-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d08d3-137">Header</span></span><br/>  | <dl> <span data-ttu-id="d08d3-138"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d08d3-138"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d08d3-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d08d3-139">Library</span></span><br/> | <dl> <span data-ttu-id="d08d3-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d08d3-140"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d08d3-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="d08d3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08d3-142">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="d08d3-142">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="d08d3-143">**ID3DXInclude:: Close**</span><span class="sxs-lookup"><span data-stu-id="d08d3-143">**ID3DXInclude::Close**</span></span>](id3dxinclude--close.md)
</dt> </dl>

 

 
