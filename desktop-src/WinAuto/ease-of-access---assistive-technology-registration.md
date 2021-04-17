---
title: Registro de la tecnología de asistencia de accesibilidad
description: En este artículo se explica cómo registrar una aplicación de accesibilidad con el centro de accesibilidad. También se explica cómo adaptar la aplicación de accesibilidad para que funcione bien con el escritorio seguro.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 66901cd899fc578b032f86e3752fcdcac0788ba1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704998"
---
# <a name="ease-of-access---assistive-technology-registration"></a><span data-ttu-id="68737-104">Registro de la tecnología de asistencia de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="68737-104">Ease of Access   Assistive Technology Registration</span></span>

<span data-ttu-id="68737-105">En este artículo se explica cómo registrar una aplicación de accesibilidad con el centro de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="68737-105">This article explains how to register an accessibility application with the Ease of Access Center.</span></span> <span data-ttu-id="68737-106">También se explica cómo adaptar la aplicación de accesibilidad para que funcione bien con el escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-106">It also explains how to tailor your accessibility application so it works well with the secure desktop.</span></span>

<span data-ttu-id="68737-107">El centro de accesibilidad es una aplicación del panel de control para Microsoft Windows que reúne la funcionalidad de accesibilidad y facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="68737-107">The Ease of Access Center is a Control Panel application for Microsoft Windows brings together functionality for accessibility and ease of use.</span></span> <span data-ttu-id="68737-108">Mediante el centro de accesibilidad, los usuarios pueden configurar sus equipos para que se adapten a sus necesidades físicas y cognitivas.</span><span class="sxs-lookup"><span data-stu-id="68737-108">By using the Ease of Access Center, users can configure their computers to suit their physical and cognitive needs.</span></span>

<span data-ttu-id="68737-109">Una función del centro de accesibilidad es ayudar a los usuarios a iniciar aplicaciones de accesibilidad, como narrador, teclado en pantalla y ampliador.</span><span class="sxs-lookup"><span data-stu-id="68737-109">One function of the Ease of Access Center is to help users launch accessibility applications, including Narrator, On-Screen Keyboard, and Magnifier.</span></span> <span data-ttu-id="68737-110">Las aplicaciones de terceros registradas también aparecen en el centro de accesibilidad y se pueden iniciar directamente desde allí.</span><span class="sxs-lookup"><span data-stu-id="68737-110">Registered third-party applications also appear in the Ease of Access Center and can be launched directly from there.</span></span>

<span data-ttu-id="68737-111">Las aplicaciones de accesibilidad deben funcionar sin problemas con el escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-111">Accessibility applications need to work smoothly with the secure desktop.</span></span> <span data-ttu-id="68737-112">El escritorio seguro es la interfaz de usuario que aparece cuando el equipo está bloqueado (en el inicio de sesión o cuando el usuario ha bloqueado el escritorio) y cuando se solicita al usuario que permita una acción potencialmente insegura.</span><span class="sxs-lookup"><span data-stu-id="68737-112">The secure desktop is the user interface that appears when the computer is locked (at log-on or when the user has locked the desktop), and when the user is prompted to allow a potentially unsafe action.</span></span> <span data-ttu-id="68737-113">Por motivos de seguridad, Windows impone límites en el software de terceros que se ejecuta en el escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-113">For security reasons, Windows places limits on third-party software running on the secure desktop.</span></span> <span data-ttu-id="68737-114">Si desea que la aplicación de accesibilidad se ejecute en el escritorio seguro, debe registrar la aplicación con el centro de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="68737-114">If you want your accessibility application to run on the secure desktop, you need to register the application with the Ease of Access Center.</span></span>

## <a name="registering-with-the-ease-of-access-center"></a><span data-ttu-id="68737-115">Registro con el centro de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="68737-115">Registering with the Ease of Access Center</span></span>

<span data-ttu-id="68737-116">Las aplicaciones de accesibilidad se registran con el centro de facilidad de acceso mediante la creación de una o varias claves del registro cuando se instala la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68737-116">Accessibility applications register with the Ease of Access Center by creating one or more registry keys when the application is installed.</span></span> <span data-ttu-id="68737-117">En la tabla siguiente se muestra la información contenida en las claves del registro.</span><span class="sxs-lookup"><span data-stu-id="68737-117">The following table lists the information contained in the registry keys.</span></span>



