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
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a><span data-ttu-id="6a234-103">Windows 8.1 solo permite URI https, no URI http</span><span class="sxs-lookup"><span data-stu-id="6a234-103">Windows 8.1 allows only https URIs, not http URIs</span></span>

## <a name="platforms"></a><span data-ttu-id="6a234-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="6a234-104">Platforms</span></span>

<dl> <span data-ttu-id="6a234-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6a234-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="6a234-106">Servidores: Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6a234-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="6a234-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a234-107">Description</span></span>

<span data-ttu-id="6a234-108">Aunque las aplicaciones compiladas para Windows 8 pueden incluir URI http y https en sus URI de contenido de aplicación, las aplicaciones compiladas para Windows 8.1 solo pueden incluir URI de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6a234-108">While apps built for Windows 8 can include http and https URIs in their application content URIs, apps built for Windows 8.1 may include only https URIs.</span></span>

<span data-ttu-id="6a234-109">La única excepción son las ContentUriRuless dinámicas que se especifican en el archivo de AppxManifest.xml de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6a234-109">The only exception is for dynamic ContentUriRules that are specified in the app’s AppxManifest.xml file.</span></span> <span data-ttu-id="6a234-110">Con ContentUriRules dinámico, las aplicaciones pueden acceder a dominios o recursos de red adicionales proporcionados por el administrador, como directiva de grupo URI.</span><span class="sxs-lookup"><span data-stu-id="6a234-110">With dynamic ContentUriRules, apps can access additional domains or network resources that are provided by the admin, such as Group Policy URIs.</span></span> <span data-ttu-id="6a234-111">Sin embargo, los ContentUriRules dinámicos solo están disponibles para las aplicaciones de la tienda Windows si cumplen estas condiciones:</span><span class="sxs-lookup"><span data-stu-id="6a234-111">However, dynamic ContentUriRules are only available to Windows Store apps if they meet these conditions:</span></span>

-   <span data-ttu-id="6a234-112">La directiva de grupo está habilitada</span><span class="sxs-lookup"><span data-stu-id="6a234-112">The Group Policy is enabled</span></span>
-   <span data-ttu-id="6a234-113">El paquete ha especificado la funcionalidad enterpriseAuthentication</span><span class="sxs-lookup"><span data-stu-id="6a234-113">The package has specified the enterpriseAuthentication capability</span></span>
-   <span data-ttu-id="6a234-114">El OSMaxVersionTested del paquete es Windows 8.1 o superior</span><span class="sxs-lookup"><span data-stu-id="6a234-114">The package’s OSMaxVersionTested is Windows 8.1 or greater</span></span>

<span data-ttu-id="6a234-115">Las nuevas restricciones de Windows 8.1 forman parte de las restricciones de seguridad mejoradas para proteger aún más la plataforma.</span><span class="sxs-lookup"><span data-stu-id="6a234-115">The new restrictions in Windows 8.1 are part of enhanced security restrictions to further protect the platform.</span></span>

## <a name="manifestations"></a><span data-ttu-id="6a234-116">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="6a234-116">Manifestations</span></span>

<span data-ttu-id="6a234-117">Al ejecutar una aplicación compilada para Windows 8 en Windows 8.1, se permite el uso de URI http en [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) .</span><span class="sxs-lookup"><span data-stu-id="6a234-117">When running an app built for Windows 8 on Windows 8.1, the use of http URIs in the [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) is allowed.</span></span>

## <a name="mitigations"></a><span data-ttu-id="6a234-118">Mitigaciones</span><span class="sxs-lookup"><span data-stu-id="6a234-118">Mitigations</span></span>

<span data-ttu-id="6a234-119">Se recomienda que los desarrolladores de WWA cambien del [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) control [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-MS-WebView>).</span><span class="sxs-lookup"><span data-stu-id="6a234-119">We recommend that WWA developers switch from [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) to the [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) control (<x-ms-webview>).</span></span> <span data-ttu-id="6a234-120">Sin embargo, si necesita compatibilidad con AppCache, IndexedDB, geolocation o el acceso al portapapeles mediante programación, tendrá que seguir usando</span><span class="sxs-lookup"><span data-stu-id="6a234-120">However, if you need support for AppCache, IndexedDB, geolocation, or programmatic clipboard access, you will need to continue using</span></span> <iframe> <span data-ttu-id="6a234-121">por Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="6a234-121">for Windows 8.1.</span></span>

<span data-ttu-id="6a234-122">Uso continuado de</span><span class="sxs-lookup"><span data-stu-id="6a234-122">Continued usage of</span></span> <iframe> <span data-ttu-id="6a234-123">para contenido remoto, necesitará una nueva entrada en el ApplicationContentUriRules de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6a234-123">for remote content will require a new entry in the ApplicationContentUriRules for the app.</span></span> <span data-ttu-id="6a234-124">Las aplicaciones con WebView requieren nuevas entradas en el ApplicationContentUriRules si el contenido web necesita invocar Window. external. Notify para generar un evento [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="6a234-124">Apps with WebView require new entries in the ApplicationContentUriRules if the web content needs to invoke window.external.notify for generating a [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) event.</span></span> <span data-ttu-id="6a234-125">Si no tiene Visual Studio, puede actualizar el manifiesto de la aplicación agregando el siguiente código XML, incluidos los caracteres comodín para los subdominios (por ejemplo, https:// \* . Microsoft.com):</span><span class="sxs-lookup"><span data-stu-id="6a234-125">If you do not have Visual Studio, you can update the app manifest by adding the following XML, including wildcards for subdomains (e.g. https://\*.microsoft.com):</span></span>


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



## <a name="resources"></a><span data-ttu-id="6a234-126">Recursos</span><span class="sxs-lookup"><span data-stu-id="6a234-126">Resources</span></span>

-   [<span data-ttu-id="6a234-127">ApplicationContentUriRules</span><span class="sxs-lookup"><span data-stu-id="6a234-127">ApplicationContentUriRules</span></span>](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<span data-ttu-id="6a234-128"><iframe>objeto de elemento \| <iframe></span><span class="sxs-lookup"><span data-stu-id="6a234-128"><iframe> element \| <iframe> object</span></span>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [<span data-ttu-id="6a234-129">WebView (clase)</span><span class="sxs-lookup"><span data-stu-id="6a234-129">Webview class</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [<span data-ttu-id="6a234-130">Evento WebView. ScriptNotify</span><span class="sxs-lookup"><span data-stu-id="6a234-130">WebView.ScriptNotify event</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 