---
title: XTYP_EXECUTE transacción (ddeml. h)
description: Un cliente usa la \_ transacción de ejecución XTYP para enviar una cadena de comandos al servidor. Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), DdeCallback, recibe esta transacción cuando un cliente especifica XTYP \_ Execute en la función DdeClientTransaction.
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- Intercambio de datos de transacciones XTYP_EXECUTE
topic_type:
- apiref
api_name:
- XTYP_EXECUTE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff08bfa60d07f3b8333f1de808359f77984cbba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079627"
---
# <a name="xtyp_execute-transaction"></a>XTYP \_ Ejecutar transacción

Un cliente usa la transacción de **\_ ejecución XTYP** para enviar una cadena de comandos al servidor. Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica **XTYP \_ Execute** en la función [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_EXECUTE            (0x0050 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uType* 
</dt> <dd>

El tipo de transacción.

</dd> <dt>

*uFmt* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*hconv* 
</dt> <dd>

Identificador de la conversación.

</dd> <dt>

*hsz1* 
</dt> <dd>

Identificador del nombre del tema.

</dd> <dt>

*hsz2* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*hdata* 
</dt> <dd>

Identificador de la cadena de comandos.

</dd> <dt>

*dwData1* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*dwData2* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una función de devolución de llamada de servidor debe devolver **DDE \_ Fack** si procesa esta transacción, **DDE \_ FBUSY** si está demasiado ocupado para procesar esta transacción o **\_ FNOTPROCESSED de DDE** si rechaza esta transacción.

## <a name="remarks"></a>Observaciones

Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ FAIL \_ executes** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Una aplicación debe liberar el identificador de datos obtenido durante esta transacción. Sin embargo, una aplicación debe copiar la cadena de comandos asociada al identificador de datos si la aplicación debe procesar la cadena después de que la función de devolución de llamada vuelva. Una aplicación puede usar la función [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar los datos.

Dado que la mayoría de las aplicaciones cliente esperan que una aplicación de servidor realice sincrónicamente una transacción de **\_ ejecución XTYP** , un servidor debe intentar realizar todo el procesamiento de la transacción de **\_ ejecución XTYP** desde la función de devolución de llamada DDE o devolviendo el código de retorno del **\_ bloque CBR** . Si el parámetro *hdata* es un comando que indica al servidor que finalice, el servidor debe hacerlo después de procesar la transacción **de \_ ejecución XTYP** .

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

