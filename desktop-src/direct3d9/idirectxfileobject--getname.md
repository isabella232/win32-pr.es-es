---
description: Recupera un puntero al nombre de un objeto de archivo DirectX. En desuso.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: Método IDirectXFileObject::GetName (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e67381a26e3d0f1031e282d6530562416919e8cf52800a07301bf18820887828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846955"
---
# <a name="idirectxfileobjectgetname-method"></a>IDirectXFileObject::GetName (método)

Recupera un puntero al nombre de un objeto de archivo DirectX. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pstrNameBuf* \[ out\]
</dt> <dd>

Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**

Puntero al búfer en el que se copiará el nombre del objeto de archivo DirectX. Se establece **en NULL** si solo se necesita la longitud del búfer.

</dd> <dt>

*pdwBufLen* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Puntero a un DWORD que especifica la longitud del búfer al que apunta pstrNameBuf. El valor del parámetro pdwBufLen se modificará a la longitud del búfer necesaria para contener el nombre del objeto incluso si pstrNameBuf es **NULL.** En cualquier caso, la función devolverá DXFILEERR BADVALUE si el valor original de pdwBufLen no es tan grande como o mayor que la longitud necesaria para contener el nombre del \_ objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes valores. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 
