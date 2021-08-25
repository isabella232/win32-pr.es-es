---
description: 'Interfaz ID3DXLoadUserData: la aplicación implementa esta interfaz para guardar los datos de usuario adicionales insertados en archivos .x.'
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: Interfaz ID3DXLoadUserData (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ede66e7250a1dec095bd03a72ea69e58afb59a60b43647fd49adfc958689cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748125"
---
# <a name="id3dxloaduserdata-interface"></a>Interfaz ID3DXLoadUserData

Esta interfaz la implementa la aplicación para guardar los datos de usuario adicionales insertados en archivos .x. Una instancia de esta interfaz se pasa a [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)y D3DX llama al método adecuado en esta interfaz cada vez que se encuentran los datos adecuados. Por ejemplo, para cada objeto de marco del archivo .x, se llama a [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) y se pasan los datos secundarios.

## <a name="members"></a>Miembros

La **interfaz ID3DXLoadUserData** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXLoadUserData** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXLoadUserData** tiene estos métodos.



| Método                                                              | Descripción                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) | Cargar datos secundarios de marco desde un archivo .x.<br/> |
| [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md)   | Cargar datos secundarios de malla desde un archivo .x.<br/>  |
| [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md)     | Cargar datos de nivel superior desde un archivo .x.<br/>   |



 

## <a name="remarks"></a>Comentarios

El tipo LPD3DXLOADUSERDATA se define como un puntero a esta interfaz.


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
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

 

 
