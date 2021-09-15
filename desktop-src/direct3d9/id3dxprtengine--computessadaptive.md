---
description: Calcula un vector de transferencia que asigna el radiance de origen para salir del radiance resultante de la dispersión subsuperficial, mediante el muestreo adaptable y las propiedades de material establecidas por ID3DXPRTEngine::SetMeshMaterials.
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: Método ID3DXPRTEngine::ComputeSSAdaptive (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569904"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a>Método ID3DXPRTEngine::ComputeSSAdaptive

Calcula un vector de transferencia que asigna el radiance de origen para salir del radiance resultante de la dispersión subsuperficial, mediante el muestreo adaptable y las propiedades de material establecidas por [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). El método genera nuevos vértices y caras en la malla para aproximarse con más precisión a la señal de transferencia de base precalutada (PRT). Este método solo se puede usar para materiales definidos por vértice en un objeto de malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeSSAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDataIn* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) entrada que representa el objeto 3D del anterior salto de luz. Este búfer de entrada debe tener asignado el número adecuado de canales de color para la simulación.

</dd> <dt>

*AdaptiveThresh* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Umbral en el vector PRT que se usará para subdividir las caras y los vértices de malla. Si es menor que 1e-6f, se especifica un valor predeterminado de 1e-6f.

</dd> <dt>

*MinEdgeLength* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Longitud mínima del borde de la cara que se generará en el muestreo adaptable. Si el método determina que el valor es demasiado pequeño, se especifica un valor dependiente del modelo.

</dd> <dt>

*MaxSubdiv* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nivel máximo de subdivisión de una cara que se usará en el muestreo adaptable. Si es cero, se especifica un valor predeterminado de 4.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) salida que modela un único salto de la luz dispersa por subsuelo. Este búfer de salida debe tener asignado el número adecuado de canales de color para la simulación.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que es la suma en ejecución de todas las salidas pDataOut anteriores. Puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Para modelar la dispersión de subsuperficie, llame a este método para cada rebotón de luz después de llamar a un método [**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive.**](id3dxprtengine--computedirectlightingshadaptive.md)

La salida de este método no incluye albedo y solo se integra la luz entrante en el simulador. Al no multiplicar el albedo, puede modelar la variación de albedo a una escala más fina que la de origen, lo que produce resultados más precisos a partir de la compresión.

Llame [**a ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vector prT por el albedo.

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
</dt> <dt>

[**ID3DXPRTEngine::ComputeSS**](id3dxprtengine--computess.md)
</dt> </dl>

 

 
