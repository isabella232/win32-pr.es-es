---
description: Convierte un mapa de alto en un mapa normal. Los componentes (x, y, z) de cada normal se asignan a los canales (r, g, b) de la textura de salida.
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: Función D3DX10ComputeNormalMap (D3DX10Tex. h)
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
ms.openlocfilehash: 1d7318e6d00d921ba0d573eb6fb696eed6c6a58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718281"
---
# <a name="d3dx10computenormalmap-function"></a>D3DX10ComputeNormalMap función)

Convierte un mapa de alto en un mapa normal. Los componentes (x, y, z) de cada normal se asignan a los canales (r, g, b) de la textura de salida.

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

*pSrcTexture* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Puntero a una interfaz ID3D10Texture2D que representa la textura de mapa de alto de origen.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Una o varias \_ marcas de NORMALMAP de D3DX que controlan la generación de asignaciones normales.

</dd> <dt>

*Canal* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Una \_ marca de canal de D3DX que especifica el origen de la información de alto.

</dd> <dt>

*Amplitud* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Multiplicador de valor constante que aumenta (o reduce) los valores del mapa normal. Los valores más altos normalmente hacen que los golpes sean más visibles, los valores más bajos normalmente hacen que los golpes sean menos visibles.

</dd> <dt>

*pDestTexture* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Puntero a una interfaz ID3D10Texture2D que representa la textura de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método calcula el normal mediante el uso de la diferencia central con el tamaño del kernel 3x3. Los canales RGB del destino contienen componentes sesgados (x, y, z) de la normal. El denominador de diferencia central se codifica en 2,0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
