---
title: RAS_PORT_0 estructura (Rassapi.h)
description: La estructura \_ RAS PORT \_ 0 contiene información que describe un puerto RAS.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS_PORT_0 ras de estructura
- PRAS_PORT_0 de estructura ras
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67891ccd65aaa56fc41dd077ae46bd4bf61f816cdc02afeb65964886cbaf9562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673135"
---
# <a name="ras_port_0-structure"></a>Estructura \_ RAS PORT \_ 0

\[Esta versión de la **estructura \_ RAS PORT \_ 0** no se admite a partir Windows Vista. Use el puerto [**RAS \_ \_ 0 más**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) reciente definido en mprapi.h en su lugar.\]

La **estructura RAS PORT \_ \_ 0** contiene información que describe un puerto RAS.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wszPortName**
</dt> <dd>

Cadena Unicode terminada en NULL que especifica el nombre del puerto, como "COM1".

</dd> <dt>

**wszDeviceType**
</dt> <dd>

Cadena Unicode terminada en NULL que especifica el tipo del dispositivo en el que se realizó la conexión, como Módem o ISDN. La lista de tipos de dispositivo que se pueden especificar en este miembro incluye todos los tipos de dispositivo instalados en el servidor, incluidos los dispositivos de terceros.

</dd> <dt>

**wszDeviceName**
</dt> <dd>

Cadena Unicode terminada en NULL que especifica el nombre del dispositivo en el que se realizó la conexión, como "Hayes 9600" o "PCIMACISDN1".

</dd> <dt>

**wszMediaName**
</dt> <dd>

Especifica una cadena Unicode terminada en NULL que especifica el nombre del medio utilizado para la conexión, como *rasser* o *rastapi*.

</dd> <dt>

**reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**Marcas**
</dt> <dd>

Especifica un conjunto de marcas de bits que especifican la naturaleza de la conexión realizada en este puerto. Este miembro puede ser una combinación de las marcas siguientes.



| Valor                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <dt>**PUERTA DE \_ ENLACE ACTIVA**</dt> </dl>             | Si se establece esta marca, la puerta de enlace NetBIOS está activa en el servidor.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <dt>**MESSENGER \_ PRESENT**</dt> </dl>    | Si se establece esta marca, el servicio messenger se ejecuta en el cliente remoto.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <dt>**PUERTO \_ MULTIVINCULADO**</dt> </dl>       | Si se establece esta marca, el puerto está multivinculado con otros puertos. Use esta información para mostrar el estado de la conexión como un puerto de varios vínculos. <br/> Para un puerto de varios vínculos, la estructura [**RAS \_ PORT \_ STATISTICS**](ras-port-statistics-str.md) contiene dos conjuntos de estadísticas: una para el puerto por sí sola y otra para los puertos combinados en la conexión de varios vínculos.<br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <dt>**CLIENTE \_ PPP**</dt> </dl>                         | Si se establece esta marca, el cliente remoto conectado mediante PPP. Si no se establece esta marca, el cliente remoto conectado mediante el protocolo AMB.<br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <dt>**ESCUCHA \_ REMOTA**</dt> </dl>                | Si se establece esta marca, el parámetro RemoteListen de la puerta de enlace NetBIOS se establece en 1 en el servidor.<br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <dt>**USUARIO \_ AUTENTICADO**</dt> </dl> | Si se establece esta marca, un cliente remoto se conecta al servidor y el usuario se ha autenticado. Compruebe esta marca para asegurarse de que un cliente está conectado realmente a un puerto.<br/>                                                                                                                                                                                                   |



 

Si se establecen las marcas MESSENGER PRESENT, GATEWAY ACTIVE y REMOTE LISTEN, use el servicio de mensajería para enviar un mensaje \_ \_ administrativo al cliente \_ remoto. Si MESSENGER PRESENT y REMOTE LISTEN están establecidos, pero GATEWAY ACTIVE no, envíe mensajes al cliente solo desde el servidor RAS al que \_ \_ está conectado el \_ cliente.

</dd> <dt>

**wszUserName**
</dt> <dd>

Cadena Unicode terminada en NULL que especifica el nombre del usuario remoto conectado a este puerto.

</dd> <dt>

**wszComputer**
</dt> <dd>

Cadena Unicode terminada en NULL que especifica el nombre del equipo cliente remoto.

</dd> <dt>

**dwStartSessionTime**
</dt> <dd>

Especifica el tiempo, en segundos desde el 1 de enero de 1970, que el cliente se conectó al servidor RAS en este puerto. Use las funciones de hora estándar para dar formato a este valor para su presentación.

</dd> <dt>

**wszLogonDomain**
</dt> <dd>

Especifica una cadena Unicode terminada en NULL que especifica el nombre del dominio en el que se autenticó el usuario remoto. Esta cadena es solo el nombre de dominio, sin prefijo \\ \\ "".

</dd> <dt>

**fAdvancedServer**
</dt> <dd>

Especifica una marca que es distinta de cero si el servidor RAS asociado a este puerto es un servidor avanzado como Windows 2000 Advanced Server. Use esta información para determinar el nombre del servidor que tiene la base de datos de la cuenta de usuario. Si el servidor RAS es un servidor avanzado, obtenga el nombre del servidor de cuentas de usuario concatenando el prefijo " " con el nombre devuelto en el \\ \\ **miembro wszLogonDomain.** Esto se debe a que, para un servidor avanzado, el nombre de dominio de inicio de sesión local es el mismo que el nombre del servidor. Si el servidor RAS es una estación de trabajo, use la [**función RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obtener el nombre del servidor de cuentas de usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**PUERTO \_ \_ RAS 1**](ras-port-1-str.md)
</dt> <dt>

[**ESTADÍSTICAS \_ DE \_ PUERTO RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> </dl>

 

 





