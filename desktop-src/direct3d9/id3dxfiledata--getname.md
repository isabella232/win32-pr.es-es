---
description: Recupera el nombre de este objeto de datos de archivo.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: 'ID3DXFileData:: GetName (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718322"
---
# <a name="id3dxfiledatagetname-method"></a>ID3DXFileData:: GetName (método)

Recupera el nombre de este objeto de datos de archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szName* \[ de\]
</dt> <dd>

Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**

Dirección de un puntero para recibir el nombre de este objeto de datos de archivo. Si este parámetro es **null**, puiSize devolverá el tamaño de la cadena. Si szName apunta a la memoria válida, el nombre de este objeto de datos de archivo se copiará en szName hasta el número de caracteres proporcionado por puiSize.

</dd> <dt>

*puiSize* \[ in, out\]
</dt> <dd>

Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)\***

Puntero al tamaño de la cadena que representa el nombre de este objeto de datos de archivo. Este parámetro puede ser **null** si szName proporciona una referencia al nombre. Este parámetro devolverá el tamaño de la cadena si szName es **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Observaciones

Para que este método se ejecute correctamente, szName o *puiSize* no deben ser **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
