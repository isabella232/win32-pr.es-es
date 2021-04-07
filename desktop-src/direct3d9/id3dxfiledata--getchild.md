---
description: Recupera un objeto secundario en este objeto de datos de archivo.
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: 'ID3DXFileData:: GetChild (método) (D3DX9Xof. h)'
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
ms.openlocfilehash: 37982ca1e4801b7d70bec503ff9510fc66772651
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003876"
---
# <a name="id3dxfiledatagetchild-method"></a>ID3DXFileData:: GetChild (método)

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

*uiChild* \[ de\]
</dt> <dd>

Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**

IDENTIFICADOR del objeto secundario que se va a recuperar.

</dd> <dt>

*ppChild* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Dirección de un puntero para recibir el puntero de interfaz del objeto secundario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
