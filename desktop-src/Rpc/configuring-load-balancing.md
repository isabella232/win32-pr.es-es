---
title: Configurar el equilibrio de carga
description: Configurar el equilibrio de carga
ms.assetid: c78ffde1-1811-4065-941f-c24692eb144c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b82dbfc23e491d53a6687b50aa77b23878ce52ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359342"
---
# <a name="configuring-load-balancing"></a>Configurar el equilibrio de carga

Cada equipo proxy RPC que va a actuar como un servicio de servidor de equilibrio de carga (lb) debe configurarse como un servicio de libras con conocimiento de los servidores de la granja de servidores. Opcionalmente, se puede establecer el recurso predeterminado y se puede establecer la seguridad de las llamadas RPC de proxy a libras y lb a libras. Estas opciones se configuran mediante un conjunto de **claves del registro necesarias** y **claves del registro opcionales** , tal y como se describe a continuación.

## <a name="required-registry-keys"></a>Claves del registro requeridas

Se requieren varias claves y valores del registro para configurar un servidor de LBS. Si falta alguna clave o se especifica en un error, se registra un evento de Windows. Vea la descripción de cada clave y valor para obtener información sobre el evento registrado.

Para configurar la granja de servidores, se debe crear una clave del registro **HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy** llamado **LBSConfiguration**. En la clave **LBSConfiguration** , se crea una clave para cada recurso de la granja de servidores. El nombre de clave es la representación de cadena del GUID para el recurso. Debe existir al menos una clave de recurso y este recurso es idéntico al [**UUID**](./rpcdce/ns-rpcdce-uuid.md) establecido por los clientes en el controlador de enlace, el [**\_ \_ identificador de enlace RPC**](rpc-binding-handle.md), cuando crean el enlace RPC/HTTP (para obtener más información, vea [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)). En cada clave de UUID de recursos, debe existir un valor DWORD denominado **ConfigurationType** que describe la configuración utilizada. También debe existir un **registro de \_** servidor de identificadores de servidor delimitados por punto y coma denominado **ServerFarm**. Los servidores identificados en la clave **ServerFarm** son los servidores que son miembros de la granja de servidores de equilibrio de carga.

A continuación se describe detalladamente los valores y las claves del registro necesarios:

**HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration**

Clave del registro. La clave **LBSConfiguration** es la clave del registro que contiene la configuración de libras. Esto incluye el [**UUID**](./rpcdce/ns-rpcdce-uuid.md) de recurso que va a equilibrar la carga, el tipo de configuración para cada recurso y los servidores de las granjas de servidores que participan en el equilibrio de carga. Si esta clave falta o no es válida, LBS no se considerará configurado y el servicio lb no se ejecutará.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX**

Clave del registro. La clave **UUID de recurso** identifica el UUID del recurso cuya carga se va a equilibrar. Este UUID de recurso es el mismo que el [**UUID**](./rpcdce/ns-rpcdce-uuid.md) que los clientes establecen en el identificador de enlace, el [**\_ \_ identificador de enlace de RPC**](rpc-binding-handle.md). Debe haber al menos un UUID de recurso con equilibrio de carga, puede haber varios UUID de recurso. Solo puede haber una granja de servidores y todos los puntos de conexión deben estar en todos los servidores de la granja de servidores. Si esta clave no se puede analizar en un UUID válido, se registrará en el registro de eventos de Windows la **\_ clave no válida del evento RPCPROXY EVENTLOG \_ lb \_ \_ (0xC0000006)** .

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX \\ ConfigurationType**

DWORD. El valor DWORD **ConfigurationType** se almacena en la clave **UUID de recursos** . El único valor permitido es 1. Si este valor es distinto de 1, se registrará el evento **RPCPROXY \_ EVENTLOG \_ lb \_ Unknown \_ \_ Type (0XC0000007)** en el registro de eventos de Windows.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX \\ ServerFarm**

REG \_ . El valor del registro **ServerFarm** contiene una lista de identificadores de servidor de delimitados de punto y coma. El formato de los identificadores de servidor es:

"ServerID1, ServerPort1, LBSPort1, \[ LBSPort2,... LBSPortN \] ; "

En la clave del registro **ServerFarm** se deben incluir varios identificadores de servidor. Deben delimitarse con un punto y coma. Los campos que forman parte del identificador de servidor se describen en la tabla siguiente. Si este campo no se puede analizar correctamente, se registrará el evento **RPCPROXY \_ EVENTLOG \_ lb \_ \_ \_ (0XC0000008)** en el registro de eventos de Windows.



| Campo de identificador | Requisito | Descripción                                                                                                                                                                                                                                                                        |
|------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ServerID         | Obligatorio    | Un nombre de red que se pueda resolver para el servidor. Puede ser un nombre DNS, un nombre NetBIOS o una dirección IP.                                                                                                                                                                                |
| ServerPort       | Opcionales    | Si se especifica, el puerto en el que el servidor escucha las conexiones RPC/HTTP. Si no se especifica, el asignador de extremo del equipo servidor se usa para buscar el puerto del servidor.                                                                                                         |
| LBSPort          | Opcionales    | Si se especifica, el puerto en el que el servidor escucha en libras. Para usar esta clave, las interfaces LBS se deben establecer en un punto de conexión estático mediante un comando netsh RPC Firewall. Consulte [prácticas recomendadas de equilibrio de carga](load-balancing-best-practices.md) para obtener ejemplos del comando netsh. |



 

## <a name="optional-registry-keys"></a>Claves del registro opcionales

Hay tres valores de registro opcionales para configurar un servidor de LBS. Las claves controlan principalmente el nivel de seguridad de las llamadas a y desde el servicio lb, y también controlan el UUID de recursos predeterminado que se va a usar. Los siguientes son valores opcionales:

A continuación se describe detalladamente los valores y las claves del registro necesarios:

**HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration \\ NoSecurity**

DWORD. Cuando el valor DWORD **NoSecurity** no está presente o se establece en 0, se rechazan las llamadas entrantes no seguras al servicio lb. Cuando está presente y no es 0, no se rechazan las llamadas entrantes no seguras al servicio LBS. Esta clave se lee una vez al inicio del servicio libras.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration \\ AssumeResourceUUID**

DWORD. Cuando el valor DWORD **AssumeResourceUUID** no está presente, no se produce ningún cambio en el servicio lb. Cuando está presente, debe establecerse con un [**UUID**](./rpcdce/ns-rpcdce-uuid.md)válido. Este **UUID** se usará como el UUID de recursos para todas las conexiones que no especifiquen un UUID de recurso. Esto se suele usar en los casos en los que los clientes no especifican un UUID de recursos cuando crean el enlace RPC/HTTP, pero un administrador desea equilibrar la carga del tráfico RPC/HTTP en una granja de servidores. Si esta clave no se puede analizar en un UUID, se presenta un error interno de RPC, que genera la [**información de error de RPC \_ extendida \_ \_**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) si está habilitada.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCHTTPLBSServer \\ NoSecurity**

DWORD. Cuando el valor DWORD **NoSecurity** no se presenta o se establece en 0, todas las llamadas salientes realizadas a los servicios lb tendrán seguridad. Si está presente y no está establecido en 0, todas las llamadas salientes realizadas a los servicios de LBS no tendrán seguridad. Asegúrese de que esta configuración coincide con la configuración de **HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration \\ NoSecurity** .

 

 