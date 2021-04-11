---
title: Seguridad de RPC a través de HTTP
description: RPC a través de HTTP proporciona tres tipos de seguridad además de la seguridad RPC estándar, lo que hace que el tráfico de RPC a través de HTTP se proteja una vez por RPC y, a continuación, se protege doble mediante el mecanismo de tunelización proporcionado por RPC a través de HTTP.
ms.assetid: 3a44c72b-b74c-433a-8826-1f76ca019f40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527cf5ff74120c41606d83a248e355a6ea46d9d5
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104279755"
---
# <a name="rpc-over-http-security"></a>Seguridad de RPC a través de HTTP

RPC a través de HTTP proporciona tres tipos de seguridad además de la seguridad RPC estándar, lo que hace que el tráfico de RPC a través de HTTP se proteja una vez por RPC y, a continuación, se protege doble mediante el mecanismo de tunelización proporcionado por RPC a través de HTTP. Para obtener una descripción de los mecanismos de seguridad RPC estándar, consulte [seguridad](security.md). El mecanismo de túnel RPC a través de HTTP se agrega a la seguridad RPC normal de la siguiente manera:

-   Proporciona seguridad a través de IIS (solo disponible para RPC a través de HTTP V2).
-   Proporciona el cifrado SSL y la comprobación del proxy RPC (autenticación mutua). También está disponible únicamente en RPC a través de HTTP V2.
-   Proporciona restricciones en el nivel de proxy RPC que indican qué máquinas de la red del servidor pueden recibir llamadas RPC a través de HTTP.

Cada una de estas tres características de seguridad se describe con más detalle en las secciones siguientes.

## <a name="iis-authentication"></a>Autenticación IIS

RPC a través de HTTP puede aprovechar el mecanismo de autenticación normal de IIS. El directorio virtual del proxy RPC se puede configurar mediante el nodo RPC en el sitio web predeterminado del complemento MMC de IIS:

![Captura de pantalla que muestra el nodo RPC en el sitio web predeterminado en el complemento MMC de IIS.](images/rpc-http-1.png)

IIS puede configurarse para deshabilitar el acceso anónimo y requerir autenticación en el directorio virtual para el proxy RPC. Para ello, haga clic con el botón secundario en el nodo RPC y seleccione **propiedades**. Seleccione la pestaña **seguridad de directorios** y haga clic en el botón **Editar** del grupo **autenticación y Access Control** , como se muestra aquí:

![Captura de pantalla que muestra el cuadro de diálogo Propiedades de RPC.](images/rpc-http-2.png)

Aunque puede usar RPC a través de HTTP aunque el directorio virtual del proxy RPC permita el acceso anónimo, Microsoft recomienda encarecidamente deshabilitar el acceso anónimo a ese directorio virtual por motivos de seguridad. En su lugar, para RPC a través de HTTP, habilite la autenticación básica, la autenticación integrada de Windows o ambas. Recuerde que solo RPC a través de HTTP V2 puede autenticarse en el proxy RPC que requiere autenticación básica o integrada de Windows. RPC a través de HTTP v1 no podrá conectarse si no se **permite el acceso anónimo** está deshabilitado. Como RPC a través de HTTP V2 es la implementación más segura y robusta, el uso de una versión de Windows que sea compatible mejorará la seguridad de las instalaciones.

> [!Note]  
> De forma predeterminada, el directorio virtual del proxy RPC está marcado para permitir el acceso anónimo. Sin embargo, el proxy RPC para RPC a través de HTTP V2 rechaza las solicitudes que no se autentican de forma predeterminada.

 

## <a name="traffic-encryption"></a>Cifrado de tráfico

RPC a través de HTTP puede cifrar el tráfico entre el cliente RPC a través de HTTP y el proxy RPC con SSL. El tráfico entre el proxy RPC y el servidor RPC a través de HTTP se cifra mediante mecanismos de seguridad RPC normales y no usa SSL (aunque se elija SSL entre el cliente y el proxy RPC). Esto se debe a que esa parte del tráfico viaja dentro de la red de una organización y detrás de un firewall.

El tráfico entre el cliente RPC a través de HTTP y el proxy RPC, que generalmente viaja a través de Internet, se puede cifrar con SSL además del mecanismo de cifrado que se ha elegido para RPC. En este caso, se vuelve a cifrar el tráfico en la parte de Internet de la ruta. El cifrado del tráfico a través del proxy RPC proporciona una defensa secundaria, en el caso de que se pongan en peligro el proxy RPC u otras máquinas de la red perimetral. Puesto que el proxy RPC no puede descifrar el nivel de cifrado secundario, el proxy RPC no tiene acceso a los datos que se envían. Consulte [recomendaciones de implementación de RPC sobre http](rpc-over-http-deployment-recommendations.md) para obtener más información. El cifrado SSL solo está disponible con RPC sobre HTTP V2.

