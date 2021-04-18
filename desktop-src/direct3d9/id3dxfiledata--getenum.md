---
description: Recupera el objeto de enumeración en este objeto de datos de archivo.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: 'ID3DXFileData:: GetEnum (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7dd565f6f76d42159d77d8b83c638c75648f293b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718323"
---
# <a name="id3dxfiledatagetenum-method"></a>ID3DXFileData:: GetEnum (método)

Recupera el objeto de enumeración en este objeto de datos de archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppObj* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Dirección de un puntero para recibir el objeto de enumeración en este objeto de datos de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




