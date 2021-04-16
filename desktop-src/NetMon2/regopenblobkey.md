---
description: La función RegOpenBlobKey recupera un BLOB almacenado en la clave del registro especificada.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Función RegOpenBlobKey (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678513"
---
# <a name="regopenblobkey-function"></a>RegOpenBlobKey función)

La función **RegOpenBlobKey** recupera un BLOB almacenado en la clave del registro especificada.

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

*HKEY* \[ de\]
</dt> <dd>

Identificador de la clave del registro que contiene el BLOB.

</dd> <dt>

*szBlobName* \[ de\]
</dt> <dd>

Nombre que identifica el BLOB especificado en el registro.

</dd> <dt>

*phBlob* \[ enuncia\]
</dt> <dd>

Puntero al BLOB que se recupera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[RegCreateBlobKey](regcreateblobkey.md)
</dt> </dl>

 

 




