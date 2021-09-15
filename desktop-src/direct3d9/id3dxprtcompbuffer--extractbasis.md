---
description: Extrae los vectores de base de análisis de componentes principales y medio (PCA) para un clúster determinado de un búfer de datos comprimido ID3DXPRTCompBuffer.
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: Método ID3DXPRTCompBuffer::ExtractBasis (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ebedef91c9f3d1e277a099ffd295903e9ba77ba8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127565868"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a>Método ID3DXPRTCompBuffer::ExtractBasis

Extrae los vectores de base de análisis de componentes principales y medio (PCA) para un clúster determinado de un búfer de datos comprimido [**ID3DXPRTCompBuffer.**](id3dxprtcompbuffer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clúster* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Clúster para el que se extraerá la base.

</dd> <dt>

*pClusterBasis* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a una matriz de datos vectoriales de base para Cluster. El tamaño de los datos FLOAT almacenados será: (1 + Número de vectores de PCA por clúster) (Número de \* coeficientes) \* (Número de canales de color)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
