---
title: XTYP_POKE transacción (ddeml. h)
description: Un cliente usa la transacción de XTYP \_ para enviar datos no solicitados al servidor. Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), DdeCallback, recibe esta transacción cuando un cliente especifica XTYP \_ en la función DdeClientTransaction.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- Intercambio de datos de transacciones XTYP_POKE
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
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996303"
---
# <a name="xtyp_poke-transaction"></a>XTYP \_

Un cliente usa la **transacción \_ de XTYP** para enviar datos no solicitados al servidor. Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica [](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) **XTYP \_** en la función DdeClientTransaction.


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

El formato de los datos enviados desde el servidor.

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

No se utiliza.

</dd> <dt>

*dwData2* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una función de devolución de llamada de servidor debe devolver la marca **DDE \_ Fack** si procesa esta transacción, la marca **\_ FBUSY de DDE** si está demasiado ocupada para procesar esta transacción o la marca **\_ FNOTPROCESSED de DDE** si rechaza esta transacción.

## <a name="remarks"></a>Observaciones

Esta transacción se filtra si la aplicación de servidor especificó la marca de **\_ error CBF \_ fails** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

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

**Vista**
</dt> <dt>

[Biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

