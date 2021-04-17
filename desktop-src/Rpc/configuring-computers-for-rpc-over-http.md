---
title: Configuración de equipos para RPC a través de HTTP
description: Para usar HTTP como protocolo de transporte para RPC, el proxy RPC que se ejecuta en Internet Information Server (IIS) debe estar configurado en la red del programa de servidor.
ms.assetid: 5a67af51-924a-4f2b-b013-a4fd1bfaeddd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d1b39276633f3b827f778deef77edd5630c599
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651308"
---
# <a name="configuring-computers-for-rpc-over-http"></a>Configuración de equipos para RPC a través de HTTP

Para usar HTTP como protocolo de transporte para RPC, el proxy RPC que se ejecuta en Internet Information Server (IIS) debe estar configurado en la red del programa de servidor. En esta sección se describen las opciones de configuración. Para obtener recomendaciones sobre las prácticas recomendadas de programación y configuración cuando se usa RPC a través de HTTP, vea [recomendaciones de implementación de RPC sobre http](rpc-over-http-deployment-recommendations.md). La tarea principal es configurar el proxy RPC para aceptar y reenviar conexiones RPC a través de HTTP a un programa de servidor RPC a través de HTTP.

IIS debe instalarse primero en el equipo que ejecuta el proxy RPC. Una vez instalado IIS, el proxy RPC está instalado. Tanto IIS como el proxy RPC se pueden instalar simultáneamente desde **Agregar o quitar componentes de Windows** en el panel de control. El proxy RPC se instala desde los **servicios de red** y se denomina **proxy RPC sobre http** en el programa de instalación de Windows. Si tanto IIS como el proxy RPC se instalan al mismo tiempo, Windows se asegura de que se instalan en el orden correcto.

> [!Note]  
> Una vez completada la instalación, IIS debe reiniciarse si se estaba ejecutando durante el proceso de instalación.

 

Después de instalar el proxy RPC, se deben realizar algunas tareas de configuración adicionales:

1.  Abra el complemento MMC de IIS y configure el directorio virtual del proxy RPC para que requiera seguridad, como se explica en [seguridad de RPC a través de http](rpc-over-http-security.md). Este paso solo es necesario si tiene previsto usar RPC a través de HTTP V2.
2.  Si IIS no tiene un certificado instalado, se debe obtener e instalar un certificado válido para ese equipo con el fin de usar SSL al comunicarse con el proxy RPC. Este paso solo es relevante para RPC a través de HTTP V2. Como RPC a través de HTTP v1 no es compatible con SSL, este paso se puede omitir para RPC a través de HTTP v1.
3.  Establezca la clave **ValidPorts** tal y como se describe en [seguridad de RPC a través de http](rpc-over-http-security.md).

Cuando se completan estas tareas de configuración, el proxy RPC a través de HTTP está listo para reenviar las solicitudes del cliente RPC a través de HTTP al servidor RPC a través de HTTP.

## <a name="rpc-over-http-registry-keys"></a>Claves del registro de RPC sobre HTTP

En esta sección se explican las claves del registro adicionales que se usan para configurar el cliente, el servidor o el proxy RPC en una conexión de RPC a través de HTTP. Normalmente, estas claves no son necesarias; se proporcionan aquí por integridad.

**HKLM \\ software \\ Microsoft \\ RPC \\ DefaultChannelLifetime**

DWORD. Invalida la duración predeterminada del canal. Se utiliza en el cliente y en el proxy RPC. La duración del canal se expresa en bytes. Si no se especifica, se usa 1 GB. Solo se usa en RPC a través de HTTP V2. Cuando se cambia en el proxy RPC, IIS debe reiniciarse para que el cambio surta efecto.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ ClientReceiveWindow**

DWORD. Cuando está presente, especifica la ventana de recepción utilizada por el cliente para los datos recibidos del proxy RPC. El valor válido mínimo es 8 KB. El máximo es 1 GB. Si el valor no está presente, se utiliza 64K. Solo se usa en RPC a través de HTTP V2.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ InProxyReceiveWindow**

