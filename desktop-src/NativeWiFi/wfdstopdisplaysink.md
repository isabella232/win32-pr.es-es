---
description: Detiene el Miracast receptor, desactiva la detectabilidad y des registra la devolución de llamada.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: Función WFDDisplaySinkStop (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: a5e2da91e29535c1e2fd9553a2b6ec2bb0008e61f33cd55ebcda2746b93eb657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797935"
---
# <a name="wfddisplaysinkstop-function"></a>Función WFDDisplaySinkStop

Detiene el Miracast receptor, desactiva la detectabilidad y des registra la devolución de llamada. La aplicación debe llamar a esto una vez en el apagado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

## <a name="remarks"></a>Comentarios

Se espera que la aplicación haya desbloqueado las devoluciones de llamada en curso antes de llamar a **WFDStopDisplaySink.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 10<br/>                                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2016<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wifidisplay.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




