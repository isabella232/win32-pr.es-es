---
description: La función PdhVbGetDoubleCounterValue devuelve el valor actual del contador especificado como un valor de punto flotante de precisión doble.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: PdhVbGetDoubleCounterValue función)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360701"
---
# <a name="pdhvbgetdoublecountervalue-function"></a>PdhVbGetDoubleCounterValue función)

La función **PdhVbGetDoubleCounterValue** devuelve el valor actual del contador especificado como un valor de punto flotante de precisión doble. Debe comprobar la *contracondición* antes de usar el número devuelto, ya que es posible que el contador no sea válido cuando se lea. Para comprobar el estado del contador, llame a la función [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) .

> [!IMPORTANT]
> La función que se describe en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbGetDoubleCounterValue ( \_ ByVal Contrahandle as Long, \_ ByVal perstatus as Long \_ ) as Double

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Control de contracargo* 
</dt> <dd>

IDENTIFICADOR del contador cuyo valor actual se va a leer.

</dd> <dt>

*ContraEstado* 
</dt> <dd>

Variable en la que el estado actual del valor del contador se devuelve al autor de la llamada. El valor de los datos devueltos es válido si y solo si el valor devuelto en el estado de los datos es PDH \_ CSTATUS válido o los datos de \_ \_ PDH \_ CSTATUS \_ nuevos \_ (vea códigos de error de PDH). Si el valor devuelto en contrastatus es cualquier otro valor, no use los datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el valor de punto flotante de precisión doble del contador actual, calculado y con formato tal y como se define en el tipo de contador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




