---
description: Multiplica cada vector de transferencia Radiance (PRT) precalculado por el albedo por vértice.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'ID3DXPRTEngine:: MultiplyAlbedo (método) (D3DX9Mesh. h)'
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
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708049"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a>ID3DXPRTEngine:: MultiplyAlbedo (método)

Multiplica cada vector de transferencia Radiance (PRT) precalculado por el albedo por vértice.

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

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que contendrá vectores PRT multiplicado por el albedo por vértice. Si este búfer de salida es un objeto de textura, se debe tener cuidado para almacenar el albedo de la textura con la misma resolución que el búfer de simulación. Puede establecer la resolución adecuada en Albedo con [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)y aplicar regiones de medianil de texturas si es necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Los métodos ID3DXPRTEngine:: Computexxx calculan los búferes de salida en los que la señal luminosa no se ha multiplicado por Albedo. Si no se multiplica el albedo, puede modelar la variación de Albedo en una escala más precisa que el Radiance de origen, con lo que se obtienen resultados más precisos de la compresión.

Para incluir Albedo en el modelo representado-Light, llame a este método después de uno de los métodos Computexxx.

Se debe llamar a [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) antes de llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




