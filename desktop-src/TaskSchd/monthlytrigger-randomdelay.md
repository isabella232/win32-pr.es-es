---
title: MonthlyTrigger.RandomDelay, propiedad
description: Para el scripting, obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. | MonthlyTrigger.RandomDelay, propiedad
ms.assetid: 5334356f-fef1-4d0e-9879-6ec996b75dff
keywords:
- Propiedad RandomDelay Programador de tareas
- Propiedad RandomDelay Programador de tareas objeto , MonthlyTrigger
- Objeto MonthlyTrigger Programador de tareas , propiedad RandomDelay
topic_type:
- apiref
api_name:
- MonthlyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7f5c3a1831681cca2b3dc006ffb7a7d44a7a6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170666"
---
# <a name="monthlytriggerrandomdelay-property"></a>MonthlyTrigger.RandomDelay, propiedad

Para el scripting, obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.

## <a name="syntax"></a>Sintaxis


```VB
MonthlyTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valor de propiedad

Tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, P2DT5S es un retraso de 2 días y 5 segundos).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MonthlyTrigger**](monthlytrigger.md)
</dt> </dl>

 

 





