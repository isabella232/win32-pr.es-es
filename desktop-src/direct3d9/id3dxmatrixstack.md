---
description: 'Interfaz ID3DXMATRIXStack: las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matrices.'
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: Interfaz ID3DXMATRIXStack (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b8fa483be72d29cc869b2bd468cff25033a80187bef69317af4894fc05b096dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856455"
---
# <a name="id3dxmatrixstack-interface"></a>Interfaz ID3DXMATRIXStack

Las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matrices.

## <a name="members"></a>Miembros

La **interfaz ID3DXMATRIXStack** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXMATRIXStack** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXMATRIXStack** tiene estos métodos.



| Método                                                                       | Descripción                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack--gettop.md)                                   | Recupera la matriz actual en la parte superior de la pila.<br/>                                                                           |
| [**LoadIdentity**](id3dxmatrixstack--loadidentity.md)                       | Carga la identidad en la matriz actual.<br/>                                                                                           |
| [**LoadMatrix**](id3dxmatrixstack--loadmatrix.md)                           | Carga la matriz dada en la matriz actual.<br/>                                                                                 |
| [**MultMatrix**](id3dxmatrixstack--multmatrix.md)                           | Determina el producto de la matriz actual y la matriz dada.<br/>                                                              |
| [**MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)                 | Determina el producto de la matriz dada y la matriz actual.<br/>                                                              |
| [**Pop**](id3dxmatrixstack--pop.md)                                         | Quita la matriz actual de la parte superior de la pila.<br/>                                                                           |
| [**Empuje**](id3dxmatrixstack--push.md)                                       | Agrega una matriz a la pila.<br/>                                                                                                     |
| [**RotateAxis**](id3dxmatrixstack--rotateaxis.md)                           | Gira (en relación con el espacio de coordenadas universal) alrededor de un eje arbitrario.<br/>                                                          |
| [**RotateAxisLocal**](id3dxmatrixstack--rotateaxislocal.md)                 | Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.<br/>                                             |
| [**RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)           | Gira (en relación con el espacio de coordenadas universal) alrededor de un eje arbitrario.<br/>                                                          |
| [**RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md) | Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.<br/>                                             |
| [**Escala**](id3dxmatrixstack--scale.md)                                     | Escale la matriz actual sobre el origen de la coordenada mundial.<br/>                                                                     |
| [**ScaleLocal**](id3dxmatrixstack--scalelocal.md)                           | Escale la matriz actual sobre el origen del objeto.<br/>                                                                               |
| [**Traducir**](id3dxmatrixstack--translate.md)                             | Determina el producto de la matriz actual y la matriz de traducción calculada determinada por los factores especificados (x, y y z).<br/> |
| [**TranslateLocal**](id3dxmatrixstack--translatelocal.md)                   | Determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.<br/> |



 

## <a name="remarks"></a>Comentarios

La **interfaz ID3DXMATRIXStack** se obtiene mediante una llamada a la función [**D3DXCreateMatrixStack.**](d3dxcreatematrixstack.md)

El tipo LPD3DXMATRIXSTACK se define como un puntero a la **interfaz ID3DXMATRIXStack.**


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
