---
description: Calcular vectores tangentes, binormales y normales para una malla.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: Función D3DXComputeTangentFrame (D3DX9Mesh.h)
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
ms.openlocfilehash: 532b265f387179d88581f6f0a05227162de6a8402e324e7be2e13a16ca4a3ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849835"
---
# <a name="d3dxcomputetangentframe-function"></a>Función D3DXComputeTangentFrame

Calcular vectores tangentes, binormales y normales para una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***

Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) de entrada.

</dd> <dt>

*dwOptions* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias [**marcas D3DXTANGENT.**](./d3dxtangent.md)

Use **NULL** para especificar las siguientes opciones:

-   Ponderar la longitud del vector normal por el ángulo, en radianes, subterfundo por los dos bordes que salen del vértice.
-   Calcular coordenadas cartesianas ortogonales a partir de las coordenadas de textura UV.
-   Las texturas no se encapsulan en direcciones U o V
-   Los derivados parciales con respecto a las coordenadas de textura se normalizan.
-   Los vértices se ordenan en sentido contrario a las agujas del reloj alrededor de cada triángulo.
-   Use vectores normales por vértice ya presentes en la malla de entrada.
-   Los resultados se almacenarán en la malla de entrada original. Se producirá un error en la función si es necesario crear nuevos vértices.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Esta función simplemente llama [**a D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con los siguientes parámetros de entrada:


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



Las singularidades se controlan según sea necesario mediante la agrupación de bordes y la división de vértices. Si es necesario dividir los vértices, se producirá un error en la función. El vector normal calculado en cada vértice siempre se normaliza para tener longitud de unidad.

La solución más sólida para calcular coordenadas ortogonales cartesianas es no establecer marcas D3DXTANGENT \_ ORTHOGONALIZE FROM you y \_ \_ D3DXTANGENT \_ ORTHOGONALIZE FROM V, para que las coordenadas \_ \_ ortogonales se calcule a partir de ambas coordenadas de textura UV. Sin embargo, en este caso, si U o V es cero, la función calculará las coordenadas ortogonales mediante D3DXTANGENT \_ ORTHOGONALIZE FROM V o \_ \_ D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> <dt>

[**D3DXTANGENT**](./d3dxtangent.md)
</dt> </dl>

 

 
