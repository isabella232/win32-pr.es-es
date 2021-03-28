---
title: Interfaz ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Una interfaz de matriz variable tiene acceso a una matriz.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5c4c89a231d429fc0a1f8fecbcbb4d06db35cb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987042"
---
# <a name="id3dx11effectmatrixvariable-interface"></a>Interfaz ID3DX11EffectMatrixVariable

Una interfaz de matriz variable tiene acceso a una matriz.

## <a name="members"></a>Miembros

La interfaz **ID3DX11EffectMatrixVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectMatrixVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11EffectMatrixVariable** tiene estos métodos.



| Método                                                                                 | Descripción                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**GetMatrix**](id3dx11effectmatrixvariable-getmatrix.md)                             | Obtiene una matriz.<br/>                                          |
| [**GetMatrixArray**](id3dx11effectmatrixvariable-getmatrixarray.md)                   | Obtiene una matriz de matrices.<br/>                              |
| [**GetMatrixTranspose**](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | Transponer y obtener una matriz de punto flotante.<br/>             |
| [**GetMatrixTransposeArray**](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | Transponer y obtener una matriz de matrices de punto flotante.<br/> |
| [**SetMatrix**](id3dx11effectmatrixvariable-setmatrix.md)                             | Establezca una matriz de punto flotante.<br/>                           |
| [**SetMatrixArray**](id3dx11effectmatrixvariable-setmatrixarray.md)                   | Establezca una matriz de matrices de punto flotante.<br/>               |
| [**SetMatrixTranspose**](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | Transponer y establecer una matriz de punto flotante.<br/>             |
| [**SetMatrixTransposeArray**](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | Transponer y establecer una matriz de matrices de punto flotante.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





