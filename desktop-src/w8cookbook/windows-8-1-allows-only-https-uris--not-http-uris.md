---
title: URI en Windows 8.1
description: Windows 8.1 solo permite URI https, no URI http
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421254"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 solo permite URI https, no URI http

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

Aunque las aplicaciones compiladas para Windows 8 pueden incluir URI http y https en sus URI de contenido de aplicación, las aplicaciones compiladas para Windows 8.1 solo pueden incluir URI de HTTPS.

La única excepción son las ContentUriRuless dinámicas que se especifican en el archivo de AppxManifest.xml de la aplicación. Con ContentUriRules dinámico, las aplicaciones pueden acceder a dominios o recursos de red adicionales proporcionados por el administrador, como directiva de grupo URI. Sin embargo, los ContentUriRules dinámicos solo están disponibles para las aplicaciones de la tienda Windows si cumplen estas condiciones:

-   La directiva de grupo está habilitada
-   El paquete ha especificado la funcionalidad enterpriseAuthentication
-   El OSMaxVersionTested del paquete es Windows 8.1 o superior

Las nuevas restricciones de Windows 8.1 forman parte de las restricciones de seguridad mejoradas para proteger aún más la plataforma.

## <a name="manifestations"></a>Manifestaciones

Al ejecutar una aplicación compilada para Windows 8 en Windows 8.1, se permite el uso de URI http en [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) .

## <a name="mitigations"></a>Mitigaciones

Se recomienda que los desarrolladores de WWA cambien del [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) control [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-MS-WebView>). Sin embargo, si necesita compatibilidad con AppCache, IndexedDB, geolocation o el acceso al portapapeles mediante programación, tendrá que seguir usando <iframe> por Windows 8.1.

Uso continuado de <iframe> para contenido remoto, necesitará una nueva entrada en el ApplicationContentUriRules de la aplicación. Las aplicaciones con WebView requieren nuevas entradas en el ApplicationContentUriRules si el contenido web necesita invocar Window. external. Notify para generar un evento [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) . Si no tiene Visual Studio, puede actualizar el manifiesto de la aplicación agregando el siguiente código XML, incluidos los caracteres comodín para los subdominios (por ejemplo, https:// \* . Microsoft.com):


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a>Recursos

-   [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<iframe>objeto de elemento \| <iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [WebView (clase)](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [Evento WebView. ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 