---
description: Las aplicaciones usan los métodos de la interfaz ID3DXMesh para manipular objetos de malla.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: Interfaz ID3DXMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070349"
---
# <a name="id3dxmesh-interface"></a>Interfaz ID3DXMesh

Las aplicaciones usan los métodos de la interfaz ID3DXMesh para manipular objetos de malla.

## <a name="members"></a>Members

La **interfaz ID3DXMesh** hereda de [**ID3DXBaseMesh**](id3dxbasemesh.md). **ID3DXMesh** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXMesh** tiene estos métodos.



| Método                                                            | Descripción                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)     | Bloquea el búfer de malla que contiene los datos del atributo de malla y devuelve un puntero a él.<br/>                                   |
| [**Optimización**](id3dxmesh--optimize.md)                           | Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.<br/>                                     |
| [**OptimizeInplace**](id3dxmesh--optimizeinplace.md)             | Genera una malla con caras y vértices reordenados para optimizar el rendimiento del dibujo. Este método reordena la malla existente.<br/> |
| [**SetAttributeTable**](id3dxmesh--setattributetable.md)         | Establece la tabla de atributos para una malla y el número de entradas almacenadas en la tabla.<br/>                                          |
| [**UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md) | Desbloquea un búfer de atributos.<br/>                                                                                                |



 

## <a name="remarks"></a>Observaciones

Para obtener la **interfaz ID3DXMesh,** llame a las funciones [**D3DXCreateMesh**](d3dxcreatemesh.md) o [**D3DXCreateMeshFVF.**](d3dxcreatemeshfvf.md)

Esta interfaz hereda funcionalidad adicional de la [**interfaz ID3DXBaseMesh.**](id3dxbasemesh.md)

El tipo LPD3DXMESH se define como un puntero a la **interfaz ID3DXMesh.**


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




