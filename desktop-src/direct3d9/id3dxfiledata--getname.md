---
description: Recupera el nombre de este objeto de datos de archivo.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: Método ID3DXFileData::GetName (D3DX9Xof.h)
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
ms.openlocfilehash: f98e20d5bfa5efdb756e414808cda2506fda56fdf417f54b658f17d0b5c9658b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847935"
---
# <a name="id3dxfiledatagetname-method"></a>Método ID3DXFileData::GetName

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

*szName* \[ En\]
</dt> <dd>

Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**

Dirección de un puntero para recibir el nombre de este objeto de datos de archivo. Si este parámetro es **NULL,** puiSize devolverá el tamaño de la cadena. Si szName apunta a una memoria válida, el nombre de este objeto de datos de archivo se copiará en szName hasta el número de caracteres especificado por puiSize.

</dd> <dt>

*puiSize* \[ in, out\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Puntero al tamaño de la cadena que representa el nombre de este objeto de datos de archivo. Este parámetro puede ser **NULL si** szName proporciona una referencia al nombre. Este parámetro devolverá el tamaño de la cadena si szName es **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Comentarios

Para que este método se haga correctamente, szName o *puiSize* deben ser distintos de **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
