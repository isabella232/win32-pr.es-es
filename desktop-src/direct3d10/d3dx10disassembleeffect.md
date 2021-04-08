---
description: Tenga en cuenta que, en lugar de usar esta función heredada, se recomienda usar la API de D3DDisassemble. Esta función, que desensambla un efecto compilado en una cadena de texto que contiene las instrucciones de ensamblado y las asignaciones de registro, ha quedado en desuso.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: Función D3DX10DisassembleEffect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 67fe19365616e779bd17ab689550b34737288317
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003888"
---
# <a name="d3dx10disassembleeffect-function"></a><span data-ttu-id="2b7ed-104">D3DX10DisassembleEffect función)</span><span class="sxs-lookup"><span data-stu-id="2b7ed-104">D3DX10DisassembleEffect function</span></span>

> [!Note]  
> <span data-ttu-id="2b7ed-105">En lugar de usar esta función heredada, se recomienda usar la API de [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="2b7ed-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="2b7ed-106">Esta función, que desensambla un efecto compilado en una cadena de texto que contiene las instrucciones de ensamblado y las asignaciones de registro, ha quedado en desuso.</span><span class="sxs-lookup"><span data-stu-id="2b7ed-106">This function -- which disassembles a compiled effect into a text string that contains assembly instructions and register assignments -- has been deprecated.</span></span> <span data-ttu-id="2b7ed-107">En su lugar, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="2b7ed-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b7ed-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b7ed-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="2b7ed-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b7ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b7ed-110">*pEffect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b7ed-110">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b7ed-111">Tipo: **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span><span class="sxs-lookup"><span data-stu-id="2b7ed-111">Type: **[**ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span></span>

<span data-ttu-id="2b7ed-112">Un puntero a la interfaz de efecto (vea la [**interfaz ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span><span class="sxs-lookup"><span data-stu-id="2b7ed-112">A pointer to the effect interface (see [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span></span>

</dd> <dt>

<span data-ttu-id="2b7ed-113">*EnableColorCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b7ed-113">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b7ed-114">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b7ed-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b7ed-115">Incluya etiquetas HTML en la salida para el código de color del resultado.</span><span class="sxs-lookup"><span data-stu-id="2b7ed-115">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="2b7ed-116">*ppDisassembly* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2b7ed-116">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b7ed-117">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="2b7ed-117">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="2b7ed-118">Dirección de un búfer (vea la [**interfaz ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene el efecto desensamblado.</span><span class="sxs-lookup"><span data-stu-id="2b7ed-118">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b7ed-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b7ed-119">Return value</span></span>

<span data-ttu-id="2b7ed-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b7ed-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b7ed-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2b7ed-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b7ed-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b7ed-122">Requirements</span></span>



| <span data-ttu-id="2b7ed-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b7ed-123">Requirement</span></span> | <span data-ttu-id="2b7ed-124">Value</span><span class="sxs-lookup"><span data-stu-id="2b7ed-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b7ed-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b7ed-125">Header</span></span><br/> | <dl> <span data-ttu-id="2b7ed-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b7ed-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b7ed-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b7ed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b7ed-128">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="2b7ed-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
