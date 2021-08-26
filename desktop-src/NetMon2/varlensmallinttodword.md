---
description: La función VarLenSmallIntToDword convierte un entero pequeño de longitud variable en DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Función VarLenSmallIntToDword (Netmon.h)
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
ms.openlocfilehash: ffec440adc903ddb9a5157e8e5f36037e092f0c4bf0cd52da79b0839220366ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962735"
---
# <a name="varlensmallinttodword-function"></a>Función VarLenSmallIntToDword

La **función VarLenSmallIntToDword** convierte un entero pequeño de longitud variable en **DWORD.**

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

Longitud (en bytes) del entero pequeño de longitud variable .

</dd> <dt>

*fIsByteswapped* 
</dt> <dd>

Marca que indica si el entero pequeño de longitud variable se intercambia en bytes.

</dd> <dt>

*lpDword* 
</dt> <dd>

DWORD **al** que se convierte el entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un puntero a **DWORD.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




