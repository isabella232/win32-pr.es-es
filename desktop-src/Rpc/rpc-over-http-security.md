---
title: Seguridad de RPC a través de HTTP
description: RPC a través de HTTP proporciona tres tipos de seguridad además de la seguridad de RPC estándar, lo que da lugar a que RPC sobre el tráfico HTTP esté protegido una vez por RPC y, a continuación, protegido doblemente por el mecanismo de tunelización proporcionado por RPC a través de HTTP.
ms.assetid: 3a44c72b-b74c-433a-8826-1f76ca019f40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f1ebd5a7198a2b2ccae7703b92011bbd45b037db2f7ef8eb116e28ef06d8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926144"
---
# <a name="rpc-over-http-security"></a>Seguridad de RPC a través de HTTP

RPC a través de HTTP proporciona tres tipos de seguridad además de la seguridad de RPC estándar, lo que da lugar a que RPC sobre el tráfico HTTP esté protegido una vez por RPC y, a continuación, protegido doblemente por el mecanismo de tunelización proporcionado por RPC a través de HTTP. Para obtener una descripción de los mecanismos de seguridad rpc estándar, vea [Seguridad.](security.md) El mecanismo de tunelización RPC a través de HTTP agrega a la seguridad de RPC normal de la siguiente manera:

-   Proporciona seguridad a través de IIS (disponible solo para RPC a través de HTTP v2).
-   Proporciona cifrado SSL y comprobación de proxy RPC (autenticación mutua). También está disponible solo en RPC a través de HTTP v2.
-   Proporciona restricciones en el nivel de proxy RPC que dicta qué máquinas de la red del servidor pueden recibir rpc a través de llamadas HTTP.

Cada una de estas tres características de seguridad se describe con más detalle en las secciones siguientes.

## <a name="iis-authentication"></a>Autenticación IIS

RPC a través de HTTP puede aprovechar el mecanismo de autenticación normal de IIS. El directorio virtual para el proxy RPC se puede configurar mediante el nodo Rpc en el sitio web predeterminado en el complemento MMC de IIS:

![Captura de pantalla que muestra el nodo Rpc en el sitio web predeterminado en el complemento MMC de IIS.](images/rpc-http-1.png)

IIS se puede configurar para deshabilitar el acceso anónimo y requerir autenticación en el directorio virtual para el proxy RPC. Para ello, haga clic con el botón derecho en el nodo Rpc y seleccione **Propiedades.** Seleccione la **pestaña Seguridad de** directorio y haga clic en **el** botón Editar del grupo **Autenticación Access Control,** como se muestra aquí:

![Captura de pantalla que muestra el cuadro de diálogo Propiedades de RPC.](images/rpc-http-2.png)

Aunque puede usar RPC a través de HTTP incluso cuando el directorio virtual del proxy RPC permite el acceso anónimo, Microsoft recomienda encarecidamente deshabilitar el acceso anónimo a ese directorio virtual por motivos de seguridad. En su lugar, para RPC a través de HTTP, habilite la autenticación básica, Windows autenticación integrada o ambas. Recuerde que solo RPC a través de HTTP v2 puede autenticarse en el proxy RPC que requiere autenticación básica Windows integrada; RPC a través de HTTP v1 no podrá conectarse si **No permitir acceso anónimo** está deshabilitado. Puesto que RPC sobre HTTP v2 es la implementación más segura y sólida, el uso de una versión de Windows que la admita mejorará la seguridad de las instalaciones.

> [!Note]  
> De forma predeterminada, el directorio virtual del proxy RPC está marcado para permitir el acceso anónimo. Sin embargo, el proxy RPC para RPC a través de HTTP v2 rechaza las solicitudes que no están autenticadas de forma predeterminada.

 

## <a name="traffic-encryption"></a>Cifrado de tráfico

RPC a través de HTTP puede cifrar el tráfico entre el cliente RPC a través de HTTP y el proxy RPC con SSL. El tráfico entre el proxy RPC y RPC a través del servidor HTTP se cifra mediante mecanismos de seguridad RPC normales y no usa SSL (incluso si se elige SSL entre el cliente y el proxy RPC). Esto se debe a que esa parte del tráfico viaja dentro de la red de una organización y detrás de un firewall.

El tráfico entre el cliente RPC a través de HTTP y el proxy RPC, que normalmente viaja a través de Internet, se puede cifrar con SSL, además del mecanismo de cifrado elegido para RPC. En este caso, el tráfico en la parte de Internet de la ruta se cifra doblemente. El cifrado del tráfico a través del proxy RPC proporciona una defensa secundaria, en caso de que el proxy RPC u otras máquinas de la red perimetral estén en peligro. Dado que el proxy RPC no puede descifrar la capa de cifrado secundaria, el proxy RPC no tiene acceso a los datos que se envían. Para [más información,](rpc-over-http-deployment-recommendations.md) consulte RPC a través de Recomendaciones HTTP. El cifrado SSL solo está disponible con RPC a través de HTTP v2.

