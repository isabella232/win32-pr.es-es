---
title: XTYP_DISCONNECT transacción (ddeml. h)
description: La función de devolución de llamada de Intercambio dinámico de datos de la aplicación (DDE), DdeCallback, recibe la \_ transacción XTYP Disconnect cuando el asociado de la aplicación en una conversación usa la función DdeDisconnect para finalizar la conversación.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- Intercambio de datos de transacciones XTYP_DISCONNECT
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801399"
---
# <a name="xtyp_disconnect-transaction"></a>XTYP \_ desconectar transacción

La función de devolución de llamada de Intercambio dinámico de datos de la aplicación (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción **XTYP \_ Disconnect** cuando el asociado de la aplicación en una conversación usa la función [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) para finalizar la conversación.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Identificador de que se ha terminado la conversación.

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

No se utiliza.

</dd> <dt>

*dwData2* 
</dt> <dd>

Especifica si los asociados de la conversación son la misma instancia de aplicación. Si este parámetro es 1, los asociados son la misma instancia. Si este parámetro es 0, los asociados son instancias diferentes.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta transacción se filtra si la aplicación especificó la marca **CBF \_ SKIP \_ desconnects** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

La aplicación puede obtener el estado de la conversación terminada llamando a la función [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) mientras procesa esta transacción. El identificador de conversación deja de ser válido después de que la función de devolución de llamada vuelva.

Una aplicación no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** .

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

[**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

