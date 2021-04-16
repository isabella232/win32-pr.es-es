---
title: Consideraciones de seguridad para las tecnologías de asistencia
description: Las tecnologías de asistencia son aplicaciones que se ejecutan en el escritorio de Windows y ayudan a los usuarios de accesibilidad a interactuar con el sistema operativo y otras aplicaciones que se ejecutan en el equipo, incluidas las aplicaciones de la nueva interfaz de usuario de Windows.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- uiAccess (atributo)
- Automatización de la interfaz de usuario, atributo uiAccess
- Security, atributo uiAccess
- requestedExecutionLevel (etiqueta)
- Automatización de la interfaz de usuario, etiqueta requestedExecutionLevel
- Automatización de la interfaz de usuario, consideraciones de seguridad
- Automatización de la interfaz de usuario, archivos de manifiesto
- archivos de manifiesto
- control de cuentas de usuario
- seguridad, control de cuentas de usuario
- seguridad, archivos de manifiesto
- seguridad, etiqueta requestedExecutionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2020
ms.locfileid: "105695801"
---
# <a name="security-considerations-for-assistive-technologies"></a><span data-ttu-id="db27c-115">Consideraciones de seguridad para las tecnologías de asistencia</span><span class="sxs-lookup"><span data-stu-id="db27c-115">Security Considerations for Assistive Technologies</span></span>

<span data-ttu-id="db27c-116">Las tecnologías de asistencia son aplicaciones que se ejecutan en el escritorio de Windows y ayudan a los usuarios de accesibilidad a interactuar con el sistema operativo y otras aplicaciones que se ejecutan en el equipo, incluidas las aplicaciones de la nueva interfaz de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="db27c-116">Assistive technologies are applications that run on the Windows desktop and help accessibility users interact with the operating system and other applications running on the computer, including applications in the new Windows UI.</span></span> <span data-ttu-id="db27c-117">Las aplicaciones de tecnología de Asistencia funcionan mediante la recuperación de información del sistema operativo y de otras aplicaciones y, a continuación, la presentación de la información de forma que sea accesible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="db27c-117">Assistive technology applications work by retrieving information from the operating system and other applications, and then presenting the information in a way that is accessible to the user.</span></span> <span data-ttu-id="db27c-118">Una aplicación de tecnología de asistencia también puede "impulsar" el sistema operativo y otras aplicaciones en función de la entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="db27c-118">An assistive technology application can also programmatically "drive" the operating system and other applications based on input from the user.</span></span>

<span data-ttu-id="db27c-119">La naturaleza de las aplicaciones de tecnología de asistencia requiere que crucen los límites del proceso y que tengan acceso a los procesos que se ejecutan en un nivel de integridad más alto (IL) que ellos mismos.</span><span class="sxs-lookup"><span data-stu-id="db27c-119">The nature of assistive technology applications requires that they cross process boundaries, and that they have access to processes that run at a higher integrity level (IL) than themselves.</span></span> <span data-ttu-id="db27c-120">(Las aplicaciones de tecnología de asistencia se ejecutan en IL medio). Por ejemplo, cuando el usuario intenta realizar una tarea que requiere privilegios administrativos, Windows presenta un cuadro de diálogo que pide al usuario su consentimiento para continuar.</span><span class="sxs-lookup"><span data-stu-id="db27c-120">(An assistive technology application runs at medium IL.) For example, when the user attempts to perform a task that requires administrative privileges, Windows presents a dialog box asking the user for consent to continue.</span></span> <span data-ttu-id="db27c-121">Este cuadro de diálogo se ejecuta en un IL más alto para protegerlo de la comunicación entre procesos, de modo que el software malintencionado no puede simular la entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="db27c-121">This dialog box runs at a higher IL to protect it from cross-process communication, so that malicious software cannot simulate user input.</span></span> <span data-ttu-id="db27c-122">De forma similar, la pantalla de inicio de sesión de escritorio se ejecuta en un IL superior para evitar que otros procesos tengan acceso a él.</span><span class="sxs-lookup"><span data-stu-id="db27c-122">Similarly, the desktop logon screen runs at a higher IL to prevent it from being accessed by other processes.</span></span>

