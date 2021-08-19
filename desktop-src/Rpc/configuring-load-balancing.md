---
title: Configuración del equilibrio de carga
description: Configuración del equilibrio de carga
ms.assetid: c78ffde1-1811-4065-941f-c24692eb144c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3560359bd5ad064dc270e0840845674b97b093af66796dc92f31f7a15170f467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931698"
---
# <a name="configuring-load-balancing"></a>Configuración del equilibrio de carga

Cada máquina de proxy RPC que va a actuar como un servicio de servidor de equilibrio de carga (LBS) debe configurarse como un servicio LBS con conocimiento de los servidores de la granja de servidores. Opcionalmente, se puede establecer el recurso predeterminado y se puede establecer la seguridad de proxy en las llamadas RPC de LBS y LBS a LBS. Esta configuración se configura mediante un conjunto de claves **del Registro necesarias** y claves del Registro **opcionales,** como se describe a continuación.

## <a name="required-registry-keys"></a>Claves del Registro necesarias

Se requieren varias claves y valores del Registro para configurar un servidor LBS. Si falta alguna clave o se introduce un error, se registra Windows evento. Consulte la descripción de cada clave y valor para obtener información sobre el evento registrado.

Para configurar la granja de servidores, se debe crear una clave del Registro **HKLM \\ SOFTWARE Microsoft \\ Rpc \\ \\ RpcProxy** denominada **LBSConfiguration.** En la **clave LBSConfiguration,** se crea una clave para cada recurso de la granja de servidores. El nombre de clave es la representación de cadena del GUID del recurso. Debe existir al menos una clave de recurso y este recurso es idéntico al [**UUID**](./rpcdce/ns-rpcdce-uuid.md) establecido por los clientes en el identificador de enlace, [**RPC BINDING \_ \_ HANDLE**](rpc-binding-handle.md), cuando crean el enlace RPC/HTTP (para obtener más información, vea [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)). En cada clave UUID de recurso, debe existir un valor DWORD denominado **ConfigurationType** que describa la configuración utilizada. También debe existir un **\_ REG SZ de** identificadores de servidor delimitados por punto y coma denominado **ServerFarm**. Los servidores identificados en la **clave ServerFarm** son los servidores que son miembros de la granja de servidores de equilibrio de carga.

A continuación se muestra un desglose detallado de los valores y las claves del Registro necesarios:

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration**

Clave del Registro. La **clave LBSConfiguration** es la clave del Registro que contiene la configuración de LBS. Esto incluye los [**UUID de**](./rpcdce/ns-rpcdce-uuid.md) recursos que se van a equilibrar la carga, el tipo de configuración para cada recurso y los servidores de las granjas de servidores que participan en el equilibrio de carga. Si falta esta clave o no es válida, no se considerará que está configurada y el servicio LBS no se ejecutará.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX**

Clave del Registro. La **clave UUID del** recurso identifica el UUID del recurso que se va a equilibrar la carga. Este UUID de recurso es el mismo que el [**UUID**](./rpcdce/ns-rpcdce-uuid.md) que los clientes establecen en el identificador de enlace, [**RPC BINDING \_ \_ HANDLE**](rpc-binding-handle.md). Debe haber al menos un UUID de recurso para equilibrar la carga, puede haber varios UUID de recursos. Solo puede haber una granja de servidores y todos los puntos de conexión deben estar en todos los servidores dentro de la granja de servidores. Si esta clave no se puede analizar en un UUID válido, el evento **RPCPROXY \_ EVENTLOG \_ LB INVALID KEY \_ \_ (0xC0000006)** se registrará en el registro de eventos Windows eventos.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX \\ ConfigurationType**

DWORD. ConfigurationType DWORD se almacena en la **clave UUID del** recurso.  El único valor permitido es 1. Si este valor es distinto de 1, el evento **RPCPROXY \_ EVENTLOG \_ LB UNKNOWN \_ \_ CFG TYPE \_ (0xC0000007)** se registrará en el registro de eventos Windows eventos.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX \\ ServerFarm**

