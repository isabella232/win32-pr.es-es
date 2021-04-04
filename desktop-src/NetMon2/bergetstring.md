---
description: La función BERGetString descodifica una cadena codificada en BER.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: Función BERGetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909422"
---
# <a name="bergetstring-function"></a>BERGetString función)

La función **BERGetString** descodifica una cadena codificada en BER.

## <a name="syntax"></a>Sintaxis


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

Puntero a la cadena descodificada.

</dd> <dt>

*ppValuePointer* 
</dt> <dd>

Puntero al puntero de la cadena descodificada.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Puntero a la longitud de encabezado devuelta.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Puntero a la longitud de la cadena.

</dd> <dt>

*ppNext* 
</dt> <dd>

Puntero al puntero de la siguiente entrada de BER.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (es decir, si se descodifica una cadena con codificación BER válida), el valor devuelto es **true**.

Si la función no es correcta, el valor devuelto es **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Analizador. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




