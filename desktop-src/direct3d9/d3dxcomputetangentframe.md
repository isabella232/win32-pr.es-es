---
description: Vectores de la tangente de proceso, binormalización y normal para una malla.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: Función D3DXComputeTangentFrame (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718445"
---
# <a name="d3dxcomputetangentframe-function"></a>D3DXComputeTangentFrame función)

Vectores de la tangente de proceso, binormalización y normal para una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***

Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) de entrada.

</dd> <dt>

*dwOptions* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas de [**D3DXTANGENT**](./d3dxtangent.md) .

Use **null** para especificar las siguientes opciones:

-   Pondera la longitud del vector normal por el ángulo, en radianes, que se repite en los dos bordes que abandonan el vértice.
-   Calcula las coordenadas cartesianas ortogonales a partir de las coordenadas de textura UV.
-   Las texturas no se ajustan en las direcciones U o V
-   Se normalizan las derivadas parciales con respecto a las coordenadas de textura.
-   Los vértices se ordenan en sentido contrario a las agujas del reloj alrededor de cada triángulo.
-   Use vectores normales por vértice ya presentes en la malla de entrada.
-   Los resultados se almacenarán en la malla de entrada original. Se producirá un error en la función si es necesario crear nuevos vértices.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función simplemente llama a [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con los siguientes parámetros de entrada:


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



Las singularidades se controlan según sea necesario mediante la agrupación de los bordes y la división de los vértices. Si es necesario dividir los vértices, se producirá un error en la función. El vector normal calculado en cada vértice siempre se normaliza para tener una longitud de unidad.

La solución más sólida para calcular coordenadas cartesianas ortogonales consiste en no establecer marcas D3DXTANGENT \_ ortogonales \_ desde el \_ usuario y D3DXTANGENT \_ ortogonal \_ desde \_ V, de modo que las coordenadas ortogonales se calculan a partir de las coordenadas de textura UV. Sin embargo, en este caso, si U o V es cero, la función calculará las coordenadas ortogonales mediante D3DXTANGENT \_ ortogonal \_ desde \_ V o D3DXTANGENT se \_ ortogonala \_ desde \_ U, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> <dt>

[**D3DXTANGENT**](./d3dxtangent.md)
</dt> </dl>

 

 
