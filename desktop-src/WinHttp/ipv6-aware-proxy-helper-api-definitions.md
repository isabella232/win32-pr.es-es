---
description: Con el fin de aprovechar las funciones habilitadas para IPv6, los administradores de TI deben definir dentro de su script WPAD, una función llamada FindProxyForURLEx (URL, host) que reemplazará la función FindProxyForUrl (URL, host) heredada.
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: IPv6-Aware definiciones de API de aplicación auxiliar de proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688311"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a>IPv6-Aware definiciones de API de aplicación auxiliar de proxy

Con el fin de aprovechar las funciones habilitadas para IPv6, los administradores de TI deben definir dentro de su script WPAD, una función llamada FindProxyForURLEx (URL, host) que reemplazará la función FindProxyForUrl (URL, host) heredada. Solo los administradores podrán ejecutar las nuevas funciones desde la nueva función FindProxyForURLEx.

También intentamos simplificar el trabajo de los desarrolladores, mediante la alineación de las funciones para que devuelvan diferentes tipos de direcciones IP en el mismo orden de preferencia que otros componentes de red, específicamente direcciones IPv6 seguidas de direcciones IPv4 (es decir, el comportamiento actual de la función función getaddrinfo (..) de Winsock).

Las siguientes funciones son extensiones de la [especificación de formato de archivo de configuración automática de proxy (PAC) de navegador](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) para permitir que los scripts de WPAD controlen las redes compatibles con IPv6.

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a>Funciones y entorno predefinidos para la función de JavaScript FindProxyforURLEx

Condiciones basadas en el nombre de host

<dl> <dt>

[**isResolvableEx**](isresolvableex.md)
</dt> <dd>

Determina si una cadena de host determinada puede resolverse en una dirección IP.

</dd> <dt>

[**isInNetEx**](isinnetex.md)
</dt> <dd>

Determina si una dirección IP se encuentra en una subred específica.

</dd> </dl>

Funciones de utilidad relacionadas

<dl> <dt>

[**dnsResolveEx**](dnsresolveex.md)
</dt> <dd>

Resuelva una cadena de host en su dirección IP.

</dd> <dt>

[**myIPAddressEx**](myipaddressex.md)
</dt> <dd>

Busca todas las direcciones IP del host local.

</dd> <dt>

[**sortIpAddressList**](sortipaddresslist.md)
</dt> <dd>

Ordena una lista de direcciones IP.

</dd> <dt>

[**getClientVersion**](getclientversion.md)
</dt> <dd>

Obtiene la versión del motor de procesamiento WPAD.

</dd> </dl>

> [!Note]  
> Esta funcionalidad requiere Windows Internet Explorer 7 o posterior.

 

 

 



