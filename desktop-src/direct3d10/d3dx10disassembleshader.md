---
description: Tenga en cuenta que, en lugar de usar esta función heredada, se recomienda usar la API de D3DDisassemble. Esta función, que desensambla un sombreador compilado en una cadena de texto que contiene las instrucciones de ensamblado y las asignaciones de registro, ya no existe.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: Función D3DX10DisassembleShader (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 13716fd5d25e2e8602379ea3864c516fa5388475
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678765"
---
# <a name="d3dx10disassembleshader-function"></a><span data-ttu-id="e6844-104">D3DX10DisassembleShader función)</span><span class="sxs-lookup"><span data-stu-id="e6844-104">D3DX10DisassembleShader function</span></span>

> [!Note]  
> <span data-ttu-id="e6844-105">En lugar de usar esta función heredada, se recomienda usar la API de [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="e6844-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="e6844-106">Esta función, que desensambla un sombreador compilado en una cadena de texto que contiene las instrucciones de ensamblado y las asignaciones de registro, ya no existe.</span><span class="sxs-lookup"><span data-stu-id="e6844-106">This function -- which disassembles a compiled shader into a text string that contains assembly instructions and register assignments -- no longer exists.</span></span> <span data-ttu-id="e6844-107">En su lugar, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="e6844-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6844-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6844-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="e6844-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6844-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6844-110">*pShader* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6844-110">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6844-111">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="e6844-111">Type: **const void\***</span></span>

<span data-ttu-id="e6844-112">Puntero al [**sombreador compilado**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="e6844-112">A pointer to the [**compiled shader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="e6844-113">*BytecodeLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6844-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6844-114">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6844-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6844-115">Tamaño de pShader.</span><span class="sxs-lookup"><span data-stu-id="e6844-115">The size of pShader.</span></span>

</dd> <dt>

<span data-ttu-id="e6844-116">*EnableColorCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6844-116">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6844-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6844-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6844-118">Incluya etiquetas HTML en la salida para el código de color del resultado.</span><span class="sxs-lookup"><span data-stu-id="e6844-118">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="e6844-119">*pComments* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6844-119">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6844-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6844-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6844-121">Cadena de comentario en la parte superior del sombreador que identifica las constantes y variables del sombreador.</span><span class="sxs-lookup"><span data-stu-id="e6844-121">The comment string at the top of the shader that identifies the shader constants and variables.</span></span>

</dd> <dt>

<span data-ttu-id="e6844-122">*ppDisassembly* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e6844-122">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6844-123">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="e6844-123">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="e6844-124">Dirección de un búfer (vea la [**interfaz ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene el sombreador desensamblado.</span><span class="sxs-lookup"><span data-stu-id="e6844-124">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6844-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6844-125">Return value</span></span>

<span data-ttu-id="e6844-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e6844-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e6844-127">Devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e6844-127">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e6844-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6844-128">Remarks</span></span>

<span data-ttu-id="e6844-129">Este texto devuelto incluye un encabezado con la versión del compilador de HLSL usada para generar este objeto, comentarios que describen el diseño de memoria de los búferes de constantes utilizados por el sombreador, las firmas de entrada y salida y los puntos de enlace de recursos.</span><span class="sxs-lookup"><span data-stu-id="e6844-129">This returned text includes a header with the version of the HLSL compiler used to generate this object, comments describing the memory layout of the constant buffers used by the shader, input and output signatures, and resource binding points.</span></span>

<span data-ttu-id="e6844-130">Este es un ejemplo del desensamblado de un sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="e6844-130">Here is an example of disassembling a compiled shader.</span></span> <span data-ttu-id="e6844-131">En el ejemplo se da por supuesto que empieza con un sombreador compilado (mostrado como *pVSBuf* , que puede ver en el [ejemplo de HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span><span class="sxs-lookup"><span data-stu-id="e6844-131">The example assumes you start with a compiled shader (shown as *pVSBuf* which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="e6844-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6844-132">Requirements</span></span>



| <span data-ttu-id="e6844-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6844-133">Requirement</span></span> | <span data-ttu-id="e6844-134">Value</span><span class="sxs-lookup"><span data-stu-id="e6844-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6844-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6844-135">Header</span></span><br/> | <dl> <span data-ttu-id="e6844-136"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6844-136"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6844-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6844-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6844-138">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="e6844-138">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
