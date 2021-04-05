---
title: XTYP_ADVSTART transacción (ddeml. h)
description: Un cliente usa la \_ transacción XTYP ADVSTART para establecer un bucle de notificación con un servidor.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- Intercambio de datos de transacciones XTYP_ADVSTART
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852351ad902a0552ee012d6c1e5c4d61501e6e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802545"
---
# <a name="xtyp_advstart-transaction"></a>XTYP \_ ADVSTART

Un cliente usa la transacción **XTYP \_ ADVSTART** para establecer un bucle de notificación con un servidor. Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica **XTYP \_ ADVSTART** como parámetro *wType* de la función [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uType* 
</dt> <dd>

El tipo de transacción.

</dd> <dt>

*uFmt* 
</dt> <dd>

El formato de datos solicitado por el cliente.

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

No se utiliza.

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

Una función de devolución de llamada de servidor debe devolver **true** para permitir un bucle de notificaciones en el nombre de tema especificado y en el par de nombre de elemento, o **false** para denegar el bucle de notificación. Si la función de devolución de llamada devuelve **true**, las llamadas subsiguientes a la función [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) del servidor en el mismo nombre de tema y nombre de elemento hacen que el sistema envíe transacciones de [**XTYP \_ ADVREQ**](xtyp-advreq.md) al servidor.

## <a name="remarks"></a>Observaciones

Si un cliente solicita un bucle de notificaciones en el nombre de un tema, el nombre del elemento y el formato de datos de un bucle de notificaciones que ya está establecido, la biblioteca de administración de Intercambio dinámico de datos (DDEML) no crea un bucle de notificaciones de notificación, sino que modifica las marcas de bucle de aviso (**XTYPF \_ ACKREQ** y **XTYPF \_ NoData**) para que coincidan con la solicitud más

Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ FAIL \_ asesora** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

