---
description: Esta interfaz la implementa la aplicación para asignar o liberar objetos de contenedor de malla y marco. Se llama a métodos al cargar y destruir jerarquías de fotogramas.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: Interfaz ID3DXAllocateHierarchy (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e971248b5510ec59e904b51d12f8ee03e45132e64561315c13bb8f826f37c970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094587"
---
# <a name="id3dxallocatehierarchy-interface"></a>Interfaz ID3DXAllocateHierarchy

Esta interfaz la implementa la aplicación para asignar o liberar objetos de contenedor de malla y marco. Se llama a métodos al cargar y destruir jerarquías de fotogramas.

## <a name="members"></a>Miembros

La **interfaz ID3DXAllocateHierarchy** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXAllocateHierarchy** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXAllocateHierarchy** tiene estos métodos.



| Método                                                                       | Descripción                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CreateFrame**](id3dxallocatehierarchy--createframe.md)                   | Solicita la asignación de un objeto de marco.<br/>            |
| [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md)   | Solicita la asignación de un objeto de contenedor de malla.<br/>   |
| [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md)                 | Solicita la desasignación de un objeto de marco.<br/>          |
| [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) | Solicita la desasignación de un objeto de contenedor de malla.<br/> |



 

## <a name="remarks"></a>Comentarios

El tipo LPD3DXALLOCATEHIERARCHY se define como un puntero a esta interfaz.


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
