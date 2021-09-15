---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileDataReference para admitir objetos de referencia de datos.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Interfaz IDirectXFileDataReference (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466055"
---
# <a name="idirectxfiledatareference-interface"></a>IDirectXFileDataReference (interfaz)

Las aplicaciones usan los métodos de la interfaz IDirectXFileDataReference para admitir objetos de referencia de datos. Un objeto de referencia de datos hace referencia a un objeto de datos definido anteriormente en el archivo. Esto le permite usar el mismo objeto varias veces sin repetirlo en el archivo. En desuso.

## <a name="members"></a>Members

La **interfaz IDirectXFileDataReference** hereda de [**IDirectXFileObject.**](idirectxfileobject.md) **IDirectXFileDataReference** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDirectXFileDataReference** tiene estos métodos.



| Método                                                | Descripción                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [**Resolver**](idirectxfiledatareference--resolve.md) | Resuelve las referencias de datos. En desuso.<br/> |



 

## <a name="remarks"></a>Observaciones

Después de determinar que un objeto es un objeto de referencia de datos, use el método [**IDirectXFileDataReference::Resolve**](idirectxfiledatareference--resolve.md) para recuperar el objeto al que se hace referencia definido anteriormente en el archivo. Para obtener información sobre cómo identificar un objeto de referencia de datos, vea la [**interfaz IDirectXFileData.**](idirectxfiledata.md)

El GUID de la interfaz IDirectXFileDataReference es IID \_ IDirectXFileDataReference.

El tipo LPDIRECTXFILEDataReference se define como un puntero a esta interfaz.


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[Interfaces de archivo X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




