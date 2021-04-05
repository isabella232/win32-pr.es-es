---
title: XTYP_UNREGISTER transacción (ddeml. h)
description: Una función de devolución de llamada de Intercambio dinámico de datos (DDE), DdeCallback, recibe la \_ transacción de anulación del registro de XTYP cada vez que una aplicación de servidor de biblioteca de administración de intercambio dinámico de datos (ddeml) utiliza la función DdeNameService para anular el registro de un nombre de servicio o cuando se termina una aplicación que no es de ddeml que admite el tema del sistema.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- Intercambio de datos de transacciones XTYP_UNREGISTER
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
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803302"
---
# <a name="xtyp_unregister-transaction"></a>XTYP \_ anular el registro de la transacción

Una función de devolución de llamada de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción de **\_ anulación del registro de XTYP** cada vez que una aplicación de servidor de biblioteca de administración de intercambio dinámico de datos (ddeml) utiliza la función [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para anular el registro de un nombre de servicio o cuando se termina una aplicación que no es de ddeml que admite el tema del sistema.


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

No se utiliza.

</dd> <dt>

*hconv* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*hsz1* 
</dt> <dd>

Identificador del nombre del servicio base cuya registro se va a anular.

</dd> <dt>

*hsz2* 
</dt> <dd>

Identificador del nombre del servicio específico de la instancia que se va a eliminar del registro.

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

## <a name="remarks"></a>Observaciones

Esta transacción se filtra si la aplicación especificó la marca **CBF \_ SKIP \_ registrations** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Una aplicación no puede bloquear este tipo de transacción; \_se omite el código de retorno del bloque CBR.

Una aplicación debe usar el parámetro *hsz1* para quitar el nombre del servicio de la lista de servidores disponibles para el usuario. Una aplicación debe usar el parámetro *hsz2* para identificar la instancia de la aplicación que ha finalizado.

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

