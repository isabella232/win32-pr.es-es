---
description: La función BERGetHeader descodifica un encabezado de elección.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Función BERGetHeader (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d6dfd50856202e78177d2ad259b16638f466d9bca236a691c65802ce2758c948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012323"
---
# <a name="bergetheader-function"></a>Función BERGetHeader

La **función BERGetHeader** descodifica un encabezado de elección.

## <a name="syntax"></a>Sintaxis


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

Puntero al encabezado de elección.

</dd> <dt>

*pTag* 
</dt> <dd>

Puntero a la etiqueta devuelta.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Puntero a la longitud de encabezado devuelta.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Puntero a la longitud de datos devuelta.

</dd> <dt>

*ppNext* 
</dt> <dd>

Puntero al contenido del encabezado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (es decir, se encuentra un encabezado de opción BER válido), el valor devuelto es **TRUE.**

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




