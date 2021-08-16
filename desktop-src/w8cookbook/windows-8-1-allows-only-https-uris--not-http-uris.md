---
title: URI en Windows 8.1
description: Windows 8.1 solo permite los URI https, no los URI http
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3246cad0fb6114a3a01d781ed990e0c277547e2b9ee489572c8124a23e7e81b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028813"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 solo permite los URI https, no los URI http

## <a name="platforms"></a>Plataformas

<dl> Clientes: Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

Aunque las aplicaciones creadas para Windows 8 pueden incluir URI http y https en sus URI de contenido de la aplicación, las aplicaciones creadas para Windows 8.1 pueden incluir solo URI https.

La única excepción es para contentUriRules dinámicos que se especifican en el archivo de AppxManifest.xml aplicación. Con ContentUriRules dinámico, las aplicaciones pueden acceder a dominios o recursos de red adicionales proporcionados por el administrador, como directiva de grupo URI. Sin embargo, contentUriRules dinámico solo está disponible para Windows store si cumplen estas condiciones:

-   El directiva de grupo está habilitado
-   El paquete ha especificado la funcionalidad enterpriseAuthentication.
-   OSMaxVersionTested del paquete es Windows 8.1 o superior

Las nuevas restricciones de Windows 8.1 forman parte de las restricciones de seguridad mejoradas para proteger aún más la plataforma.

## <a name="manifestations"></a>Manifestaciones

Al ejecutar una aplicación creada para Windows 8 en Windows 8.1, se permite el uso de URI http en [ApplicationContentUriRules.](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)

## <a name="mitigations"></a>Mitigaciones

Se recomienda que los desarrolladores de WWA cambien de al [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) control [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-ms-webview>). Sin embargo, si necesita compatibilidad con AppCache, IndexedDB, geolocalización o acceso mediante programación al Portapapeles, deberá seguir usando <iframe> para Windows 8.1.

Uso continuado de <iframe> para el contenido remoto requerirá una nueva entrada en ApplicationContentUriRules para la aplicación. Las aplicaciones con WebView requieren nuevas entradas en ApplicationContentUriRules si el contenido web necesita invocar window.external.notify para generar un [evento ScriptNotify.](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) Si no tiene Visual Studio, puede actualizar el manifiesto de aplicación agregando el siguiente XML, incluidos caracteres comodín para subdominios (por ejemplo, https:// \* .microsoft.com):


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
-   [<iframe> objeto \| <iframe> de elemento](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [Clase Webview](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [Evento WebView.ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 