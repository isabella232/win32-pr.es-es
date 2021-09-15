---
description: Para aprovechar las funciones habilitadas para IPv6, los administradores de TI deben definir dentro de su script WPAD, una función denominada FindProxyForURLEx (url, host) que reemplazará a la función Heredada FindProxyForUrl (url, host).
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: IPv6-Aware de api auxiliar de proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258676"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a>IPv6-Aware de api auxiliar de proxy

Para aprovechar las funciones habilitadas para IPv6, los administradores de TI deben definir dentro de su script WPAD, una función denominada FindProxyForURLEx (url, host) que reemplazará a la función Heredada FindProxyForUrl (url, host). Solo desde la nueva función FindProxyForURLEx los administradores podrán ejecutar las nuevas funciones.

También hemos intentado simplificar el trabajo para los desarrolladores, alineando nuestras funciones para devolver distintos tipos de direcciones IP en el mismo orden de preferencia que otros componentes de red, en concreto direcciones IPv6 seguidas de direcciones IPv4 (es decir, el comportamiento actual de la función getaddrinfo(..) de Winsock).

Las siguientes funciones son extensiones de la especificación de formato de archivo de configuración automática [(PAC)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) del proxy del navegador para permitir que los scripts de WPAD controle las redes compatibles con IPv6.

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a>Funciones predefinidas y entorno para la función de JavaScript FindProxyforURLEx

Condiciones basadas en nombre de host

<dl> <dt>

[**isResolvableEx**](isresolvableex.md)
</dt> <dd>

Determina si una cadena de host determinada puede resolverse en una dirección IP.

</dd> <dt>

[**isInNetEx**](isinnetex.md)
</dt> <dd>

Determina si una dirección IP está en una subred específica.

</dd> </dl>

Funciones de utilidad relacionadas

<dl> <dt>

[**dnsResolveEx**](dnsresolveex.md)
</dt> <dd>

Resuelva una cadena de host en su dirección IP.

</dd> <dt>

[**myIPAddressEx**](myipaddressex.md)
</dt> <dd>

Busca todas las direcciones IP de localhost.

</dd> <dt>

[**sortIpAddressList**](sortipaddresslist.md)
</dt> <dd>

Ordena una lista de direcciones IP.

</dd> <dt>

[**getClientVersion**](getclientversion.md)
</dt> <dd>

Obtiene la versión del motor de procesamiento de WPAD.

</dd> </dl>

> [!Note]  
> Esta funcionalidad requiere Windows Internet Explorer 7 o superior.

 

 

 



