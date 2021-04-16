---
description: La función RegCreateBlobKey almacena un BLOB en la clave del registro especificada.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Función RegCreateBlobKey (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678514"
---
# <a name="regcreateblobkey-function"></a>RegCreateBlobKey función)

La función **RegCreateBlobKey** almacena un BLOB en la clave del registro especificada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HKEY* \[ enuncia\]
</dt> <dd>

Identificador de la clave del registro donde se almacenará el BLOB.

</dd> <dt>

*szBlobName* \[ de\]
</dt> <dd>

Nombre (definido por la aplicación) que representa el BLOB en el registro.

</dd> <dt>

*hBlob* \[ de\]
</dt> <dd>

Identificador del BLOB que se guarda.

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

[RegOpenBlobKey](regopenblobkey.md)
</dt> </dl>

 

 




