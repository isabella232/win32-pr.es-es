---
title: XTYP_XACT_COMPLETE transacción (Ddeml.h)
description: Una datos dinámicos Exchange de devolución de llamada de cliente (DDE), DdeCallback, recibe la transacción XACT COMPLETE de XTYP cuando se ha completado una transacción asincrónica, iniciada por una llamada a la función \_ \_ DdeClientTransaction.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- XTYP_XACT_COMPLETE datos de transacción Exchange
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3833207371bbfab059f67ecb5bdb72b77334ef3ffc73618e013ce137835c6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678015"
---
# <a name="xtyp_xact_complete-transaction"></a>Transacción \_ XTYP XACT \_ COMPLETE

Una datos dinámicos Exchange de devolución de llamada de cliente (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción **\_ XTYP XACT \_ COMPLETE** cuando se ha completado una transacción asincrónica, iniciada por una llamada a la función [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uType* 
</dt> <dd>

El tipo de transacción.

</dd> <dt>

*uFmt* 
</dt> <dd>

Formato de los datos asociados a la transacción completada (si procede) o **NULL** si no se ha intercambiado ningún dato durante la transacción.

</dd> <dt>

*hconv* 
</dt> <dd>

Identificador de la conversación.

</dd> <dt>

*hsz1* 
</dt> <dd>

Identificador del nombre del tema implicado en la transacción completada.

</dd> <dt>

*hsz2* 
</dt> <dd>

Identificador del nombre del elemento implicado en la transacción completada.

</dd> <dt>

*hdata* 
</dt> <dd>

Identificador de los datos implicados en la transacción completada, si procede. Si la transacción se ha realizado correctamente pero no ha implicado ningún dato, este parámetro es **TRUE.** Este parámetro es **NULL si** la transacción no se ha realizada correctamente.

</dd> <dt>

*dwData1* 
</dt> <dd>

Identificador de transacción de la transacción completada.

</dd> <dt>

*dwData2* 
</dt> <dd>

Cualquier marca **de estado de DDE \_** aplicable en la palabra baja. Este parámetro proporciona compatibilidad con aplicaciones dependientes de bits **\_ APPSTATUS de DDE.** Se recomienda que las aplicaciones ya no usen estos bits y que no se puedan usar en versiones futuras de DDEML.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una aplicación no debe liberar el identificador de datos obtenido durante esta transacción. Sin embargo, una aplicación debe copiar los datos asociados al identificador de datos si la aplicación debe procesar los datos después de que se devuelva la función de devolución de llamada. Una aplicación puede usar la [**función DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar los datos.

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

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

**Conceptual**
</dt> <dt>

[datos dinámicos Exchange management library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

