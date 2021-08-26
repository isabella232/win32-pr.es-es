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
ms.openlocfilehash: 4507bed7a5f3f461c80b8eed1e5c07c15cfd34b7aab7a02c3e803a43a88ae132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095635"
---
# <a name="idirectxfiledatareference-interface"></a>IDirectXFileDataReference (interfaz)

Las aplicaciones usan los métodos de la interfaz IDirectXFileDataReference para admitir objetos de referencia de datos. Un objeto de referencia de datos hace referencia a un objeto de datos definido anteriormente en el archivo. Esto le permite usar el mismo objeto varias veces sin repetirlo en el archivo. En desuso.

## <a name="members"></a>Miembros

La **interfaz IDirectXFileDataReference** hereda de [**IDirectXFileObject.**](idirectxfileobject.md) **IDirectXFileDataReference** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDirectXFileDataReference** tiene estos métodos.



| Método                                                | Descripción                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [**Resolver**](idirectxfiledatareference--resolve.md) | Resuelve las referencias de datos. En desuso.<br/> |



 

## <a name="remarks"></a>Comentarios

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

 

 




