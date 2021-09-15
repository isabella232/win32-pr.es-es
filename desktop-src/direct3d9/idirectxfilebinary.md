---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileBinary para leer y recuperar información sobre datos binarios. En desuso.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Interfaz IDirectXFileBinary (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: b6707e4e685289f16b85ab85c2cce13dcd1da962
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466065"
---
# <a name="idirectxfilebinary-interface"></a>IDirectXFileBinary (interfaz)

Las aplicaciones usan los métodos de la interfaz IDirectXFileBinary para leer y recuperar información sobre datos binarios. En desuso.

## <a name="members"></a>Members

La **interfaz IDirectXFileBinary** hereda de [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileBinary** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDirectXFileBinary** tiene estos métodos.



| Método                                                 | Descripción                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetMimeType**](idirectxfilebinary--getmimetype.md) | Recupera el tipo de extensiones multipropósito de Correo electrónico de Internet (MIME) para los datos binarios. En desuso.<br/> |
| [**GetSize**](idirectxfilebinary--getsize.md)         | Recupera el tamaño de los datos binarios. En desuso.<br/>                                               |
| [**Lectura**](idirectxfilebinary--read.md)               | Lee los datos binarios. En desuso.<br/>                                                               |



 

## <a name="remarks"></a>Observaciones

El GUID de la interfaz IDirectXFileBinary es IID \_ IDirectXFileBinary.

El tipo LPDIRECTXFileBinary se define como un puntero a esta interfaz.


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
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

 

 




