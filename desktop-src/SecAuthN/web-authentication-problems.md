---
description: En este tema se describen las sugerencias de solución de problemas para usar las API de agente de autenticación Web para las páginas Web.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Problemas de autenticación web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc4611461effd9cbc5546059e71fc8ca3f1f0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563170"
---
# <a name="web-authentication-problems"></a>Problemas de autenticación web

En este tema se describen las sugerencias de solución de problemas para usar las API de agente de autenticación Web para las páginas Web.

-   [Registros operativos](#operational-logs)
-   [Usar Fiddler con el agente de autenticación Web](#using-fiddler-with-web-authentication-broker)
-   [Temas relacionados](#related-topics)

## <a name="operational-logs"></a>Registros operativos

Con frecuencia, los registros operativos ayudan a determinar qué no está funcionando. Hay un canal de registro de eventos dedicado Microsoft-Windows-webauth \\ operativo que permite a los desarrolladores de sitios web comprender cómo el agente de autenticación Web está procesando sus páginas Web. Para habilitarlo, inicie eventvwr.exe y habilite el registro operativo en la aplicación y los servicios \\ Microsoft \\ Windows \\ webauth. Además, el agente de autenticación Web anexa una cadena única a la cadena de agente de usuario para identificarse en el servidor Web. La cadena es "MSAuthHost/1.0". Ten en cuenta que el número de versión podría cambiar en el futuro, por lo que no debes depender de dicho número de versión en tu código. A continuación se muestra un ejemplo de la cadena de agente de usuario completa:

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

Ejemplo de uso de registros operativos

1.  Habilitar registros operativos
2.  Ejecutar la aplicación social de Contoso![visor de eventos que muestra los registros operativos webauth](images/wab-figure15.png)
3.  Las entradas de los registros generados se pueden usar para comprender con mayor detalle el comportamiento del agente de autenticación Web. En este caso, pueden incluir:
    -   Navegación - iniciar: registra cuándo se inicia AuthHost y contiene información sobre las direcciones URL de inicio y terminación.
    -   ![ilustra los detalles de Inicio de navegación](images/wab-figure16.png)
    -   Navegación - completa: registra la finalización de la carga de una página web.
    -   Etiqueta meta: registra cuándo se encuentra una etiqueta meta, incluidos los detalles.
    -   Navegación - finalizar: navegación terminada por el usuario.
    -   Navegación - error: AuthHost encuentra un error de navegación en una dirección URL e incluye HttpStatusCode.
    -   Navegación - fin: se ha encontrado la dirección URL de terminación.

## <a name="using-fiddler-with-web-authentication-broker"></a>Usar Fiddler con el agente de autenticación Web

El depurador web Fiddler se puede usar con aplicaciones de Windows 8.

1.  Dado que AuthHost se ejecuta en su propio contenedor de aplicaciones para darle la funcionalidad de red privada, debes establecer una clave del Registro: Editor del Registro de Windows 5.00

    **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Image File Execution Options** \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001<dl> <dt>

                     Data type
</dt> <dd>                     DWORD</dd> </dl>

2.  Agrega una regla para AuthHost, ya que esto es lo que genera el tráfico saliente.
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  Agrega una regla de firewall para el tráfico entrante a Fiddler.

Para obtener más información, consulte el [blog sobre cómo usar el depurador Web de Fiddler con aplicaciones de la tienda Windows](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones para el desarrollo de páginas web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Preguntas más frecuentes sobre el agente de autenticación Web](faq-for-web-authentication-broker.md)
</dt> <dt>

[Aplicación de ejemplo del SDK del agente de autenticación Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
