---
title: RAS_PORT_1 estructura (Rassapi.h)
description: La estructura \_ RAS PORT \_ 1 contiene información sobre un puerto RAS.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS_PORT_1 ras de estructura
- PRAS_PORT_1 de estructura ras
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c73677b10743434bb9548c8d6add95100c4cf017d25bb44d7436e2f68b9ca4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673115"
---
# <a name="ras_port_1-structure"></a>Estructura \_ RAS PORT \_ 1

\[Esta versión de la **estructura \_ RAS PORT \_ 1** no se admite a partir Windows Vista. Use el puerto [**RAS \_ \_ 1 más**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) reciente definido en mprapi.h en su lugar.\]

La **estructura RAS PORT \_ \_ 1** contiene información sobre un puerto RAS.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**rasport0**
</dt> <dd>

Especifica una estructura [**RAS \_ PORT \_ 0**](ras-port-0-str.md) que contiene información sobre el puerto, como el nombre del puerto, el nombre del usuario remoto conectado al puerto, y así sucesivamente.

</dd> <dt>

**LineCondition**
</dt> <dd>

Especifica el estado del puerto. Este miembro puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                            | Significado                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <dt>**PUERTO RAS \_ \_ NO \_ OPERATIVO**</dt> </dl> | El puerto no está operativo. Compruebe en el registro de eventos si hay errores notificados por el servidor.<br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <dt>**PUERTO \_ RAS \_ DESCONECTADO**</dt> </dl>           | El puerto está desconectado actualmente.<br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <dt>**PUERTO RAS \_ QUE \_ LLAMA DE \_ NUEVO**</dt> </dl>          | El servidor RAS está llamando de nuevo al cliente RAS.<br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <dt>**ESCUCHA \_ DE PUERTO \_ RAS**</dt> </dl>                    | El puerto está esperando a que un cliente llame a .<br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <dt>**AUTENTICACIÓN \_ DE \_ PUERTO RAS**</dt> </dl>     | El servidor está en proceso de autenticación del cliente remoto.<br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <dt>**PUERTO \_ RAS \_ AUTENTICADO**</dt> </dl>        | El cliente remoto ahora está autenticado.<br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <dt>**INICIALIZACIÓN \_ DE \_ PUERTO RAS**</dt> </dl>           | Se está inicializando el dispositivo conectado al puerto. El estado del puerto cambiará a RAS \_ PORT LISTENING cuando se haya completado la \_ inicialización.<br/> |



 

</dd> <dt>

**HardwareCondition**
</dt> <dd>

Especifica uno de los siguientes valores para indicar el estado del dispositivo conectado al puerto.



| Value                                                                                                                                                                                                  | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <dt>**MÓDEM \_ RAS \_ OPERATIVO**</dt> </dl>                 | El módem conectado a este puerto está operativo y está listo para recibir llamadas de cliente.<br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <dt>**ERROR \_ DE HARDWARE DEL MÓDEM \_ \_ RAS**</dt> </dl> | El módem conectado a este puerto tiene un problema de hardware.<br/>                              |



 

</dd> <dt>

**LineSpeed**
</dt> <dd>

Especifica la velocidad, en bits por segundo, con la que el equipo puede comunicarse con el puerto.

</dd> <dt>

**NumStatistics**
</dt> <dd>

Este miembro no se usa. Las funciones de administración de RAS, como la [**función RasAdminPortGetInfo,**](rasadminportgetinfo.md) usan la estructura [**RAS PORT \_ \_ STATISTICS**](ras-port-statistics-str.md) para devolver estadísticas de puerto.

</dd> <dt>

**NumMediaParms**
</dt> <dd>

Especifica el número de parámetros específicos del medio para este puerto. En el caso de los medios serie, suele ser el número de valores que aparecen en el SERIAL.INI serie.

</dd> <dt>

**SizeMediaParms**
</dt> <dd>

Especifica el tamaño, en bytes, del búfer necesario para todos los parámetros específicos del medio. La [**función RasAdminPortGetInfo**](rasadminportgetinfo.md) devuelve un búfer que contiene una matriz de estructuras [**DE PARÁMETROS \_ RAS**](ras-parameters-str.md) con los parámetros multimedia y los valores del puerto.

</dd> <dt>

**ProjResult**
</dt> <dd>

Estructura [**RAS PPP PROJECTION \_ \_ \_ RESULT**](ras-ppp-projection-result-str.md) que especifica la información de proyección PPP para este puerto. Esta estructura proporciona información para cada protocolo que se negocia cuando un cliente RAS se conecta a un servidor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al Servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**PARÁMETROS \_ RAS**](ras-parameters-str.md)
</dt> <dt>

[**PUERTO \_ \_ RAS 0**](ras-port-0-str.md)
</dt> <dt>

[**ESTADÍSTICAS \_ DE \_ PUERTO RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RESULTADO DE \_ PROYECCIÓN DE RAS PPP \_ \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionConnectionConnectionupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





