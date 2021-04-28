---
description: 'Interfaz ID3DXMatrixStack: las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matrices.'
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: Interfaz ID3DXMatrixStack (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMatrixStack
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65e9a5cd041431e1939346fec79dcf94fccd4ae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094413"
---
# <a name="id3dxmatrixstack-interface"></a>Interfaz ID3DXMatrixStack

Las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matrices.

## <a name="members"></a>Miembros

La **interfaz ID3DXMatrixStack** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXMatrixStack también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXMatrixStack** tiene estos métodos.



| Método                                                                      | Descripción                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack-gettop.md)                                   | Recupera la matriz actual en la parte superior de la pila.<br/>                                                                           |
| [**LoadIdentity**](id3dxmatrixstack-loadidentity.md)                       | Carga la identidad en la matriz actual.<br/>                                                                                           |
| [**LoadMatrix**](id3dxmatrixstack-loadmatrix.md)                           | Carga la matriz dada en la matriz actual.<br/>                                                                                 |
| [**MultMatrix**](id3dxmatrixstack-multmatrix.md)                           | Determina el producto de la matriz actual y la matriz dada.<br/>                                                              |
| [**MultMatrixLocal**](id3dxmatrixstack-multmatrixlocal.md)                 | Determina el producto de la matriz dada y la matriz actual.<br/>                                                              |
| [**Pop**](id3dxmatrixstack-pop.md)                                         | Quita la matriz actual de la parte superior de la pila.<br/>                                                                           |
| [**Insertar**](id3dxmatrixstack-push.md)                                       | Agrega una matriz a la pila.<br/>                                                                                                     |
| [**RotateAxis**](id3dxmatrixstack-rotateaxis.md)                           | Gira (en relación con el espacio de coordenadas universal) alrededor de un eje arbitrario.<br/>                                                          |
| [**RotateAxisLocal**](id3dxmatrixstack-rotateaxislocal.md)                 | Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.<br/>                                             |
| [**RotateYawPitchRoll**](id3dxmatrixstack-rotateyawpitchroll.md)           | Gira (en relación con el espacio de coordenadas universal) alrededor de un eje arbitrario.<br/>                                                          |
| [**RotateYawPitchRollLocal**](id3dxmatrixstack-rotateyawpitchrolllocal.md) | Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.<br/>                                             |
| [**Escala**](id3dxmatrixstack-scale.md)                                     | Escale la matriz actual sobre el origen de la coordenada mundial.<br/>                                                                     |
| [**ScaleLocal**](id3dxmatrixstack-scalelocal.md)                           | Escale la matriz actual sobre el origen del objeto.<br/>                                                                               |
| [**Traducir**](id3dxmatrixstack-translate.md)                             | Determina el producto de la matriz actual y la matriz de traducción calculada determinada por los factores especificados (x, y y z).<br/> |
| [**TranslateLocal**](id3dxmatrixstack-translatelocal.md)                   | Determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.<br/> |



 

## <a name="remarks"></a>Comentarios

La interfaz ID3DX10MATRIXStack se obtiene mediante una llamada a la función [**D3DXCreateMatrixStack.**](d3d10-d3dxcreatematrixstack.md)

El tipo LPD3DX10MATRIXSTACK se define como un puntero a la **interfaz ID3DXMatrixStack.**


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
