---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileObject para recuperar información sobre los objetos de archivo de Microsoft DirectX. En desuso.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Interfaz IDirectXFileObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689874"
---
# <a name="idirectxfileobject-interface"></a>Interfaz IDirectXFileObject

Las aplicaciones usan los métodos de la interfaz IDirectXFileObject para recuperar información sobre los objetos de archivo de Microsoft DirectX. En desuso.

## <a name="members"></a>Miembros

La interfaz **IDirectXFileObject** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFileObject** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDirectXFileObject** tiene estos métodos.



| Método                                         | Descripción                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetId**](idirectxfileobject--getid.md)     | Recupera un puntero al GUID que identifica un objeto de archivo de DirectX. En desuso.<br/> |
| [**GetName**](idirectxfileobject--getname.md) | Recupera un puntero al nombre de un objeto de archivo de DirectX. En desuso.<br/>                   |



 

## <a name="remarks"></a>Observaciones

El GUID de la interfaz IDirectXFileObject es IID \_ IDirectXFileObject.

El tipo LPDIRECTXFILEOBJECT se define como un puntero a esta interfaz.


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de archivo X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
