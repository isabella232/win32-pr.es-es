---
title: Llamar a WDS desde páginas web
description: Puede llamar a Microsoft Windows Desktop Search (WDS) desde cualquier página web que cree o mantenga mediante el objeto auxiliar de explorador (BHO) y Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "104077424"
---
# <a name="calling-wds-from-web-pages"></a><span data-ttu-id="d08d1-103">Llamar a WDS desde páginas web</span><span class="sxs-lookup"><span data-stu-id="d08d1-103">Calling WDS from Web Pages</span></span>

> [!NOTE]
> <span data-ttu-id="d08d1-104">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d08d1-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d08d1-105">En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d08d1-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="d08d1-106">Puede llamar a Microsoft Windows Desktop Search (WDS) desde cualquier página web que cree o mantenga mediante el objeto auxiliar de explorador (BHO) y Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d08d1-106">You can call Microsoft Windows Desktop Search (WDS) from any webpage you create or maintain using the Browser Helper Object (BHO) and Windows Internet Explorer.</span></span> <span data-ttu-id="d08d1-107">Puede ver cómo funciona esto en la Página Web de MSN.</span><span class="sxs-lookup"><span data-stu-id="d08d1-107">You can see how this works on the MSN webpage.</span></span> <span data-ttu-id="d08d1-108">Encima del cuadro de búsqueda en https://www.msn.com hay varios tipos de búsqueda: Web, News, images, Desktop, Encarta y local.</span><span class="sxs-lookup"><span data-stu-id="d08d1-108">Above the search box on https://www.msn.com are several search types: Web, News, Images, Desktop, Encarta, and Local.</span></span> <span data-ttu-id="d08d1-109">Si hace clic en escritorio, los parámetros de búsqueda se pasan a la búsqueda de escritorio de Windows, que busca en el catálogo y muestra los resultados en la interfaz de usuario de WDS.</span><span class="sxs-lookup"><span data-stu-id="d08d1-109">If you click Desktop, the search parameters are passed to Windows Desktop Search, which searches the catalog and displays results in the WDS user interface.</span></span> <span data-ttu-id="d08d1-110">Para que los usuarios puedan iniciar una búsqueda en el escritorio desde las páginas web, el WDSBHO debe estar instalado y habilitado en sus sistemas, las páginas web deben estar registradas con WDS como una dirección URL permitida y debe crear un vínculo para pasar la consulta User-enetered a WDS.</span><span class="sxs-lookup"><span data-stu-id="d08d1-110">For users to start a desktop search from your webpage(s), the WDSBHO must be installed and enabled on their systems, your webpage(s) must be registered with WDS as an allowed URL, and you must create a link to pass the user-enetered query to WDS.</span></span>

## <a name="enabling-the-wds-browser-help-object"></a><span data-ttu-id="d08d1-111">Habilitar el objeto de ayuda del explorador de WDS</span><span class="sxs-lookup"><span data-stu-id="d08d1-111">Enabling the WDS Browser Help Object</span></span>

<span data-ttu-id="d08d1-112">El BHO se instala y se habilita en Internet Explorer de forma predeterminada al instalar WDS, pero puede comprobar fácilmente que no se ha deshabilitado o desinstalado.</span><span class="sxs-lookup"><span data-stu-id="d08d1-112">The BHO is installed and enabled within Internet Explorer by default when you install WDS, but you can easily verify that it hasn't been disabled or uninstalled.</span></span> <span data-ttu-id="d08d1-113">En el sistema de un usuario, abra Internet Explorer, seleccione **Opciones de Internet** en el menú **herramientas** , haga clic en la pestaña **programas** y, a continuación, haga clic en **Administrar complementos**.</span><span class="sxs-lookup"><span data-stu-id="d08d1-113">On a user's system, open Internet Explorer , select **Internet Options** from the **Tools** menu, click the **Programs** tab, and then click **Manage Add-Ons**.</span></span> <span data-ttu-id="d08d1-114">En la lista de complementos, busque la clase dsWebAllowBHO y asegúrese de que está habilitada.</span><span class="sxs-lookup"><span data-stu-id="d08d1-114">In your list of add-ons, look for the dsWebAllowBHO Class and make sure it is enabled.</span></span> <span data-ttu-id="d08d1-115">Cuando se deshabilita el BHO, WDS seguirá funcionando con normalidad; sin embargo, no podrá buscar en el escritorio desde una página web.</span><span class="sxs-lookup"><span data-stu-id="d08d1-115">When the BHO is disabled, WDS will continue to work normally; however, you will not be able to search the desktop from a webpage.</span></span>

