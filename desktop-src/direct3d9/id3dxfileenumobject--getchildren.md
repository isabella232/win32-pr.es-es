---
description: Recupera el número de objetos secundarios de este objeto de datos de archivo.
ms.assetid: 4409819f-a346-40b1-8e12-86e8128ece47
title: 'ID3DXFileEnumObject:: GetChildren (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cafa79844e89602d3b88756e04ca460f611516dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821207"
---
# <a name="id3dxfileenumobjectgetchildren-method"></a>ID3DXFileEnumObject:: GetChildren (método)

Recupera el número de objetos secundarios de este objeto de datos de archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*puiChildren* \[ de\]
</dt> <dd>

Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)\***

Dirección de un puntero para recibir el número de objetos secundarios en este objeto de datos de archivo.

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

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
