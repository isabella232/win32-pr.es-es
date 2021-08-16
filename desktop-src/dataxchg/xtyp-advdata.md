---
title: XTYP_ADVDATA transacción (Ddeml.h)
description: Informa al cliente de que el valor del elemento de datos ha cambiado. La datos dinámicos Exchange de devolución de llamada de cliente (DDE), DdeCallback, recibe esta transacción después de establecer un bucle de asesoramiento con un servidor.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- XTYP_ADVDATA datos de transacción Exchange
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
ms.openlocfilehash: d9bf3f3b94f4454547d987ab6536929d1fe2998e7dc0394564143536f1da28d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544870"
---
# <a name="xtyp_advdata-transaction"></a>Transacción \_ ADVDATA de XTYP

Informa al cliente de que el valor del elemento de datos ha cambiado. La datos dinámicos Exchange de devolución de llamada de cliente (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción después de establecer un bucle de aviso con un servidor.


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

El atom de formato de los datos enviados desde el servidor.

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

Identificador de los datos asociados con el nombre del tema y el par de nombres de elemento. Este parámetro es **NULL** si el cliente especificó la **marca \_ XTYPF NODATA** cuando solicitó el bucle advise.

</dd> <dt>

*dwData1* 
</dt> <dd>

No se usa.

</dd> <dt>

*dwData2* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una función de devolución de llamada DDE debe devolver **DDE \_ FACK** si procesa esta transacción, **DDE \_ FBUSY** si está demasiado ocupado para procesar esta transacción o **DDE \_ FNOTPROCESSED** si rechaza esta transacción.

## <a name="remarks"></a>Comentarios

Una aplicación no debe liberar el identificador de datos obtenido durante esta transacción. Sin embargo, una aplicación debe copiar los datos asociados al identificador de datos si la aplicación debe procesar los datos después de que se devuelva la función de devolución de llamada. Una aplicación puede usar la [**función DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar los datos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Ddeml.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Conceptual**
</dt> <dt>

[datos dinámicos Exchange management library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

