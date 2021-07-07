---
description: En este tema se describen las sugerencias de solución de problemas para usar las API del Agente de autenticación web para las páginas web.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Problemas de autenticación web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f996527c58b9620b8417ac3e6cdd6e0f61bd5217
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353668"
---
# <a name="web-authentication-problems"></a>Problemas de autenticación web

En este tema se describen las sugerencias de solución de problemas para usar las API del Agente de autenticación web para las páginas web.

-   [Registros operativos](#operational-logs)
-   [Uso de Fiddler con el Agente de autenticación web](#using-fiddler-with-web-authentication-broker)
-   [Temas relacionados](#related-topics)

## <a name="operational-logs"></a>Registros operativos

Con frecuencia, los registros operativos ayudan a determinar qué no está funcionando. Hay un canal de registro de eventos dedicado Microsoft-Windows-WebAuth Operational que permite a los desarrolladores de sitios web comprender cómo el Agente de autenticación web procesa sus páginas \\ web. Para habilitarlo, inicie eventvwr.exe y habilite el registro operativo en La aplicación y servicios \\ Microsoft \\ Windows \\ WebAuth. Además, el Agente de autenticación web anexa una cadena única a la cadena del agente de usuario para identificarse en el servidor web. La cadena es "MSAuthHost/1.0". Ten en cuenta que el número de versión podría cambiar en el futuro, por lo que no debes depender de dicho número de versión en tu código. A continuación se muestra un ejemplo de la cadena de agente de usuario completa:

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

Ejemplo de uso de registros operativos

1.  Habilitar registros operativos
2.  Ejecución de la aplicación social Contoso![visor de eventos que muestra los registros operativos webauth](images/wab-figure15.png)
3.  Las entradas de registros generadas se pueden usar para comprender el comportamiento del Agente de autenticación web con más detalle. En este caso, pueden incluir:
    -   Navegación - iniciar: registra cuándo se inicia AuthHost y contiene información sobre las direcciones URL de inicio y terminación.
    -   ![ilustra los detalles de Inicio de navegación](images/wab-figure16.png)
    -   Navegación - completa: registra la finalización de la carga de una página web.
    -   Etiqueta meta: registra cuándo se encuentra una etiqueta meta, incluidos los detalles.
    -   Navegación - finalizar: navegación terminada por el usuario.
    -   Navegación - error: AuthHost encuentra un error de navegación en una dirección URL e incluye HttpStatusCode.
    -   Navegación - fin: se ha encontrado la dirección URL de terminación.

## <a name="using-fiddler-with-web-authentication-broker"></a>Uso de Fiddler con el Agente de autenticación web

El depurador web de Fiddler se puede usar con Windows 8 aplicaciones.

1.  Dado que AuthHost se ejecuta en su propio contenedor de aplicaciones para darle la funcionalidad de red privada, debes establecer una clave del Registro: Editor del Registro de Windows 5.00

    **HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** Image File Execution \\ **Options** \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001<dl> <dt>

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

Para obtener más información, vea [Blog sobre el uso del depurador web de Fiddler con Windows store.](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones para el desarrollo de páginas web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Preguntas más frecuentes sobre el Agente de autenticación web](faq-for-web-authentication-broker.yml)
</dt> <dt>

[Aplicación de ejemplo del SDK del Agente de autenticación web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041&preserve-view=true)
</dt> </dl>

 

 
