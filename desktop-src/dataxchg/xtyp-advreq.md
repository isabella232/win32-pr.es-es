---
title: XTYP_ADVREQ transacción (Ddeml.h)
description: La transacción XTYP AD FTPQ informa al servidor de que hay una transacción de aviso pendiente en el par de nombre de tema y nombre de elemento especificado y que los datos correspondientes al nombre del tema y al par de nombres de elemento han \_ cambiado.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- XTYP_ADVREQ transacciones De datos Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2884e838268342ab10c556c6ae3cfc8349ed5d2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465770"
---
# <a name="xtyp_advreq-transaction"></a>Transacción \_ de XTYP AD ESTAQ

La transacción **\_ XTYP AD FTPQ** informa al servidor de que hay una transacción de aviso pendiente en el par de nombre de tema y nombre de elemento especificado y que los datos correspondientes al nombre del tema y al par de nombres de elemento han cambiado. El sistema envía esta transacción a la función de devolución de llamada datos dinámicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), después de que el servidor llame a la función [**DdePostAdvise.**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uType* 
</dt> <dd>

El tipo de transacción.

</dd> <dt>

*uFmt* 
</dt> <dd>

Formato en el que se deben enviar los datos al cliente.

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

Identificador del nombre del elemento que ha cambiado.

</dd> <dt>

*hdata* 
</dt> <dd>

No se usa.

</dd> <dt>

*dwData1* 
</dt> <dd>

El recuento, en la palabra de orden bajo, de las transacciones **\_ adjetivo XTYP** que permanecen para procesarse en el mismo tema, elemento y nombre de formato establecidos en el contexto de la llamada actual a la función [**DdePostAdvise.**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) El recuento es cero si la transacción **\_ adverso XTYP** actual es la última. Un servidor puede usar este recuento para determinar si se va a crear un identificador de datos **\_ APPOWNED** de HDATA para los datos de asesoramiento.

La palabra de orden bajo se establece en **CADV \_ LATEACK** si la DDEML emitió la transacción **\_ ADBIZQ de XTYP** debido a un mensaje DDE ACK de llegada tardía de un cliente que el servidor ha \_ sobrepasado.

No se usa la palabra de orden superior.

</dd> <dt>

*dwData2* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El servidor debe llamar primero a la función [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) para crear un identificador de datos que identifique los datos modificados y, a continuación, devolver el identificador. El servidor debe devolver **NULL** si no puede completar la transacción.

## <a name="remarks"></a>Observaciones

Un servidor no puede bloquear este tipo de transacción; Se omite el código de retorno **\_ CBR BLOCK.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Ddeml.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Conceptual**
</dt> <dt>

[datos dinámicos Exchange management library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

