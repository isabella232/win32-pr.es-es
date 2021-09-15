---
description: Calcula el brillo de origen resultante de la dispersión de subsuelo, utilizando las propiedades de material establecidas por ID3DXPRTEngine::SetMeshMaterials. Este método solo se puede usar para materiales definidos por vértice en un objeto de malla.
ms.assetid: cdf0d9c1-70e3-44d5-b97a-0521e6739daf
title: Método ID3DXPRTEngine::ComputeSS (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSS
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 89a69be6cc946ff6695d234b8bfb82532385526e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569905"
---
# <a name="id3dxprtenginecomputess-method"></a>Método ID3DXPRTEngine::ComputeSS

Calcula el brillo de origen resultante de la dispersión de subsuelo, utilizando las propiedades de material establecidas [**por ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). Este método solo se puede usar para materiales definidos por vértice en un objeto de malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeSS(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDataIn* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) entrada que representa el objeto 3D de la luz anterior. Este búfer de entrada debe tener asignado el número adecuado de canales de color para la simulación.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) salida que modela un único salto de la luz dispersa por subsuelo. Este búfer de salida debe tener el número adecuado de canales de color asignados para la simulación.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que es la suma en ejecución de todas las salidas pDataOut anteriores. Puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Para modelar la dispersión de subsuelo, llame a este método para cada efecto de efecto de luz después de llamar a un método ID3DXPRTEngine::ComputeDirectLighting.

Use la siguiente secuencia de llamada para modelar la dispersión de subsuelo.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
    
hr = m_pPRTEngine->ComputeDirectLightingSH( SHOrder, pDataA );
    
// *pDataC should be set to zero. The ComputeSS call will add together the    
// direct lighting results from pDataA for non-subsurface scattering elements   
// and subsurface scattering results for the subsurface scattering elements.
    
hr = m_pPRTEngine->ComputeSS( pDataA, pDataB, pDataC );
if ( FAILED( hr ) ) goto Exit;
```



La salida de este método no incluye albedo y solo se integra la luz entrante en el simulador. Al no multiplicar el albedo, puede modelar la variación de albedo a una escala más precisa que la de origen, lo que produce resultados más precisos a partir de la compresión.

Llame [**a ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vector de transferencia de radiancia precalutizado (PRT) por el albedo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounce**](id3dxprtengine--computebounce.md)
</dt> </dl>

 

 