## <a name="restricting-rpc-over-http-calls-to-certain-computers"></a>Restricción de llamadas de RPC a través de HTTP a determinados equipos

La configuración de seguridad de IIS se basa en intervalos permitidos de equipos y puertos. La capacidad de usar RPC a través de HTTP se controla mediante dos entradas del registro en el equipo que ejecuta IIS y el proxy RPC. La primera entrada es una marca que alterna la funcionalidad del proxy RPC. La segunda es una lista opcional de equipos a los que el proxy puede reenviar las llamadas RPC.

De forma predeterminada, un cliente que se pone en contacto con el proxy RPC para Tunelizar llamadas de RPC a través de HTTP no puede tener acceso a los procesos de servidor RPC, excepto el servidor RPC a través de HTTP, que se ejecuta en el mismo equipo que el proxy RPC. Si la marca HABILITAda no está definida o está establecida en un valor cero, IIS deshabilita el proxy RPC. Si se define la marca HABILITAda y se establece en un valor distinto de cero, un cliente puede conectarse a los servidores RPC a través de HTTP en el equipo en el que se ejecuta IIS. Para que el cliente pueda Tunelizar a un proceso de servidor RPC a través de HTTP en otro equipo, debe agregar una entrada del registro a la lista de servidores RPC a través de HTTP del equipo de IIS.

Los servidores RPC no pueden aceptar llamadas RPC a través de HTTP a menos que soliciten específicamente RPC para escuchar en RPC a través de HTTP.

En el ejemplo siguiente se muestra cómo configurar el registro para permitir que los clientes se conecten a los servidores a través de Internet:

```
HKEY_LOCAL_MACHINE\
   Software\Microsoft\Rpc\RpcProxy\Enabled:REG_DWORD
   Software\Microsoft\Rpc\RpcProxy\ValidPorts:REG_SZ
```

La entrada **ValidPorts** es una \_ entrada de reg SZ que contiene una lista de equipos a los que el proxy RPC de IIS puede reenviar las llamadas RPC y los puertos que debe utilizar para conectarse a los servidores RPC. La \_ entrada reg SZ tiene el siguiente formato: Rosco: 593; Rosco: 2000-8000; datos \* : 4000-8000.

En este ejemplo, IIS puede reenviar llamadas RPC a través de HTTP al servidor "Rosco" en los puertos 593 y 2000 a 8000. También puede enviar llamadas a cualquier servidor cuyo nombre empiece por "Data". Se conectará en los puertos de 4000 a 8000. Además, antes de reenviar el tráfico a un puerto determinado en el servidor RPC a través de HTTP, el proxy RPC realiza un intercambio de paquetes especial con el servicio RPC escuchando en ese puerto para comprobar que está dispuesto a aceptar solicitudes a través de HTTP.

Para obtener un ejemplo basado en esta configuración de ejemplo, si un servicio RPC escucha en el puerto 4500 en el servidor "data1" pero no ha llamado a una de las funciones [ * *RpcServerUseProtseq \** _](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) con _ * ncacn \_ http * *, rechazará la solicitud. Este comportamiento proporciona protección adicional para los servidores que escuchan en un puerto abierto debido a un error de configuración. a menos que el servidor solicite específicamente escuchar en RPC a través de HTTP, no recibirá las llamadas que se originan fuera del firewall.

Las entradas de la clave **ValidPorts** deben coincidir exactamente con el servidor RPC a través de http solicitado por el cliente (no distingue entre mayúsculas y minúsculas). Para simplificar el procesamiento, el proxy RPC no realiza la canonización del nombre proporcionado por el cliente RPC a través de HTTP. Por lo tanto, si el cliente solicita rosco.microsoft.com y en **ValidPorts** solo contiene Rosco, el proxy RPC no coincidirá con los nombres, aunque ambos nombres puedan hacer referencia al mismo equipo. Además, si la dirección IP de Rosco es 66.77.88.99 y el cliente solicita 66.77.88.99 pero la clave **ValidPorts** solo contiene Rosco, el proxy RPC rechazará la conexión. Si un cliente puede solicitar el servidor RPC a través de HTTP por nombre, o por dirección IP, inserte ambos en la clave **ValidPorts** .

> [!Note]  
> Aunque RPC está habilitado para IPv6, el proxy RPC no admite direcciones IPv6 en la clave **ValidPorts** . Si IPv6 se usa para conectar el proxy RPC y el servidor RPC a través de HTTP, solo se pueden usar nombres DNS.

 

IIS Lee las entradas de registro **habilitadas** y **ValidPorts** en el inicio. Además, RPC a través de HTTP relee el contenido de la clave **ValidPorts** aproximadamente cada 5 minutos. Si se cambia la entrada **ValidPorts** , los cambios se implementan en un plazo de 5 minutos.

**RPC a través de http v1:** El servicio WEB debe detenerse y reiniciarse mediante el Service Manager de Internet para los nuevos valores de las entradas del registro que se van a implementar.

 

 




