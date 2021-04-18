---
title: XTYP_XACT_COMPLETE transacción (ddeml. h)
description: Una función de devolución de llamada de cliente de Intercambio dinámico de datos (DDE), DdeCallback, recibe la \_ \_ transacción de transacciones completadas de XTYP cuando se ha completado una transacción asincrónica, iniciada por una llamada a la función DdeClientTransaction.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- Intercambio de datos de transacciones XTYP_XACT_COMPLETE
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685918"
---
# <a name="xtyp_xact_complete-transaction"></a>\_ \_ Transacción completa XTYP Xact

Una función de devolución de llamada de cliente de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción de transacciones **\_ \_ completadas de XTYP** cuando se ha completado una transacción asincrónica, iniciada por una llamada a la función [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uType* 
</dt> <dd>

El tipo de transacción.

</dd> <dt>

*uFmt* 
</dt> <dd>

El formato de los datos asociados a la transacción completada (si es aplicable) o **null** si no se intercambiaron datos durante la transacción.

</dd> <dt>

*hconv* 
</dt> <dd>

Identificador de la conversación.

</dd> <dt>

*hsz1* 
</dt> <dd>

Identificador del nombre de tema implicado en la transacción completada.

</dd> <dt>

*hsz2* 
</dt> <dd>

Identificador del nombre de elemento implicado en la transacción completada.

</dd> <dt>

*hdata* 
</dt> <dd>

Identificador de los datos implicados en la transacción completada, si procede. Si la transacción se realizó correctamente pero no implicaba ningún dato, este parámetro es **true**. Este parámetro es **null** si la transacción no se ha realizado correctamente.

</dd> <dt>

*dwData1* 
</dt> <dd>

Identificador de transacción de la transacción completada.

</dd> <dt>

*dwData2* 
</dt> <dd>

Cualquier marca de estado **DDE \_** aplicable en la palabra baja. Este parámetro proporciona compatibilidad con aplicaciones que dependen de los bits **\_ APPSTATUS de DDE** . Se recomienda que las aplicaciones dejen de usar estos bits, ya que es posible que no se admitan en versiones futuras de DDEML.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una aplicación no debe liberar el identificador de datos obtenido durante esta transacción. Sin embargo, una aplicación debe copiar los datos asociados al identificador de datos si la aplicación debe procesar los datos después de que se devuelva la función de devolución de llamada. Una aplicación puede usar la función [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar los datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Ddeml. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