<span data-ttu-id="d08d1-116">Las dos opciones siguientes para permitir una búsqueda en el escritorio ejecutarán la búsqueda localmente con la aplicación de búsqueda registrada.</span><span class="sxs-lookup"><span data-stu-id="d08d1-116">Both of the following options for allowing a desktop search will execute the search locally with the registered search application.</span></span>

## <a name="registering-web-page-urls"></a><span data-ttu-id="d08d1-117">Registro de direcciones URL de páginas web</span><span class="sxs-lookup"><span data-stu-id="d08d1-117">Registering Web Page URLs</span></span>

<span data-ttu-id="d08d1-118">El registro incluye una lista de direcciones URL de dominio "permitidas" desde las que se puede llamar a WDS.</span><span class="sxs-lookup"><span data-stu-id="d08d1-118">The Registry includes a list of "allowed" domain URLs from which WDS can be called.</span></span> <span data-ttu-id="d08d1-119">Para incluir las páginas web, debe mostrar las direcciones URL de dominio como REG \_ SZ en el registro como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="d08d1-119">To include your webpage(s), you need to list your domain URL(s) as REG\_SZ in the Registry as follows:</span></span>

<span data-ttu-id="d08d1-120">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **permitido**\\*<number>* = <domainURL></span><span class="sxs-lookup"><span data-stu-id="d08d1-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows Desktop Search**\\**DSW**\\**Allowed**\\*<number>* = <domainURL></span></span>

<span data-ttu-id="d08d1-121">Donde **<number>** se numera secuencialmente, y **<domainURL>** es la dirección URL de la Página Web de la que desea permitir búsquedas de WDS.</span><span class="sxs-lookup"><span data-stu-id="d08d1-121">Where **<number>** is sequentially numbered, and **<domainURL>** is the URL of the Web Page you want to allow WDS searches from.</span></span> <span data-ttu-id="d08d1-122">Esta cadena de dirección URL puede incluir el asterisco comodín \* al principio o al final de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="d08d1-122">This URL string can include the wildcard asterisk \* at the beginning or end of the URL.</span></span> <span data-ttu-id="d08d1-123">Por ejemplo, si la cadena es " \* . mydomain.com", puede iniciar una búsqueda de WDS desde https://www.mydomain.com y https://mydomain.com .</span><span class="sxs-lookup"><span data-stu-id="d08d1-123">For example, if the string is "\*.mydomain.com", then you can start a WDS search from both https://www.mydomain.com and https://mydomain.com.</span></span>

## <a name="enabling-desktop-search-by-url"></a><span data-ttu-id="d08d1-124">Habilitación de la búsqueda en el escritorio por dirección URL</span><span class="sxs-lookup"><span data-stu-id="d08d1-124">Enabling Desktop Search by URL</span></span>

<span data-ttu-id="d08d1-125">Otra opción que no requiere acceso al registro es usar la siguiente dirección URL en las páginas web:</span><span class="sxs-lookup"><span data-stu-id="d08d1-125">Another option that does not require access to the Registry is to use the following URL on your webpage(s):</span></span>

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

<span data-ttu-id="d08d1-126">donde **query** es la cadena con codificación URL en la que el usuario realiza la búsqueda, incluidos los términos de [Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md) .</span><span class="sxs-lookup"><span data-stu-id="d08d1-126">where **QUERY** is the URL-encoded string the user is searching on, including any [Advanced Query Syntax](-search-2x-wds-aqsreference.md) terms.</span></span>

 

 




