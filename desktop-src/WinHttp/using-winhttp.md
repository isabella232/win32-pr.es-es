---
description: En esta sección se describe cómo usar la API de C/C++ para los servicios HTTP de Microsoft Windows (WinHTTP) y la interfaz COM que expone el objeto WinHttpRequest.
ms.assetid: 16178bb8-5e95-46a5-825a-880edc402445
title: Usar WinHTTP
ms.topic: article
ms.date: 07/22/2020
ms.openlocfilehash: cda0a7772b88dfd9c03675c522f4b7504ea00b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497501"
---
# <a name="using-winhttp"></a><span data-ttu-id="2c423-103">Usar WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-103">Using WinHTTP</span></span>

<span data-ttu-id="2c423-104">En esta sección se describe cómo usar la API de C/C++ para los servicios HTTP de Microsoft Windows (WinHTTP) y la interfaz COM que expone el objeto **WinHttpRequest** .</span><span class="sxs-lookup"><span data-stu-id="2c423-104">This section describes how to use both the C/C++ API for Microsoft Windows HTTP Services (WinHTTP) and the COM interface exposed by the **WinHttpRequest** Object.</span></span> <span data-ttu-id="2c423-105">Vea [elegir una interfaz WinHTTP](choosing-a-winhttp-interface.md) para obtener una comparación de estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="2c423-105">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span> <span data-ttu-id="2c423-106">También se describe cómo usar las herramientas administrativas incluidas con WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="2c423-106">It also describes how to use the administrative tools included with WinHTTP.</span></span>

## <a name="how-to-topics"></a><span data-ttu-id="2c423-107">Temas de procedimientos</span><span class="sxs-lookup"><span data-stu-id="2c423-107">How-To Topics</span></span>

[<span data-ttu-id="2c423-108">Uso de la API de C/C++ de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-108">Using the WinHTTP C/C++ API</span></span>](using-the-winhttp-c-c---api.md)

-   [<span data-ttu-id="2c423-109">Información general sobre las sesiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-109">WinHTTP Sessions Overview</span></span>](winhttp-sessions-overview.md)
-   [<span data-ttu-id="2c423-110">Controladores HINTERNET en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-110">HINTERNET Handles in WinHTTP</span></span>](hinternet-handles-in-winhttp.md)
-   [<span data-ttu-id="2c423-111">Localizadores de recursos uniformes (URL) en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-111">Uniform Resource Locators (URLs) in WinHTTP</span></span>](uniform-resource-locators--urls--in-winhttp.md)
-   [<span data-ttu-id="2c423-112">Autenticación en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-112">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
-   [<span data-ttu-id="2c423-113">Autenticación de Passport en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-113">Passport Authentication in WinHTTP</span></span>](passport-authentication-in-winhttp.md)
-   [<span data-ttu-id="2c423-114">SSL en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-114">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
-   [<span data-ttu-id="2c423-115">Usar WinHTTP como un ensamblado en paralelo</span><span class="sxs-lookup"><span data-stu-id="2c423-115">Using WinHTTP as a Side-by-side Assembly</span></span>](using-winhttp-as-a-side-by-side-assembly.md)
-   [<span data-ttu-id="2c423-116">Control de cookies en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-116">Cookie Handling in WinHTTP</span></span>](cookie-handling-in-winhttp.md)
-   [<span data-ttu-id="2c423-117">Control de errores en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-117">Error Handling in WinHTTP</span></span>](error-handling-in-winhttp.md)
-   [<span data-ttu-id="2c423-118">Compatibilidad con el AutoProxy WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-118">WinHTTP AutoProxy Support</span></span>](winhttp-autoproxy-support.md)

[<span data-ttu-id="2c423-119">Usar el objeto COM WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="2c423-119">Using the WinHttpRequest COM Object</span></span>](using-the-winhttprequest-com-object.md)

-   [<span data-ttu-id="2c423-120">Recuperación de datos mediante script</span><span class="sxs-lookup"><span data-stu-id="2c423-120">Retrieving Data Using Script</span></span>](retrieving-data-using-script.md)
-   [<span data-ttu-id="2c423-121">Autenticación mediante script</span><span class="sxs-lookup"><span data-stu-id="2c423-121">Authentication Using Script</span></span>](authentication-using-script.md)

[<span data-ttu-id="2c423-122">Uso de las herramientas de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2c423-122">Using WinHTTP Tools</span></span>](using-winhttp-tools.md)

-   [<span data-ttu-id="2c423-123">WinHttpCfg.exe, una herramienta de configuración de certificados</span><span class="sxs-lookup"><span data-stu-id="2c423-123">WinHttpCfg.exe, a Certificate Configuration Tool</span></span>](winhttpcertcfg-exe--a-certificate-configuration-tool.md)
-   [<span data-ttu-id="2c423-124">ProxyCfg.exe, una herramienta de configuración de proxy</span><span class="sxs-lookup"><span data-stu-id="2c423-124">ProxyCfg.exe, a Proxy Configuration Tool</span></span>](proxycfg-exe--a-proxy-configuration-tool.md)
-   [<span data-ttu-id="2c423-125">WinHttpTraceCfg, una herramienta de configuración de seguimiento</span><span class="sxs-lookup"><span data-stu-id="2c423-125">WinHttpTraceCfg, a Trace Configuration Tool</span></span>](winhttptracecfg-exe--a-trace-configuration-tool.md)

 

 



