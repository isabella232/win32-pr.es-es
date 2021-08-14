---
description: Guarda un búfer de transferencia de radiancia precalutados (PRT) en el disco.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: Función D3DXSavePRTBufferToFile (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfa3d06970d138ff1c868403c20bb41cf14f0a5cbb7116cbe0f0843a51258dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524535"
---
# <a name="d3dxsaveprtbuffertofile-function"></a>Función D3DXSavePRTBufferToFile

Guarda un búfer de transferencia de radiancia precalutados (PRT) en el disco.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a>Parámetros

*pFileName* \[ En\]

Tipo: **[LPCSTR](../winprog/windows-data-types.md)**

Nombre del archivo en el que se va a guardar el búfer.

*pBuffer* \[ En\]

Tipo: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**

Dirección de un puntero al objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) entrada.

## <a name="return-value"></a>Valor devuelto

Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**

Si el método se realiza correctamente, el valor devuelto es **D3D \_ OK**. Si se produce un error en el método , el valor devuelto puede ser **D3DERR \_ INVALIDCALL**.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en [D3DXSavePRTBufferToFileW](). De lo contrario, la llamada de función se resuelve en **D3DXSavePRTBufferToFileA**.

El formato de archivo PRT es un archivo binario en forma de encabezado y, a continuación, un bloque de datos.

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

En el caso de *que bIsTex* sea distinto de cero, *NumSamples* debe ser igual a `TexWidth * TexHeight` .

El bloque de datos que sigue al encabezado es `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |

## <a name="see-also"></a>Consulte también

[Funciones de transferencia de radiancia precalcaladas](dx9-graphics-reference-d3dx-functions-prt.md)
