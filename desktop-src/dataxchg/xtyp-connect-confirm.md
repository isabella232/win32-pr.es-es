---
title: XTYP_CONNECT_CONFIRM transacción (Ddeml.h)
description: Una función de devolución de llamada de servidor datos dinámicos Exchange (DDE), DdeCallback, recibe la transacción CONFIRM de XTYP CONNECT para confirmar que se ha establecido una conversación con un cliente y para proporcionar al servidor el identificador de \_ \_ conversación.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- XTYP_CONNECT_CONFIRM datos de transacción Exchange
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0259540801a49bc631dc60e33979a8730b46bdfc06ac81142098e851b8a51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499094"
---
# <a name="xtyp_connect_confirm-transaction"></a>Transacción XTYP \_ CONNECT \_ CONFIRM

Una función datos dinámicos Exchange de devolución de llamada de servidor (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción **XTYP \_ CONNECT \_ CONFIRM** para confirmar que se ha establecido una conversación con un cliente y para proporcionar al servidor el identificador de conversación. El sistema envía esta transacción como resultado de una [**transacción XTYP \_ CONNECT**](xtyp-connect.md) o [**\_ XTYP WILDCONNECT**](xtyp-wildconnect.md) anterior.


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uType* 
</dt> <dd>

El tipo de transacción.

</dd> <dt>

*uFmt* 
</dt> <dd>

No se usa.

</dd> <dt>

*hconv* 
</dt> <dd>

Identificador de la nueva conversación.

</dd> <dt>

*hsz1* 
</dt> <dd>

Identificador del nombre del tema en el que se ha establecido la conversación.

</dd> <dt>

*hsz2* 
</dt> <dd>

Identificador del nombre del servicio en el que se ha establecido la conversación.

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

Especifica si el cliente es la misma instancia de aplicación que el servidor. Si el parámetro es 1, el cliente es la misma instancia. Si el parámetro es 0, el cliente es una instancia diferente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ SKIP CONNECT \_ \_ CONFIRMS** en la [**función DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

Un servidor no puede bloquear este tipo de transacción; Se omite el código de retorno **\_ CBR BLOCK.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Ddeml.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[datos dinámicos Exchange management library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

