---
title: RAS_PORT_0 estructura (rassapi. h)
description: La estructura del puerto de RAS \_ \_ 0 contiene información que describe un puerto ras.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS_PORT_0 de la estructura RAS
- PRAS_PORT_0 de puntero de estructura RAS
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
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534269"
---
# <a name="ras_port_0-structure"></a>\_Estructura del puerto 0 de Ras \_

\[Esta versión de la estructura del **\_ Puerto \_ 0 de Ras** no es compatible con Windows Vista. En su lugar, use el [**\_ Puerto ras \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) más reciente definido en mprapi. h.\]

La estructura del **Puerto de Ras \_ \_ 0** contiene información que describe un puerto ras.

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

Una cadena Unicode terminada en null que especifica el nombre del puerto, como "COM1".

</dd> <dt>

**wszDeviceType**
</dt> <dd>

Una cadena Unicode terminada en null que especifica el tipo de dispositivo en el que se realizó la conexión, como módem o ISDN (RDSI). La lista de tipos de dispositivos que se pueden especificar en este miembro incluye todos los tipos de dispositivos instalados en el servidor, incluidos los dispositivos de terceros.

</dd> <dt>

**wszDeviceName**
</dt> <dd>

Una cadena Unicode terminada en null que especifica el nombre del dispositivo en el que se realizó la conexión, como "Hayes 9600" o "PCIMACISDN1".

</dd> <dt>

**wszMediaName**
</dt> <dd>

Especifica una cadena Unicode terminada en null que especifica el nombre del medio utilizado para la conexión, como *Rasser* o *rastapi*.

</dd> <dt>

**sector**
</dt> <dd>

Reservado.

</dd> <dt>

**Marcas**
</dt> <dd>

Especifica un conjunto de marcadores de bits que especifican la naturaleza de la conexión realizada en este puerto. Este miembro puede ser una combinación de las marcas siguientes.



| Value                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <dt>**PUERTA de enlace \_ activa**</dt> </dl>             | Si se establece esta marca, la puerta de enlace NetBIOS está activa en el servidor.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <dt>**MESSENGER \_ presente**</dt> </dl>    | Si se establece esta marca, el servicio mensajero se está ejecutando en el cliente remoto.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <dt>**PUERTO con \_ MULTIvínculo**</dt> </dl>       | Si se establece esta marca, el puerto está vinculado a otros puertos. Use esta información para mostrar el estado de la conexión como un puerto multivínculo. <br/> En el caso de un puerto multivínculo, la estructura de [**\_ \_ estadísticas del puerto ras**](ras-port-statistics-str.md) contiene dos conjuntos de estadísticas: uno para el puerto independiente y otro para los puertos combinados en la conexión de multivínculo.<br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <dt>**\_cliente ppp**</dt> </dl>                         | Si se establece esta marca, el cliente remoto se conecta mediante PPP. Si no se establece esta marca, el cliente remoto se conecta mediante el protocolo AMB.<br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <dt>**\_escucha remota**</dt> </dl>                | Si se establece esta marca, el parámetro RemoteListen de la puerta de enlace de NetBIOS se establece en 1 en el servidor.<br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <dt>**USUARIO \_ autenticado**</dt> </dl> | Si se establece esta marca, un cliente remoto está conectado al servidor y el usuario se ha autenticado. Active esta marca para asegurarse de que un cliente está conectado realmente a un puerto.<br/>                                                                                                                                                                                                   |



 

Si \_ están configuradas las marcas Messenger presente, puerta de enlace \_ activa y \_ escucha remota, utilice el servicio mensajero para enviar un mensaje administrativo al cliente remoto. Si \_ se establecen Messenger presente y \_ la escucha remota, pero la puerta de enlace \_ activa no, envía mensajes al cliente solo desde el servidor RAS al que está conectado el cliente.

</dd> <dt>

**wszUserName**
</dt> <dd>

Una cadena Unicode terminada en null que especifica el nombre del usuario remoto conectado a este puerto.

</dd> <dt>

**wszComputer**
</dt> <dd>

Una cadena Unicode terminada en null que especifica el nombre del equipo cliente remoto.

</dd> <dt>

**dwStartSessionTime**
</dt> <dd>

Especifica el tiempo, en segundos desde el 1 de enero de 1970, que el cliente conectó al servidor RAS en este puerto. Use las funciones estándar de hora para dar formato a este valor para su presentación.

</dd> <dt>

**wszLogonDomain**
</dt> <dd>

Especifica una cadena Unicode terminada en null que especifica el nombre del dominio en el que se autenticó el usuario remoto. Esta cadena es solo el nombre de dominio, sin el \\ \\ prefijo "".

</dd> <dt>

**fAdvancedServer**
</dt> <dd>

Especifica una marca que es distinto de cero si el servidor RAS asociado a este puerto es un servidor avanzado, como Windows 2000 Advanced Server. Utilice esta información para determinar el nombre del servidor que tiene la base de datos de cuentas de usuario. Si el servidor RAS es un servidor avanzado, obtenga el nombre del servidor de cuentas de usuario mediante la concatenación del prefijo " \\ \\ " en el nombre devuelto en el miembro **wszLogonDomain** . Esto se debe a que para un servidor avanzado, el nombre de dominio de inicio de sesión local es el mismo que el nombre del servidor. Si el servidor RAS es una estación de trabajo, utilice la función [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obtener el nombre del servidor de cuentas de usuario.

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

[**\_Puerto ras \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_estadísticas de Puerto ras \_**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> </dl>

 

 





