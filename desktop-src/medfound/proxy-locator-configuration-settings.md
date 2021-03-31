---
description: Opciones de configuración del localizador proxy
ms.assetid: d74a85cf-293e-4322-9aff-55b06d6fda5e
title: Opciones de configuración del localizador proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3503a90bcccc990865769b6bf02a65fc383511f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155332"
---
# <a name="proxy-locator-configuration-settings"></a>Opciones de configuración del localizador proxy

En este tema se describen los valores de configuración del localizador de proxy predeterminado. Para obtener información acerca de cómo crear el localizador de proxy con opciones de configuración personalizadas, consulte [How to Configure the proxy Locator](how-to-configure-the-proxy-locator.md).

El localizador proxy puede configurarse para funcionar en tres modos: *modo manual*, *modo de detección automática* y *modo explorador*. Los valores se definen en la enumeración [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) . La aplicación puede configurar el modo estableciendo la propiedad [**MFNETSOURCE \_ PROXYSETTINGS**](mfnetsource-proxysettings-property.md) . El localizador proxy también se puede configurar para que no use un servidor proxy estableciendo esta propiedad en **MFNET \_ PROXYSETTING \_ None**. El servidor proxy no se utiliza si el servidor multimedia es un host local o la aplicación solicita una dirección (127. x. x. x), reservada para las pruebas de bucle invertido.

> [!Caution]  
> Un servidor proxy es una barrera de seguridad entre la intranet e Internet. No usar un servidor proxy puede exponer la red a amenazas de seguridad.

 

-   Modo manual. La aplicación establece este modo estableciendo la propiedad [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) en **MFNET \_ PROXYSETTING \_ manual**. La aplicación debe especificar la siguiente información de conexión:

    -   Nombre de host del servidor proxy: propiedad [**MFNETSOURCE \_ PROXYHOSTNAME**](mfnetsource-proxyhostname-property.md) .
    -   Número de puerto: [**MFNETSOURCE \_ PROXYPORT**](mfnetsource-proxyport-property.md) Property.
    -   Si se va a usar un servidor proxy para direcciones locales: [**MFNETSOURCE \_ PROXYBYPASSFORLOCAL**](mfnetsource-proxybypassforlocal-property.md) propiedad. Esta configuración es opcional. Si no se especifica, el localizador proxy utiliza un valor predeterminado de **false**.

        > [!Note]  
        > Al omitir el servidor proxy, es posible que la aplicación pueda conectarse a los servidores multimedia de la intranet con más rapidez.

         

    -   Lista de direcciones de servidor multimedia que no requieren un servidor proxy para establecer una conexión: propiedad [**MFNETSOURCE \_ PROXYEXCEPTIONLIST**](mfnetsource-proxyexceptionlist-property.md) . Esta configuración es opcional.

-   Modo de detección automática. La aplicación establece este modo estableciendo la propiedad [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) en **MFNET \_ PROXYSETTING \_ auto**. En este modo, el localizador proxy usa el mecanismo de proxy autoservicio WinHTTP para obtener el nombre de host y el número de puerto del servidor proxy. Esta información de conexión se recupera mediante el script de proxy automático WPAD, configurado por el administrador del dominio. Para obtener más información acerca de este mecanismo, vea el [sitio web de Microsoft](../winhttp/winhttp-autoproxy-support.md).

    El localizador proxy almacena en caché la información de conexión en el registro. En las llamadas de detección de proxy posteriores, el localizador proxy Lee información de proxy de la memoria caché del registro para reducir la sobrecarga que conlleva la detección automática. Sin embargo, la aplicación puede forzar la redetección automática del proxy mediante el establecimiento de la propiedad [**\_ PROXYRERUNAUTODETECTION de MFNETSOURCE**](mfnetsource-proxyrerunautodetection-property.md) .

-   Modo de explorador. La aplicación establece este modo estableciendo la propiedad [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) en **MFNET \_ PROXYSETTING \_ Explorador**. En este modo, el localizador proxy utiliza la configuración de proxy de la aplicación de explorador. Este modo se establece de forma predeterminada si el protocolo es HTTP o HTTPD.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con proxy para orígenes de red](proxy-support-for-network-sources.md)
</dt> </dl>

 

 
