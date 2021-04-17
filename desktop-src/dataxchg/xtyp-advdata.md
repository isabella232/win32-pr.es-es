---
title: XTYP_ADVDATA transacción (ddeml. h)
description: Informa al cliente de que el valor del elemento de datos ha cambiado. La función de devolución de llamada de cliente de Intercambio dinámico de datos (DDE), DdeCallback, recibe esta transacción después de establecer un bucle de notificaciones con un servidor.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- Intercambio de datos de transacciones XTYP_ADVDATA
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685868"
---
# <a name="xtyp_advdata-transaction"></a>XTYP \_ ADVDATA

Informa al cliente de que el valor del elemento de datos ha cambiado. La función de devolución de llamada de cliente de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción después de establecer un bucle de notificaciones con un servidor.


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uType* 
</dt> <dd>

El tipo de transacción.

</dd> <dt>

*uFmt* 
</dt> <dd>

El formato Atom de los datos enviados desde el servidor.

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

Identificador del nombre del elemento.

</dd> <dt>

*hdata* 
</dt> <dd>

Identificador de los datos asociados con el par nombre del tema y nombre del elemento. Este parámetro es **null** si el cliente especificó la marca **\_ NoData de XTYPF** cuando solicitó el bucle de notificación.

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

Una función de devolución de llamada DDE debe devolver **DDE \_ Fack** si procesa esta transacción, **DDE \_ FBUSY** si está demasiado ocupado para procesar esta transacción, **o \_ FNOTPROCESSED DDE** si rechaza esta transacción.

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

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