## <a name="restricting-rpc-over-http-calls-to-certain-computers"></a>Restricción de RPC a través de llamadas HTTP a determinados equipos

La configuración de seguridad de IIS se basa en los intervalos de equipos y puertos permitidos. La capacidad de usar RPC a través de HTTP se controla mediante dos entradas del Registro en el equipo que ejecuta IIS y el proxy RPC. La primera entrada es una marca que alterna la funcionalidad de proxy RPC. La segunda es una lista opcional de equipos a los que el proxy puede reenviar llamadas RPC.

De forma predeterminada, un cliente que se pone en contacto con el proxy RPC para tunelar las llamadas RPC a través de HTTP no puede acceder a ningún proceso de servidor RPC, excepto a los procesos de servidor RPC a través de HTTP que se ejecutan en el mismo equipo que el proxy RPC. Si la marca ENABLED no está definida o establecida en un valor cero, IIS deshabilita el proxy RPC. Si la marca ENABLED está definida y establecida en un valor distinto de cero, un cliente puede conectarse a RPC a través de servidores HTTP en el equipo que ejecuta IIS. Para permitir que el cliente tunele a un proceso de servidor RPC a través de HTTP en otro equipo, debe agregar una entrada del Registro a la lista de RPC a través de servidores HTTP del equipo IIS.

Los servidores RPC no pueden aceptar llamadas RPC a través de HTTP a menos que soliciten específicamente a RPC que escuche en RPC a través de HTTP.

En el ejemplo siguiente se muestra cómo configurar el Registro para permitir que los clientes se conecten a servidores a través de Internet:

```
HKEY_LOCAL_MACHINE\
   Software\Microsoft\Rpc\RpcProxy\Enabled:REG_DWORD
   Software\Microsoft\Rpc\RpcProxy\ValidPorts:REG_SZ
```

La **entrada ValidPorts** es una entrada REG SZ que contiene una lista de equipos a los que el proxy RPC de IIS puede reenviar llamadas RPC y los puertos que debe usar para conectarse a los \_ servidores RPC. La entrada \_ REG SZ tiene la siguiente forma: Rosco:593; Rosco:2000-8000;Data \* :4000-8000.

En este ejemplo, IIS puede reenviar RPC a través de llamadas HTTP al servidor "Rosco" en los puertos 593 y 2000 a 8000. También puede enviar llamadas a cualquier servidor cuyo nombre comience por "Data". Se conectará en los puertos 4000 a 8000. Además, antes de reenviar el tráfico a un puerto determinado en el servidor RPC a través de HTTP, el proxy RPC realiza un intercambio de paquetes especial con el servicio RPC que escucha en ese puerto para comprobar que está dispuesto a aceptar solicitudes a través de HTTP.

Para obtener un ejemplo basado en esta configuración de ejemplo, si un servicio RPC escucha en el puerto 4500 en el servidor "Data1", pero no ha llamado a una de las funciones [ * *RpcServerUseProtseq \** _](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) con _*ncacn http**, rechazará \_ la solicitud. Este comportamiento proporciona protección adicional para los servidores que escuchan en un puerto abierto debido a un error de configuración. a menos que el servidor solicite específicamente escuchar en RPC a través de HTTP, no recibirá llamadas procedentes de fuera del firewall.

Las entradas de la **clave ValidPorts** deben ser una coincidencia exacta del servidor RPC sobre HTTP solicitado por el cliente (no distingue mayúsculas de minúsculas). Para simplificar el procesamiento, el proxy RPC no realiza la canonización del nombre proporcionado por el cliente RPC sobre HTTP. Por lo tanto, si el cliente solicita rosco.microsoft.com y en **ValidPorts** solo contienen Rosco, el proxy RPC no coincidirá con los nombres, aunque ambos nombres puedan hacer referencia a la misma máquina. Además, si la dirección IP de Rosco es 66.77.88.99 y el cliente solicita 66.77.88.99, pero la clave **ValidPorts** solo contiene Rosco, el proxy RPC rechazará la conexión. Si un cliente puede solicitar la RPC a través del servidor HTTP por nombre o por dirección IP, inserte ambos en la **clave ValidPorts.**

> [!Note]  
> Aunque RPC está habilitado para IPv6, el proxy RPC no admite direcciones IPv6 en la **clave ValidPorts.** Si se usa IPv6 para conectar el proxy RPC y el servidor RPC a través de HTTP, solo se pueden usar nombres DNS.

 

IIS lee las entradas del Registro **Enabled** y **ValidPorts** en el inicio. Además, RPC a través de HTTP vuelve a leer el contenido de la clave **ValidPorts** aproximadamente cada 5 minutos. Si se **cambia la entrada ValidPorts,** los cambios se implementan en un plazo de 5 minutos.

**RPC a través de HTTP v1:** El servicio WEB debe detenerse y reiniciarse mediante internet Service Manager para que se implementen nuevos valores en las entradas del Registro.

 

 




