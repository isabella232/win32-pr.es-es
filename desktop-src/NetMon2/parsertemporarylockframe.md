---
description: La función ParserTemporaryLockFrame bloquea un fotograma cuando entra en un analizador y desbloquea el fotograma cuando la función sale del analizador.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: Función ParserTemporaryLockFrame (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074103"
---
# <a name="parsertemporarylockframe-function"></a>Función ParserTemporaryLockFrame

La **función ParserTemporaryLockFrame** bloquea un fotograma cuando entra en un analizador y desbloquea el fotograma cuando la función sale del analizador.

## <a name="syntax"></a>Sintaxis


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Controle el marco al que apunta el analizador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero al primer byte de datos del marco.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

Los analizadores no deben llamar a **la función LockFrame.** Si un analizador toma un bloqueo y, a continuación, genera un error o devuelve sin desbloquear el marco, el analizador deja el sistema en un estado en el que no puede cambiar los protocolos ni cortar o copiar fotogramas. Los analizadores deben usar la función **ParserTemporaryLockFrame,** que concede un bloqueo solo durante el contexto de la entrada de función en el analizador. Al salir del analizador, se libera el bloqueo de ese marco. Como resultado, el puntero solo será válido después de que el analizador vuelva de la llamada a la **función AttachProperties** **o RecognizeFrame.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