<span data-ttu-id="db27c-123">Las aplicaciones de tecnología de asistencia normalmente necesitan tener acceso a los elementos de la interfaz de usuario del sistema protegidos o a otros procesos que podrían estar ejecutándose en un nivel de privilegios superior.</span><span class="sxs-lookup"><span data-stu-id="db27c-123">Assistive technology applications typically need access to the protected system UI elements, or to other processes that might be running at a higher privilege level.</span></span> <span data-ttu-id="db27c-124">Por lo tanto, las aplicaciones de tecnología de asistencia deben ser de confianza para el sistema y deben ejecutarse con privilegios especiales.</span><span class="sxs-lookup"><span data-stu-id="db27c-124">Therefore, assistive technology applications must be trusted by the system, and must run with special privileges.</span></span>

<span data-ttu-id="db27c-125">Para obtener acceso a los procesos de IL más altos, una aplicación de tecnología de ayuda debe establecer la marca UIAccess en el manifiesto de la aplicación e iniciarla un usuario con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="db27c-125">To get access to higher IL processes, an assistive technology application must set the UIAccess flag in the application's manifest and be launched by a user with administrator privileges.</span></span>

> [!NOTE]
> <span data-ttu-id="db27c-126">Los privilegios de acceso se restringen de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="db27c-126">Access privileges are constrained as follows:</span></span>
>
> - <span data-ttu-id="db27c-127">Una aplicación que no tiene UIAccess en el manifiesto comienza con un IL medio y no puede tener acceso a la interfaz de usuario del proceso con privilegios elevados ("medio +" IL).</span><span class="sxs-lookup"><span data-stu-id="db27c-127">An application that doesn't have UIAccess in the manifest starts with medium IL and cannot access elevated ("medium+" IL) process UI.</span></span>
> - <span data-ttu-id="db27c-128">Una aplicación que tiene UIAccess en el manifiesto y que es iniciada por un usuario que no está en el grupo de administradores, se inicia como IL "medio +" y no puede tener acceso a la interfaz de usuario con privilegios elevados (nada que se ejecute como "alto" IL, como las aplicaciones iniciadas con un **clic secundario > ejecutar como administrador**).</span><span class="sxs-lookup"><span data-stu-id="db27c-128">An application that has UIAccess in the manifest and is launched by a user who is not in the administrators group, starts as "medium+" IL and cannot access elevated UI (nothing running as "high" IL, such as apps launched through a **Right click -> Run as administrator**).</span></span>
> - <span data-ttu-id="db27c-129">Una aplicación tiene acceso a la interfaz de usuario y es iniciada por un usuario administrador que se inicia como IL "alto" y puede tener acceso a la interfaz de usuario con privilegios elevados porque tiene el mismo IL.</span><span class="sxs-lookup"><span data-stu-id="db27c-129">An application has UI Access and is launched by an admin user starts as "high" IL and can access elevated UI because it has the same IL.</span></span>
>
> <span data-ttu-id="db27c-130">UIAccess no es suficiente para que un proceso se desplace por el límite de IL.</span><span class="sxs-lookup"><span data-stu-id="db27c-130">UIAccess is not enough for a process to move up through the IL boundary.</span></span>

<span data-ttu-id="db27c-131">Además de tener acceso a procesos de IL más altos, una aplicación de tecnología de asistencia con estos privilegios puede ejecutarse como la aplicación de nivel superior en el orden z en cualquier momento, lo que significa que una aplicación de tecnología de asistencia puede estar visible y disponible siempre que el usuario la necesite.</span><span class="sxs-lookup"><span data-stu-id="db27c-131">In addition to having access to higher IL processes, an assistive technology application with these privileges can run as the topmost application in the z-order at any time, meaning that an assistive technology application can be visible and available whenever the user needs it.</span></span>

