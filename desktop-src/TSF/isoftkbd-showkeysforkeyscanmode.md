---
title: Método ISoftKbd ShowKeysForKeyScanMode (Softkbdc.h)
description: El método ISoftKbd ShowKeysForKeyScanMode muestra las teclas usadas para el modo de examen de claves para un teclado soft.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Método ShowKeysForKeyScanMode Text Services Framework
- Método ShowKeysForKeyScanMode Text Services Framework interfaz , ISoftKbd
- Interfaz ISoftKbd Text Services Framework método , ShowKeysForKeyScanMode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361800"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a>ISoftKbd::ShowKeysForKeyScanMode (método)

El **método ISoftKbd::ShowKeysForKeyScanMode** muestra las teclas usadas para el modo de examen de claves para un teclado flexible.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpKeyID* \[ En\]
</dt> <dd>

Puntero a una matriz de elementos KEYID que indica los identificadores de las claves que se mostrarán.

</dd> <dt>

*iKeyNum* \[ En\]
</dt> <dd>

Número de claves que se mostrarán.

</dd> <dt>

*fHighL* \[ En\]
</dt> <dd>

TRUE si el método va a resaltar las claves y **FALSE** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Método realizado correctamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno de los parámetros no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





