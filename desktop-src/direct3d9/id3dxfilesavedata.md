---
description: Las aplicaciones usan los métodos de la interfaz ID3DXFileSaveData para agregar objetos de datos como elementos secundarios de un nodo de datos de archivo. x.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: Interfaz ID3DXFileSaveData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698236"
---
# <a name="id3dxfilesavedata-interface"></a>Interfaz ID3DXFileSaveData

Las aplicaciones usan los métodos de la interfaz ID3DXFileSaveData para agregar objetos de datos como elementos secundarios de un nodo de datos de archivo. x.

## <a name="members"></a>Miembros

La interfaz **ID3DXFileSaveData** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileSaveData** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXFileSaveData** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesavedata--adddataobject.md)       | Agrega un objeto de datos como elemento secundario del nodo de datos del archivo **ID3DXFileSaveData** .<br/>                                                      |
| [**AddDataReference**](id3dxfilesavedata--adddatareference.md) | Agrega una referencia de datos como un elemento secundario de este nodo de datos de archivo **ID3DXFileSaveData** . La referencia de datos apunta a un objeto de datos de archivo.<br/> |
| [**GetId**](id3dxfilesavedata--getid.md)                       | Recupera el GUID de este nodo de datos del archivo **ID3DXFileSaveData** .<br/>                                                                |
| [**GetName**](id3dxfilesavedata--getname.md)                   | Recupera el nombre de este nodo de datos del archivo **ID3DXFileSaveData** .<br/>                                                                |
| [**GetSave**](id3dxfilesavedata--getsave.md)                   | Recupera un puntero a este nodo de datos del archivo [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .<br/>                                  |
| [**GetType**](id3dxfilesavedata--gettype.md)                   | Recupera el identificador de plantilla de este nodo de datos de archivo.<br/>                                                                               |



 

## <a name="remarks"></a>Observaciones

El GUID de la interfaz ID3DXFileSaveObject es IID \_ ID3DXFileSaveObject.

El tipo LPD3DXFileSaveData se define como un puntero a esta interfaz.


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de archivo de D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
