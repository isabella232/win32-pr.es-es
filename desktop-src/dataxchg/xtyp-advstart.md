---
title: XTYP_ADVSTART transacción (Ddeml.h)
description: Un cliente usa la transacción ADVSTART de XTYP \_ para establecer un bucle de asesoramiento con un servidor.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- XTYP_ADVSTART datos de transacción Exchange
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
ms.openlocfilehash: fb18bda3dce4db465045991e26cdc2d97ddd87ddc69c494ffaf103c566955da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544764"
---
# <a name="xtyp_advstart-transaction"></a>Transacción ADVSTART de XTYP \_

Un cliente usa la **transacción \_ ADVSTART de XTYP** para establecer un bucle de asesoramiento con un servidor. Una datos dinámicos Exchange de devolución de llamada de servidor (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica **\_ XTYP ADVSTART como** el parámetro *wType* de la [**función DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)


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

Formato de datos solicitado por el cliente.

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

No se usa.

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

Una función de devolución de llamada de servidor debe devolver **TRUE** para permitir un bucle advise en el par de nombre de tema y nombre de elemento especificado, o **FALSE** para denegar el bucle advise. Si la función de devolución de llamada devuelve **TRUE**, las llamadas posteriores al servidor a la función [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) en el mismo par de nombre de tema y nombre de elemento hace que el sistema envíe transacciones [**\_ XTYP ADBIZQ**](xtyp-advreq.md) al servidor.

## <a name="remarks"></a>Comentarios

Si un cliente solicita un bucle de asesoramiento en un nombre de tema, nombre de elemento y formato de datos para un bucle de asesoramiento que ya está establecido, la biblioteca de administración de datos dinámicos Exchange (DDEML) no crea un bucle de asesoramiento duplicado, sino que modifica las marcas de bucle de aviso **(XTYPF \_ ACKREQ** y **\_ XTYPF NODATA)** para que coincidan con la solicitud más reciente.

Esta transacción se filtra si la aplicación de servidor especificó la **marca CBF \_ FAIL \_ ADVISES** en la [**función DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Conceptual**
</dt> <dt>

[datos dinámicos Exchange management library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