> [!Important]
> <span data-ttu-id="db27c-132">Ninguno de los escenarios enumerados anteriormente proporciona acceso a la interfaz de usuario que se ejecuta en el sistema IL.</span><span class="sxs-lookup"><span data-stu-id="db27c-132">None of the previously listed scenarios provide access to UI running under the system IL.</span></span> <span data-ttu-id="db27c-133">Esto solo es posible si el proceso se inicia en el escritorio de control de cuentas de usuario (UAC) en sistema (y en el sistema IL).</span><span class="sxs-lookup"><span data-stu-id="db27c-133">This is only possible if the process is launched in the user account control (UAC) desktop under SYSTEM (and system IL).</span></span> <span data-ttu-id="db27c-134">En este caso, la configuración de UIAccess no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="db27c-134">In this case, setting UIAccess has no effect.</span></span>

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a><span data-ttu-id="db27c-135">Requisitos de UIAccess para aplicaciones de tecnología de asistencia</span><span class="sxs-lookup"><span data-stu-id="db27c-135">UIAccess Requirements for Assistive Technology Applications</span></span>

<span data-ttu-id="db27c-136">Una aplicación de tecnología de asistencia es una aplicación de escritorio Windows de Windows que interactúa con otros procesos que se ejecutan en el escritorio y en la nueva interfaz de usuario de Windows para obtener información del sistema y de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="db27c-136">An assistive technology application is a Windows Windows desktop application that interacts with other processes running on the desktop and in the new Windows UI to get information from the system and applications.</span></span> <span data-ttu-id="db27c-137">A continuación, la aplicación de tecnología de asistencia puede proporcionar la información a los usuarios de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="db27c-137">The assistive technology application can then provide the information to accessibility users.</span></span>

<span data-ttu-id="db27c-138">Una aplicación de tecnología de asistencia obtiene acceso a otros procesos estableciendo la marca UIAccess en el manifiesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="db27c-138">An assistive technology application gets access to other processes by setting the UIAccess flag in the application manifest.</span></span> <span data-ttu-id="db27c-139">Para usar la marca UIAccess, una aplicación de tecnología de asistencia debe cumplir los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="db27c-139">To use the UIAccess flag, an assistive technology application must meet the following requirements.</span></span>

-   <span data-ttu-id="db27c-140">Requiere que se muestre, interactúe o refleje información de otra aplicación para proporcionar información para un escenario de accesibilidad, o</span><span class="sxs-lookup"><span data-stu-id="db27c-140">Require to display, interact with, or reflect information from another application to provide information for an accessibility scenario, and/or</span></span>
-   <span data-ttu-id="db27c-141">Requiere la ejecución como ventana de nivel superior para obtener o mostrar esta información.</span><span class="sxs-lookup"><span data-stu-id="db27c-141">Require running as the top-most window to obtain or display this information.</span></span>

<span data-ttu-id="db27c-142">Para usar UIAccess, una aplicación de tecnología de asistencia debe:</span><span class="sxs-lookup"><span data-stu-id="db27c-142">To use UIAccess, an assistive technology application needs to:</span></span>

-   <span data-ttu-id="db27c-143">Debe estar firmado con un certificado para interactuar con aplicaciones que se ejecutan en un nivel de privilegios superior.</span><span class="sxs-lookup"><span data-stu-id="db27c-143">Be signed with a certificate to interact with applications running at a higher privilege level.</span></span>
-   <span data-ttu-id="db27c-144">Ser de confianza para el sistema.</span><span class="sxs-lookup"><span data-stu-id="db27c-144">Be trusted by the system.</span></span> <span data-ttu-id="db27c-145">La aplicación debe instalarse en una ubicación segura que requiera un aviso de control de cuentas de usuario (UAC) para el acceso.</span><span class="sxs-lookup"><span data-stu-id="db27c-145">The application must be installed in a secure location that requires a user account control (UAC) prompt for access.</span></span> <span data-ttu-id="db27c-146">Por ejemplo, la carpeta archivos de programa.</span><span class="sxs-lookup"><span data-stu-id="db27c-146">For example, the Program Files folder.</span></span>
-   <span data-ttu-id="db27c-147">Compilar con un archivo de manifiesto que incluya la marca uiAccess.</span><span class="sxs-lookup"><span data-stu-id="db27c-147">Be built with a manifest file that includes the uiAccess flag.</span></span>

