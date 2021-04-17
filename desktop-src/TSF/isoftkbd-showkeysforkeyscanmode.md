---
title: Método ISoftKbd ShowKeysForKeyScanMode (Softkbdc. h)
description: El método ISoftKbd ShowKeysForKeyScanMode muestra las teclas utilizadas para el modo de exploración de teclas para un teclado en pantalla.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Método ShowKeysForKeyScanMode marco de trabajo de servicios de texto
- Método ShowKeysForKeyScanMode marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método ShowKeysForKeyScanMode
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492095"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a>ISoftKbd:: ShowKeysForKeyScanMode (método)

El método **ISoftKbd:: ShowKeysForKeyScanMode** muestra las teclas utilizadas para el modo de exploración de teclas para un teclado en pantalla.

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

*lpKeyID* \[ de\]
</dt> <dd>

Puntero a una matriz de elementos de clave de tipo que indica los identificadores de las claves que se van a mostrar.

</dd> <dt>

*iKeyNum* \[ de\]
</dt> <dd>

Número de claves que se van a mostrar.

</dd> <dt>

*fHighL* \[ de\]
</dt> <dd>

TRUE si el método va a resaltar las claves y **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno de los parámetros no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





