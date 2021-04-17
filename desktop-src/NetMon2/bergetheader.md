---
description: La función BERGetHeader descodifica un encabezado Choice.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Función BERGetHeader (Netmon. h)
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
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677739"
---
# <a name="bergetheader-function"></a>BERGetHeader función)

La función **BERGetHeader** descodifica un encabezado Choice.

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

Puntero al encabezado Choice.

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

Si la función es correcta (es decir, se encuentra un encabezado de opción BER válido), el valor devuelto es **true**.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Analizador. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




