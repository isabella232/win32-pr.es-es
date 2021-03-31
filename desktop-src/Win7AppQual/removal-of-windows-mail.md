---
description: .
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Eliminación de Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836b2f447735c8e3595955ca7e99f1ae818c3d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278787"
---
# <a name="removal-of-windows-mail"></a><span data-ttu-id="a8064-103">Eliminación de Windows Mail</span><span class="sxs-lookup"><span data-stu-id="a8064-103">Removal of Windows Mail</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="a8064-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="a8064-104">Affected Platforms</span></span>

<span data-ttu-id="a8064-105">**Clientes** : Windows 7</span><span class="sxs-lookup"><span data-stu-id="a8064-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="a8064-106">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8064-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="a8064-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="a8064-107">Feature Impact</span></span>

<span data-ttu-id="a8064-108">**Gravedad** alta</span><span class="sxs-lookup"><span data-stu-id="a8064-108">**Severity** - High</span></span>  
<span data-ttu-id="a8064-109">**Frecuencia** : alta</span><span class="sxs-lookup"><span data-stu-id="a8064-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="a8064-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8064-110">Description</span></span>

<span data-ttu-id="a8064-111">Microsoft está dejando de usar la utilidad Windows Mail y deshabilitando la API CoStartOutlookExpress.</span><span class="sxs-lookup"><span data-stu-id="a8064-111">Microsoft is deprecating the Windows Mail utility and disabling the API CoStartOutlookExpress.</span></span> <span data-ttu-id="a8064-112">Las otras API de correo se han marcado como desusadas y están preparadas para su eliminación en una versión posterior de Windows.</span><span class="sxs-lookup"><span data-stu-id="a8064-112">The other mail APIs have been marked as deprecated and are slated for removal in a later Windows version.</span></span> <span data-ttu-id="a8064-113">Sin embargo, las API documentadas públicamente que no estén marcadas como desusadas u obsoletas seguirán funcionando en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a8064-113">However, the publicly documented APIs that are not marked as deprecated or obsolete will continue to function in Windows 7.</span></span> <span data-ttu-id="a8064-114">Los archivos binarios permanecerán en los sistemas de los usuarios y seguirán siendo accesibles a través de las API, específicamente en los casos mencionados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a8064-114">Binaries will remain on the users' systems and will continue to be accessible via the APIs, specifically in the cases mentioned above.</span></span> <span data-ttu-id="a8064-115">Además, los archivos de correo electrónico (. eml) y News (. NWS) de los usuarios permanecerán en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a8064-115">In addition, the users' email (.eml) and news (.nws) files will remain on the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="a8064-116">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="a8064-116">Manifestation of Impact</span></span>

<span data-ttu-id="a8064-117">La eliminación de Windows Mail da como resultado lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a8064-117">Removal of Windows Mail results in the following:</span></span>

-   <span data-ttu-id="a8064-118">Todos los puntos de entrada a correo y contactos de Windows (por ejemplo, menú Inicio, accesos directos creados por el usuario, Inicio > ejecución, etc.) se quitan o deshabilitan.</span><span class="sxs-lookup"><span data-stu-id="a8064-118">All entry points to Windows Mail and Contacts (for example, Start Menu, user-created Shortcuts, Start -> Run, and so on) are removed or disabled.</span></span> <span data-ttu-id="a8064-119">Algunos de ellos se quitan por completo, se producirá un error en otros al intentar iniciar.</span><span class="sxs-lookup"><span data-stu-id="a8064-119">Some of these are completely removed, others will fail when trying to launch.</span></span>
-   <span data-ttu-id="a8064-120">Todos los archivos DLL se incluyen en el cuadro</span><span class="sxs-lookup"><span data-stu-id="a8064-120">All DLLs ship in the box</span></span>
-   <span data-ttu-id="a8064-121">Las API documentadas públicamente continúan funcionando como en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8064-121">Publicly documented APIs continue to work as they did in Windows Vista</span></span>
-   <span data-ttu-id="a8064-122">Todas las API que intenten iniciar la interfaz de usuario principal del explorador se han modificado para crear un error silencioso.</span><span class="sxs-lookup"><span data-stu-id="a8064-122">Any APIs that attempt to launch the main browser UI have been modified to create a silent failure.</span></span> <span data-ttu-id="a8064-123">La función devolverá un valor correcto, pero no mostrará la interfaz de usuario al usuario.</span><span class="sxs-lookup"><span data-stu-id="a8064-123">The function will return success, but will not show the UI to the user.</span></span> <span data-ttu-id="a8064-124">Las API que llaman a otros cuadros de diálogo (por ejemplo, el administrador de trabajos de impresión o el cuadro de diálogo cuentas) siguen mostrando esa interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="a8064-124">APIs that call other dialog boxes (for example, the Spooler or the Accounts dialog) continue to show that UI</span></span>
-   <span data-ttu-id="a8064-125">Los controladores de protocolo (mailto, LDAP, News, SNEWS, NNTP) no se asociarán a Windows Mail ni a los contactos.</span><span class="sxs-lookup"><span data-stu-id="a8064-125">Protocol (mailto, ldap, news, snews, nntp) handlers will not be associated with Windows Mail or Contacts.</span></span> <span data-ttu-id="a8064-126">Al intentar iniciarlos, los clientes verán un cuadro de diálogo de error que apuntan a la ubicación en la que pueden establecer estas asociaciones en otro programa.</span><span class="sxs-lookup"><span data-stu-id="a8064-126">When attempting to launch these, customers will see an error dialog pointing them to the location where they can set these associations to another program</span></span>
-   <span data-ttu-id="a8064-127">Las asociaciones de archivo (. eml,. NWS,. contact,. Group,. WAB,. p7c,. VFC) están dañadas o deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="a8064-127">File associations (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) are broken or disabled.</span></span> <span data-ttu-id="a8064-128">Al intentar abrir un archivo con estas extensiones, los clientes recibirán un cuadro de diálogo que les ofrece otras aplicaciones que se instalan y que pueden apuntar a una página web que ofrece soluciones.</span><span class="sxs-lookup"><span data-stu-id="a8064-128">When attempting to open a file with these extensions, customers will get a dialog box offering them other apps that are installed that they can use and point them to a webpage that offers solutions</span></span>
-   <span data-ttu-id="a8064-129">Los archivos de usuario (por ejemplo, los archivos o mensajes de contacto) permanecen en el sistema en el escenario de actualización</span><span class="sxs-lookup"><span data-stu-id="a8064-129">Any user files (for example, contact files or messages) remain on the system in the upgrade scenario</span></span>
-   <span data-ttu-id="a8064-130">La carpeta contactos está oculta de forma predeterminada para que los clientes no la vean</span><span class="sxs-lookup"><span data-stu-id="a8064-130">The Contacts folder is hidden by default so customers will not see it</span></span>
-   <span data-ttu-id="a8064-131">Las API se marcan como desusadas en MSDN</span><span class="sxs-lookup"><span data-stu-id="a8064-131">APIs are marked as deprecated in MSDN</span></span>
-   <span data-ttu-id="a8064-132">Se ha quitado la función de vista previa de archivo</span><span class="sxs-lookup"><span data-stu-id="a8064-132">The file preview function is removed</span></span>
-   <span data-ttu-id="a8064-133">Se quitan los enlaces de Shell en el menú contextual</span><span class="sxs-lookup"><span data-stu-id="a8064-133">Shell hooks in the right-click menu are removed</span></span>
-   <span data-ttu-id="a8064-134">Se quita la función de búsqueda de archivos</span><span class="sxs-lookup"><span data-stu-id="a8064-134">The file search function is removed</span></span>

