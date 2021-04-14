---
description: La función ParserTemporaryLockFrame bloquea un marco cuando entra en un analizador y desbloquea el marco cuando la función sale del analizador.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: Función ParserTemporaryLockFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 48fa646e709982d88093e0cbeb5e60375643351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668407"
---
# <a name="parsertemporarylockframe-function"></a>ParserTemporaryLockFrame función)

La función **ParserTemporaryLockFrame** bloquea un marco cuando entra en un analizador y desbloquea el marco cuando la función sale del analizador.

## <a name="syntax"></a>Sintaxis


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador del marco al que apunta el analizador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero al primer byte de datos del marco.

Si la función no se realiza correctamente, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

Los analizadores no deben llamar a la función **LockFrame** . Si un analizador toma un bloqueo y, a continuación, genera un error o devuelve sin desbloquear el fotograma, el analizador deja el sistema en un estado en el que no puede cambiar los protocolos ni cortar o copiar fotogramas. Los analizadores deben usar la función **ParserTemporaryLockFrame** , que concede un bloqueo solo durante el contexto de la entrada de función en el analizador. Al salir del analizador, se libera el bloqueo para ese marco. Como resultado, el puntero será válido solo después de que el analizador vuelva de la llamada a la función **AttachProperties** o **RecognizeFrame** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




