---
description: La función PdhVbGetDoubleCounterValue devuelve el valor actual del contador especificado como un valor de punto flotante de precisión doble.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: Función PdhVbGetDoubleCounterValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476657"
---
# <a name="pdhvbgetdoublecountervalue-function"></a>Función PdhVbGetDoubleCounterValue

La **función PdhVbGetDoubleCounterValue** devuelve el valor actual del contador especificado como un valor de punto flotante de precisión doble. Debe comprobar *CounterStatus antes* de usar el número devuelto, ya que es posible que el contador no sea válido cuando se lee. Para comprobar el estado del contador, llame a la [**función PdhVbIsStatusStatus.**](pdhvbisgoodstatus.md)

> [!IMPORTANT]
> La función que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbGetDoubleCounterValue( \_ ByVal CounterHandle As Long, \_ ByVal CounterStatus as Long \_ ) as Double

## <a name="parameters"></a>Parámetros

<dl> <dt>

*CounterHandle* 
</dt> <dd>

Identificador del contador cuyo valor actual se va a leer.

</dd> <dt>

*CounterStatus* 
</dt> <dd>

Variable en la que el estado actual del valor del contador se devuelve al autor de la llamada. El valor de datos devuelto es válido si y solo si el valor devuelto en CounterStatus es PDH CSTATUS VALID DATA o \_ \_ \_ PDH \_ CSTATUS NEW DATA (vea Códigos de error de \_ \_ PDH). Si el valor devuelto en CounterStatus es cualquier otro valor, no use los datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el valor de punto flotante de precisión doble del contador actual, calculado y con formato definido por el tipo de contador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhVbIsStatus**](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




