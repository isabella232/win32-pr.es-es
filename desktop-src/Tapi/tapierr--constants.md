---
description: Las constantes TAPIERR \_ proporcionan información sobre los errores de ejecución de la función.
ms.assetid: 6d1cf18b-efeb-4703-9b8e-fce59b61b63f
title: TAPIERR_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f84e8f5cbe840ba428575d3ea6aeff40242fdbd2b97440d7538893421eab7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773045"
---
# <a name="tapierr_-constants"></a>Constantes \_ TAPIERR

Las **constantes TAPIERR \_ proporcionan** información sobre los errores de ejecución de la función.

<dl> <dt>

<span id="TAPIERR_CONNECTED"></span><span id="tapierr_connected"></span>**TAPIERR \_ CONECTADO**
</dt> <dd> <dl> <dt>



La operación no se puede realizar mientras el estado de la llamada está conectado.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTBUSY"></span><span id="tapierr_destbusy"></span>**TAPIERR \_ DESTBUSY**
</dt> <dd> <dl> <dt>



El destino de la llamada está ocupado.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTNOANSWER"></span><span id="tapierr_destnoanswer"></span>**TAPIERR \_ DESTNOANSWER**
</dt> <dd> <dl> <dt>



El destino de la llamada no respondió.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTUNAVAIL"></span><span id="tapierr_destunavail"></span>**TAPIERR \_ DESTUNAVAIL**
</dt> <dd> <dl> <dt>



El destino de la llamada no está disponible.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICECLASSUNAVAIL"></span><span id="tapierr_deviceclassunavail"></span>**TAPIERR \_ DEVICECLASSUNAVAIL**
</dt> <dd> <dl> <dt>



La clase de dispositivo necesaria no está disponible.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICEIDUNAVAIL"></span><span id="tapierr_deviceidunavail"></span>**TAPIERR \_ DEVICEIDUNAVAIL**
</dt> <dd> <dl> <dt>



El identificador de dispositivo necesario no está disponible.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICEINUSE"></span><span id="tapierr_deviceinuse"></span>**TAPIERR \_ DEVICEINUSE**
</dt> <dd> <dl> <dt>



El dispositivo necesario está en uso.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DROPPED"></span><span id="tapierr_dropped"></span>**TAPIERR \_ DROPPED**
</dt> <dd> <dl> <dt>



Se ha eliminado la llamada.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDESTADDRESS"></span><span id="tapierr_invaldestaddress"></span>**TAPIERR \_ INVALDESTADDRESS**
</dt> <dd> <dl> <dt>



El puntero a la dirección de destino no es válido, **es NULL** o la cadena de dirección de destino es demasiado larga.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDEVICECLASS"></span><span id="tapierr_invaldeviceclass"></span>**TAPIERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



La clase de dispositivo solicitada no es válida.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDEVICEID"></span><span id="tapierr_invaldeviceid"></span>**TAPIERR \_ INVALDEVICEID**
</dt> <dd> <dl> <dt>



El identificador de clase de dispositivo solicitado no es válido.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALPOINTER"></span><span id="tapierr_invalpointer"></span>**TAPIERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



El puntero no hace referencia a una ubicación de memoria válida. Se han especificado uno o varios de los punteros *lpszDestAddress*, *lpszAppName*, *lpszCalledParty o* *lpszComment,* pero no son válidos.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALWINDOWHANDLE"></span><span id="tapierr_invalwindowhandle"></span>**TAPIERR \_ INVALWINDOWHANDLE**
</dt> <dd> <dl> <dt>



El identificador de ventana no es válido.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_NOREQUESTRECIPIENT"></span><span id="tapierr_norequestrecipient"></span>**TAPIERR \_ NOREQUESTRECIPIENT**
</dt> <dd> <dl> <dt>



No hay ninguna aplicación de destinatario disponible para controlar la solicitud. El usuario debe iniciar la aplicación de destinatario e intentarlo de nuevo.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_NOTADMIN"></span><span id="tapierr_notadmin"></span>**TAPIERR \_ NOTADMIN**
</dt> <dd> <dl> <dt>



La operación solicitada requiere privilegios de administrador.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTCANCELLED"></span><span id="tapierr_requestcancelled"></span>**TAPIERR \_ REQUESTCANCELLED**
</dt> <dd> <dl> <dt>



Se canceló la solicitud de telefonía asistida.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTFAILED"></span><span id="tapierr_requestfailed"></span>**TAPIERR \_ REQUESTFAILED**
</dt> <dd> <dl> <dt>



Error en la solicitud por motivos no especificados.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTQUEUEFULL"></span><span id="tapierr_requestqueuefull"></span>**TAPIERR \_ REQUESTQUEUEFULL**
</dt> <dd> <dl> <dt>



Una aplicación de destinatario está activa, pero la cola de solicitudes está llena o no hay memoria suficiente para expandir la cola. La aplicación puede volver a intentarlo más adelante.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_UNKNOWNREQUESTID"></span><span id="tapierr_unknownrequestid"></span>**TAPIERR \_ UNKNOWNREQUESTID**
</dt> <dd> <dl> <dt>



El identificador de solicitud al que se hace referencia no es válido.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_UNKNOWNWINHANDLE"></span><span id="tapierr_unknownwinhandle"></span>**TAPIERR \_ UNKNOWNWINHANDLE**
</dt> <dd> <dl> <dt>



Se hubo una referencia a un identificador de ventana desconocido.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Cualquier otro valor TAPIERR \_ está obsoleto y no se debe usar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




