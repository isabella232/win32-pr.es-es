---
description: Guarda en el disco un búfer comprimido de Radiance (PRT) comprimido previamente.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: Función D3DXSavePRTCompBufferToFile (D3DX9Mesh. h)
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
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003806"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a>D3DXSavePRTCompBufferToFile función)

Guarda en el disco un búfer comprimido de Radiance (PRT) comprimido previamente.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a>Parámetros

*pFileName* \[ de\]

Tipo: **[LPCSTR](../winprog/windows-data-types.md)**

Nombre del archivo en el que se va a guardar el búfer comprimido.

*pBuffer* \[ de\]

Tipo: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**

Dirección de un puntero al objeto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de entrada.

## <a name="return-value"></a>Valor devuelto

Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**

Si el método se ejecuta correctamente, el valor devuelto es **D3D \_ OK**. Si se produce un error en el método, el valor devuelto puede ser **D3DERR \_ INVALIDCALL**.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como [D3DXSavePRTCompBufferToFileW](). De lo contrario, la llamada de función se resuelve como **D3DXSavePRTCompBufferToFileA**.

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

En el caso de que *bIsTex* sea distinto de cero, *NumSamples* debe ser igual `TexWidth * TexHeight` .

El bloque de datos base que sigue al encabezado es `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.

A continuación se indican los bloques de datos de pesos del PCA, que son `NumPCA * NumSamples * sizeof(float)` bytes.

Si *NumClusters* es mayor que 1, el archivo finaliza con el bloque de datos de los identificadores de clúster de `NumSamples * sizeof(UINT)` bytes.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>Vea también

[Funciones de transferencia Radiance precalculadas](dx9-graphics-reference-d3dx-functions-prt.md)
