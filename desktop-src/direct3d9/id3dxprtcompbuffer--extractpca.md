---
description: Extrae los coeficientes de proyección de análisis de componentes principales (PCA) por ejemplo de un búfer de datos comprimido ID3DXPRTCompBuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: Método ID3DXPRTCompBuffer::ExtractPCA (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6b172682883c5e5272ece103879aefbbdfb79193b0576e9be04432b5d48b1bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856145"
---
# <a name="id3dxprtcompbufferextractpca-method"></a>Método ID3DXPRTCompBuffer::ExtractPCA

Extrae los coeficientes de proyección de análisis de componentes principales (PCA) por ejemplo de un búfer de datos comprimido [**ID3DXPRTCompBuffer.**](id3dxprtcompbuffer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartPCA* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice inicial para los coeficientes de proyección PCA que se extraerán del búfer.

</dd> <dt>

*NumExtract* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de coeficientes de proyección de PCA que se extraerán del búfer.

</dd> <dt>

*pPCACoefficients* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a la ubicación donde se escriben los coeficientes de análisis de componentes principales agrupados (DAXA). El tamaño de los datos escritos es (número de muestras) \* (número de coeficientes pca).

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

 

 