<span data-ttu-id="db27c-148">No se debe usar UIAccess:</span><span class="sxs-lookup"><span data-stu-id="db27c-148">UIAccess should not be used:</span></span>

-   <span data-ttu-id="db27c-149">Por aplicaciones que no son tecnologías de asistencia.</span><span class="sxs-lookup"><span data-stu-id="db27c-149">By applications that are not assistive technologies.</span></span>
-   <span data-ttu-id="db27c-150">Por aplicaciones de tecnología de asistencia que muestran información o interfaz de usuario que no es relevante para el escenario de accesibilidad de destino.</span><span class="sxs-lookup"><span data-stu-id="db27c-150">By assistive technology applications that display information or UI that is not relevant to the accessibility scenario they target.</span></span>
-   <span data-ttu-id="db27c-151">Por aplicaciones que solo quieren aparecer por encima de otras aplicaciones en la nueva interfaz de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="db27c-151">By applications that just want to appear above other applications in the new Windows UI.</span></span>
    > [!Note]  
    > <span data-ttu-id="db27c-152">Las aplicaciones desarrolladas para la nueva interfaz de usuario de Windows no tienen UIAccess como una opción disponible.</span><span class="sxs-lookup"><span data-stu-id="db27c-152">Applications developed for the new Windows UI do not have UIAccess as an available option.</span></span>

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a><span data-ttu-id="db27c-153">Establecer UIAccess en el archivo de manifiesto de aplicación</span><span class="sxs-lookup"><span data-stu-id="db27c-153">Setting UIAccess in the Application Manifest File</span></span>

<span data-ttu-id="db27c-154">Para obtener acceso a la interfaz de usuario del sistema protegida, las aplicaciones deben compilarse con un archivo de manifiesto que incluya un atributo especial en el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="db27c-154">To gain access to the protected system UI, applications must be built with a manifest file that includes a special attribute in the manifest file.</span></span> <span data-ttu-id="db27c-155">Este atributo **UIAccess** se incluye en la etiqueta **requestedExecutionLevel** , tal como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="db27c-155">This **uiAccess** attribute is included in the **requestedExecutionLevel** tag, as shown in the following code example.</span></span>


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



<span data-ttu-id="db27c-156">El valor del atributo **LEVEL** en este código es solo un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="db27c-156">The value of the **level** attribute in this code is an example only.</span></span>

<span data-ttu-id="db27c-157">**UIAccess** es "false" de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="db27c-157">**UIAccess** is "false" by default.</span></span> <span data-ttu-id="db27c-158">Si se omite el atributo o si no hay ningún manifiesto, la aplicación no puede obtener acceso a la interfaz de usuario protegida.</span><span class="sxs-lookup"><span data-stu-id="db27c-158">If the attribute is omitted, or if there is no manifest, the application cannot gain access to the protected UI.</span></span>

<span data-ttu-id="db27c-159">Para obtener más información sobre la seguridad de Windows, sobre la firma de aplicaciones y sobre la creación de manifiestos, consulte [el artículo sobre el desarrollador de Windows Vista y Windows Server 2008: requisitos de desarrollo de aplicaciones de Windows Vista para el control de cuentas de usuario (UAC)](/previous-versions/aa905330(v=msdn.10)) en MSDN.</span><span class="sxs-lookup"><span data-stu-id="db27c-159">For more information on Windows security, on signing applications, and on creating manifests, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db27c-160">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db27c-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db27c-161">Fundamentos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="db27c-161">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 