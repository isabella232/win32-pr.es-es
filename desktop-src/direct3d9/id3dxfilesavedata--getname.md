---
description: Recupera el nombre de este nodo de datos de archivo ID3DXFileSaveData.
ms.assetid: ea697d23-42e7-4661-b605-3654f6a31055
title: Método ID3DXFileSaveData::GetName (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00fa8c60f423343d3d4c594d31141a2f192802d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888457"
---
# <a name="id3dxfilesavedatagetname-method"></a>Método ID3DXFileSaveData::GetName

Recupera el nombre de este nodo de datos [**de archivo ID3DXFileSaveData.**](id3dxfilesavedata.md)

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

Dirección de un puntero para recibir el nombre de este nodo de datos de archivo. Si este parámetro es **NULL,** *puiSize* devolverá el tamaño de la cadena. Si szName apunta a una memoria válida, el nombre de este nodo de datos de archivo se copiará en szName hasta el número de caracteres especificado por *puiSize* .

</dd> <dt>

*puiSize* \[ in, out\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Puntero al tamaño de la cadena que representa el nombre de este nodo de datos de archivo. Este parámetro puede ser **NULL si** szName proporciona una referencia al nombre. Este parámetro devolverá el tamaño de la cadena si szName es **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el siguiente valor: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Observaciones

Para que este método se haga correctamente, *szName* o *puiSize* deben ser distintos de **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
