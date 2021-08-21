---
description: Guarda un búfer comprimido de transferencia de base precalcalada (PRT) en el disco.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: Función D3DXSavePRTCompBufferToFile (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a62bd164ce8eb8175c62658b19dd5ce6282d6c75b081db45f8b0af4994322579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524515"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a>Función D3DXSavePRTCompBufferToFile

Guarda un búfer comprimido de transferencia de base precalcalada (PRT) en el disco.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a>Parámetros

*pFileName* \[ En\]

Tipo: **[LPCSTR](../winprog/windows-data-types.md)**

Nombre del archivo en el que se va a guardar el búfer comprimido.

*pBuffer* \[ En\]

Tipo: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**

Dirección de un puntero al objeto [**ID3DXPRTCompBuffer de**](id3dxprtcompbuffer.md) entrada.

## <a name="return-value"></a>Valor devuelto

Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**

Si el método se realiza correctamente, el valor devuelto es **D3D \_ OK**. Si se produce un error en el método , el valor devuelto puede ser **D3DERR \_ INVALIDCALL**.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en [D3DXSavePRTCompBufferToFileW](). De lo contrario, la llamada de función se resuelve en **D3DXSavePRTCompBufferToFileA**.

El formato de archivo PCA es un archivo binario en forma de encabezado y, a continuación, dos o tres bloques de datos.

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

En el caso de *que bIsTex* sea distinto de cero, *NumSamples* debe ser igual a `TexWidth * TexHeight` .

El bloque de datos base que sigue al encabezado es `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.

A continuación, se muestra el bloque de datos PCA weights, que es `NumPCA * NumSamples * sizeof(float)` bytes.

Si *NumClusters es* mayor que 1, el archivo finaliza con el bloque de datos de bytes de los IDs del `NumSamples * sizeof(UINT)` clúster.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |

## <a name="see-also"></a>Vea también

[Funciones de transferencia de radiancia precalcaladas](dx9-graphics-reference-d3dx-functions-prt.md)
