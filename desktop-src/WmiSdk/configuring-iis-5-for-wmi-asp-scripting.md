---
description: Toda la configuración de autenticación se realiza a través del Administrador de servicios Internet.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Configuración de IIS 5,0 y versiones posteriores para el scripting de ASP de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4b5ddde139b3eef32fd7c80f4cca4e10fd816a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715851"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a><span data-ttu-id="9e769-103">Configuración de IIS 5,0 y versiones posteriores para el scripting de ASP de WMI</span><span class="sxs-lookup"><span data-stu-id="9e769-103">Configuring IIS 5.0 and Later for WMI ASP Scripting</span></span>

<span data-ttu-id="9e769-104">Toda la configuración de autenticación se realiza a través del Administrador de servicios Internet.</span><span class="sxs-lookup"><span data-stu-id="9e769-104">All authentication settings are made through the Internet Services Manager.</span></span>

<span data-ttu-id="9e769-105">Al configurar Internet Information Server (IIS) 5,0 y la seguridad de IIS 6,0 para los scripts ASP de WMI, tenga en cuenta los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="9e769-105">When configuring Internet Information Server (IIS) 5.0 and IIS 6.0 security for WMI ASP scripts, consider the following issues:</span></span>

-   [<span data-ttu-id="9e769-106">Nivel de autenticación</span><span class="sxs-lookup"><span data-stu-id="9e769-106">Authentication level</span></span>](#authentication-level)

    <span data-ttu-id="9e769-107">Puede configurar en el nivel de servidor, directorio o archivo.</span><span class="sxs-lookup"><span data-stu-id="9e769-107">You can configure at the server, directory, or file level.</span></span>

-   [<span data-ttu-id="9e769-108">Configuración de autenticación</span><span class="sxs-lookup"><span data-stu-id="9e769-108">Authentication setting</span></span>](#authentication-setting)

    <span data-ttu-id="9e769-109">Puede establecer la autenticación en las ventanas anónimas, integradas o en ambas.</span><span class="sxs-lookup"><span data-stu-id="9e769-109">You can set authentication to Anonymous, Integrated Windows, or both.</span></span>

-   [<span data-ttu-id="9e769-110">Protección</span><span class="sxs-lookup"><span data-stu-id="9e769-110">Protection</span></span>](#protection)

    <span data-ttu-id="9e769-111">Puede configurar el ASP para que se ejecute en proceso (protección baja) o fuera de proceso mediante Dllhost.exe (protección media o alta).</span><span class="sxs-lookup"><span data-stu-id="9e769-111">You can set the ASP to run in-process (low protection), or out-of-process by using Dllhost.exe (medium or high protection).</span></span>

## <a name="authentication-level"></a><span data-ttu-id="9e769-112">Nivel de autenticación</span><span class="sxs-lookup"><span data-stu-id="9e769-112">Authentication Level</span></span>

<span data-ttu-id="9e769-113">Para mayor seguridad, puede configurar la autenticación en el nivel de directorio o de archivo.</span><span class="sxs-lookup"><span data-stu-id="9e769-113">For added security, you can configure the authentication at the directory or file level.</span></span>

<span data-ttu-id="9e769-114">Si la autenticación se establece en el nivel de servidor, todos los archivos y directorios posteriores se adhieren a la autenticación del servidor, a menos que se modifiquen explícitamente en el nivel de directorio o archivo.</span><span class="sxs-lookup"><span data-stu-id="9e769-114">If authentication is set at the server level, all subsequent directories and files adhere to the server authentication unless explicitly altered at the directory or file level.</span></span> <span data-ttu-id="9e769-115">Puede crear una estructura de directorios que contenga todos los scripts ASP de WMI donde las páginas HTML y los ASP específicos de WMI se pueden configurar independientemente del resto del servidor.</span><span class="sxs-lookup"><span data-stu-id="9e769-115">You can create a directory structure to contain all WMI ASP scripts where HTML pages and ASPs specific to WMI can be configured independently from the rest of the server.</span></span> <span data-ttu-id="9e769-116">Realice el procedimiento siguiente para cambiar el nivel de autenticación de un servidor, directorio o archivo.</span><span class="sxs-lookup"><span data-stu-id="9e769-116">Perform the following procedure to change the authentication level of a server, directory, or file.</span></span>

<span data-ttu-id="9e769-117">**Para establecer la autenticación en cualquier nivel**</span><span class="sxs-lookup"><span data-stu-id="9e769-117">**To set the authentication at any level**</span></span>

1.  <span data-ttu-id="9e769-118">En el panel de control, haga doble clic en **herramientas administrativas** y, a continuación, haga doble clic en el complemento IIS.</span><span class="sxs-lookup"><span data-stu-id="9e769-118">In Control Panel, double-click **Administrative Tools**, and then double-click the IIS snap-in.</span></span>

2.  <span data-ttu-id="9e769-119">Busque el icono de la página ASP y, a continuación, abra las propiedades del nivel que se va a establecer, que puede ser servidor, directorio o archivo.</span><span class="sxs-lookup"><span data-stu-id="9e769-119">Locate the ASP page icon, and then open the properties for the level to set, which can be server, directory, or file.</span></span>

    > [!Note]  
    > <span data-ttu-id="9e769-120">La configuración de autenticación se encuentra en la pestaña **seguridad de directorios** o **seguridad de archivos** de la hoja de **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="9e769-120">Authentication settings are located on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

     

## <a name="authentication-setting"></a><span data-ttu-id="9e769-121">Configuración de autenticación</span><span class="sxs-lookup"><span data-stu-id="9e769-121">Authentication Setting</span></span>

<span data-ttu-id="9e769-122">En el caso de los scripts ASP de WMI, la combinación de autenticación anónima desactivada (desactivada) y la autenticación integrada de Windows activada (activada) proporciona una mayor oportunidad para establecer la seguridad.</span><span class="sxs-lookup"><span data-stu-id="9e769-122">For WMI ASP scripts, the combination of Anonymous authentication turned off (unchecked), and Integrated Windows authentication turned on (checked) provides greater opportunity to set security.</span></span> <span data-ttu-id="9e769-123">Para usar las opciones de autenticación de NT LAN Manager (NTLM), Passport o Digest de IIS, debe activar los privilegios de habilitación remota, ya que el usuario se trata como una identidad de red y se registra de forma remota.</span><span class="sxs-lookup"><span data-stu-id="9e769-123">To use NT LAN Manager (NTLM), Passport, or Digest IIS authentication settings, you must turn on the remote enable privileges, because the user is treated as a network identity and logged remotely.</span></span> <span data-ttu-id="9e769-124">La configuración de habilitación remota no es necesaria para la autenticación anónima y básica.</span><span class="sxs-lookup"><span data-stu-id="9e769-124">The remote enable setting is not required for Anonymous and Basic authentication.</span></span> <span data-ttu-id="9e769-125">Sin embargo, el sistema es mucho menos seguro cuando se utiliza la autenticación anónima y la autenticación básica.</span><span class="sxs-lookup"><span data-stu-id="9e769-125">However, the system is much less secure when you are using Anonymous and Basic authentication.</span></span>

<span data-ttu-id="9e769-126">Si se usa la autenticación anónima con o sin la autenticación integrada de Windows, el enfoque más seguro consiste en usar un inicio de sesión que requiera que un usuario escriba un nombre de usuario y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="9e769-126">If Anonymous authentication is used with or without Integrated Windows authentication, the most secure approach is to use a logon that requires a user to enter a username and password.</span></span> <span data-ttu-id="9e769-127">El inicio de sesión predeterminado es la identidad de IIS, pero se puede crear un inicio de sesión con permisos específicos adecuados para los scripts ASP de WMI que se pueden usar como cuenta para las conexiones anónimas o de invitado.</span><span class="sxs-lookup"><span data-stu-id="9e769-127">The default logon is the IIS identity, but a logon can be created by using specific permissions suited for the WMI ASP Scripts that can be used as the account for the anonymous or guest connections.</span></span>

<span data-ttu-id="9e769-128">Si elige un identificador de inicio de sesión que no sea una identidad de IIS, desactive la casilla **permitir que IIS controle la contraseña** y escriba la contraseña correcta.</span><span class="sxs-lookup"><span data-stu-id="9e769-128">If you choose a logon identifier that is not an IIS identity, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="9e769-129">Esto obliga a todas las conexiones anónimas o de invitado a usar el identificador de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="9e769-129">This forces all anonymous or guest connections to use the logon identifier.</span></span> <span data-ttu-id="9e769-130">Al crear un inicio de sesión independiente de la identidad de IIS, se pueden controlar los privilegios de una cuenta que tenga acceso a WMI sin que afecte a los demás directorios o archivos del servidor IIS, a menos que la autenticación se establezca en el nivel de servidor.</span><span class="sxs-lookup"><span data-stu-id="9e769-130">By creating a logon separate from the IIS identity, the privileges of an account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="9e769-131">Realice el procedimiento siguiente para establecer los requisitos de autenticación para la página ASP con el complemento IIS en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="9e769-131">Perform the following procedure to set the authentication requirements for the ASP page using the IIS snap-in in the Control Panel.</span></span>

<span data-ttu-id="9e769-132">**Para acceder a la configuración de la cuenta**</span><span class="sxs-lookup"><span data-stu-id="9e769-132">**To get to the account setting**</span></span>

1.  <span data-ttu-id="9e769-133">En el panel de control, haga doble clic en el icono **herramientas administrativas** , abra el complemento IIS, busque la página ASP y abra las propiedades del nivel que se va a establecer, que puede ser servidor, directorio o archivo.</span><span class="sxs-lookup"><span data-stu-id="9e769-133">In Control Panel, double-click the **Administrative Tools** icon, open the IIS snap-in, locate your ASP page, and open the properties of the level to set, which can be server, directory, or file.</span></span>

    <span data-ttu-id="9e769-134">La configuración de autenticación se puede encontrar en la pestaña **seguridad de directorios** o **seguridad de archivos** de la hoja de **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="9e769-134">Authentication settings can be found on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

2.  <span data-ttu-id="9e769-135">En el área autenticación anónima, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="9e769-135">In the Anonymous authentication area, click **Edit**.</span></span>

3.  <span data-ttu-id="9e769-136">Si se selecciona un identificador de inicio de sesión distinto de la identidad de IIS, desactive la casilla **permitir que IIS controle la contraseña** y escriba la contraseña correcta.</span><span class="sxs-lookup"><span data-stu-id="9e769-136">If a logon identifier other than the IIS identity is selected, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="9e769-137">Esto obliga a todas las conexiones anónimas o de invitado a usar el identificador de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="9e769-137">This forces all anonymous or guest connections to use the logon identifier.</span></span>

<span data-ttu-id="9e769-138">Al usar un inicio de sesión diferente de la identidad de IIS, se pueden controlar los privilegios de la cuenta que tiene acceso a WMI sin que afecte a los demás directorios o archivos del servidor IIS, a menos que la autenticación se establezca en el nivel de servidor.</span><span class="sxs-lookup"><span data-stu-id="9e769-138">By using a logon different from the IIS identity, the privileges of the account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="9e769-139">La configuración anterior permite que el servidor IIS use la autenticación anónima en algunas áreas, y la autenticación mixta o integrada de Windows en otros.</span><span class="sxs-lookup"><span data-stu-id="9e769-139">The previous configuration allows the IIS server to use Anonymous authentication in some areas, and Integrated Windows or mixed authentication in others.</span></span>

## <a name="protection"></a><span data-ttu-id="9e769-140">Protección</span><span class="sxs-lookup"><span data-stu-id="9e769-140">Protection</span></span>

<span data-ttu-id="9e769-141">La última consideración al configurar el servidor IIS es la protección que se debe usar al ejecutar un ASP.</span><span class="sxs-lookup"><span data-stu-id="9e769-141">The last consideration when configuring the IIS server is which protection to use when executing an ASP.</span></span>

<span data-ttu-id="9e769-142">Puede establecer un ASP para ejecutar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9e769-142">You can set an ASP to run the following:</span></span>

-   <span data-ttu-id="9e769-143">En curso a IIS (protección baja).</span><span class="sxs-lookup"><span data-stu-id="9e769-143">In-process to IIS (low protection).</span></span>

-   <span data-ttu-id="9e769-144">Externo a IIS con Dllhost.exe como agrupado o fuera de proceso (protección mediana agrupada).</span><span class="sxs-lookup"><span data-stu-id="9e769-144">External to IIS with Dllhost.exe as pooled or out-of-process (pooled medium protection).</span></span>

-   <span data-ttu-id="9e769-145">Self-of-Process-host (protección alta).</span><span class="sxs-lookup"><span data-stu-id="9e769-145">Out-of-process self-host (high protection).</span></span>

> [!Note]  
> <span data-ttu-id="9e769-146">Para obtener el mejor equilibrio de seguridad y rendimiento, use el host agrupado.</span><span class="sxs-lookup"><span data-stu-id="9e769-146">For the best balance of security and performance, use pooled host.</span></span>

 

 

 



