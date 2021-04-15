---
description: Recupera el identificador de plantilla en este objeto de datos de archivo.
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'ID3DXFileData:: GetType (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 566052c06d5f7e55629a26442dd774a2f80fd647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424456"
---
# <a name="id3dxfiledatagettype-method"></a>ID3DXFileData:: GetType (método)

Recupera el identificador de plantilla en este objeto de datos de archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pType* \[ de\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Puntero al GUID que representa la plantilla en este objeto de datos de archivo.

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

 

 




