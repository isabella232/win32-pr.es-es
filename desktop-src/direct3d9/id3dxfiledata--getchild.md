---
description: 'Método ID3DXFileData::GetChild: recupera un objeto secundario en este objeto de datos de archivo.'
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: Método ID3DXFileData::GetChild (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7fe6c0393e5cfb9ed8aeaf5808d33175e7f9bfe5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090383"
---
# <a name="id3dxfiledatagetchild-method"></a>Método ID3DXFileData::GetChild

Recupera un objeto secundario en este objeto de datos de archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uiChild* \[ En\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Identificador del objeto secundario que se recuperará.

</dd> <dt>

*ppChild* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Dirección de un puntero para recibir el puntero de interfaz del objeto secundario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes valores: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
