---
title: Modo kernel SSL
description: Modo kernel SSL
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- Modo kernel SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9dcfeb87b1a98539d7bd6a3b8b82dcfd5ee41fc9ad4c4c306f4c399aebd18a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393923"
---
# <a name="kernel-mode-ssl"></a>Modo kernel SSL

Ssl en modo kernel se introdujo en Windows Server 2003 con Service Pack 1 (SP1) con compatibilidad limitada. Para los equipos que se ejecutan Windows Server 2003 con SP1, se debe establecer una clave del Registro para habilitar SSL del kernel. En el caso de los equipos Windows Server 2008 y Windows Vista, se proporciona compatibilidad completa del modo kernel con SSL.

En las secciones siguientes se describe la compatibilidad con SSL en modo kernel:

-   Kernel Modes SSL in Windows Server 2003 with SP1
-   Modo kernel SSL en Windows Server 2008 y Windows Vista

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a>Kernel Modes SSL in Windows Server 2003 with SP1

En Windows Server 2003 con SP1, la API del servidor HTTP proporciona la opción de ejecutar la seguridad SSL en modo kernel (ssl en modo de usuario es el valor predeterminado). La característica de modo kernel mejora el rendimiento de SSL al mover las operaciones de cifrado y descifrado al kernel, lo que reduce el número de transiciones entre el modo kernel y el modo de usuario.

Las siguientes características no se admiten cuando SSL se ejecuta en modo kernel:

-   Certificados de cliente
-   Cifrados RC2
-   Protocolo PCT 1.0
-   Los cambios de configuración del certificado de servidor requieren un reinicio del servicio HTTP
-   Compatibilidad con cifrado masivo y descarga

## <a name="configuring-kernel-mode-ssl"></a>Configuración de SSL en modo kernel

Ssl en modo kernel se controla mediante el valor del Registro **EnableKernelSSL** y se habilita estableciendo el valor en 1. La habilitación de SSL en modo kernel deshabilitará ssl en modo de usuario y requiere que el servicio HTTP se reinicie para que suba efecto. La clave del Registro **EnableKernelSSL** se encuentra en:

**HKEY \_ Parámetros \_** HTTP de Local Machine \\  \\ **System CurrentControlSet** \\ **Services** \\  \\  \\ **EnableKernelSSL**

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a>Modo kernel SSL en Windows Server 2008 y Windows Vista

En el caso de los equipos Windows Server 2008 y Windows Vista, la API del servidor HTTP ofrece una funcionalidad SSL mejorada.

Se admiten las siguientes características nuevas:

-   Compatibilidad completa con certificados de cliente en el modo kernel SSL
-   SSL en modo kernel para todas las transacciones HTTP SSL
-   Compatibilidad con cifrado masivo y descarga
-   Protocolo PCT 1.0
-   Cifrados RC2
-   Mayor rendimiento sobre SSL en modo de usuario

## <a name="configuration"></a>Configuración

SSL en modo kernel se puede configurar a través de dos valores del Registro en la clave parámetros HTTP ubicada en:

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

Un usuario debe tener privilegios de administrador o sistema local para modificar los valores del Registro y ver o modificar los archivos de registro y la carpeta que los contiene.

La información de configuración de los valores del Registro se lee cuando se inicia el controlador de API del servidor HTTP. Como resultado, si se cambia la configuración, el controlador debe detenerse y reiniciarse para leer los nuevos valores. Esto se puede lograr mediante los siguientes comandos de consola:

**net stop http**

**net start http**

En la tabla siguiente se enumeran los valores de configuración del Registro.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor del Registro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EnableKernelSSL</td>
<td><strong>Windows Server 2008 y Windows Vista:</strong> Este valor del Registro está obsoleto.<br/></td>
</tr>
<tr class="even">
<td>EnableSslCloseNotify</td>
<td>Valor <strong>DWORD</strong> que se establece en <strong>TRUE para</strong> habilitar close-notify o <strong>FALSE</strong> para deshabilitar el requisito de notificación de cierre. La notificación de cierre está deshabilitada de forma predeterminada.<br/> Cuando está habilitada la notificación de cierre, la aplicación cliente debe enviar un mensaje de notificación de cierre antes de cerrar las conexiones TCP. La API del servidor HTTP también envía una notificación de cierre antes de cerrar la conexión.<br/> Cuando close-notify está habilitado y el cliente envía un mensaje de notificación de cierre, la API del servidor HTTP reutilizará la sesión SSL en futuras conexiones al cliente. Si el cliente no envía una notificación de cierre, la API del servidor HTTP no reutilizará la misma sesión SSL en futuras conexiones. Por lo tanto, se desencadena un protocolo de enlace SSL completo en la nueva conexión, lo que reduce el rendimiento. <br/>
<blockquote>
[!Note]<br />
La habilitación de la notificación de cierre ayuda a mitigar los ataques de truncamiento contra las solicitudes y respuestas HTTPS.
</blockquote>
<br/> <br/> Cuando se deshabilita la notificación de cierre, la API del servidor HTTP reutiliza la sesión SSL para futuras conexiones.<br/></td>
</tr>
<tr class="odd">
<td>DisableSslCertChainCacheOnlyUrlRetrieval</td>
<td>Valor <strong>DWORD</strong> que se establece en <strong>TRUE</strong> para permitir que la API del servidor HTTP recupere certificados intermedios de Internet o del almacén local, o <strong>FALSE</strong> para recuperar certificados intermedios solo del almacén local. El valor predeterminado del Registro es <strong>FALSE.</strong><br/> De forma predeterminada, la API del servidor HTTP crea una cadena de certificados de cliente mediante la recuperación de los certificados intermedios del almacén de la entidad de certificación intermedia en la cuenta de equipo local. Al establecer este valor en <strong>TRUE,</strong> la API del servidor HTTP puede recuperar los certificados intermedios no solo del almacén local, sino también de la entidad de certificación intermedia de Internet.<br/></td>
</tr>
</tbody>
</table>



 

 

 





