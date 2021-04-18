---
description: Guarda un búfer de Radiance Transfer (PRT) precalculado en el disco.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: Función D3DXSavePRTBufferToFile (D3DX9Mesh. h)
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
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698228"
---
# <a name="d3dxsaveprtbuffertofile-function"></a>D3DXSavePRTBufferToFile función)

Guarda un búfer de Radiance Transfer (PRT) precalculado en el disco.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a>Parámetros

*pFileName* \[ de\]

Tipo: **[LPCSTR](../winprog/windows-data-types.md)**

Nombre del archivo en el que se va a guardar el búfer.

*pBuffer* \[ de\]

Tipo: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**

Dirección de un puntero al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada.

## <a name="return-value"></a>Valor devuelto

Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**

Si el método se ejecuta correctamente, el valor devuelto es **D3D \_ OK**. Si se produce un error en el método, el valor devuelto puede ser **D3DERR \_ INVALIDCALL**.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como [D3DXSavePRTBufferToFileW](). De lo contrario, la llamada de función se resuelve como **D3DXSavePRTBufferToFileA**.

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

En el caso de que *bIsTex* sea distinto de cero, *NumSamples* debe ser igual `TexWidth * TexHeight` .

El bloque de datos que sigue al encabezado es `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>Vea también

[Funciones de transferencia Radiance precalculadas](dx9-graphics-reference-d3dx-functions-prt.md)
