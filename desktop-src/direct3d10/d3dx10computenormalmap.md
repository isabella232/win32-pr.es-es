---
description: 'Función D3DX10ComputeNormalMap: convierte un mapa de alto en un mapa normal. Los componentes (x,y,z) de cada normal se asignan a los canales (r,g,b) de la textura de salida.'
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: Función D3DX10ComputeNormalMap (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 173a8e0c1b3130a399152187eb52288a0306051c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105323"
---
# <a name="d3dx10computenormalmap-function"></a>Función D3DX10ComputeNormalMap

Convierte un mapa de alto en un mapa normal. Los componentes (x,y,z) de cada normal se asignan a los canales (r,g,b) de la textura de salida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcTexture* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Puntero a una interfaz ID3D10Texture2D, que representa la textura del mapa de alto de origen.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Una o varias marcas NORMALMAP de D3DX \_ que controlan la generación de mapas normales.

</dd> <dt>

*Canal* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Una marca D3DX \_ CHANNEL que especifica el origen de la información de alto.

</dd> <dt>

*Amplitude* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Multiplicador de valor constante que aumenta (o disminuye) los valores del mapa normal. Los valores más altos suelen hacer que los aumentos sean más visibles, y los valores más bajos suelen hacer que los aumentos sean menos visibles.

</dd> <dt>

*pDestTexture* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Puntero a una interfaz ID3D10Texture2D, que representa la textura de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Este método calcula lo normal mediante la diferencia central con un tamaño de kernel de 3x3. Los canales RGB del destino contienen componentes sesgados (x, y,z) de lo normal. El denominador de diferenciación central se codifica de forma rígida en 2.0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de textura en D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
