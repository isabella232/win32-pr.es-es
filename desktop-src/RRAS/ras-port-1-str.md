---
title: RAS_PORT_1 estructura (rassapi. h)
description: La \_ estructura del puerto ras \_ 1 contiene información acerca de un puerto ras.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS_PORT_1 de la estructura RAS
- PRAS_PORT_1 de puntero de estructura RAS
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
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651398"
---
# <a name="ras_port_1-structure"></a>\_Estructura del puerto 1 de Ras \_

\[Esta versión de la estructura del **\_ Puerto \_ 1 de Ras** no es compatible con Windows Vista. En su lugar, use el [**\_ Puerto ras \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) más reciente definido en mprapi. h.\]

La estructura del **\_ Puerto ras \_ 1** contiene información acerca de un puerto ras.

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

Especifica una estructura de [**\_ Puerto \_ 0 de Ras**](ras-port-0-str.md) que contiene información sobre el puerto, como el nombre del puerto, el nombre del usuario remoto conectado al puerto, etc.

</dd> <dt>

**LineCondition**
</dt> <dd>

Especifica el estado del puerto. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                            | Significado                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <dt>**\_Puerto ras \_ no \_ operativo**</dt> </dl> | El puerto no es operativo. Busque en el registro de eventos los errores detectados por el servidor.<br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <dt>**\_Puerto ras \_ desconectado**</dt> </dl>           | El puerto está actualmente desconectado.<br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <dt>**\_devolución de \_ llamada del puerto ras \_**</dt> </dl>          | El servidor RAS está devolviendo al cliente RAS.<br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <dt>**\_escucha de Puerto ras \_**</dt> </dl>                    | El puerto está esperando a que un cliente llame a en.<br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <dt>**\_autenticación de Puerto ras \_**</dt> </dl>     | El servidor está en proceso de autenticación del cliente remoto.<br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <dt>**\_Puerto ras \_ autenticado**</dt> </dl>        | El cliente remoto ya está autenticado.<br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <dt>**\_inicialización del puerto ras \_**</dt> </dl>           | El dispositivo conectado al puerto se está inicializando. El estado del puerto cambiará al puerto RAS \_ \_ escuchando cuando se haya completado la inicialización.<br/> |



 

</dd> <dt>

**HardwareCondition**
</dt> <dd>

Especifica uno de los siguientes valores para indicar el estado del dispositivo conectado al puerto.



| Value                                                                                                                                                                                                  | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <dt>**\_módem ras \_ operativo**</dt> </dl>                 | El módem conectado a este puerto está operativo y está listo para recibir llamadas de cliente.<br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <dt>**\_error de \_ hardware del módem ras \_**</dt> </dl> | El módem conectado a este puerto tiene un problema de hardware.<br/>                              |



 

</dd> <dt>

**LineSpeed**
</dt> <dd>

Especifica la velocidad, en bits por segundo, con la que el equipo puede comunicarse con el puerto.

</dd> <dt>

**NumStatistics**
</dt> <dd>

Este miembro no se usa. Las funciones de administración de RAS, como la función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) , utilizan la estructura de [**\_ \_ estadísticas de Puerto ras**](ras-port-statistics-str.md) para devolver estadísticas de puerto.

</dd> <dt>

**NumMediaParms**
</dt> <dd>

Especifica el número de parámetros específicos del medio para este puerto. En el caso de los medios en serie, suele ser el número de valores que aparecen en el archivo de SERIAL.INI.

</dd> <dt>

**SizeMediaParms**
</dt> <dd>

Especifica el tamaño, en bytes, del búfer necesario para todos los parámetros específicos del medio. La función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) devuelve un búfer que contiene una matriz de estructuras de [**\_ parámetros ras**](ras-parameters-str.md) con los valores y parámetros multimedia del puerto.

</dd> <dt>

**ProjResult**
</dt> <dd>

Estructura del resultado de la [**\_ \_ proyección \_ PPP de Ras**](ras-ppp-projection-result-str.md) que especifica la información de proyección PPP para este puerto. Esta estructura proporciona información para cada protocolo que se negocia cuando un cliente RAS se conecta a un servidor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**parámetros de RAS \_**](ras-parameters-str.md)
</dt> <dt>

[**\_Puerto ras \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**\_estadísticas de Puerto ras \_**](ras-port-statistics-str.md)
</dt> <dt>

[**\_resultado de \_ proyección \_ PPP de Ras**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





