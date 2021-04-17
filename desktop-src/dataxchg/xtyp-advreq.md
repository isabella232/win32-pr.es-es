---
title: XTYP_ADVREQ transacción (ddeml. h)
description: La \_ transacción XTYP ADVREQ informa al servidor de que una transacción de notificación está pendiente en el par nombre de tema y nombre de elemento especificado y que han cambiado los datos correspondientes a los pares nombre de tema y nombre de elemento.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- Intercambio de datos de transacciones XTYP_ADVREQ
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422375"
---
# <a name="xtyp_advreq-transaction"></a>XTYP \_ ADVREQ

La transacción **XTYP \_ ADVREQ** informa al servidor de que una transacción de notificación está pendiente en el par nombre de tema y nombre de elemento especificado y que han cambiado los datos correspondientes a los pares nombre de tema y nombre de elemento. El sistema envía esta transacción a la función de devolución de llamada de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), una vez que el servidor llama a la función [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .


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

No se utiliza.

</dd> <dt>

*dwData1* 
</dt> <dd>

El recuento, en la palabra de orden inferior, de las transacciones de **XTYP \_ ADVREQ** que quedan por procesarse en el mismo tema, elemento y nombre de formato establecidos en el contexto de la llamada actual a la función [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) . El recuento es cero si la transacción actual de **XTYP \_ ADVREQ** es la última. Un servidor puede usar este recuento para determinar si se debe crear un identificador de datos de **HDATA \_ APPOWNED** para los datos de notificación.

La palabra de orden inferior se establece en **CADV \_ LATEACK** si el objeto ddeml emitió la transacción **XTYP \_ ADVREQ** debido a un mensaje de confirmación de DDE de llegada tardía \_ desde un cliente que se Outrun por el servidor.

No se usa la palabra de orden superior.

</dd> <dt>

*dwData2* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El servidor debe llamar primero a la función [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) para crear un identificador de datos que identifique los datos modificados y, a continuación, devuelva el identificador. El servidor debe devolver **null** si no puede completar la transacción.

## <a name="remarks"></a>Observaciones

Un servidor no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** .

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

[**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