DWORD. Cuando está presente, especifica la ventana de recepción utilizada por el proxy RPC para los datos recibidos del cliente. El valor válido mínimo es 8 KB. El máximo es 1 GB. Si el valor no está presente, se utiliza 64K. Solo se usa en RPC a través de HTTP V2. Cuando se realizan cambios en este valor, se debe reiniciar IIS para que el cambio surta efecto.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ OutProxyReceiveWindow**

DWORD. Cuando está presente, especifica la ventana de recepción utilizada por el proxy RPC para los datos recibidos del servidor. El valor válido mínimo es 8 KB. El máximo es 1 GB. Si el valor no está presente, se utiliza 64K. Solo se usa en RPC a través de HTTP V2. Cuando se realizan cambios en este valor, se debe reiniciar IIS para que el cambio surta efecto.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ ServerReceiveWindow**

DWORD. Cuando está presente, especifica la ventana de recepción utilizada por el servidor para los datos recibidos del proxy RPC. El valor válido mínimo es 8 KB. El máximo es 1 GB. Si el valor no está presente, se utiliza 64K. Solo se usa en RPC a través de HTTP V2. Cuando se realizan cambios en este valor, se debe reiniciar IIS para que el cambio surta efecto.

\-

**HKLM \\ software \\ directivas \\ Microsoft \\ Windows NT \\ RPC \\ MinimumConnectionTimeout**

DWORD. Cuando está presente, especifica el tiempo de espera mínimo de conexión utilizado por el cliente y el proxy RPC, en segundos. El tiempo de espera real utilizado es el inferior de este valor y el tiempo de espera de conexión inactiva de IIS. Si es cero, o la clave no está presente, se utiliza el tiempo de espera de conexión inactiva de IIS. Solo se usa en RPC a través de HTTP V2. Cuando se realizan cambios en este valor en el proxy RPC, IIS debe reiniciarse para que el cambio surta efecto.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ UseProxyForIPAddrIfRDNSFails**

Cuando está presente y se establece en un valor distinto de cero, y se proporciona una dirección IP numérica como dirección del proxy RPC, un cliente RPC a través de HTTP intentará invertir la resolución de nombres y, si se produce un error, intentará conectarse al proxy RPC a través de un proxy HTTP. Se puede usar para emular el comportamiento de Windows NT en instalaciones que requieren este comportamiento. Se omite para RPC a través de HTTP V2. Solo se usa cuando se usa RPC a través de HTTP v1. Solo se admite en Windows 2000 con Service Pack 3 (SP3) y versiones posteriores.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy \\ AllowAnonymous**

DWORD. Si no está presente o se establece en cero, el proxy RPC comprueba si se ha autenticado la conexión y si es segura (se usa SSL u otra forma de cifrado). Si es false, se rechaza la conexión. Si este valor contiene un valor distinto de cero, se permiten conexiones anónimas y no cifradas. Esta configuración es una adición a cualquier configuración del directorio virtual. Por ejemplo, si el acceso anónimo está deshabilitado en el nivel de directorio virtual, pero **AllowAnonymous** es distinto de cero, el acceso anónimo seguirá estando bloqueado en el nivel de IIS. Se utiliza en el proxy RPC solo en RPC a través de HTTP V2. Cuando se realizan cambios en este valor en el proxy RPC, IIS debe reiniciarse para que el cambio surta efecto.

> [!WARNING]
> Microsoft recomienda encarecidamente no establecer el valor de **AllowAnonymous** en sistemas de producción por motivos de seguridad. El único motivo por el que se debe establecer esta clave es realizar pruebas en redes cerradas sin acceso externo. Cualquier sistema conectado a Internet y que ejecute el proxy RPC con la clave **AllowAnonymous** establecida en un valor distinto de cero puede ser vulnerable a los ataques.

 

 

 




