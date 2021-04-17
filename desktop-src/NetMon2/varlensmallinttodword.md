---
description: La función VarLenSmallIntToDword convierte un entero pequeño de longitud variable en un valor DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Función VarLenSmallIntToDword (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677669"
---
# <a name="varlensmallinttodword-function"></a>VarLenSmallIntToDword función)

La función **VarLenSmallIntToDword** convierte un entero pequeño de longitud variable en un **valor DWORD**.

## <a name="syntax"></a>Sintaxis


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pValue* 
</dt> <dd>

Puntero al entero pequeño de longitud variable.

</dd> <dt>

*ValueLen* 
</dt> <dd>

Longitud (en bytes) del entero pequeño de longitud variable.

</dd> <dt>

*fIsByteswapped* 
</dt> <dd>

Marca que indica si el entero de longitud variable pequeño es un intercambio de bytes.

</dd> <dt>

*lpDword* 
</dt> <dd>

**DWORD** en la que se convierte el entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un puntero a la **DWORD**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Analizador. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