REG \_ SZ. El **valor del Registro ServerFarm** contiene una lista delimitada por punto y coma de identificadores de servidor. El formato de los identificadores de servidor es:

"ServerID1,ServerPort1,LBSPort1, \[ LBSPort2, ... LBSPortN \] ;"

Se deben enumerar varios identificadores de servidor en la clave del Registro **ServerFarm.** Deben delimitarse mediante un punto y coma. Los campos que forman parte del identificador del servidor se describen en la tabla siguiente. Si este campo no se puede analizar correctamente, el evento **RPCPROXY \_ EVENTLOG \_ LB BAD CONFIG ENTRY \_ \_ \_ (0xC0000008)** se registrará en el registro de eventos Windows eventos.



| Campo de identificador | Requisito | Descripción                                                                                                                                                                                                                                                                        |
|------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ServerID         | Requerido    | Nombre de red que se puede resolver para el servidor. Puede ser un nombre DNS, un nombre netbios o una dirección IP.                                                                                                                                                                                |
| ServerPort       | Opcionales    | Si se especifica, el puerto en el que el servidor escucha las conexiones RPC/HTTP. Si no se especifica, se usa el asignador de punto de conexión en la máquina del servidor para buscar el puerto del servidor.                                                                                                         |
| LBSPort          | Opcionales    | Si se especifica, el puerto en el que el servidor escucha lbs. Para usar esta clave, las interfaces LBS deben establecerse en un punto de conexión estático mediante un comando de firewall RPC netsh. Consulte [Procedimientos recomendados de equilibrio de carga](load-balancing-best-practices.md) para obtener ejemplos del comando netsh. |



 

## <a name="optional-registry-keys"></a>Claves del Registro opcionales

Hay tres valores opcionales del Registro para configurar un servidor LBS. Las claves controlan principalmente el nivel de seguridad de las llamadas hacia y desde el servicio LBS, y también controlan el UUID del recurso predeterminado que se va a usar. Los siguientes son valores opcionales:

A continuación se muestra un desglose detallado de los valores y las claves del Registro necesarios:

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ NoSecurity**

DWORD. Cuando **NoSecurity** DWORD no está presente o establecido en 0, se rechazan las llamadas entrantes no seguras al servicio LBS. Cuando está presente y no es 0, las llamadas entrantes no seguras al servicio LBS no se rechazan. Esta clave se lee una vez al iniciar el servicio LBS.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ AssumeResourceUUID**

DWORD. Cuando **el DWORD AssumeResourceUUID** no está presente, no se produce ningún cambio en el servicio LBS. Cuando está presente, debe establecerse con un [**UUID válido.**](./rpcdce/ns-rpcdce-uuid.md) Este **UUID se** usará como UUID de recurso para todas las conexiones que no especifiquen un UUID de recurso. Esto se usa normalmente en casos en los que los clientes no especifican un UUID de recurso al crear el enlace RPC/HTTP, pero un administrador desea equilibrar la carga del tráfico RPC/HTTP a una granja de servidores. Si esta clave no se puede analizar en un UUID, se genera un error interno de RPC que genera información de [**\_ \_ error \_**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) extendida de RPC si está habilitada.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ RPCHTTPLBSServer \\ NoSecurity**

DWORD. Cuando **NoSecurity** DWORD no se presenta o se establece en 0, todas las llamadas salientes realizadas a los servicios LBS tendrán seguridad. Si está presente y no se establece en 0, todas las llamadas salientes realizadas a los servicios LBS no tendrán seguridad. Asegúrese de que esta configuración coincide con la configuración **HKLM \\ SOFTWARE Microsoft \\ Rpc \\ \\ RpcProxy \\ LBSConfiguration \\ NoSecurity.**

 

 