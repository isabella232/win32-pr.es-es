---
description: Nota En lugar de usar esta función heredada, se recomienda usar la API D3DDisassemble. Esta función , que desensambla un sombreador compilado en una cadena de texto que contiene instrucciones de ensamblado y registra asignaciones, ya no existe.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: Función D3DX10DisassembleShader (D3DX10Core.h)
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
ms.openlocfilehash: bd69b6dc2cede96e6ca07983195d202cfd248633f44a13fe1967393c446ca329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753225"
---
# <a name="d3dx10disassembleshader-function"></a>Función D3DX10DisassembleShader

> [!Note]  
> En lugar de usar esta función heredada, se recomienda usar la API [**D3DDisassemble.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble)

 

Esta función , que desensambla un sombreador compilado en una cadena de texto que contiene instrucciones de ensamblado y registra asignaciones, ya no existe. En su lugar, [**use D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

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

*pShader* \[ En\]
</dt> <dd>

Tipo: **const \* void**

Puntero al [**sombreador compilado.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)

</dd> <dt>

*BytecodeLength* \[ En\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Tamaño de pShader.

</dd> <dt>

*EnableColorCode* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Incluya etiquetas HTML en la salida para colorear el resultado.

</dd> <dt>

*pComments* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena de comentario en la parte superior del sombreador que identifica las constantes y variables del sombreador.

</dd> <dt>

*ppDisassembly* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un búfer (vea [**Interfaz ID3D10Blob)**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)que contiene el sombreador desensamblado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Este texto devuelto incluye un encabezado con la versión del compilador HLSL utilizada para generar este objeto, comentarios que describen el diseño de memoria de los búferes constantes utilizados por el sombreador, las firmas de entrada y salida y los puntos de enlace de recursos.

Este es un ejemplo de desacompilación de un sombreador compilado. En el ejemplo se supone que comienza con un sombreador compilado (que se muestra como *pVSBuf,* que puede ver en [ejemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).


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
| Encabezado<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
