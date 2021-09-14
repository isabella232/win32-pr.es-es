---
title: Configuración de equipos para RPC a través de HTTP
description: Para usar HTTP como protocolo de transporte para RPC, el proxy RPC que se ejecuta en Internet Information Server (IIS) debe configurarse en la red del programa de servidor.
ms.assetid: 5a67af51-924a-4f2b-b013-a4fd1bfaeddd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d1b39276633f3b827f778deef77edd5630c599
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073835"
---
# <a name="configuring-computers-for-rpc-over-http"></a>Configuración de equipos para RPC a través de HTTP

Para usar HTTP como protocolo de transporte para RPC, el proxy RPC que se ejecuta en Internet Information Server (IIS) debe configurarse en la red del programa de servidor. En esta sección se describen las opciones de configuración. Para obtener recomendaciones sobre los procedimientos recomendados de programación y configuración cuando se usa RPC a través de HTTP, consulte RPC sobre la implementación [de HTTP Recomendaciones](rpc-over-http-deployment-recommendations.md). La tarea principal consiste en configurar el proxy RPC para aceptar y reenviar RPC a través de conexiones HTTP a un programa de servidor RPC a través de HTTP.

IIS debe instalarse primero en la máquina que ejecuta el proxy RPC. Una vez instalado IIS, se instala el proxy RPC. Iis y el proxy RPC se pueden instalar simultáneamente desde Agregar o quitar componentes Windows **en** el Panel de control. El proxy RPC se instala desde **Networking Services** y se denomina RPC a través del **proxy HTTP** en Windows configuración. Si IIS y el proxy RPC están instalados al mismo tiempo, Windows garantiza que se instalan en el orden correcto.

> [!Note]  
> Una vez completada la instalación, IIS debe reiniciarse si se estaba ejecutando durante el proceso de instalación.

 

Después de instalar el proxy RPC, se deben realizar algunas tareas de configuración adicionales:

1.  Abra el complemento MMC de IIS y configure el directorio virtual proxy RPC para requerir seguridad, como se explica [en RPC sobre seguridad HTTP.](rpc-over-http-security.md) Este paso solo es necesario si tiene previsto usar RPC a través de HTTP v2.
2.  Si IIS no tiene instalado un certificado, se debe obtener e instalar un certificado válido para ese equipo con el fin de usar SSL al comunicarse con el proxy RPC. Este paso solo es relevante para RPC a través de HTTP v2. Puesto que RPC sobre HTTP v1 no admite SSL, este paso se puede omitir para RPC a través de HTTP v1.
3.  Establezca la **clave ValidPorts** como se describe en [RPC sobre seguridad HTTP.](rpc-over-http-security.md)

Cuando se completan estas tareas de configuración, el proxy RPC a través de HTTP está listo para reenviar las solicitudes del cliente RPC a través de HTTP al servidor RPC a través de HTTP.

## <a name="rpc-over-http-registry-keys"></a>RPC a través de claves del Registro HTTP

En esta sección se explican las claves del Registro adicionales que se usan para configurar el cliente, el servidor o el proxy RPC en una conexión RPC a través de HTTP. Por lo general, estas claves no son necesarias; se proporcionan aquí para que sean completas.

**HKLM \\ Software \\ Microsoft \\ Rpc \\ DefaultChannelLifetime**

DWORD. Invalida la duración predeterminada del canal. Se usa en el cliente y el proxy RPC. La duración del canal se expresa en bytes. Si no se especifica, se usa 1 GB. Solo se usa en RPC a través de HTTP v2. Cuando se cambia en el proxy RPC, IIS debe reiniciarse para que el cambio suba.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ ClientReceiveWindow**

DWORD. Cuando está presente, especifica la ventana de recepción utilizada por el cliente para los datos recibidos del proxy RPC. El valor mínimo válido es 8K. El máximo es 1 GB. Si el valor no está presente, se usa 64K. Solo se usa en RPC a través de HTTP v2.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ InProxyReceiveWindow**

DWORD. Cuando está presente, especifica la ventana de recepción utilizada por el proxy RPC para los datos recibidos del cliente. El valor mínimo válido es 8K. El máximo es 1 GB. Si el valor no está presente, se usa 64K. Solo se usa en RPC a través de HTTP v2. Cuando se realizan cambios en este valor, IIS debe reiniciarse para que el cambio suba.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ OutProxyReceiveWindow**

DWORD. Cuando está presente, especifica la ventana de recepción que usa el proxy RPC para los datos recibidos del servidor. El valor mínimo válido es 8K. El máximo es 1 GB. Si el valor no está presente, se usa 64K. Solo se usa en RPC a través de HTTP v2. Cuando se realizan cambios en este valor, IIS debe reiniciarse para que el cambio suba.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ ServerReceiveWindow**

DWORD. Cuando está presente, especifica la ventana de recepción utilizada por el servidor para los datos recibidos del proxy RPC. El valor mínimo válido es 8K. El máximo es 1 GB. Si el valor no está presente, se usa 64K. Solo se usa en RPC a través de HTTP v2. Cuando se realizan cambios en este valor, IIS debe reiniciarse para que el cambio suba.

\-

**Directivas de software HKLM \\ De Microsoft Windows NT Rpc \\ \\ \\ \\ \\ MinimumConnectionTimeout**

DWORD. Cuando está presente, especifica el tiempo de espera mínimo de conexión utilizado por el cliente y el proxy RPC, en segundos. El tiempo de espera real utilizado es el menor de este valor y el tiempo de espera de conexión inactiva de IIS. Si es cero o la clave no está presente, se usa el tiempo de espera de conexión inactiva de IIS. Solo se usa en RPC a través de HTTP v2. Cuando se realizan cambios en este valor en el proxy RPC, IIS debe reiniciarse para que el cambio suba.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ UseProxyForIPAddrIfRDNSFails**

Cuando está presente y se establece en distinto de cero, y se proporciona una dirección IP numérica como dirección de proxy RPC, un cliente RPC sobre HTTP intentará la resolución inversa de nombres y, si se produce un error, intentará conectarse al proxy RPC a través de un proxy HTTP. Se puede usar para emular el Windows NT en instalaciones que requieren este comportamiento. Se omite para RPC a través de HTTP v2. Solo se usa cuando se usa RPC sobre HTTP v1. Solo se admite Windows 2000 con Service Pack 3 (SP3) y versiones posteriores.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ RpcProxy \\ AllowAnonymous**

DWORD. Cuando no está presente o se establece en cero, el proxy RPC comprueba si la conexión está autenticada y si es segura (se usa SSL u otra forma de cifrado). Si alguno de los dos es false, se rechaza la conexión. Si este valor contiene conexiones no cero, se permiten conexiones anónimas y no cifradas. Esta configuración es una adición a cualquier configuración de directorio virtual. Por ejemplo, si el acceso anónimo está deshabilitado en el nivel de directorio virtual, pero **AllowAnonymous** es distinto de cero, el acceso anónimo seguirá bloqueado en el nivel de IIS. Se usa en el proxy RPC solo en RPC a través de HTTP v2. Cuando se realizan cambios en este valor en el proxy RPC, IIS debe reiniciarse para que el cambio suba.

> [!WARNING]
> Microsoft recomienda encarecidamente no establecer el valor **AllowAnonymous** en los sistemas de producción por consideraciones de seguridad. La única razón por la que se debe establecer esta clave es para realizar pruebas en redes cerradas sin acceso externo. Cualquier sistema conectado a Internet y ejecutando el proxy RPC con la clave **AllowAnonymous** establecida en un valor distinto de cero puede ser vulnerable a ataques.

 

 

 




