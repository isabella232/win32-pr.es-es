---
description: La aplicación implementa esta interfaz para asignar o liberar objetos de contenedor de fotogramas y mallas. Se llama a los métodos de este método durante la carga y la destrucción de las jerarquías de Marcos.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: Interfaz ID3DXAllocateHierarchy (D3dx9anim. h)
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
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083796"
---
# <a name="id3dxallocatehierarchy-interface"></a>Interfaz ID3DXAllocateHierarchy

La aplicación implementa esta interfaz para asignar o liberar objetos de contenedor de fotogramas y mallas. Se llama a los métodos de este método durante la carga y la destrucción de las jerarquías de Marcos.

## <a name="members"></a>Miembros

La interfaz **ID3DXAllocateHierarchy** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAllocateHierarchy** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXAllocateHierarchy** tiene estos métodos.



| Método                                                                       | Descripción                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CreateFrame**](id3dxallocatehierarchy--createframe.md)                   | Solicita la asignación de un objeto de marco.<br/>            |
| [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md)   | Solicita la asignación de un objeto de contenedor de malla.<br/>   |
| [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md)                 | Solicita la desasignación de un objeto de marco.<br/>          |
| [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) | Solicita la desasignación de un objeto de contenedor de malla.<br/> |



 

## <a name="remarks"></a>Observaciones

El tipo LPD3DXALLOCATEHIERARCHY se define como un puntero a esta interfaz.


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
