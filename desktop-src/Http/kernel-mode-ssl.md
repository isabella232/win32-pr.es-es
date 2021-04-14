---
title: SSL de modo kernel
description: SSL de modo kernel
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- SSL de modo kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737ac7c6c25bac6e7b66d91aa967fc6fa550459b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665733"
---
# <a name="kernel-mode-ssl"></a>SSL de modo kernel

SSL de modo kernel se presentó en Windows Server 2003 con Service Pack 1 (SP1) con compatibilidad limitada. En el caso de los equipos que ejecutan Windows Server 2003 con SP1, debe establecerse una clave del registro para habilitar SSL de kernel. En el caso de los equipos que ejecutan Windows Server 2008 y Windows Vista, se proporciona compatibilidad total con el modo kernel para SSL.

En las secciones siguientes se describe la compatibilidad con SSL de modo kernel:

-   Modos de kernel SSL en Windows Server 2003 con SP1
-   SSL en modo kernel en Windows Server 2008 y Windows Vista

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a>Modos de kernel SSL en Windows Server 2003 con SP1

En Windows Server 2003 con SP1, la API de servidor HTTP ofrece la opción de ejecutar la seguridad SSL en modo kernel (el valor predeterminado es SSL de modo usuario). La característica de modo kernel mejora el rendimiento de SSL moviendo las operaciones de cifrado y descifrado al kernel, con lo que se reduce el número de transiciones entre el modo kernel y el modo de usuario.

Las siguientes características no se admiten cuando SSL se ejecuta en modo kernel:

-   Certificados de cliente
-   Cifrados de RC2
-   Protocolo PCT 1,0
-   Los cambios en la configuración del certificado de servidor requieren un reinicio del servicio HTTP
-   Compatibilidad con cifrado masivo y descarga

## <a name="configuring-kernel-mode-ssl"></a>Configuración de SSL en modo kernel

SSL de modo kernel se controla mediante el valor del registro **EnableKernelSSL** y se habilita estableciendo el valor en 1. Al habilitar SSL en modo kernel, se deshabilitará el modo de usuario SSL y es necesario reiniciar el servicio HTTP para que surta efecto. La clave del registro **EnableKernelSSL** se encuentra en:

**HKEY \_ \_** \\ Parámetros http **del sistema** de equipo local \\ **CurrentControlSet** \\ **Services** \\  \\  \\ **EnableKernelSSL**

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a>SSL en modo kernel en Windows Server 2008 y Windows Vista

En el caso de los equipos que ejecutan Windows Server 2008 y Windows Vista, la API del servidor HTTP incluye la funcionalidad SSL mejorada.

Se admiten las siguientes características nuevas:

-   Compatibilidad completa con certificados de cliente en modo kernel SSL
-   SSL de modo kernel para todas las transacciones HTTP SSL
-   Compatibilidad con cifrado masivo y descarga
-   Protocolo PCT 1,0
-   Cifrados de RC2
-   Mayor rendimiento en el modo de usuario SSL

## <a name="configuration"></a>Configuración

SSL de modo kernel se puede configurar a través de dos valores de registro en la clave HTTP Parameters que se encuentra en:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

Un usuario debe tener privilegios de administrador o sistema local para modificar los valores del registro y ver o modificar los archivos de registro y la carpeta que los contiene.

La información de configuración de los valores del registro se lee cuando se inicia el controlador de la API del servidor HTTP. Como resultado, si se cambia la configuración, el controlador debe detenerse y reiniciarse para leer los nuevos valores. Esto puede realizarse mediante los siguientes comandos de la consola:

**net stop http**

**net start http**

En la tabla siguiente se enumeran los valores de configuración del registro.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor del registro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EnableKernelSSL</td>
<td><strong>Windows Server 2008 y Windows Vista:</strong> Este valor del registro está obsoleto.<br/></td>
</tr>
<tr class="even">
<td>EnableSslCloseNotify</td>
<td>Valor <strong>DWORD</strong> que se establece en <strong>true</strong> para habilitar la notificación de cierre o <strong>false</strong> para deshabilitar el requisito de notificación de cierre. Close: Notify está deshabilitado de forma predeterminada.<br/> Cuando está habilitada la notificación de cierre, se requiere la aplicación cliente para enviar un mensaje de notificación de cierre antes de cerrar las conexiones TCP. La API del servidor HTTP también envía una notificación de cierre antes de cerrar la conexión.<br/> Cuando está habilitada la notificación de cierre y el cliente envía un mensaje de notificación de cierre, la API del servidor HTTP volverá a usar la sesión SSL en futuras conexiones con el cliente. Si el cliente no envía una notificación de cierre, la API del servidor HTTP no volverá a usar la misma sesión SSL en conexiones futuras. Por lo tanto, se desencadena un protocolo de enlace SSL completo en la nueva conexión, con lo que se reduce el rendimiento. <br/>
<blockquote>
[!Note]<br />
Habilitar Close-Notify ayuda a mitigar los ataques de truncamiento contra las solicitudes y respuestas HTTPS.
</blockquote>
<br/> <br/> Cuando se deshabilita la notificación de cierre, la API del servidor HTTP vuelve a usar la sesión SSL para futuras conexiones.<br/></td>
</tr>
<tr class="odd">
<td>DisableSslCertChainCacheOnlyUrlRetrieval</td>
<td>Valor <strong>DWORD</strong> que se establece en <strong>true</strong> para permitir que la API del servidor http recupere certificados intermedios desde Internet o desde el almacén local, o bien <strong>false</strong> para recuperar certificados intermedios solo del almacén local. El valor del registro predeterminado es <strong>false</strong>.<br/> De forma predeterminada, la API del servidor HTTP crea una cadena de certificados de cliente mediante la recuperación de los certificados intermedios del almacén de entidades de certificación intermedio en la cuenta del equipo local. Establecer este valor en <strong>true</strong> permite que la API del servidor http recupere los certificados intermedios no solo del almacén local, sino también de la entidad de certificación intermedia en Internet.<br/></td>
</tr>
</tbody>
</table>



 

 

 