## <a name="mitigation"></a><span data-ttu-id="a8064-135">Mitigación</span><span class="sxs-lookup"><span data-stu-id="a8064-135">Mitigation</span></span>

<span data-ttu-id="a8064-136">Los usuarios deben instalar Windows Live Mail o cualquier otro producto de correo que pueda leer archivos. eml y. nws.</span><span class="sxs-lookup"><span data-stu-id="a8064-136">Users should install Windows Live Mail or any other mail product that is able to read .eml and .nws files.</span></span>

## <a name="solution"></a><span data-ttu-id="a8064-137">Solución</span><span class="sxs-lookup"><span data-stu-id="a8064-137">Solution</span></span>

<span data-ttu-id="a8064-138">Detecta si hay un controlador de correo predeterminado instalado.</span><span class="sxs-lookup"><span data-stu-id="a8064-138">Detect if there is a default mail handler installed.</span></span> <span data-ttu-id="a8064-139">Si no es así, aconseje a los usuarios que instalen Windows Live Mail o cualquier otro producto que pueda leer archivos. eml y. nws.</span><span class="sxs-lookup"><span data-stu-id="a8064-139">If not, advise user to install Windows Live Mail or any other product that is able to read .eml and .nws files.</span></span>

<span data-ttu-id="a8064-140">No diseñe código que llame a la API de la interfaz de usuario de Windows Mail, ya que no funcionará.</span><span class="sxs-lookup"><span data-stu-id="a8064-140">Do not design code that calls the Windows Mail UI API, since it will not work.</span></span> <span data-ttu-id="a8064-141">Debe encontrar otras maneras de acceder a los archivos. eml y. nws.</span><span class="sxs-lookup"><span data-stu-id="a8064-141">You must find other ways to access the .eml and .nws files.</span></span> <span data-ttu-id="a8064-142">Además, en cuanto sea factible, descontinúe su dependencia en todas las demás API de Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="a8064-142">In addition, as soon as is feasible, discontinue your reliance on all other Windows Mail APIs.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="a8064-143">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="a8064-143">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="a8064-144">Ejecute la aplicación en un entorno de Windows 7 para asegurarse de que la aplicación no intente llamar a la API de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a8064-144">Exercise your application in a Windows 7 environment to ensure that the application does not try to call the UI API.</span></span>
-   <span data-ttu-id="a8064-145">Como alternativa, puede ejecutar el kit de herramientas de compatibilidad de aplicaciones (ACT) mediante el evaluador de compatibilidad de Windows (WCE) para localizar cualquier posible problema debido al desuso de esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="a8064-145">Alternatively, you can run the Application Compatibility Toolkit (ACT) using the Windows Compatibility Evaluator (WCE) to locate any potential issues due to the deprecation of this functionality.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="a8064-146">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="a8064-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="a8064-147">Descarga del kit de herramientas de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a8064-147">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)  
</dl>

 

 
