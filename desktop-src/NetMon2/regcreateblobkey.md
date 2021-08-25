---
description: La función RegCreateBlobKey almacena un BLOB en la clave del Registro determinada.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Función RegCreateBlobKey (Netmon.h)
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
ms.openlocfilehash: 3267fd0ba5e6fe56b99b5d465f69718fe5509a7ead58acf1d8dafb642397af5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889655"
---
# <a name="regcreateblobkey-function"></a>Función RegCreateBlobKey

La **función RegCreateBlobKey** almacena un BLOB en la clave del Registro determinada.

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

*hkey* \[ out\]
</dt> <dd>

Identificador de la clave del Registro donde se almacenará el BLOB.

</dd> <dt>

*szBlobName* \[ En\]
</dt> <dd>

Nombre (aplicación definida) que representa el BLOB en el Registro.

</dd> <dt>

*hBlob* \[ En\]
</dt> <dd>

Controle el BLOB que se guarda.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[RegOpenBlobKey](regopenblobkey.md)
</dt> </dl>

 

 