| <span data-ttu-id="68737-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="68737-118">Name</span></span>                        | <span data-ttu-id="68737-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="68737-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="68737-120">Obligatorio/Opcional</span><span class="sxs-lookup"><span data-stu-id="68737-120">Mandatory/Optional</span></span> | <span data-ttu-id="68737-121">Idioma</span><span class="sxs-lookup"><span data-stu-id="68737-121">Language</span></span>      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| <span data-ttu-id="68737-122">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="68737-122">Application Name</span></span>            | <span data-ttu-id="68737-123">El nombre de la aplicación, que se encuentra en un archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68737-123">The name of the application, which is in a resource file.</span></span> <span data-ttu-id="68737-124">Este valor del registro contiene una cadena con un formato especificado.</span><span class="sxs-lookup"><span data-stu-id="68737-124">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="68737-125">Puede tratarse de una versión localizada del nombre de la aplicación, si la aplicación está localizada en idiomas distintos del inglés.</span><span class="sxs-lookup"><span data-stu-id="68737-125">This could be a localized version of the application name, if the application is localized in languages other than English.</span></span> <span data-ttu-id="68737-126">El nombre aparece en el centro de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="68737-126">The name appears in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="68737-127">Mandatory</span><span class="sxs-lookup"><span data-stu-id="68737-127">Mandatory</span></span>          | <span data-ttu-id="68737-128">Traducida</span><span class="sxs-lookup"><span data-stu-id="68737-128">Localized</span></span>     |
| <span data-ttu-id="68737-129">ATExe</span><span class="sxs-lookup"><span data-stu-id="68737-129">ATExe</span></span>                       | <span data-ttu-id="68737-130">Nombre del archivo ejecutable de la aplicación o de la imagen.</span><span class="sxs-lookup"><span data-stu-id="68737-130">The name of the application executable file or image.</span></span> <span data-ttu-id="68737-131">Windows usa este valor para determinar si se está ejecutando la aplicación de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="68737-131">Windows uses this value to determine whether the accessibility application is running.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="68737-132">Mandatory</span><span class="sxs-lookup"><span data-stu-id="68737-132">Mandatory</span></span>          | <span data-ttu-id="68737-133">No localizado</span><span class="sxs-lookup"><span data-stu-id="68737-133">Not localized</span></span> |
| <span data-ttu-id="68737-134">CopySettingsToLockedDesktop</span><span class="sxs-lookup"><span data-stu-id="68737-134">CopySettingsToLockedDesktop</span></span> | <span data-ttu-id="68737-135">Valor **DWORD** que indica si se debe copiar la configuración de la aplicación de accesibilidad en el escritorio bloqueado.</span><span class="sxs-lookup"><span data-stu-id="68737-135">A **DWORD** value that indicates whether to copy the accessibility application's settings to the locked desktop.</span></span><br/> <span data-ttu-id="68737-136">Si este valor es 1, la aplicación puede escribir la configuración en una ubicación del registro de usuario y Windows copia la configuración en la misma ubicación del registro de usuario para el escritorio bloqueado.</span><span class="sxs-lookup"><span data-stu-id="68737-136">If this value is 1, the application can write settings to a location in the user registry, and Windows copies the settings to the same location in the user registry for the locked desktop.</span></span> <span data-ttu-id="68737-137">Esto permite que la aplicación conserve su estado del escritorio "normal" en el escritorio bloqueado.</span><span class="sxs-lookup"><span data-stu-id="68737-137">This enables the application to persist its state from the "normal" desktop to the locked desktop.</span></span><br/>                                                                                                                                                             | <span data-ttu-id="68737-138">Opcionales</span><span class="sxs-lookup"><span data-stu-id="68737-138">Optional</span></span>           | <span data-ttu-id="68737-139">No localizado</span><span class="sxs-lookup"><span data-stu-id="68737-139">Not localized</span></span> |
| <span data-ttu-id="68737-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="68737-140">Description</span></span>                 | <span data-ttu-id="68737-141">Breve descripción de la aplicación, desde un archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68737-141">A brief description of the application, from a resource file.</span></span> <span data-ttu-id="68737-142">Este valor del registro contiene una cadena con un formato especificado.</span><span class="sxs-lookup"><span data-stu-id="68737-142">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="68737-143">Puede tratarse de una versión localizada de la descripción si la aplicación está localizada en idiomas distintos del inglés.</span><span class="sxs-lookup"><span data-stu-id="68737-143">This could be a localized version of the description, if the application is localized in languages other than English.</span></span> <span data-ttu-id="68737-144">La longitud de esta cadena debe ser inferior a 512 caracteres.</span><span class="sxs-lookup"><span data-stu-id="68737-144">The length of this string must be less than 512 characters.</span></span><br/> <span data-ttu-id="68737-145">La descripción aparece en el centro de accesibilidad para proporcionar información adicional sobre la aplicación de accesibilidad al usuario.</span><span class="sxs-lookup"><span data-stu-id="68737-145">The description appears in the Ease of Access Center to provide additional information about the accessibility application to the user.</span></span><br/> <span data-ttu-id="68737-146">Este valor también se puede usar para notificar al usuario que la aplicación no se utiliza en el escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-146">This value can also be used to notify the user that the application is not used on the secure desktop.</span></span><br/>      | <span data-ttu-id="68737-147">Mandatory</span><span class="sxs-lookup"><span data-stu-id="68737-147">Mandatory</span></span>          | <span data-ttu-id="68737-148">Traducida</span><span class="sxs-lookup"><span data-stu-id="68737-148">Localized</span></span>     |
| <span data-ttu-id="68737-149">Perfil</span><span class="sxs-lookup"><span data-stu-id="68737-149">Profile</span></span>                     | <span data-ttu-id="68737-150">Una pequeña parte de XML que especifica los alojamientos que proporciona la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68737-150">A short piece of XML that specifies the accommodations that the application provides.</span></span> <span data-ttu-id="68737-151">Garantiza que la aplicación aparece en la categoría correcto en el centro de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="68737-151">It ensures that the application appears under the correct category in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="68737-152">Mandatory</span><span class="sxs-lookup"><span data-stu-id="68737-152">Mandatory</span></span>          | <span data-ttu-id="68737-153">No localizado</span><span class="sxs-lookup"><span data-stu-id="68737-153">Not localized</span></span> |
| <span data-ttu-id="68737-154">PassiveAutoStartBehavior</span><span class="sxs-lookup"><span data-stu-id="68737-154">PassiveAutoStartBehavior</span></span>    | <p><span data-ttu-id="68737-155">Valor **DWORD** que indica si está habilitado el comportamiento de inicio automático heredado.</span><span class="sxs-lookup"><span data-stu-id="68737-155">A **DWORD** value that indicates whether legacy auto-start behavior is enabled.</span></span></p><p><span data-ttu-id="68737-156">El valor predeterminado es 0, que indica que un en requiere un comportamiento de inicio automático heredado.</span><span class="sxs-lookup"><span data-stu-id="68737-156">The default value is 0, which indicates that an AT requires legacy auto-start behavior.</span></span> <span data-ttu-id="68737-157">Esto hace que el valor "iniciar después del inicio de sesión" en se proteja en la configuración rápida (OOBE) y el panel de control (vea **Panel de control-> facilidad de acceso > centro de accesibilidad-> cambiar la configuración de inicio de sesión**) e inicia automáticamente la en después de UAC y de la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="68737-157">This  causes the “Start after sign-in” setting for that AT to be checked in the Out Of Box Experience (OOBE) and Control Panel (see **Control Panel -> Ease of Access -> Ease of Access Center -> Change sign-in settings**), and automatically starts the AT after UAC and lock-screen.</span></span></p><p><span data-ttu-id="68737-158">Un valor de 1 indica que en debe usar el nuevo comportamiento de inicio automático en el que la opción "iniciar después del inicio de sesión" de la no está activada en la configuración rápida (OOBE) y el panel de control, y en se inicia automáticamente una vez por sesión de usuario (en el inicio de sesión) solo si está activada la opción "iniciar después del inicio de sesión".</span><span class="sxs-lookup"><span data-stu-id="68737-158">A value of 1 indicates that the AT should use the new auto-start behavior where the “Start after sign-in” setting for that AT is not checked in the Out Of Box Experience (OOBE) and Control Panel, and the AT is automatically started once per user session (at login) only if the “start after sign-in” setting is checked.</span></span></p>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="68737-159">Opcionales</span><span class="sxs-lookup"><span data-stu-id="68737-159">Optional</span></span>          | <span data-ttu-id="68737-160">No localizado</span><span class="sxs-lookup"><span data-stu-id="68737-160">Not localized</span></span> |
| <span data-ttu-id="68737-161">SecureDesktopAccommodation</span><span class="sxs-lookup"><span data-stu-id="68737-161">SecureDesktopAccommodation</span></span>  | <span data-ttu-id="68737-162">El nombre de una aplicación de accesibilidad alternativa que se ejecutará en el escritorio seguro en lugar de esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="68737-162">The name of an alternate accessibility application to run on the secure desktop in the place of this application.</span></span> <span data-ttu-id="68737-163">La alternativa puede ser una aplicación diferente, una versión diferente de la misma aplicación, una de las aplicaciones de accesibilidad que se incluye en Windows o "none" si no desea ejecutar ninguna aplicación de accesibilidad en el escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-163">The alternate can be a different application, a different version of the same application, one of the accessibility applications that is included in Windows, or "none" if you do not want to run any accessibility application on the secure desktop.</span></span> <br/>                                                                                                                                                                                                               | <span data-ttu-id="68737-164">Opcionales</span><span class="sxs-lookup"><span data-stu-id="68737-164">Optional</span></span>           | <span data-ttu-id="68737-165">No localizado</span><span class="sxs-lookup"><span data-stu-id="68737-165">Not localized</span></span> |
| <span data-ttu-id="68737-166">Perfil simple</span><span class="sxs-lookup"><span data-stu-id="68737-166">Simple Profile</span></span>              | <span data-ttu-id="68737-167">Un valor que describe cómo clasificar la aplicación en una o dos palabras: lector de pantalla, lupa o teclado en pantalla, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="68737-167">A value that describes how to classify the application in a word or two: Screen reader, Magnifier, or On-screen keyboard, for example.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="68737-168">Mandatory</span><span class="sxs-lookup"><span data-stu-id="68737-168">Mandatory</span></span>          | <span data-ttu-id="68737-169">No localizado</span><span class="sxs-lookup"><span data-stu-id="68737-169">Not localized</span></span> |
| <span data-ttu-id="68737-170">Variable startexe ProcessStartInfo</span><span class="sxs-lookup"><span data-stu-id="68737-170">StartExe</span></span>                    | <span data-ttu-id="68737-171">Ruta de acceso completa del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="68737-171">The full path of the executable.</span></span> <span data-ttu-id="68737-172">Este valor se utiliza para iniciar la aplicación de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="68737-172">This value is used to launch the accessibility application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="68737-173">Mandatory</span><span class="sxs-lookup"><span data-stu-id="68737-173">Mandatory</span></span>          | <span data-ttu-id="68737-174">No localizado</span><span class="sxs-lookup"><span data-stu-id="68737-174">Not localized</span></span> |
| <span data-ttu-id="68737-175">StartParams</span><span class="sxs-lookup"><span data-stu-id="68737-175">StartParams</span></span>                 | <span data-ttu-id="68737-176">Argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="68737-176">Command-line arguments.</span></span> <span data-ttu-id="68737-177">Estos valores se usan junto con variable startexe ProcessStartInfo para iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68737-177">These values are used along with StartExe to start the application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="68737-178">Opcionales</span><span class="sxs-lookup"><span data-stu-id="68737-178">Optional</span></span>           | <span data-ttu-id="68737-179">No localizado</span><span class="sxs-lookup"><span data-stu-id="68737-179">Not localized</span></span> |
| <span data-ttu-id="68737-180">TerminateOnDesktopSwitch</span><span class="sxs-lookup"><span data-stu-id="68737-180">TerminateOnDesktopSwitch</span></span>    | <span data-ttu-id="68737-181">Valor **DWORD** que especifica el modo en que la aplicación de accesibilidad responde a las transiciones hacia o desde el escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-181">A **DWORD** value that specifies how the accessibility application responds to transitions to or from the secure desktop.</span></span><br/> <span data-ttu-id="68737-182">Si este valor no existe o es 1, Windows finaliza y reinicia la aplicación en cada transición hacia o desde el escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-182">If this value does not exist or is 1, Windows terminates and restarts the application on each transition to or from the secure desktop.</span></span> <span data-ttu-id="68737-183">Este es el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="68737-183">This is the default behavior.</span></span><br/> <span data-ttu-id="68737-184">Si este valor es 0, Windows no finaliza la aplicación de accesibilidad en una transición del escritorio.</span><span class="sxs-lookup"><span data-stu-id="68737-184">If this value is 0, Windows does not terminate the accessibility application on a desktop transition.</span></span> <span data-ttu-id="68737-185">La aplicación continúa ejecutándose en el escritorio anterior y Windows inicia una nueva instancia en el escritorio nuevo si aún no se está ejecutando una instancia.</span><span class="sxs-lookup"><span data-stu-id="68737-185">The application continues to run on the previous desktop, and Windows starts a new instance on the new desktop if an instance is not already running there.</span></span><br/> | <span data-ttu-id="68737-186">Opcionales</span><span class="sxs-lookup"><span data-stu-id="68737-186">Optional</span></span>           | <span data-ttu-id="68737-187">No localizado</span><span class="sxs-lookup"><span data-stu-id="68737-187">Not localized</span></span> |


 

