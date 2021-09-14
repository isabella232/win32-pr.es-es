---
description: El mensaje \_ LINE PROXYSTATUS se envía cuando los servidores proxy disponibles cambian en una línea que la aplicación tiene abierta actualmente.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: LINE_PROXYSTATUS mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb00c5df4f531309bdd1311fb7c34c3e9967a8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250058"
---
# <a name="line_proxystatus-message"></a>Mensaje \_ DE LINE PROXYSTATUS

El **mensaje \_ LINE PROXYSTATUS** se envía cuando los servidores proxy disponibles cambian en una línea que la aplicación tiene abierta actualmente.

TAPISRV genera este mensaje durante una función [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) mediante LINEPROXYSTATUS OPEN y \_ LINEPROXYSTATUS ALLOPENFORACD o una función \_ [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) mediante LINEPROXYSTATUS CLOSE (todas las constantes \_ [**LINEPROXYSTATUS \_**](lineproxystatus--constants.md)).


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

Identificador de la aplicación al dispositivo de línea. Esto está relacionado con el controlador del agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Especifica el estado de la cola que ha cambiado. Puede ser una o varias de las [**constantes LINEPROXYSTATUS \_**](lineproxystatus--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Si *dwParam1* está establecido en LINEPROXYSTATUS OPEN o \_ LINEPROXYSTATUS \_ CLOSE, *dwParam2* indica el tipo de solicitud de proxy relacionado, que es uno de los siguientes:

-   LINEPROXYREQUEST \_ SETAGENTGROUP
-   LINEPROXYREQUEST \_ SETAGENTSTATE
-   LINEPROXYREQUEST \_ SETAGENTACTIVITY
-   LINEPROXYREQUEST \_ GETAGENTCAPS
-   LINEPROXYREQUEST \_ GETAGENTSTATUS
-   LINEPROXYREQUEST \_ AGENTSPECIFIC
-   LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST
-   LINEPROXYREQUEST \_ GETAGENTGROUPLIST
-   LINEPROXYREQUEST \_ CREATEAGENT
-   LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETAGENTINFO
-   LINEPROXYREQUEST \_ CREATEAGENTSESSION
-   LINEPROXYREQUEST \_ GETAGENTSESSIONLIST
-   LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE
-   LINEPROXYREQUEST \_ GETAGENTSESSIONINFO
-   LINEPROXYREQUEST \_ GETQUEUELIST
-   LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETQUEUEINFO
-   LINEPROXYREQUEST \_ GETGROUPLIST
-   LINEPROXYREQUEST \_ SETAGENTSTATEEX

De lo contrario, *dwParam2* se establece en cero.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado. Establecer en cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**LINE \_ PROXYREQUEST**](line-proxyrequest.md)
</dt> <dt>

[**Constantes \_ LINEPROXYREQUEST**](lineproxyrequest--constants.md)
</dt> </dl>

 

 




