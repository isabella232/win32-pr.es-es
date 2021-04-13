---
title: XTYP_CONNECT_CONFIRM transacción (ddeml. h)
description: Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), DdeCallback, recibe la transacción de confirmación de XTYP \_ Connect \_ para confirmar que se ha establecido una conversación con un cliente y para proporcionar al servidor el identificador de conversación.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- Intercambio de datos de transacciones XTYP_CONNECT_CONFIRM
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
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422373"
---
# <a name="xtyp_connect_confirm-transaction"></a>XTYP \_ conectar \_ confirmar transacción

Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción de **confirmación de XTYP \_ Connect \_** para confirmar que se ha establecido una conversación con un cliente y para proporcionar al servidor el identificador de conversación. El sistema envía esta transacción como resultado de una transacción [**XTYP \_ Connect**](xtyp-connect.md) o [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) anterior.


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

No se utiliza.

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

No se utiliza.

</dd> <dt>

*dwData1* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*dwData2* 
</dt> <dd>

Especifica si el cliente es la misma instancia de aplicación que el servidor. Si el parámetro es 1, el cliente es la misma instancia. Si el parámetro es 0, el cliente es una instancia diferente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ SKIP \_ Connect \_ Confirmations** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Un servidor no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** .

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

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

