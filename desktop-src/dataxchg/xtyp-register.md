---
title: XTYP_REGISTER transacción (ddeml. h)
description: Una función de devolución de llamada de Intercambio dinámico de datos (DDE), DdeCallback, recibe el \_ tipo de transacción de registro XTYP cada vez que una aplicación de servidor de la biblioteca de administración de intercambio dinámico de datos (ddeml) utiliza la función DdeNameService para registrar un nombre de servicio, o cuando se inicia una aplicación que no es de ddeml que admite el tema del sistema.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- Intercambio de datos de transacciones XTYP_REGISTER
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
ms.openlocfilehash: cd56bf4f5ac2b4eb0f714e5348174942f685c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490072"
---
# <a name="xtyp_register-transaction"></a>XTYP \_ registrar transacción

Una función de devolución de llamada de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe el tipo de transacción de **\_ registro XTYP** cada vez que una aplicación de servidor de la biblioteca de administración de intercambio dinámico de datos (ddeml) utiliza la función [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar un nombre de servicio, o cuando se inicia una aplicación que no es de ddeml que admite el tema del sistema.


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

No se utiliza.

</dd> <dt>

*hconv* 
</dt> <dd>

No se utiliza.

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

Una aplicación no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** .

Una aplicación debe usar el parámetro *hsz1* para agregar el nombre de servicio a la lista de servidores disponibles para el usuario. Una aplicación debe usar el parámetro *hsz2* para identificar la instancia de la aplicación que se ha iniciado.

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

 

