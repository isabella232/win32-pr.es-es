---
title: XTYP_ADVSTOP transacción (Ddeml.h)
description: Un cliente usa la transacción ADVSTOP de XTYP \_ para finalizar un bucle de asesoramiento con un servidor. Una datos dinámicos Exchange de devolución de llamada de servidor (DDE), DdeCallback, recibe esta transacción cuando un cliente especifica XTYP ADVSTOP en la función \_ DdeClientTransaction.
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- XTYP_ADVSTOP datos de transacción Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37e81f1fe407186410e604a259f6e8039c074da039fc23b2f8a090c34ff58154
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544774"
---
# <a name="xtyp_advstop-transaction"></a>Transacción \_ ADVSTOP de XTYP

Un cliente usa la **transacción \_ ADVSTOP de XTYP** para finalizar un bucle de asesoramiento con un servidor. Una datos dinámicos Exchange de devolución de llamada de servidor (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica **\_ XTYP ADVSTOP** en la función [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uType* 
</dt> <dd>

El tipo de transacción.

</dd> <dt>

*uFmt* 
</dt> <dd>

Formato de datos asociado al bucle de aviso que se va a finalizar.

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

## <a name="remarks"></a>Comentarios

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

 

