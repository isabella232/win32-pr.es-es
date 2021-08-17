---
title: XTYP_REGISTER transacción (Ddeml.h)
description: Una función de devolución de llamada de datos dinámicos Exchange (DDE), DdeCallback, recibe el tipo de transacción XTYP REGISTER siempre que una aplicación de servidor de biblioteca de administración de datos dinámicos Exchange (DDEML) use la función DdeNameService para registrar un nombre de servicio o cada vez que se inicia una aplicación que no sea DDEML que admita el tema \_ System.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- XTYP_REGISTER datos de transacción Exchange
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c4ffdb48b7a69109659e65d816b4ab146a1f38bde976e7f8330746f564bc64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544754"
---
# <a name="xtyp_register-transaction"></a>Transacción XTYP \_ REGISTER

Una función de devolución de llamada de datos dinámicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe el tipo de transacción **XTYP \_ REGISTER** cada vez que una aplicación de servidor de biblioteca de administración de datos dinámicos Exchange (DDEML) usa la función [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar un nombre de servicio o cada vez que se inicia una aplicación que no es DDEML que admite el tema System.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Identificador del nombre del servicio base que se va a registrar.

</dd> <dt>

*hsz2* 
</dt> <dd>

Identificador del nombre de servicio específico de la instancia que se va a registrar.

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

Esta transacción se filtra si la aplicación especificó la **marca \_ CBF SKIP \_ REGISTRATIONS** en la [**función DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

Una aplicación no puede bloquear este tipo de transacción; Se omite el código de retorno **\_ CBR BLOCK.**

Una aplicación debe usar el *parámetro hsz1* para agregar el nombre del servicio a la lista de servidores disponibles para el usuario. Una aplicación debe usar el *parámetro hsz2* para identificar qué instancia de aplicación se ha iniciado.

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Conceptual**
</dt> <dt>

[datos dinámicos Exchange management library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

