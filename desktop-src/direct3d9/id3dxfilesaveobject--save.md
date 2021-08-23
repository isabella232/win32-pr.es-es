---
description: Guarda un objeto de datos y sus secundarios en un archivo .x en el disco.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: Método ID3DXFileSaveObject::Save (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a49c4776f9ce590d287869436b329ddf9a378e73f04f0127246fc890944ffee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563965"
---
# <a name="id3dxfilesaveobjectsave-method"></a>Método ID3DXFileSaveObject::Save

Guarda un objeto de datos y sus secundarios en un archivo .x en el disco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser el siguiente: D3DXFERR \_ BADOBJECT.

## <a name="remarks"></a>Comentarios

Una vez que este método se realiza correctamente, ya no se puede llamar a [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData::AddDataObject::AddDataReference**](id3dxfilesavedata--adddataobject.md) hasta que se cree un nuevo objeto [**ID3DXFile.**](id3dxfile.md) [](id3dxfilesavedata--adddatareference.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