### <a name="localization"></a><span data-ttu-id="68737-188">Localización</span><span class="sxs-lookup"><span data-stu-id="68737-188">Localization</span></span>

<span data-ttu-id="68737-189">Los valores del registro de nombre y descripción de la aplicación deben ser localizables para admitir la interfaz de usuario multilingüe (MUI).</span><span class="sxs-lookup"><span data-stu-id="68737-189">The registry values of Application Name and Description need to be localizable to support Multilingual User Interface (MUI).</span></span>

<span data-ttu-id="68737-190">Estas cadenas tienen el formato siguiente, donde los corchetes angulares indican los elementos necesarios y los corchetes, lo que significa un elemento opcional.</span><span class="sxs-lookup"><span data-stu-id="68737-190">These strings are in the following format, where angle brackets signify required elements and square brackets signify an optional element.</span></span>

<span data-ttu-id="68737-191">*@ <ResDllPath \\ ResDLLFilename>,- <resID> \[ ;<comment>\]*</span><span class="sxs-lookup"><span data-stu-id="68737-191">*@<ResDllPath\\ResDLLFilename>,-<resID>\[;<comment>\]*</span></span>

<span data-ttu-id="68737-192">*<ResDllPath \\ ResDLLFilename>* es la ruta de acceso al archivo dll de recursos.</span><span class="sxs-lookup"><span data-stu-id="68737-192">*<ResDllPath\\ResDLLFilename>* is the path to the resource DLL.</span></span> <span data-ttu-id="68737-193">La ruta de acceso puede contener variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="68737-193">The path can contain environmental variables.</span></span>

<span data-ttu-id="68737-194">*<resID>* es el identificador de recurso de la cadena.</span><span class="sxs-lookup"><span data-stu-id="68737-194">*<resID>* is the resource ID for the string.</span></span>

<span data-ttu-id="68737-195">el *\[ comentario \]* contiene cualquier comentario opcional.</span><span class="sxs-lookup"><span data-stu-id="68737-195">*\[comment\]* contains any optional comments.</span></span>

<span data-ttu-id="68737-196">Este es un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="68737-196">Here is an example:</span></span>


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



