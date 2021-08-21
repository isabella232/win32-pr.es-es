---
description: Multiplica cada vector de transferencia de radiancia precalutada (PRT) por el albedo por vértice.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: Método ID3DXPRTEngine::MultiplyAlbedo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2989ce2a662be5a1ec53c961b8fafa072862fc2b43b6003b04f6b887ef3c077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790545"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a>Método ID3DXPRTEngine::MultiplyAlbedo

Multiplica cada vector de transferencia de radiancia precalutada (PRT) por el albedo por vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) salida que contendrá vectores PRT multiplicados por el albedo por vértice. Si este búfer de salida es un objeto de textura, se debe tener cuidado para almacenar el albedo de la textura en la misma resolución que el búfer de simulación. Puede establecer la resolución adecuada en el albedo con [**D3DXLoadSurfaceFromSurface,**](d3dxloadsurfacefromsurface.md)aplicando las regiones de medianías de textura si procede.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Los métodos ID3DXPRTEngine::Computexxx calculan los búferes de salida en los que la señal de luz no se ha multiplicado por albedo. Al no multiplicar el albedo, puede modelar la variación de albedo a una escala más fina que la de origen, lo que produce resultados más precisos a partir de la compresión.

Para incluir albedo en el modelo de luz representado, llame a este método después de uno de los métodos Computexxx.

Se debe llamar a [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) antes de llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




