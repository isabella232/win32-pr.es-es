---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileBinary para leer y recuperar información sobre los datos binarios. En desuso.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Interfaz IDirectXFileBinary (DXFile. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280282"
---
# <a name="idirectxfilebinary-interface"></a>Interfaz IDirectXFileBinary

Las aplicaciones usan los métodos de la interfaz IDirectXFileBinary para leer y recuperar información sobre los datos binarios. En desuso.

## <a name="members"></a>Miembros

La interfaz **IDirectXFileBinary** hereda de [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileBinary** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDirectXFileBinary** tiene estos métodos.



| Método                                                 | Descripción                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetMimeType**](idirectxfilebinary--getmimetype.md) | Recupera el tipo de extensiones multipropósito de correo Internet (MIME) para los datos binarios. En desuso.<br/> |
| [**GetSize (**](idirectxfilebinary--getsize.md)         | Recupera el tamaño de los datos binarios. En desuso.<br/>                                               |
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
| Encabezado<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[Interfaces de archivo X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




