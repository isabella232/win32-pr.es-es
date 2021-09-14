---
description: La función RegOpenBlobKey recupera un BLOB almacenado en la clave del Registro dada.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Función RegOpenBlobKey (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074093"
---
# <a name="regopenblobkey-function"></a>Función RegOpenBlobKey

La **función RegOpenBlobKey** recupera un BLOB almacenado en la clave del Registro dada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hkey* \[ En\]
</dt> <dd>

Identificador de la clave del Registro que contiene el BLOB.

</dd> <dt>

*szBlobName* \[ En\]
</dt> <dd>

Nombre que identifica el BLOB especificado en el Registro.

</dd> <dt>

*phBlob* \[ out\]
</dt> <dd>

Puntero al BLOB que se recupera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un valor NMERR que indica el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[RegCreateBlobKey](regcreateblobkey.md)
</dt> </dl>

 

 




