---
description: Las aplicaciones usan los métodos de la interfaz ID3DXFile para crear instancias de las interfaces ID3DXFileEnumObject e ID3DXFileSaveObject y para registrar plantillas.
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: Interfaz ID3DXFile (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718297"
---
# <a name="id3dxfile-interface"></a>Interfaz ID3DXFile

Las aplicaciones usan los métodos de la interfaz ID3DXFile para crear instancias de las interfaces [**ID3DXFileEnumObject**](id3dxfileenumobject.md) e [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) y para registrar plantillas.

## <a name="members"></a>Miembros

La interfaz **ID3DXFile** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFile** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXFile** tiene estos métodos.



| Método                                                            | Descripción                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**CreateEnumObject**](id3dxfile--createenumobject.md)           | Crea un objeto enumerador que leerá un archivo. x.<br/>                                                      |
| [**CreateSaveObject**](id3dxfile--createsaveobject.md)           | Crea un objeto Save que se usará para guardar los datos en un archivo. x.<br/>                                          |
| [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) | Registra plantillas personalizadas, dado un objeto de enumeración [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .<br/> |
| [**RegisterTemplates**](id3dxfile--registertemplates.md)         | Registra plantillas personalizadas.<br/>                                                                                 |



 

## <a name="remarks"></a>Observaciones

Un objeto ID3DXFile también contiene un almacén de plantillas local. Este almacenamiento local se puede Agregar solo a con los métodos [**ID3DXFile:: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) y [**ID3DXFile:: RegisterTemplates**](id3dxfile--registertemplates.md) .

Los objetos [**ID3DXFileEnumObject**](id3dxfileenumobject.md) y [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) creados con [**ID3DXFile:: CreateEnumObject**](id3dxfile--createenumobject.md) y [**ID3DXFile:: CreateSaveObject**](id3dxfile--createsaveobject.md) también usan el almacén de plantillas del objeto primario ID3DXFile.

La interfaz ID3DXFile se obtiene mediante una llamada a la función [**D3DXFileCreate**](d3dxfilecreate.md) .

El identificador único global (GUID) de la interfaz ID3DXFile es IID \_ ID3DXFile.

El tipo LPD3DXFILE se define como un puntero a la interfaz ID3DXFile.


```
typedef interface ID3DXFile *LPD3DXFILE;
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

 

 
