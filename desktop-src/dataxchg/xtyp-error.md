---
title: XTYP_ERROR transacción (ddeml. h)
description: Una función de devolución de llamada de Intercambio dinámico de datos (DDE), DdeCallback, recibe la \_ transacción de error XTYP cuando se produce un error crítico.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- Intercambio de datos de transacciones XTYP_ERROR
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705136"
---
# <a name="xtyp_error-transaction"></a>\_Transacción de error XTYP

Una función de devolución de llamada de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción de **\_ error XTYP** cuando se produce un error crítico.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
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

Identificador de la conversación asociada al error. Este parámetro es **null** si el error no está asociado a una conversación.

</dd> <dt>

*hsz1* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*hsz2* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*hdata* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*dwData1* 
</dt> <dd>

Código de error en la palabra de orden inferior. Actualmente, solo se admite el siguiente código de error.



| Value                                                                                                                                                                      | Significado                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <dt>**DMLERR \_ de \_ memoria insuficiente**</dt> </dl> | Memoria insuficiente; es posible que se pierdan los datos de aconsejar, escribir o ejecutar, o bien se puede producir un error en el sistema.<br/> |



 

</dd> <dt>

*dwData2* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una aplicación no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** . La biblioteca de administración de Intercambio dinámico de datos (DDEML) intenta liberar memoria quitando recursos no críticos. Una aplicación que tenga conversaciones bloqueadas debe desbloquearla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Ddeml. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de la biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

