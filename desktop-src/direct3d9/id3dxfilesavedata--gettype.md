---
description: Recupera el identificador de plantilla de este nodo de datos de archivo.
ms.assetid: ff0662da-b4f8-4ed2-81d4-6771e91da262
title: Método ID3DXFileSaveData::GetType (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ec0dddd2106acddc5d09354ba7919eb32a8217a115410a9830803aaae589c891
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987435"
---
# <a name="id3dxfilesavedatagettype-method"></a>Método ID3DXFileSaveData::GetType

Recupera el identificador de plantilla de este nodo de datos de archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetType(
  [in] GUID *type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* \[ En\]
</dt> <dd>

Tipo: **[ **GUID**](guid.md)\***

Puntero al GUID que representa la plantilla en este nodo de datos de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




