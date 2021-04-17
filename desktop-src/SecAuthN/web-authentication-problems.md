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
# <a name="web-authentication-problems"></a><span data-ttu-id="90e79-103">Problemas de autenticación web</span><span class="sxs-lookup"><span data-stu-id="90e79-103">Web authentication problems</span></span>

<span data-ttu-id="90e79-104">En este tema se describen las sugerencias de solución de problemas para usar las API de agente de autenticación Web para las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="90e79-104">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span>

-   [<span data-ttu-id="90e79-105">Registros operativos</span><span class="sxs-lookup"><span data-stu-id="90e79-105">Operational logs</span></span>](#operational-logs)
-   [<span data-ttu-id="90e79-106">Usar Fiddler con el agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="90e79-106">Using Fiddler with Web Authentication Broker</span></span>](#using-fiddler-with-web-authentication-broker)
-   [<span data-ttu-id="90e79-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90e79-107">Related topics</span></span>](#related-topics)

## <a name="operational-logs"></a><span data-ttu-id="90e79-108">Registros operativos</span><span class="sxs-lookup"><span data-stu-id="90e79-108">Operational logs</span></span>

<span data-ttu-id="90e79-109">Con frecuencia, los registros operativos ayudan a determinar qué no está funcionando.</span><span class="sxs-lookup"><span data-stu-id="90e79-109">Often you can determine what is not working by using the operational logs.</span></span> <span data-ttu-id="90e79-110">Hay un canal de registro de eventos dedicado Microsoft-Windows-webauth \\ operativo que permite a los desarrolladores de sitios web comprender cómo el agente de autenticación Web está procesando sus páginas Web.</span><span class="sxs-lookup"><span data-stu-id="90e79-110">There is a dedicated event log channel Microsoft-Windows-WebAuth\\Operational that allows website developers to understand how their web pages are being processed by the Web Authentication Broker.</span></span> <span data-ttu-id="90e79-111">Para habilitarlo, inicie eventvwr.exe y habilite el registro operativo en la aplicación y los servicios \\ Microsoft \\ Windows \\ webauth.</span><span class="sxs-lookup"><span data-stu-id="90e79-111">To enable it, launch eventvwr.exe and enable Operational log under the Application and Services\\Microsoft\\Windows\\WebAuth.</span></span> <span data-ttu-id="90e79-112">Además, el agente de autenticación Web anexa una cadena única a la cadena de agente de usuario para identificarse en el servidor Web.</span><span class="sxs-lookup"><span data-stu-id="90e79-112">Also, the Web Authentication Broker appends a unique string to the user agent string to identify itself on the web server.</span></span> <span data-ttu-id="90e79-113">La cadena es "MSAuthHost/1.0".</span><span class="sxs-lookup"><span data-stu-id="90e79-113">The string is "MSAuthHost/1.0".</span></span> <span data-ttu-id="90e79-114">Ten en cuenta que el número de versión podría cambiar en el futuro, por lo que no debes depender de dicho número de versión en tu código.</span><span class="sxs-lookup"><span data-stu-id="90e79-114">Note that the version number may change in the future, so you should not to depend on that version number in your code.</span></span> <span data-ttu-id="90e79-115">A continuación se muestra un ejemplo de la cadena de agente de usuario completa:</span><span class="sxs-lookup"><span data-stu-id="90e79-115">An example of the full user agent string is as follows:</span></span>

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

<span data-ttu-id="90e79-116">Ejemplo de uso de registros operativos</span><span class="sxs-lookup"><span data-stu-id="90e79-116">Example of using operational logs</span></span>

1.  <span data-ttu-id="90e79-117">Habilitar registros operativos</span><span class="sxs-lookup"><span data-stu-id="90e79-117">Enable operational logs</span></span>
2.  <span data-ttu-id="90e79-118">Ejecutar la aplicación social de Contoso</span><span class="sxs-lookup"><span data-stu-id="90e79-118">Run Contoso social application</span></span>![visor de eventos que muestra los registros operativos webauth](images/wab-figure15.png)
3.  <span data-ttu-id="90e79-120">Las entradas de los registros generados se pueden usar para comprender con mayor detalle el comportamiento del agente de autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="90e79-120">The generated logs entries can be used to understand the behavior of Web Authentication Broker in greater detail.</span></span> <span data-ttu-id="90e79-121">En este caso, pueden incluir:</span><span class="sxs-lookup"><span data-stu-id="90e79-121">In this case, these can include:</span></span>
    -   <span data-ttu-id="90e79-122">Navegación - iniciar: registra cuándo se inicia AuthHost y contiene información sobre las direcciones URL de inicio y terminación.</span><span class="sxs-lookup"><span data-stu-id="90e79-122">Navigation Start: Logs when the AuthHost is started and contains information about the start and termination URLs.</span></span>
    -   ![ilustra los detalles de Inicio de navegación](images/wab-figure16.png)
    -   <span data-ttu-id="90e79-124">Navegación - completa: registra la finalización de la carga de una página web.</span><span class="sxs-lookup"><span data-stu-id="90e79-124">Navigation Complete: Logs the completion of loading a web page.</span></span>
    -   <span data-ttu-id="90e79-125">Etiqueta meta: registra cuándo se encuentra una etiqueta meta, incluidos los detalles.</span><span class="sxs-lookup"><span data-stu-id="90e79-125">Meta Tag: Logs when a meta-tag is encountered including the details.</span></span>
    -   <span data-ttu-id="90e79-126">Navegación - finalizar: navegación terminada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="90e79-126">Navigation Terminate: Navigation terminated by the user.</span></span>
    -   <span data-ttu-id="90e79-127">Navegación - error: AuthHost encuentra un error de navegación en una dirección URL e incluye HttpStatusCode.</span><span class="sxs-lookup"><span data-stu-id="90e79-127">Navigation Error: AuthHost encounters a navigation error at a URL including HttpStatusCode.</span></span>
    -   <span data-ttu-id="90e79-128">Navegación - fin: se ha encontrado la dirección URL de terminación.</span><span class="sxs-lookup"><span data-stu-id="90e79-128">Navigation End: Terminating URL is encountered.</span></span>

## <a name="using-fiddler-with-web-authentication-broker"></a><span data-ttu-id="90e79-129">Usar Fiddler con el agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="90e79-129">Using Fiddler with Web Authentication Broker</span></span>

<span data-ttu-id="90e79-130">El depurador web Fiddler se puede usar con aplicaciones de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="90e79-130">The Fiddler web debugger can be used with Windows 8 apps.</span></span>

1.  <span data-ttu-id="90e79-131">Dado que AuthHost se ejecuta en su propio contenedor de aplicaciones para darle la funcionalidad de red privada, debes establecer una clave del Registro: Editor del Registro de Windows 5.00</span><span class="sxs-lookup"><span data-stu-id="90e79-131">Since the AuthHost runs in its own app container to give it the private network capability, you must set a registry key: Windows Registry Editor Version 5.00</span></span>

    <span data-ttu-id="90e79-132">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Image File Execution Options** \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001</span><span class="sxs-lookup"><span data-stu-id="90e79-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Image File Execution Options**\\**authhost.exe**\\**EnablePrivateNetwork** = 00000001</span></span><dl> <dt>

                     Data type
</dt> <dd>                     <span data-ttu-id="90e79-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="90e79-133">DWORD</span></span></dd> </dl>

2.  <span data-ttu-id="90e79-134">Agrega una regla para AuthHost, ya que esto es lo que genera el tráfico saliente.</span><span class="sxs-lookup"><span data-stu-id="90e79-134">Add a rule for the AuthHost as this is what is generating the outbound traffic.</span></span>
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

    

3.  <span data-ttu-id="90e79-135">Agrega una regla de firewall para el tráfico entrante a Fiddler.</span><span class="sxs-lookup"><span data-stu-id="90e79-135">Add a firewall rule for incoming traffic to Fiddler.</span></span>

<span data-ttu-id="90e79-136">Para obtener más información, consulte el [blog sobre cómo usar el depurador Web de Fiddler con aplicaciones de la tienda Windows](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span><span class="sxs-lookup"><span data-stu-id="90e79-136">For more information, see [Blog on using Fiddler web debugger with Windows Store apps](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90e79-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90e79-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90e79-138">Consideraciones para el desarrollo de páginas web</span><span class="sxs-lookup"><span data-stu-id="90e79-138">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="90e79-139">Preguntas más frecuentes sobre el agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="90e79-139">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="90e79-140">Aplicación de ejemplo del SDK del agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="90e79-140">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="90e79-141">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="90e79-141">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
