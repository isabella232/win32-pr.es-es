---
description: Las aplicaciones usan los métodos de la interfaz ID3DXFileSaveObject para escribir un archivo. x en el disco, y para agregar y guardar objetos y plantillas de datos.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: Interfaz ID3DXFileSaveObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8d657c327c75045cf4feb2080a2e57d80f752df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717748"
---
# <a name="id3dxfilesaveobject-interface"></a>Interfaz ID3DXFileSaveObject

Las aplicaciones usan los métodos de la interfaz ID3DXFileSaveObject para escribir un archivo. x en el disco, y para agregar y guardar objetos y plantillas de datos.

## <a name="members"></a>Miembros

La interfaz **ID3DXFileSaveObject** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileSaveObject** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXFileSaveObject** tiene estos métodos.



| Método                                                      | Descripción                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesaveobject--adddataobject.md) | Agrega un objeto de datos como elemento secundario del objeto [**ID3DXFileSaveData**](id3dxfilesavedata.md) .<br/>                       |
| [**GetFile**](id3dxfilesaveobject--getfile.md)             | Obtiene la interfaz [**ID3DXFile**](id3dxfile.md) del objeto que creó este objeto **ID3DXFileSaveObject** .<br/> |
| [**Guardar**](id3dxfilesaveobject--save.md)                   | Guarda un objeto de datos y sus elementos secundarios en un archivo. x en el disco.<br/>                                                        |



 

## <a name="remarks"></a>Observaciones

No se requieren plantillas en todos los archivos. Por ejemplo, puede colocar todas las plantillas en un solo archivo. x en lugar de duplicarlas en cada archivo. x.

La interfaz ID3DXFileSaveObject se obtiene llamando al método [**ID3DXFile:: CreateSaveObject**](id3dxfile--createsaveobject.md) .

El identificador único global (GUID) de la interfaz ID3DXFileSaveObject es IID \_ ID3DXFileSaveObject.

El tipo LPD3DXFILESAVEOBJECT se define como un puntero a esta interfaz.


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
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

 

 