<span data-ttu-id="68737-197">Para obtener más información sobre MUI, vea [centro de conocimientos de Windows mui](../intl/about-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="68737-197">For more information about MUI, see [Windows MUI Knowledge Center](../intl/about-multilingual-user-interface.md).</span></span>

### <a name="hci-profile"></a><span data-ttu-id="68737-198">Perfil de HCI</span><span class="sxs-lookup"><span data-stu-id="68737-198">HCI Profile</span></span>

<span data-ttu-id="68737-199">El perfil de interacción de equipo humano (HCI) es una manera de determinar qué alojamientos debe proporcionar en función de las necesidades del usuario.</span><span class="sxs-lookup"><span data-stu-id="68737-199">The Human Computer Interaction (HCI) profile is a way to determine what accommodations to provide based on the needs of the user.</span></span> <span data-ttu-id="68737-200">Las aplicaciones de accesibilidad deben registrar información sobre el tipo de discapacidad que la aplicación ayuda a acomodar.</span><span class="sxs-lookup"><span data-stu-id="68737-200">Accessibility applications should register information about the kind of disability the application helps to accommodate.</span></span>

<span data-ttu-id="68737-201">El valor del registro profile contiene XML que describe el tipo de discapacidad de destino de la aplicación de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="68737-201">The Profile registry value contains XML that describes the kind of disability targeted by the accessibility application.</span></span> <span data-ttu-id="68737-202">Este XML tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="68737-202">This XML has the following format:</span></span>


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



<span data-ttu-id="68737-203">Los valores válidos para el atributo de **tipo de alojamiento** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="68737-203">The valid values for the **Accommodation type** attribute are as follows:</span></span>

-   <span data-ttu-id="68737-204">visión leve</span><span class="sxs-lookup"><span data-stu-id="68737-204">mild vision</span></span>
-   <span data-ttu-id="68737-205">visión seria</span><span class="sxs-lookup"><span data-stu-id="68737-205">severe vision</span></span>
-   <span data-ttu-id="68737-206">cognitiva leve</span><span class="sxs-lookup"><span data-stu-id="68737-206">mild cognitive</span></span>
-   <span data-ttu-id="68737-207">cognitivo grave</span><span class="sxs-lookup"><span data-stu-id="68737-207">severe cognitive</span></span>
-   <span data-ttu-id="68737-208">destreza leve</span><span class="sxs-lookup"><span data-stu-id="68737-208">mild dexterity</span></span>
-   <span data-ttu-id="68737-209">destreza grave</span><span class="sxs-lookup"><span data-stu-id="68737-209">severe dexterity</span></span>
-   <span data-ttu-id="68737-210">audición leve</span><span class="sxs-lookup"><span data-stu-id="68737-210">mild hearing</span></span>
-   <span data-ttu-id="68737-211">audiencia grave</span><span class="sxs-lookup"><span data-stu-id="68737-211">severe hearing</span></span>
-   <span data-ttu-id="68737-212">voz leve</span><span class="sxs-lookup"><span data-stu-id="68737-212">mild speech</span></span>
-   <span data-ttu-id="68737-213">voz seria</span><span class="sxs-lookup"><span data-stu-id="68737-213">severe speech</span></span>

> [!Note]  
> <span data-ttu-id="68737-214">Estos valores distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="68737-214">These values are case sensitive.</span></span>

 

<span data-ttu-id="68737-215">Si una aplicación de accesibilidad admite varias adaptaciones, el valor del registro de perfil debe incluir un atributo de **tipo de alojamiento** para cada alojamiento.</span><span class="sxs-lookup"><span data-stu-id="68737-215">If an accessibility application supports multiple accommodations, the Profile registry value should include an **Accommodation type** attribute for each accommodation.</span></span>

### <a name="ease-of-access-registry-details"></a><span data-ttu-id="68737-216">Detalles del registro de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="68737-216">Ease of Access registry details</span></span>

<span data-ttu-id="68737-217">Para registrar la aplicación de accesibilidad, debe crear una clave para la aplicación en la siguiente ubicación del registro y rellenarla con pares nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="68737-217">To register your accessibility application, you need to create a key for your application at the following registry location and populate it with name-value pairs.</span></span>

<span data-ttu-id="68737-218">**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS\\**</span><span class="sxs-lookup"><span data-stu-id="68737-218">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\**</span></span>

<span data-ttu-id="68737-219">Asigne un nombre a la clave del registro de la aplicación con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="68737-219">Name your application's registry key using the following format:</span></span>

<span data-ttu-id="68737-220">*"CompanyName \_ ProductName \_ v \# "*</span><span class="sxs-lookup"><span data-stu-id="68737-220">*"CompanyName\_ProductName\_v\#"*</span></span>

<span data-ttu-id="68737-221">Por ejemplo, "Contoso \_ Magnifier \_ v 2.0".</span><span class="sxs-lookup"><span data-stu-id="68737-221">For example, "Contoso\_Magnifier\_v2.0".</span></span>

<span data-ttu-id="68737-222">Para agregar valores de registro, el programa de instalación debe ejecutarse con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="68737-222">To add registry values, your installation program must be running with elevated privileges.</span></span>

### <a name="secure-desktop-accommodation"></a><span data-ttu-id="68737-223">Alojamiento de escritorio seguro</span><span class="sxs-lookup"><span data-stu-id="68737-223">Secure desktop accommodation</span></span>

<span data-ttu-id="68737-224">La clave del registro **SecureDesktopAccommodation** le permite especificar el modo en que la aplicación de accesibilidad responde al escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-224">The **SecureDesktopAccommodation** registry key lets you specify how your accessibility application responds to the secure desktop.</span></span> <span data-ttu-id="68737-225">De forma predeterminada, el centro de accesibilidad inicia la aplicación en el escritorio seguro si ya se estaba ejecutando en el escritorio normal, o si está configurado para ejecutarse en el escritorio de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="68737-225">By default, the Ease of Access Center launches your application on the secure desktop if it was already running on the normal desktop, or if it is configured to run on the logon desktop.</span></span> <span data-ttu-id="68737-226">Mediante el uso de la clave **SecureDesktopAccommodation** , puede:</span><span class="sxs-lookup"><span data-stu-id="68737-226">By using the **SecureDesktopAccommodation** key, you can:</span></span>

-   <span data-ttu-id="68737-227">Especifique una versión alternativa de la aplicación para usarla en el escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-227">Specify an alternate version of your application for use on the secure desktop.</span></span> <span data-ttu-id="68737-228">Por ejemplo, podría tener una versión alternativa que deshabilita características no seguras o está optimizada para usar menos memoria e iniciarse más rápido.</span><span class="sxs-lookup"><span data-stu-id="68737-228">For example, you might have an alternate version that disables unsecured features, or is optimized to use less memory and launch faster.</span></span>

    <span data-ttu-id="68737-229">Para especificar la versión alternativa, establezca la clave **SecureDesktopAccommodation** en el nombre de la versión alternativa.</span><span class="sxs-lookup"><span data-stu-id="68737-229">To specify the alternate version, set the **SecureDesktopAccommodation** key to the name of the alternate version.</span></span> <span data-ttu-id="68737-230">Por ejemplo, si registró su aplicación en la \_ clave lector de pantalla de Contoso \_ v 1.0, podría registrar la versión alternativa en la pantalla de Contoso \_ ReaderSecure \_ v 1.0.</span><span class="sxs-lookup"><span data-stu-id="68737-230">For example, if you registered your application at the Contoso\_Screen Reader\_v1.0 key, you could register the alternate version at Contoso\_Screen ReaderSecure\_v1.0.</span></span> <span data-ttu-id="68737-231">A continuación, establezca la clave **SecureDesktopAccommodation** del \_ lector de pantalla de Contoso \_ v 1.0 en "Contoso \_ Screen ReaderSecure \_ v 1.0".</span><span class="sxs-lookup"><span data-stu-id="68737-231">Then, set the **SecureDesktopAccommodation** key of Contoso\_Screen Reader\_v1.0 to "Contoso\_Screen ReaderSecure\_v1.0".</span></span>

-   <span data-ttu-id="68737-232">Especifique una aplicación de accesibilidad de Microsoft para usarla en el escritorio seguro en lugar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68737-232">Specify a Microsoft accessibility application to use on the secure desktop in place of your application.</span></span> <span data-ttu-id="68737-233">Para esta opción, establezca **SecureDesktopAccommodation** en el nombre de la aplicación de accesibilidad de Microsoft determinada: "Osk", "magnifierpane" o "narrador".</span><span class="sxs-lookup"><span data-stu-id="68737-233">For this option, set **SecureDesktopAccommodation** to the name of the particular Microsoft accessibility application: "osk", "magnifierpane", or "Narrator".</span></span>
-   <span data-ttu-id="68737-234">Especifique que la aplicación no debe ejecutarse en el escritorio seguro y que ninguna otra aplicación alternativa.</span><span class="sxs-lookup"><span data-stu-id="68737-234">Specify that your application should not run on the secure desktop, and neither should any alternate application.</span></span> <span data-ttu-id="68737-235">Para esta opción, establezca **SecureDesktopAccommodation** en "none" (recomendado) o el nombre de una aplicación inexistente.</span><span class="sxs-lookup"><span data-stu-id="68737-235">For this option, set **SecureDesktopAccommodation** to "none" (recommend) or the name of a nonexistent application.</span></span>

<span data-ttu-id="68737-236">Si la clave del registro **SecureDesktopAccommodation** de la aplicación de accesibilidad especifica que una aplicación de accesibilidad de Microsoft se ejecute en el escritorio seguro en lugar de la aplicación, Windows notifica al usuario de este al realizar la transición al escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-236">If the **SecureDesktopAccommodation** registry key for your accessibility application specifies a Microsoft accessibility application to run on the secure desktop in place of your application, Windows notifies the user of this when making the transition to the secure desktop.</span></span> <span data-ttu-id="68737-237">Para notificar al usuario, Windows muestra la cadena especificada en la clave del registro de descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68737-237">To notify the user, Windows displays the string specified in the Description registry key for your application.</span></span> <span data-ttu-id="68737-238">Por ejemplo, si la aplicación ScreenReader Deluxe 1,0 usa Microsoft Narrator en el escritorio seguro, incluiría una cadena de descripción como, "el narrador de Microsoft se usará en el bloque, el inicio de sesión y otros escritorios seguros en lugar de ScreenReader Deluxe 1,0".</span><span class="sxs-lookup"><span data-stu-id="68737-238">For example, if the ScreenReader Deluxe 1.0 application uses Microsoft Narrator on the secure desktop, it would include a Description string such as, "Microsoft Narrator will be used in the locked, logon, and other secure desktops in place of ScreenReader Deluxe 1.0."</span></span>

<span data-ttu-id="68737-239">Si la clave **SecureDesktopAccommodation** de la aplicación se establece en "none", use la clave **Description** para indicar al usuario que la aplicación no está disponible en el escritorio seguro y no se proporciona ninguna alternativa.</span><span class="sxs-lookup"><span data-stu-id="68737-239">If your application's **SecureDesktopAccommodation** key is set to "none", use the **Description** key to tell the user your application is not available on the secure desktop and no alternative is provided.</span></span>

<span data-ttu-id="68737-240">Windows muestra el texto de descripción en las ubicaciones correspondientes del centro de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="68737-240">Windows displays the Description text in the relevant locations in the Ease of Access Center.</span></span>

### <a name="running-at-installation-and-on-the-logon-desktop"></a><span data-ttu-id="68737-241">Ejecutar durante la instalación y en el escritorio de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="68737-241">Running at installation and on the logon desktop</span></span>

<span data-ttu-id="68737-242">Si anexa el nombre de clave registrado de la aplicación de accesibilidad a la cadena en la siguiente ubicación del registro, Windows iniciará la aplicación inmediatamente después de instalarla.</span><span class="sxs-lookup"><span data-stu-id="68737-242">If you append your accessibility application's registered key name to the string at the following registry location, Windows will launch your application immediately after it is installed.</span></span> <span data-ttu-id="68737-243">Además, Windows ejecutará automáticamente la aplicación cada vez que el escritorio de inicio de sesión esté activo.</span><span class="sxs-lookup"><span data-stu-id="68737-243">Also, Windows will automatically run your application whenever the logon desktop is active.</span></span>

<span data-ttu-id="68737-244">**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ Configuration**</span><span class="sxs-lookup"><span data-stu-id="68737-244">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\Configuration**</span></span>

<span data-ttu-id="68737-245">La clave de configuración es una cadena delimitada por comas.</span><span class="sxs-lookup"><span data-stu-id="68737-245">The Configuration key is a comma-delimited string.</span></span> <span data-ttu-id="68737-246">Para agregar la aplicación, anexe una cadena que sea la misma que la clave del registro de la aplicación en HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ .</span><span class="sxs-lookup"><span data-stu-id="68737-246">To add your application, append a string that is the same as your application's registry key at HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\.</span></span>

### <a name="running-in-a-job"></a><span data-ttu-id="68737-247">Ejecutar en un trabajo</span><span class="sxs-lookup"><span data-stu-id="68737-247">Running in a job</span></span>

<span data-ttu-id="68737-248">Si la clave del registro **TerminateOnDesktopSwitch** no está presente o se establece en un valor distinto de cero, Windows ejecuta la aplicación en el contexto de un trabajo, finalizando y reiniciando la aplicación con cada transición del escritorio.</span><span class="sxs-lookup"><span data-stu-id="68737-248">If the **TerminateOnDesktopSwitch** registry key is not present or is set to non-zero, Windows runs the application in the context of a job, terminating and restarting the application with each desktop transition.</span></span> <span data-ttu-id="68737-249">La ejecución en un trabajo garantiza que solo una instancia de la aplicación se ejecuta en un momento determinado y libera a la aplicación de tener que supervisar el estado del escritorio.</span><span class="sxs-lookup"><span data-stu-id="68737-249">Running in a job ensures that only a single instance of the application is running at a particular time, and frees the application from having to monitor the desktop state.</span></span> <span data-ttu-id="68737-250">Las desventajas de ejecutar en un trabajo incluyen:</span><span class="sxs-lookup"><span data-stu-id="68737-250">The disadvantages of running in a job include:</span></span>

-   <span data-ttu-id="68737-251">La aplicación incurre en un costo de inicio con cada transición de escritorio.</span><span class="sxs-lookup"><span data-stu-id="68737-251">The application incurs a startup cost with each desktop transition.</span></span>
-   <span data-ttu-id="68737-252">La aplicación solo se puede iniciar a través del centro de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="68737-252">The application can be started only through the Ease of Access Center.</span></span>
-   <span data-ttu-id="68737-253">La aplicación debe guardar continuamente su configuración porque una transición de escritorio puede terminar en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="68737-253">The application must continually save its settings because it can be terminated at any time by a desktop transition.</span></span>

<span data-ttu-id="68737-254">Si la clave **TerminateOnDesktopSwitch** existe y está establecida en 0, Windows no ejecuta la aplicación de accesibilidad en un trabajo.</span><span class="sxs-lookup"><span data-stu-id="68737-254">If the **TerminateOnDesktopSwitch** key exists and is set to 0, Windows doesn't run the accessibility application in a job.</span></span> <span data-ttu-id="68737-255">Esto tiene las ventajas siguientes:</span><span class="sxs-lookup"><span data-stu-id="68737-255">This has the following advantages:</span></span>

-   <span data-ttu-id="68737-256">No hay costos de inicio asociados a las transiciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="68737-256">No startup costs are associated with desktop transitions.</span></span>
-   <span data-ttu-id="68737-257">La aplicación se puede iniciar fuera del centro de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="68737-257">The application can be started outside of the Ease of Access Center.</span></span>

<span data-ttu-id="68737-258">Las desventajas de no ejecutar en un trabajo incluyen:</span><span class="sxs-lookup"><span data-stu-id="68737-258">The disadvantages of not running in a job include:</span></span>

-   <span data-ttu-id="68737-259">Dado que la aplicación no se reinicia en las transiciones del escritorio, debe detectar cuándo está inactivo el escritorio actual y responder de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="68737-259">Because the application isn t restarted on desktop transitions, it must detect when the current desktop is inactive and respond appropriately.</span></span> <span data-ttu-id="68737-260">Por ejemplo, la aplicación debe ceder el control del hardware para que la versión de escritorio seguro de la aplicación pueda usarla, y la aplicación debe entrar en modo de suspensión para evitar el uso de los recursos del procesador.</span><span class="sxs-lookup"><span data-stu-id="68737-260">For example, the application must relinquish control of hardware so the secure desktop version of the application can use it, and the application should enter sleep mode to avoid using processor resources.</span></span>
-   <span data-ttu-id="68737-261">Si la aplicación se puede iniciar a través del menú Inicio, el explorador de Windows o la línea de comandos, se debe informar al centro de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="68737-261">If the application can be started through the Start menu, Windows Explorer, or the command line, the Ease of Access Center needs to be informed.</span></span> <span data-ttu-id="68737-262">Para obtener más información, consulte **tecla del logotipo de Windows + U**.</span><span class="sxs-lookup"><span data-stu-id="68737-262">For more information, see **Windows Logo key + U**.</span></span>
-   <span data-ttu-id="68737-263">Dado que se pueden ejecutar varias copias de la aplicación simultáneamente en distintos equipos de escritorio, la aplicación debe estar escrita para admitir varias copias en ejecución.</span><span class="sxs-lookup"><span data-stu-id="68737-263">Because multiple copies of the application can run simultaneously on different desktops, the application must be written to support multiple running copies.</span></span>

### <a name="windows-logo-key--u"></a><span data-ttu-id="68737-264">Tecla del logotipo de Windows + U</span><span class="sxs-lookup"><span data-stu-id="68737-264">Windows Logo key + U</span></span>

<span data-ttu-id="68737-265">Si la aplicación de accesibilidad está configurada para ejecutarse en un trabajo, el código de inicio de la aplicación debe incluir una llamada a la función [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) para determinar si la aplicación se está iniciando en un trabajo.</span><span class="sxs-lookup"><span data-stu-id="68737-265">If your accessibility application is configured to run in a job, your application's startup code should include a call to the [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) function to determine whether the application is starting in a job.</span></span> <span data-ttu-id="68737-266">Si es así, la aplicación debe iniciar el centro de accesibilidad y, a continuación, salir.</span><span class="sxs-lookup"><span data-stu-id="68737-266">If it is, the application should start the Ease of Access Center and then exit.</span></span> <span data-ttu-id="68737-267">En el ejemplo siguiente se muestra cómo llamar a **IsProcessInJob**.</span><span class="sxs-lookup"><span data-stu-id="68737-267">The following example shows how to call **IsProcessInJob**.</span></span>


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



<span data-ttu-id="68737-268">Si la aplicación de accesibilidad está configurada para ejecutarse fuera de un trabajo, debe notificar al centro de accesibilidad que la aplicación se está iniciando y continuar de la forma habitual.</span><span class="sxs-lookup"><span data-stu-id="68737-268">If the accessibility application is configured to run outside of a job, it should notify the Ease of Access Center that the application is starting and continue as normal.</span></span>

<span data-ttu-id="68737-269">Independientemente de cómo se configure la aplicación, si proporciona una manera de salir de la aplicación, como un botón Cerrar, la aplicación debe notificar al centro de accesibilidad que se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="68737-269">Regardless of how the application is configured, if it provides a way to exit from within the application, such as a Close button, the application must notify the Ease of Access Center that it is exiting.</span></span>

<span data-ttu-id="68737-270">Una aplicación notifica al centro de accesibilidad mediante el establecimiento de una clave del registro temporal y, después, la inserción de la combinación de teclas del logotipo de Windows + U en el flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="68737-270">An application notifies the Ease of Access Center by setting a temporary registry key and then injecting the Windows Logo key + U key combination into the input stream.</span></span>

<span data-ttu-id="68737-271">La aplicación debe crear la clave temporal en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="68737-271">The application should create the temporary key at the following location.</span></span>

<span data-ttu-id="68737-272">**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AccessibilityTemp**</span><span class="sxs-lookup"><span data-stu-id="68737-272">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\AccessibilityTemp**</span></span>

<span data-ttu-id="68737-273">La clave temporal debe tener el mismo nombre que el nombre de la aplicación registrada, como " \_ lector de pantalla de Contoso \_ v 1.0".</span><span class="sxs-lookup"><span data-stu-id="68737-273">The temporary key should have the same name as the registered application name, such as "Contoso\_Screen Reader\_v1.0".</span></span> <span data-ttu-id="68737-274">El valor de la clave es una **DWORD** establecida en 0x0003 cuando se inicia o 0x0002 cuando la aplicación se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="68737-274">The value of the key is a **DWORD** set to 0x0003 when it is starting, or 0x0002 when the application is exiting.</span></span>


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a><span data-ttu-id="68737-275">Tecla del logotipo de Windows + subir volumen</span><span class="sxs-lookup"><span data-stu-id="68737-275">Windows Logo key + Volume Up</span></span>

<span data-ttu-id="68737-276">Cuando el usuario inicia la aplicación de accesibilidad presionando la tecla del logotipo de Windows + combinación de teclas del volumen (por ejemplo, en un dispositivo de tableta gráfica), el centro de accesibilidad pasa el siguiente argumento de línea de comandos a la aplicación:</span><span class="sxs-lookup"><span data-stu-id="68737-276">When the user starts your accessibility application by pressing the Windows Logo key + Volume Up key combination (such as on a tablet device), the Ease of Access Center passes the following command-line argument to the application:</span></span>

<span data-ttu-id="68737-277">**/hardwarebuttonlaunch**</span><span class="sxs-lookup"><span data-stu-id="68737-277">**/hardwarebuttonlaunch**</span></span>

<span data-ttu-id="68737-278">La aplicación puede usar este argumento para determinar si se va a iniciar con normalidad o para ajustar el comportamiento en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="68737-278">Your application can use this argument to determine whether to start normally, or to adjust behavior accordingly.</span></span>

### <a name="transferring-secure-desktop-settings"></a><span data-ttu-id="68737-279">Transferencia de la configuración de escritorio seguro</span><span class="sxs-lookup"><span data-stu-id="68737-279">Transferring secure desktop settings</span></span>

<span data-ttu-id="68737-280">Si su aplicación de accesibilidad es compatible con el escritorio seguro, puede usar el registro para copiar la configuración cuando la aplicación pase al escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-280">If your accessibility application supports the secure desktop, you can use the registry to copy settings when the application transitions to the secure desktop.</span></span> <span data-ttu-id="68737-281">La copia de la configuración permite que la transición al escritorio seguro sea más fluida para el usuario.</span><span class="sxs-lookup"><span data-stu-id="68737-281">Copying settings helps makes the transition to the secure desktop more seamless for the user.</span></span>

<span data-ttu-id="68737-282">Para copiar la configuración, establezca la clave del registro CopySettingsToLockedDesktop de la aplicación en 1 y almacene la configuración en la siguiente ubicación del registro.</span><span class="sxs-lookup"><span data-stu-id="68737-282">To copy settings, set the application's CopySettingsToLockedDesktop registry key to 1, and store the settings in the following registry location.</span></span>

<span data-ttu-id="68737-283">**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATConfig\\<AT Key Name>**</span><span class="sxs-lookup"><span data-stu-id="68737-283">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATConfig\\<AT Key Name>**</span></span>

<span data-ttu-id="68737-284">El centro de accesibilidad supervisa esta ubicación del registro mientras la aplicación se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="68737-284">The Ease of Access Center monitors this registry location while the application is running.</span></span> <span data-ttu-id="68737-285">Cuando se produce una transición al escritorio seguro, el centro de accesibilidad copia la configuración en la misma ubicación del subárbol HKCU de escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-285">When a transition to the secure desktop occurs, the Ease of Access Center copies the settings to the same location in the secure desktop s HKCU hive.</span></span> <span data-ttu-id="68737-286">A continuación, la aplicación puede leer la configuración y reanudar su estado.</span><span class="sxs-lookup"><span data-stu-id="68737-286">The application can then read the settings and resume its state.</span></span>

<span data-ttu-id="68737-287">La aplicación de accesibilidad debe escribir su configuración a intervalos regulares o cada vez que cambien los valores.</span><span class="sxs-lookup"><span data-stu-id="68737-287">Your accessibility application should write its settings at regular intervals or whenever the values change.</span></span> <span data-ttu-id="68737-288">La escritura de la configuración en la salida de la aplicación no funcionará.</span><span class="sxs-lookup"><span data-stu-id="68737-288">Writing settings on application exit will not work.</span></span> <span data-ttu-id="68737-289">Si la aplicación se ejecuta en un trabajo, se termina en la transición fuera del escritorio seguro, antes de que el código de salida tenga la oportunidad de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="68737-289">If the application is running in a job, it is terminated on the transition away from the secure desktop, before the exit code has a chance to run.</span></span> <span data-ttu-id="68737-290">Si la aplicación no se está ejecutando en un trabajo, la aplicación no se termina en la transición fuera del escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68737-290">If the application is not running in a job, the application is not terminated on the transition away from the secure desktop.</span></span>

### <a name="caution"></a><span data-ttu-id="68737-291">Precaución</span><span class="sxs-lookup"><span data-stu-id="68737-291">Caution</span></span>

<span data-ttu-id="68737-292">Dado que las claves del registro que se describen aquí están escritas en modo de usuario, no son seguras.</span><span class="sxs-lookup"><span data-stu-id="68737-292">Because the registry keys described here are written in user mode, they are not secure.</span></span> <span data-ttu-id="68737-293">Si la aplicación de accesibilidad lee el contenido de estas claves, debe comprobar cuidadosamente los datos y utilizarlos con precaución.</span><span class="sxs-lookup"><span data-stu-id="68737-293">If your accessibility application reads the contents of these keys, it should carefully check the data and use it with caution.</span></span> <span data-ttu-id="68737-294">En concreto, la aplicación debe realizar una comprobación de los límites de los valores **DWORD** , tener cuidado con las longitudes de cadena, no debe leer los nombres de los archivos DLL del complemento y no debe ejecutar ningún comando que se encuentre en las cadenas.</span><span class="sxs-lookup"><span data-stu-id="68737-294">Specifically, your application should do a bounds check on **DWORD** values, be careful with string lengths, should not read plug-in DLL names, and should not execute any commands found in strings.</span></span>

## <a name="registry-examples"></a><span data-ttu-id="68737-295">Ejemplos del registro</span><span class="sxs-lookup"><span data-stu-id="68737-295">Registry Examples</span></span>

<span data-ttu-id="68737-296">En el ejemplo siguiente se muestran los posibles valores de registro de un producto ficticio denominado contoso ScreenReader versión 2,0, cuyo nombre localizado se almacena como un recurso.</span><span class="sxs-lookup"><span data-stu-id="68737-296">The following example shows the possible registry values for a fictitious product called Contoso ScreenReader version 2.0, whose localized name is stored as a resource.</span></span>

<span data-ttu-id="68737-297">Los valores de la tabla están bajo la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="68737-297">The values in the table are under the following key:</span></span>

<span data-ttu-id="68737-298">**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ contoso \_ Screen Reader \_ v 2.0**</span><span class="sxs-lookup"><span data-stu-id="68737-298">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\Contoso\_Screen Reader\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68737-299">Nombre</span><span class="sxs-lookup"><span data-stu-id="68737-299">Name</span></span></th>
<th><span data-ttu-id="68737-300">Tipo</span><span class="sxs-lookup"><span data-stu-id="68737-300">Type</span></span></th>
<th><span data-ttu-id="68737-301">Datos</span><span class="sxs-lookup"><span data-stu-id="68737-301">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68737-302">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="68737-302">ApplicationName</span></span></td>
<td><span data-ttu-id="68737-303">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-303">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-304">@% SystemRoot% \system32\ContosoRes.dll,-5020</span><span class="sxs-lookup"><span data-stu-id="68737-304">@%SystemRoot%\system32\ContosoRes.dll,-5020</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68737-305">Descripción</span><span class="sxs-lookup"><span data-stu-id="68737-305">Description</span></span></td>
<td><span data-ttu-id="68737-306">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-306">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-307">@% SystemRoot% \system32\ContosoRes.dll,-5040</span><span class="sxs-lookup"><span data-stu-id="68737-307">@%SystemRoot%\system32\ContosoRes.dll,-5040</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68737-308">Perfil</span><span class="sxs-lookup"><span data-stu-id="68737-308">Profile</span></span></td>
<td><span data-ttu-id="68737-309">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-309">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68737-310">XML</span><span class="sxs-lookup"><span data-stu-id="68737-310">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="68737-311">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="68737-311">SimpleProfile</span></span></td>
<td><span data-ttu-id="68737-312">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-312">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-313">ScreenReader</span><span class="sxs-lookup"><span data-stu-id="68737-313">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68737-314">Variable startexe ProcessStartInfo</span><span class="sxs-lookup"><span data-stu-id="68737-314">StartExe</span></span></td>
<td><span data-ttu-id="68737-315">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-315">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-316">C:\ContosoTools\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="68737-316">C:\ContosoTools\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68737-317">StartParams</span><span class="sxs-lookup"><span data-stu-id="68737-317">StartParams</span></span></td>
<td><span data-ttu-id="68737-318">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-318">REG_SZ</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="68737-319">SecureDesktopAccommodation</span><span class="sxs-lookup"><span data-stu-id="68737-319">SecureDesktopAccommodation</span></span></td>
<td><span data-ttu-id="68737-320">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-320">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-321">Narrador</span><span class="sxs-lookup"><span data-stu-id="68737-321">Narrator</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="68737-322">Si la aplicación proporciona un lector de pantalla y un ampliador de pantalla en un solo archivo ejecutable, los valores del componente lector de pantalla pueden tener este aspecto:</span><span class="sxs-lookup"><span data-stu-id="68737-322">If the application provides both a screen reader and a screen magnifier in a single executable, the values for the screen reader component might look like this:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68737-323">Nombre</span><span class="sxs-lookup"><span data-stu-id="68737-323">Name</span></span></th>
<th><span data-ttu-id="68737-324">Tipo</span><span class="sxs-lookup"><span data-stu-id="68737-324">Type</span></span></th>
<th><span data-ttu-id="68737-325">Datos</span><span class="sxs-lookup"><span data-stu-id="68737-325">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68737-326">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="68737-326">ApplicationName</span></span></td>
<td><span data-ttu-id="68737-327">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-327">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-328">@C:\Program Files\Contoso\Contosores.dll,-30</span><span class="sxs-lookup"><span data-stu-id="68737-328">@C:\Program Files\Contoso\Contosores.dll,-30</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68737-329">Descripción</span><span class="sxs-lookup"><span data-stu-id="68737-329">Description</span></span></td>
<td><span data-ttu-id="68737-330">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-330">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-331">@C:\Program Files\Contoso\Contosores.dll,-32</span><span class="sxs-lookup"><span data-stu-id="68737-331">@C:\Program Files\Contoso\Contosores.dll,-32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68737-332">Perfil</span><span class="sxs-lookup"><span data-stu-id="68737-332">Profile</span></span></td>
<td><span data-ttu-id="68737-333">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-333">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68737-334">XML</span><span class="sxs-lookup"><span data-stu-id="68737-334">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="68737-335">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="68737-335">SimpleProfile</span></span></td>
<td><span data-ttu-id="68737-336">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-336">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-337">ScreenReader</span><span class="sxs-lookup"><span data-stu-id="68737-337">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68737-338">Variable startexe ProcessStartInfo</span><span class="sxs-lookup"><span data-stu-id="68737-338">StartExe</span></span></td>
<td><span data-ttu-id="68737-339">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-339">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-340">C:\Archivos de Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="68737-340">C:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68737-341">StartParams</span><span class="sxs-lookup"><span data-stu-id="68737-341">StartParams</span></span></td>
<td><span data-ttu-id="68737-342">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-342">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-343">/r</span><span class="sxs-lookup"><span data-stu-id="68737-343">/r</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="68737-344">Los valores para el componente del ampliador tendrían la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="68737-344">The values for the magnifier component would be in the following key:</span></span>

<span data-ttu-id="68737-345">**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Contosoibility \\ ATS \\ contoso \_ Magnifier \_ v 2.0**</span><span class="sxs-lookup"><span data-stu-id="68737-345">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Contosoibility\\ATs\\Contoso\_Magnifier\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68737-346">Nombre</span><span class="sxs-lookup"><span data-stu-id="68737-346">Name</span></span></th>
<th><span data-ttu-id="68737-347">Tipo</span><span class="sxs-lookup"><span data-stu-id="68737-347">Type</span></span></th>
<th><span data-ttu-id="68737-348">Datos</span><span class="sxs-lookup"><span data-stu-id="68737-348">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68737-349">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="68737-349">ApplicationName</span></span></td>
<td><span data-ttu-id="68737-350">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-350">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-351">@c:\Program Files\Contoso\Contosores.dll,-31</span><span class="sxs-lookup"><span data-stu-id="68737-351">@c:\Program Files\Contoso\Contosores.dll,-31</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68737-352">Descripción</span><span class="sxs-lookup"><span data-stu-id="68737-352">Description</span></span></td>
<td><span data-ttu-id="68737-353">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-353">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-354">@c:\Program Files\Contoso\Contosores.dll,-42</span><span class="sxs-lookup"><span data-stu-id="68737-354">@c:\Program Files\Contoso\Contosores.dll,-42</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68737-355">Perfil</span><span class="sxs-lookup"><span data-stu-id="68737-355">Profile</span></span></td>
<td><span data-ttu-id="68737-356">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-356">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68737-357">XML</span><span class="sxs-lookup"><span data-stu-id="68737-357">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="68737-358">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="68737-358">SimpleProfile</span></span></td>
<td><span data-ttu-id="68737-359">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-359">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-360">Aumento</span><span class="sxs-lookup"><span data-stu-id="68737-360">Magnification</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68737-361">Variable startexe ProcessStartInfo</span><span class="sxs-lookup"><span data-stu-id="68737-361">StartExe</span></span></td>
<td><span data-ttu-id="68737-362">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-362">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-363">C:\Archivos de Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="68737-363">c:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68737-364">StartParams</span><span class="sxs-lookup"><span data-stu-id="68737-364">StartParams</span></span></td>
<td><span data-ttu-id="68737-365">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="68737-365">REG_SZ</span></span></td>
<td><span data-ttu-id="68737-366">/m</span><span class="sxs-lookup"><span data-stu-id="68737-366">/m</span></span></td>
</tr>
</tbody>
</table>



 

 

