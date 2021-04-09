---
description: Recupera el GUID de este objeto de datos de archivo.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: 'ID3DXFileData:: GetId (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1dafb296541b1702e9163dcc6d460cf149b4007
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821218"
---
# <a name="id3dxfiledatagetid-method"></a>ID3DXFileData:: GetId (método)

Recupera el GUID de este objeto de datos de archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pId* \[ de enuncia\]
</dt> <dd>

Tipo: **LPGUID**

Puntero a un GUID para recibir el identificador de este objeto de datos de archivo. Si el objeto de datos de archivo no tiene ningún identificador, el valor del parámetro devuelto será el GUID \_ null.

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

 

 




