---
description: Las aplicaciones usan los métodos de la interfaz ID3DXFileData para compilar o tener acceso a la jerarquía inmediata del objeto de datos. Las restricciones de las plantillas determinan la jerarquía.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: Interfaz ID3DXFileData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280402"
---
# <a name="id3dxfiledata-interface"></a>Interfaz ID3DXFileData

Las aplicaciones usan los métodos de la interfaz ID3DXFileData para compilar o tener acceso a la jerarquía inmediata del objeto de datos. Las restricciones de las plantillas determinan la jerarquía.

## <a name="members"></a>Miembros

La interfaz **ID3DXFileData** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileData** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXFileData** tiene estos métodos.



| Método                                            | Descripción                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetChild**](id3dxfiledata--getchild.md)       | Recupera un objeto secundario en este objeto de datos de archivo.<br/>                                                        |
| [**GetChildren**](id3dxfiledata--getchildren.md) | Recupera el número de elementos secundarios de este objeto de datos de archivo.<br/>                                                |
| [**GetEnum**](id3dxfiledata--getenum.md)         | Recupera el objeto de enumeración en este objeto de datos de archivo.<br/>                                                |
| [**GetId**](id3dxfiledata--getid.md)             | Recupera el GUID de este objeto de datos de archivo.<br/>                                                              |
| [**GetName**](id3dxfiledata--getname.md)         | Recupera el nombre de este objeto de datos de archivo.<br/>                                                              |
| [**GetType**](id3dxfiledata--gettype.md)         | Recupera el identificador de plantilla en este objeto de datos de archivo.<br/>                                                       |
| [**IsReference**](id3dxfiledata--isreference.md) | Indica si este objeto de datos de archivo es un objeto de referencia que apunta a otro objeto de datos secundario.<br/>   |
| [**Lock**](id3dxfiledata--lock.md)               | Obtiene acceso a los datos del archivo. x.<br/>                                                                                |
| [**Pulsa**](id3dxfiledata--unlock.md)           | Finaliza la duración del puntero *ppData* devuelto por [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).<br/> |



 

## <a name="remarks"></a>Observaciones

Los tipos de datos permitidos por la plantilla se denominan miembros opcionales. Los miembros opcionales no son necesarios, pero es posible que un objeto pierda información importante sin ellos. Estos miembros opcionales se guardan como elementos secundarios del objeto de datos. Un elemento secundario puede ser otro objeto de datos o una referencia a un objeto de datos anterior.

El GUID de la interfaz ID3DXFileData es IID \_ ID3DXFileData.

El tipo LPD3DXFILEDATA se define como un puntero a esta interfaz.


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
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

 

 
