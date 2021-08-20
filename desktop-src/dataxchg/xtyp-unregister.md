---
title: XTYP_UNREGISTER transacción (Ddeml.h)
description: Una función de devolución de llamada de datos dinámicos Exchange (DDE), DdeCallback, recibe la transacción UNREGISTER de XTYP cada vez que una aplicación de servidor de la biblioteca de administración de datos dinámicos Exchange (DDEML) usa la función DdeNameService para anular el registro de un nombre de servicio, o cada vez que finaliza una aplicación que no es DDEML que admite el tema \_ System.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- XTYP_UNREGISTER datos de transacción Exchange
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ddce7528f24c5ee9e6f4364448ebaf473a48e1be5547d71338cee4fc45d688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118102011"
---
# <a name="xtyp_unregister-transaction"></a>Transacción UNREGISTER de XTYP \_

Una función de devolución de llamada de datos dinámicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción **\_ UNREGISTER de XTYP** cada vez que una aplicación de servidor de la biblioteca de administración de datos dinámicos Exchange (DDEML) usa la función [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para anular el registro de un nombre de servicio, o cada vez que finaliza una aplicación que no es DDEML que admite el tema System.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

No se usa.

</dd> <dt>

*hsz1* 
</dt> <dd>

Identificador del nombre del servicio base que se va a anular del registro.

</dd> <dt>

*hsz2* 
</dt> <dd>

Identificador del nombre de servicio específico de la instancia que se va a anular del registro.

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

Esta transacción se filtra si la aplicación especificó la **marca CBF \_ SKIP \_ REGISTRATIONS** en la [**función DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

Una aplicación no puede bloquear este tipo de transacción; Se omite \_ el código de retorno CBR BLOCK.

Una aplicación debe usar el *parámetro hsz1* para quitar el nombre del servicio de la lista de servidores disponibles para el usuario. Una aplicación debe usar el *parámetro hsz2* para identificar qué instancia de aplicación ha finalizado.

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Conceptual**
</dt> <dt>

[datos dinámicos Exchange management library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

