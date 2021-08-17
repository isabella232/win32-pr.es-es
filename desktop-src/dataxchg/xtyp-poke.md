---
title: XTYP_POKE transacción (Ddeml.h)
description: Un cliente usa la transacción XTYP RADIUSE para enviar datos \_ no solicitados al servidor. Una datos dinámicos Exchange de devolución de llamada de servidor (DDE), DdeCallback, recibe esta transacción cuando un cliente especifica XTYP TFTPE en la función \_ DdeClientTransaction.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- XTYP_POKE datos de transacción Exchange
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a179f4130ae06c4548b52586d6086201c2d832a158cef877d9aaf524160f4b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914755"
---
# <a name="xtyp_poke-transaction"></a>Transacción \_ XTYPPTOE

Un cliente usa la **transacción \_ XTYP RADIUSE** para enviar datos no solicitados al servidor. Una datos dinámicos Exchange de devolución de llamada de servidor (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica **XTYP \_ TFTPE** en la función [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uType* 
</dt> <dd>

El tipo de transacción.

</dd> <dt>

*uFmt* 
</dt> <dd>

Formato de los datos enviados desde el servidor.

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

Identificador de los datos que el cliente envía al servidor.

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

Una función de devolución de llamada de servidor debe devolver la marca **\_ DDE FACK** si procesa esta transacción, la marca **\_ FBUSY** de DDE si está demasiado ocupada para procesar esta transacción o la marca **\_ FNOTPROCESSED** de DDE si rechaza esta transacción.

## <a name="remarks"></a>Comentarios

Esta transacción se filtra si la aplicación de servidor especificó la **marca CBF \_ \_ FAILANDERES** en la [**función DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

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

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[datos dinámicos Exchange management library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

