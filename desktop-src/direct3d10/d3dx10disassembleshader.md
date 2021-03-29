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
# <a name="d3dx10disassembleshader-function"></a>D3DX10DisassembleShader función)

> [!Note]  
> En lugar de usar esta función heredada, se recomienda usar la API de [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .

 

Esta función, que desensambla un sombreador compilado en una cadena de texto que contiene las instrucciones de ensamblado y las asignaciones de registro, ya no existe. En su lugar, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pShader* \[ de\]
</dt> <dd>

Tipo: **const void \***

Puntero al [**sombreador compilado**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).

</dd> <dt>

*BytecodeLength* \[ de\]
</dt> <dd>

Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**

Tamaño de pShader.

</dd> <dt>

*EnableColorCode* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Incluya etiquetas HTML en la salida para el código de color del resultado.

</dd> <dt>

*pComments* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena de comentario en la parte superior del sombreador que identifica las constantes y variables del sombreador.

</dd> <dt>

*ppDisassembly* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un búfer (vea la [**interfaz ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene el sombreador desensamblado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Este texto devuelto incluye un encabezado con la versión del compilador de HLSL usada para generar este objeto, comentarios que describen el diseño de memoria de los búferes de constantes utilizados por el sombreador, las firmas de entrada y salida y los puntos de enlace de recursos.

Este es un ejemplo del desensamblado de un sombreador compilado. En el ejemplo se da por supuesto que empieza con un sombreador compilado (mostrado como *pVSBuf* , que puede ver en el [ejemplo de HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
