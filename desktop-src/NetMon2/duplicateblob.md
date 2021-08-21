---
description: La función DuplicateBlob copia un BLOB específico.
ms.assetid: d2478f53-328c-4799-890c-7849ce1f22e9
title: Función DuplicateBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DuplicateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a8fd41bff4700915c43ab709efa0033905cc5895c81839d399f81fc7bc4317e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064105"
---
# <a name="duplicateblob-function"></a>Función DuplicateBlob

La **función DuplicateBlob** copia un BLOB específico.

## <a name="syntax"></a>Sintaxis


```C++
DWORD DuplicateBlob(
  _In_  HBLOB hSrcBlob,
  _Out_ HBLOB *hBlobThatWillBeCreated
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSrcBlob* \[ En\]
</dt> <dd>

Identificador del BLOB que se copia.

</dd> <dt>

*hBlobThatWillBeCreated* \[ out\]
</dt> <dd>

Controle el blob duplicado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un valor NMERR que describe el error.

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

[CreateBlob](createblob.md)
</dt> <dt>

[DestroyBlob](destroyblob.md)
</dt> </dl>

 

 




