---
description: Recupera un puntero al nombre de un objeto de archivo de DirectX. En desuso.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'IDirectXFileObject:: GetName (método) (DXFile. h)'
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
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689875"
---
# <a name="idirectxfileobjectgetname-method"></a>IDirectXFileObject:: GetName (método)

Recupera un puntero al nombre de un objeto de archivo de DirectX. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pstrNameBuf* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**

Puntero al búfer en el que se copiará el nombre del objeto de archivo de DirectX. Establezca en **null** si solo se necesita la longitud del búfer.

</dd> <dt>

*pdwBufLen* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Puntero a un valor DWORD que especifica la longitud del búfer al que apunta pstrNameBuf. El valor del parámetro pdwBufLen se modificará en la longitud del búfer necesaria para contener el nombre del objeto aunque pstrNameBuf sea **null**. En cualquier caso, la función devolverá DXFILEERR \_ BADVALUE si el valor original de pdwBufLen no es tan grande como o mayor que la longitud necesaria para contener el nombre del objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 
