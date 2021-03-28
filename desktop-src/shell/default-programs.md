---
description: Use programas predeterminados para establecer la experiencia del usuario predeterminada.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Programas predeterminados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cd741794189e47888f4daa1d4585b2d8942cf
ms.sourcegitcommit: 1a97e0e0f92d4dcc2fb68738b910ba3910508df3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2021
ms.locfileid: "103913910"
---
# <a name="default-programs"></a><span data-ttu-id="63245-103">Programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="63245-103">Default Programs</span></span>

<span data-ttu-id="63245-104">Use **programas predeterminados** para establecer la experiencia del usuario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="63245-104">Use **Default Programs** to set the default user experience.</span></span> <span data-ttu-id="63245-105">Los usuarios pueden tener acceso a **programas predeterminados** desde el panel de control o directamente desde el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="63245-105">Users can access **Default Programs** from Control Panel or directly from the **Start** menu.</span></span> <span data-ttu-id="63245-106">Configurar la herramienta de [acceso a programas y valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md) , la experiencia de valores predeterminados principales para los usuarios de Windows XP, es ahora una parte de los **programas predeterminados**.</span><span class="sxs-lookup"><span data-stu-id="63245-106">[Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) tool, the primary defaults experience for users in Windows XP, is now one part of **Default Programs**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63245-107">Este tema no se aplica a Windows 10.</span><span class="sxs-lookup"><span data-stu-id="63245-107">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="63245-108">La forma en que las asociaciones de archivos predeterminadas funcionan en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="63245-108">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="63245-109">Para obtener más información, consulte la sección **cambios en la forma en que Windows 10 trata las aplicaciones predeterminadas** en [esta publicación](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span><span class="sxs-lookup"><span data-stu-id="63245-109">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

<span data-ttu-id="63245-110">Cuando un usuario establece los valores predeterminados del programa mediante **programas predeterminados**, la configuración predeterminada solo se aplica a ese usuario y no a otros usuarios que puedan usar el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="63245-110">When a user sets program defaults using **Default Programs**, the default setting applies only to that user and not to other users who might use the same computer.</span></span> <span data-ttu-id="63245-111">**Programas predeterminados** proporciona un conjunto de API (en desuso en Windows 8) que permiten a los fabricantes de software independientes (ISV) incluir sus programas o aplicaciones en el sistema de valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="63245-111">**Default Programs** provides a set of APIs (deprecated in Windows 8) that enable independent software vendors (ISVs) to include their programs or applications in the defaults system.</span></span> <span data-ttu-id="63245-112">El conjunto de API también ayuda a los ISV a administrar mejor su estado como valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="63245-112">The API set also helps ISVs better manage their status as defaults.</span></span>

<span data-ttu-id="63245-113">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="63245-113">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="63245-114">Introducción a los programas predeterminados y a su conjunto de API relacionado</span><span class="sxs-lookup"><span data-stu-id="63245-114">Introduction to Default Programs and Its Related API Set</span></span>](#introduction-to-default-programs-and-its-related-api-set)
-   [<span data-ttu-id="63245-115">Registro de una aplicación para su uso con programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="63245-115">Registering an Application for Use with Default Programs</span></span>](#registering-an-application-for-use-with-default-programs)
    -   [<span data-ttu-id="63245-116">ProgID</span><span class="sxs-lookup"><span data-stu-id="63245-116">ProgIDs</span></span>](#progids)
    -   [<span data-ttu-id="63245-117">Descripciones de subclave y valor de registro</span><span class="sxs-lookup"><span data-stu-id="63245-117">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
    -   [<span data-ttu-id="63245-118">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="63245-118">RegisteredApplications</span></span>](#registeredapplications)
    -   [<span data-ttu-id="63245-119">Ejemplo de registro completo</span><span class="sxs-lookup"><span data-stu-id="63245-119">Full Registration Example</span></span>](#full-registration-example)
-   [<span data-ttu-id="63245-120">Convertirse en el explorador predeterminado</span><span class="sxs-lookup"><span data-stu-id="63245-120">Becoming the Default Browser</span></span>](#becoming-the-default-browser)
-   [<span data-ttu-id="63245-121">Interfaz de usuario de programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="63245-121">Default Programs UI</span></span>](#default-programs-ui)
-   [<span data-ttu-id="63245-122">Prácticas recomendadas para usar programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="63245-122">Best Practices for Using Default Programs</span></span>](#best-practices-for-using-default-programs)
    -   [<span data-ttu-id="63245-123">Durante la instalación</span><span class="sxs-lookup"><span data-stu-id="63245-123">During Installation</span></span>](#during-installation)
    -   [<span data-ttu-id="63245-124">Después de la instalación</span><span class="sxs-lookup"><span data-stu-id="63245-124">After Installation</span></span>](#after-installation)
-   [<span data-ttu-id="63245-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="63245-125">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="63245-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63245-126">Related topics</span></span>](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a><span data-ttu-id="63245-127">Introducción a los programas predeterminados y a su conjunto de API relacionado</span><span class="sxs-lookup"><span data-stu-id="63245-127">Introduction to Default Programs and Its Related API Set</span></span>

<span data-ttu-id="63245-128">Los **programas predeterminados** se han diseñado principalmente para las aplicaciones que usan tipos de archivo estándar, como archivos. mp3 o. jpg o protocolos estándar, como http o mailto.</span><span class="sxs-lookup"><span data-stu-id="63245-128">**Default Programs** is primarily designed for applications that use standard file types such as .mp3 or .jpg files or standard protocols, such as HTTP or mailto.</span></span> <span data-ttu-id="63245-129">Las aplicaciones que usan sus propios protocolos y asociaciones de archivo propios no suelen usar la funcionalidad **programas predeterminados** .</span><span class="sxs-lookup"><span data-stu-id="63245-129">Applications that use their own proprietary protocols and file associations do not typically use the **Default Programs** functionality.</span></span>

<span data-ttu-id="63245-130">Después de registrar una aplicación para la funcionalidad de **programas predeterminados** , las siguientes opciones y funcionalidades están disponibles mediante el conjunto de API:</span><span class="sxs-lookup"><span data-stu-id="63245-130">After you register an application for **Default Programs** functionality, the following options and functionality are available by using the API set:</span></span>

-   <span data-ttu-id="63245-131">Restaurar todos los valores predeterminados registrados de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-131">Restore all registered defaults for an application.</span></span> <span data-ttu-id="63245-132">En desuso para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63245-132">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="63245-133">Restaurar un único valor predeterminado registrado para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-133">Restore a single registered default for an application.</span></span> <span data-ttu-id="63245-134">En desuso para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63245-134">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="63245-135">Consulta el propietario de un valor predeterminado específico en una sola llamada en lugar de buscarlo en el registro.</span><span class="sxs-lookup"><span data-stu-id="63245-135">Query for the owner of a specific default in a single call instead of searching the registry.</span></span> <span data-ttu-id="63245-136">Puede consultar el valor predeterminado de una asociación de archivo, un protocolo o un verbo canónico del menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="63245-136">You can query for the default of a file association, protocol, or **Start** menu canonical verb.</span></span>
-   <span data-ttu-id="63245-137">Inicia una interfaz de usuario para una aplicación específica en la que un usuario puede establecer valores predeterminados individuales.</span><span class="sxs-lookup"><span data-stu-id="63245-137">Launch a UI for a specific application where a user can set individual defaults.</span></span>
-   <span data-ttu-id="63245-138">Quite todas las asociaciones por usuario.</span><span class="sxs-lookup"><span data-stu-id="63245-138">Remove all per-user associations.</span></span>

<span data-ttu-id="63245-139">**Programas predeterminados** también proporciona una interfaz de usuario que permite registrar una aplicación con el fin de proporcionar información adicional al usuario.</span><span class="sxs-lookup"><span data-stu-id="63245-139">**Default Programs** also provides a UI that enables you to register an application in order to provide additional information to the user.</span></span> <span data-ttu-id="63245-140">Por ejemplo, una aplicación firmada digitalmente puede incluir una dirección URL a la Página principal del fabricante.</span><span class="sxs-lookup"><span data-stu-id="63245-140">For example, a digitally signed application can include a URL to the manufacturer's home page.</span></span>

<span data-ttu-id="63245-141">El uso del conjunto de API asociado puede ayudar a que una aplicación funcione correctamente en la característica control de cuentas de usuario (UAC) introducida en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="63245-141">Use of the associated API set can help an application function correctly under the user account control (UAC) feature introduced in Windows Vista.</span></span> <span data-ttu-id="63245-142">En UAC, un administrador aparece como un usuario estándar en el sistema, por lo que el administrador no suele escribir en el subárbol de la **\_ \_ máquina local HKEY** .</span><span class="sxs-lookup"><span data-stu-id="63245-142">Under UAC, an administrator appears to the system as a standard user, so that administrator cannot typically write to the **HKEY\_LOCAL\_MACHINE** subtree.</span></span> <span data-ttu-id="63245-143">Esta restricción es una característica de seguridad que impide que un proceso actúe como administrador sin el conocimiento del administrador.</span><span class="sxs-lookup"><span data-stu-id="63245-143">This restriction is a security feature that prevents a process from acting as an administrator without the administrator's knowledge.</span></span>

<span data-ttu-id="63245-144">La instalación de un programa por parte de un usuario se realiza normalmente como un proceso con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="63245-144">Installation of a program by a user is typically performed as an elevated process.</span></span> <span data-ttu-id="63245-145">Sin embargo, los intentos de una aplicación para modificar los comportamientos de asociación predeterminados en un nivel de equipo posterior a la instalación no se realizarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="63245-145">However, attempts by an application to modify default association behaviors at a machine level post-installation will be unsuccessful.</span></span> <span data-ttu-id="63245-146">En su lugar, los valores predeterminados deben registrarse en un nivel por usuario, lo que impide que varios usuarios sobrescriban los valores predeterminados de los demás.</span><span class="sxs-lookup"><span data-stu-id="63245-146">Instead, defaults must be registered on a per-user level, which prevents multiple users from overwriting each other's defaults.</span></span>

<span data-ttu-id="63245-147">La estructura jerárquica del registro para las asociaciones de archivos y protocolos da prioridad a los valores predeterminados por usuario a través de los valores predeterminados de nivel de equipo.</span><span class="sxs-lookup"><span data-stu-id="63245-147">The hierarchical registry structure for file and protocol associations gives precedence to per-user defaults over machine-level defaults.</span></span> <span data-ttu-id="63245-148">Algunas aplicaciones incluyen puntos en el código que elevan temporalmente sus derechos cuando reclaman valores predeterminados registrados en **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="63245-148">Some applications include points in their code that temporarily elevate their rights when they claim defaults registered in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="63245-149">Estas aplicaciones podrían experimentar resultados inesperados si otra aplicación ya está registrada como predeterminada por usuario.</span><span class="sxs-lookup"><span data-stu-id="63245-149">These applications might experience unexpected results if another application is already registered as the per-user default.</span></span> <span data-ttu-id="63245-150">El uso de **programas predeterminados** evita esta ambigüedad y garantiza los resultados esperados en un nivel por usuario.</span><span class="sxs-lookup"><span data-stu-id="63245-150">Use of **Default Programs** prevents this ambiguity and guarantees expected results on a per-user level.</span></span>

## <a name="registering-an-application-for-use-with-default-programs"></a><span data-ttu-id="63245-151">Registro de una aplicación para su uso con programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="63245-151">Registering an Application for Use with Default Programs</span></span>

<span data-ttu-id="63245-152">En esta sección se muestran las subclaves del registro y los valores necesarios para registrar una aplicación con **programas predeterminados**.</span><span class="sxs-lookup"><span data-stu-id="63245-152">This section shows you the registry subkeys and values needed to register an application with **Default Programs**.</span></span> <span data-ttu-id="63245-153">Incluye un ejemplo completo.</span><span class="sxs-lookup"><span data-stu-id="63245-153">It includes a full example.</span></span>

<span data-ttu-id="63245-154">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="63245-154">This section contains the following topics:</span></span>

-   [<span data-ttu-id="63245-155">ProgID</span><span class="sxs-lookup"><span data-stu-id="63245-155">ProgIDs</span></span>](#progids)
-   [<span data-ttu-id="63245-156">Descripciones de subclave y valor de registro</span><span class="sxs-lookup"><span data-stu-id="63245-156">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
-   [<span data-ttu-id="63245-157">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="63245-157">RegisteredApplications</span></span>](#registeredapplications)
-   [<span data-ttu-id="63245-158">Ejemplo de registro completo</span><span class="sxs-lookup"><span data-stu-id="63245-158">Full Registration Example</span></span>](#full-registration-example)

<span data-ttu-id="63245-159">**Programas predeterminados** requiere que cada aplicación se registre explícitamente las asociaciones de archivo, las asociaciones MIME y los protocolos para los que la aplicación debe aparecer como un valor predeterminado posible.</span><span class="sxs-lookup"><span data-stu-id="63245-159">**Default Programs** requires each application to register explicitly the file associations, MIME associations, and protocols for which the application should be listed as a possible default.</span></span> <span data-ttu-id="63245-160">Las asociaciones se registran mediante los siguientes elementos del registro, que se explican en detalle más adelante en este tema, en [descripciones de subclave y valor de registro](#registration-subkey-and-value-descriptions):</span><span class="sxs-lookup"><span data-stu-id="63245-160">You register the associations by using the following registry elements, which are explained in detail later in this topic under [Registration Subkey and Value Descriptions](#registration-subkey-and-value-descriptions):</span></span>

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

<span data-ttu-id="63245-161">En el ejemplo siguiente se muestran las entradas del registro para un explorador ficticio de Contoso denominado WebBrowser:</span><span class="sxs-lookup"><span data-stu-id="63245-161">The following example shows the registry entries for a fictional Contoso browser that is called WebBrowser:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a><span data-ttu-id="63245-162">ProgID</span><span class="sxs-lookup"><span data-stu-id="63245-162">ProgIDs</span></span>

<span data-ttu-id="63245-163">Una aplicación debe proporcionar un [ProgID](fa-progids.md)específico.</span><span class="sxs-lookup"><span data-stu-id="63245-163">An application must provide a specific [ProgID](fa-progids.md).</span></span> <span data-ttu-id="63245-164">Asegúrese de incluir toda la información que se escribe normalmente en la subclave predeterminada genérica de la extensión.</span><span class="sxs-lookup"><span data-stu-id="63245-164">Be sure to include all the information that is typically written into the generic default subkey for the extension.</span></span> <span data-ttu-id="63245-165">Por ejemplo, el reproductor multimedia ficticio ficticia proporciona las clases de software del **\_ \_ equipo local HKEY** específico de la aplicación \\  \\  \\ **LitwarePlayer11.AssocFile.MP3** subclave.</span><span class="sxs-lookup"><span data-stu-id="63245-165">For example, the fictional Litware media player provides the application-specific **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**LitwarePlayer11.AssocFile.MP3** subkey.</span></span> <span data-ttu-id="63245-166">Esa subclave incluye toda la información de la subclave predeterminada genérica **HKEY \_ local \_ Machine** \\ **software** \\ **classes** \\ **. mp3** y cualquier información adicional que desee que la aplicación registre.</span><span class="sxs-lookup"><span data-stu-id="63245-166">That subkey includes all the information in the generic default subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\ **.mp3** plus any additional information that you want the application to register.</span></span> <span data-ttu-id="63245-167">Esto garantiza que si el usuario restaura la asociación. mp3 al reproductor de Litware, la información del jugador de Litware está intacta y no se ha sobrescrito por otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-167">This ensures that if the user restores the .mp3 association to the Litware player, the Litware player's information is intact and has not been overwritten by another application.</span></span> <span data-ttu-id="63245-168">(Se puede sobrescribir si la subclave predeterminada es el único origen de esa información).</span><span class="sxs-lookup"><span data-stu-id="63245-168">(Overwriting might occur if the default subkey is the only source of that information.)</span></span>

<span data-ttu-id="63245-169">Cuando se asigna un ProgID a una extensión de nombre de archivo o protocolo, una aplicación puede asignar uno a uno o uno a varios.</span><span class="sxs-lookup"><span data-stu-id="63245-169">When you map a ProgID to a file name extension or protocol, an application can map one-to-one or one-to-many.</span></span> <span data-ttu-id="63245-170">En el ejemplo de Contoso, ContosoHTML señala a un ProgID único que proporciona información de ShellExecute para las extensiones. htm,. html,. shtml,. XHT y. XHTML.</span><span class="sxs-lookup"><span data-stu-id="63245-170">In the Contoso example, ContosoHTML points to a single ProgID that provides shellexecute information for the .htm, .html, .shtml, .xht, and .xhtml extensions.</span></span> <span data-ttu-id="63245-171">Dado que existe un ProgID diferente para cada protocolo, cuando se utilizan protocolos se habilita cada protocolo para que tenga su propia cadena de ejecución.</span><span class="sxs-lookup"><span data-stu-id="63245-171">Because a different ProgID exists for each protocol, when you use protocols you enable each protocol to have its own execution string.</span></span>

<span data-ttu-id="63245-172">Cuando el tipo MIME se puede ver en línea en un explorador, el ProgID del tipo MIME debe contener la subclave **CLSID** que usa el identificador de clase (CLSID) de la aplicación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="63245-172">When your MIME type can be viewed inline in a browser, the ProgID for the MIME type must contain the **CLSID** subkey that uses the class identifier (CLSID) of the corresponding application.</span></span> <span data-ttu-id="63245-173">Este CLSID se usa en una búsqueda en el CLSID en la base de datos MIME almacenada en **HKEY \_ local \_ Machine** \\ **software** \\ **classes** \\ **MIME** \\ **Database** \\ **Type**.</span><span class="sxs-lookup"><span data-stu-id="63245-173">This CLSID is used in a lookup against the CLSID in the MIME database that is stored in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**MIME**\\**Database**\\**Content Type**.</span></span> <span data-ttu-id="63245-174">Si el tipo MIME no se ha diseñado para que se vea en línea en un explorador, este paso se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="63245-174">If your MIME type is not intended to be viewed inline in a browser, this step can be omitted.</span></span>

### <a name="registration-subkey-and-value-descriptions"></a><span data-ttu-id="63245-175">Descripciones de subclave y valor de registro</span><span class="sxs-lookup"><span data-stu-id="63245-175">Registration Subkey and Value Descriptions</span></span>

<span data-ttu-id="63245-176">En esta sección se describen las subclaves individuales del registro y los valores que se usan para registrar una aplicación con **programas predeterminados**, como se muestra anteriormente.</span><span class="sxs-lookup"><span data-stu-id="63245-176">This section describes the individual registry subkeys and values used in registering an application with **Default Programs**, as illustrated previously.</span></span>

### <a name="capabilities"></a><span data-ttu-id="63245-177">Funcionalidades</span><span class="sxs-lookup"><span data-stu-id="63245-177">Capabilities</span></span>

<span data-ttu-id="63245-178">La subclave **Capabilities** contiene toda la información de **programas predeterminados** para una aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="63245-178">The **Capabilities** subkey contains all the **Default Programs** information for a specific application.</span></span> <span data-ttu-id="63245-179">El marcador de posición% ApplicationCapabilityPath% hace referencia a la ruta de acceso del registro desde **HKEY \_ Current \_ User** o **HKEY \_ local \_ Machine** a la subclave **Capabilities** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-179">The placeholder %ApplicationCapabilityPath% refers to the registry path from either **HKEY\_CURRENT\_USER** or **HKEY\_LOCAL\_MACHINE** to the application's **Capabilities** subkey.</span></span> <span data-ttu-id="63245-180">Esta subclave contiene los valores significativos que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="63245-180">This subkey contains the significant values shown in the following table.</span></span>



| <span data-ttu-id="63245-181">Value</span><span class="sxs-lookup"><span data-stu-id="63245-181">Value</span></span>                  | <span data-ttu-id="63245-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="63245-182">Type</span></span>                       | <span data-ttu-id="63245-183">Significado</span><span class="sxs-lookup"><span data-stu-id="63245-183">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63245-184">ApplicationDescription</span><span class="sxs-lookup"><span data-stu-id="63245-184">ApplicationDescription</span></span> | <span data-ttu-id="63245-185">REG \_ SZ o REG \_ Expand \_</span><span class="sxs-lookup"><span data-stu-id="63245-185">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="63245-186">**Requerido**.</span><span class="sxs-lookup"><span data-stu-id="63245-186">**Required**.</span></span> <span data-ttu-id="63245-187">Para permitir que un usuario realice una elección de asignación predeterminada informada, una aplicación debe proporcionar una cadena que describa las capacidades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-187">To enable a user to make an informed default assignment choice, an application must provide a string that describes the application's capabilities.</span></span> <span data-ttu-id="63245-188">Aunque el ejemplo de Contoso anterior asigna la descripción directamente al valor de ApplicationDescription, las aplicaciones normalmente proporcionan la descripción como un recurso que se inserta en un archivo. dll para facilitar la localización.</span><span class="sxs-lookup"><span data-stu-id="63245-188">Although the previous Contoso example assigns the description directly to the ApplicationDescription value, applications typically provide the description as a resource that is embedded in a .dll file to facilitate localization.</span></span> <span data-ttu-id="63245-189">Si no se proporciona ApplicationDescription, la aplicación no aparece en las listas de interfaz de usuario de posibles programas predeterminados.</span><span class="sxs-lookup"><span data-stu-id="63245-189">If ApplicationDescription is not provided, the application does not appear in UI lists of potential default programs.</span></span>                                                            |
| <span data-ttu-id="63245-190">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="63245-190">ApplicationName</span></span>        | <span data-ttu-id="63245-191">REG \_ SZ o REG \_ Expand \_</span><span class="sxs-lookup"><span data-stu-id="63245-191">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="63245-192">**Opcional.**</span><span class="sxs-lookup"><span data-stu-id="63245-192">**Optional.**</span></span> <span data-ttu-id="63245-193">El nombre por el que aparece el programa en la interfaz de usuario de programas predeterminados.</span><span class="sxs-lookup"><span data-stu-id="63245-193">The name by which the program appears in the Default Programs UI.</span></span> <span data-ttu-id="63245-194">Si la aplicación no proporciona estos datos, en la interfaz de usuario se usa el nombre del programa ejecutable que está asociado al primer ProgID registrado para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-194">If this data is not provided by the application, the name of the executable program that is associated with the first registered ProgID for the application is used in the UI.</span></span> <span data-ttu-id="63245-195">ApplicationName siempre debe coincidir con el nombre registrado en [RegisteredApplications](#registeredapplications).</span><span class="sxs-lookup"><span data-stu-id="63245-195">ApplicationName must always match the name that is registered under [RegisteredApplications](#registeredapplications).</span></span> <span data-ttu-id="63245-196">Puede usar ApplicationName si desea diferentes tipos de aplicaciones, como un explorador y un cliente de correo electrónico, para que apunten al mismo archivo ejecutable mientras aparecen como nombres diferentes.</span><span class="sxs-lookup"><span data-stu-id="63245-196">You can use ApplicationName if you want different application types, such as a browser and an email client, to point to the same executable file while they appear as different names.</span></span><br/> |
| <span data-ttu-id="63245-197">Hidden</span><span class="sxs-lookup"><span data-stu-id="63245-197">Hidden</span></span>                 | <span data-ttu-id="63245-198">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="63245-198">REG\_DWORD</span></span>                 | <span data-ttu-id="63245-199">**Opcional.**</span><span class="sxs-lookup"><span data-stu-id="63245-199">**Optional.**</span></span> <span data-ttu-id="63245-200">Establezca este valor en 1 para suprimir la aplicación de la lista de programas en el cuadro de diálogo **establecer programas predeterminados** .</span><span class="sxs-lookup"><span data-stu-id="63245-200">Set this value to 1 to suppress the application from the list of programs in the **Set your default programs** dialog.</span></span> <span data-ttu-id="63245-201">Si este valor es 0 o no está presente, la aplicación aparece en la lista normalmente.</span><span class="sxs-lookup"><span data-stu-id="63245-201">If this value is 0 or not present, then the application appears in the list normally.</span></span>                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a><span data-ttu-id="63245-202">FileAssociations</span><span class="sxs-lookup"><span data-stu-id="63245-202">FileAssociations</span></span>

<span data-ttu-id="63245-203">La subclave **FileAssociations** contiene asociaciones de archivo específicas que se reclaman por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-203">The **FileAssociations** subkey contains specific file associations that are claimed by the application.</span></span> <span data-ttu-id="63245-204">Estas notificaciones se almacenan como valores, con un valor para cada extensión.</span><span class="sxs-lookup"><span data-stu-id="63245-204">These claims are stored as values, with one value for each extension.</span></span> <span data-ttu-id="63245-205">Las asociaciones apuntan a un ProgID específico de la aplicación en lugar de un ProgID genérico.</span><span class="sxs-lookup"><span data-stu-id="63245-205">Associations point to an application-specific ProgID instead of a generic ProgID.</span></span> <span data-ttu-id="63245-206">Sin embargo, no es necesario que todas las asociaciones señalen al mismo ProgID.</span><span class="sxs-lookup"><span data-stu-id="63245-206">However, all associations are not required to point to the same ProgID.</span></span>

### <a name="mimeassociations"></a><span data-ttu-id="63245-207">MIMEAssociations</span><span class="sxs-lookup"><span data-stu-id="63245-207">MIMEAssociations</span></span>

<span data-ttu-id="63245-208">La subclave **MIMEAssociations** contiene tipos MIME específicos que se reclaman por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-208">The **MIMEAssociations** subkey contains specific MIME types that are claimed by the application.</span></span> <span data-ttu-id="63245-209">Estas notificaciones se almacenan como valores, con un valor para cada tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="63245-209">These claims are stored as values, with one value for each MIME type.</span></span> <span data-ttu-id="63245-210">El nombre de valor de cada tipo MIME debe coincidir exactamente con el nombre MIME almacenado en la base de datos MIME.</span><span class="sxs-lookup"><span data-stu-id="63245-210">The value name for each MIME type must exactly match the MIME name that is stored in the MIME database.</span></span> <span data-ttu-id="63245-211">También se debe asignar al valor un ProgID específico de la aplicación que contenga el CLSID correspondiente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-211">The value must also be assigned an application-specific ProgID that contains the corresponding CLSID of the application.</span></span>

### <a name="startmenu"></a><span data-ttu-id="63245-212">Inicio</span><span class="sxs-lookup"><span data-stu-id="63245-212">Startmenu</span></span>

<span data-ttu-id="63245-213">La subclave **Inicio** está asociada a las entradas de **correo electrónico** y de **Internet** asignables por el usuario en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="63245-213">The **Startmenu** subkey is associated with the user-assignable **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="63245-214">Una aplicación debe registrarse por separado como un contratador para esas entradas.</span><span class="sxs-lookup"><span data-stu-id="63245-214">An application must register separately as a contender for those entries.</span></span> <span data-ttu-id="63245-215">Para obtener más información, consulte [registrar programas con tipos de cliente](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="63245-215">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

> [!Note]  
> <span data-ttu-id="63245-216">A partir de Windows 7, ya no hay entradas de **Internet** y de **correo electrónico** en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="63245-216">As of Windows 7, there are no longer **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="63245-217">Los datos del registro asociados a la entrada de **correo electrónico** se siguen usando para el cliente MAPI predeterminado, pero Windows no utiliza los datos del registro asociados a la entrada de **Internet** .</span><span class="sxs-lookup"><span data-stu-id="63245-217">The registry data associated with the **E-mail** entry is still used for the default MAPI client, but the registry data associated with the **Internet** entry is not used by Windows at all.</span></span>

 

<span data-ttu-id="63245-218">Al asociar el registro del menú **Inicio** de una aplicación con el registro de sus **programas predeterminados** , la aplicación aparece como valor predeterminado potencial en la interfaz de usuario de **asociaciones de conjunto** .</span><span class="sxs-lookup"><span data-stu-id="63245-218">By associating the **Start** menu registration of an application with its **Default Programs** registration, the application appears as a potential default in the **Set associations** UI.</span></span> <span data-ttu-id="63245-219">Si el usuario ha elegido la aplicación como predeterminada y, a continuación, elige restaurar todos los valores predeterminados de la aplicación más tarde, la aplicación se restaura en su posición en el menú **Inicio** para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="63245-219">If the user has chosen the application as the default and then chooses to restore all application defaults later, the application is restored to its **Start** menu position for that user.</span></span> <span data-ttu-id="63245-220">Para obtener más información y una ilustración, vea la sección [interfaz de usuario de programas predeterminados](#default-programs-ui) más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="63245-220">For more information and an illustration, see the [Default Programs UI](#default-programs-ui) section later in this topic.</span></span>

<span data-ttu-id="63245-221">La subclave **Inicio** tiene dos entradas: StartMenuInternet y mail, que corresponden a las posiciones de **Internet** y **correo electrónico** canónicas en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="63245-221">The **Startmenu** subkey has two entries: StartMenuInternet and Mail, which correspond to the canonical **Internet** and **E-mail** positions in the **Start** menu.</span></span> <span data-ttu-id="63245-222">Una aplicación asigna StartMenuInternet o mail un valor igual al nombre de la subclave registrada de la aplicación en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** o **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** (como se describe en [registrar programas con tipos de cliente](reg-middleware-apps.md)).</span><span class="sxs-lookup"><span data-stu-id="63245-222">An application assigns either StartMenuInternet or Mail a value equal to the name of the application's registered subkey under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** or **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** (as described in [Registering Programs with Client Types](reg-middleware-apps.md)).</span></span>

<span data-ttu-id="63245-223">En el caso de la posición canónica de **correo electrónico** en el menú **Inicio** , representa el cliente MAPI predeterminado y, por lo tanto, se supone que es capaz de controlar las llamadas MAPI.</span><span class="sxs-lookup"><span data-stu-id="63245-223">In the case of the **E-mail** canonical position in the **Start** menu, it represents the default MAPI client and is therefore assumed capable of handing MAPI calls.</span></span> <span data-ttu-id="63245-224">En Windows 7, aunque ya no existe una posición canónica de **correo electrónico** en el menú **Inicio** , esta subclave se sigue usando para el cliente MAPI predeterminado.</span><span class="sxs-lookup"><span data-stu-id="63245-224">Under Windows 7, while there is no longer an **E-mail** canonical position in the **Start** menu, this subkey continues to be used for the default MAPI client.</span></span> <span data-ttu-id="63245-225">Una aplicación que solicite el correo predeterminado debe registrarse como controlador MAPI en la siguiente subclave:</span><span class="sxs-lookup"><span data-stu-id="63245-225">An application claiming the mail default should register as a MAPI handler under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

<span data-ttu-id="63245-226">Si un cliente de correo no admite MAPI pero aún desea competir por la posición canónica de **correo electrónico** del menú **Inicio** , puede registrar una línea de comandos en la siguiente subclave:</span><span class="sxs-lookup"><span data-stu-id="63245-226">If a mail client cannot support MAPI but still wants to contend for the **Start** menu **E-mail** canonical position, it can register a command line under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

<span data-ttu-id="63245-227">Además, en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** \\ *CanonicalName* , agregue un valor predeterminado con el nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-227">Also, under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**\\*CanonicalName* add a default value with the application name.</span></span>

<span data-ttu-id="63245-228">Estas entradas permiten que la aplicación se inicie desde la posición de **correo electrónico** del menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="63245-228">These entries allow the application to be launched from the **Start** menu's **E-mail** position.</span></span> <span data-ttu-id="63245-229">Tenga en cuenta que las llamadas MAPI todavía se realizan en la aplicación y se llevan a cabo hasta el controlador MAPI anterior, o bien se produce un error si no se ha establecido ningún controlador MAPI.</span><span class="sxs-lookup"><span data-stu-id="63245-229">Note that MAPI calls are still made to the application, and either fall through to the prior MAPI handler, or fail if no MAPI handler has been set.</span></span> <span data-ttu-id="63245-230">Para obtener más información, consulte [registrar programas con tipos de cliente](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="63245-230">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

### <a name="urlassociations"></a><span data-ttu-id="63245-231">UrlAssociations</span><span class="sxs-lookup"><span data-stu-id="63245-231">UrlAssociations</span></span>

<span data-ttu-id="63245-232">La subclave **UrlAssociations** contiene los protocolos de dirección URL específicos que solicita la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-232">The **UrlAssociations** subkey contains the specific URL protocols that are claimed by the application.</span></span> <span data-ttu-id="63245-233">Estas notificaciones se almacenan como valores, con un valor para cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="63245-233">These claims are stored as values, with one value for each protocol.</span></span> <span data-ttu-id="63245-234">Cada protocolo debe apuntar a un ProgID específico de la aplicación en lugar de a un ProgID genérico.</span><span class="sxs-lookup"><span data-stu-id="63245-234">Each protocol must point to an application-specific ProgID instead of to a generic ProgID.</span></span> <span data-ttu-id="63245-235">Como se mencionó en el ejemplo de Contoso, puede usar un ProgID diferente para cada protocolo para que cada uno tenga su propia cadena de ejecución.</span><span class="sxs-lookup"><span data-stu-id="63245-235">As mentioned in the Contoso example, you can use a different ProgID for each protocol in order for each to have its own execution string.</span></span>

### <a name="registeredapplications"></a><span data-ttu-id="63245-236">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="63245-236">RegisteredApplications</span></span>

<span data-ttu-id="63245-237">La subclave completa de **RegisteredApplications** es:</span><span class="sxs-lookup"><span data-stu-id="63245-237">The full subkey for **RegisteredApplications** is:</span></span>

<span data-ttu-id="63245-238">**HKEY \_ \_** RegisteredApplications de \\ **software** \\  de equipo local</span><span class="sxs-lookup"><span data-stu-id="63245-238">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**RegisteredApplications**</span></span>

<span data-ttu-id="63245-239">Esta subclave proporciona el sistema operativo con la ubicación del registro de la información de **programas predeterminados** para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-239">This subkey provides the operating system with the registry location of the **Default Programs** information for the application.</span></span> <span data-ttu-id="63245-240">La ubicación se almacena como un valor cuyo nombre debe coincidir con el nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-240">The location is stored as a value whose name must match the name of the application.</span></span>

### <a name="full-registration-example"></a><span data-ttu-id="63245-241">Ejemplo de registro completo</span><span class="sxs-lookup"><span data-stu-id="63245-241">Full Registration Example</span></span>

<span data-ttu-id="63245-242">En este ejemplo se muestran las subclaves y los valores que se usan para registrar el reproductor multimedia ficticio ficticia.</span><span class="sxs-lookup"><span data-stu-id="63245-242">This example shows the subkeys and values that are used in registering the fictional Litware media player.</span></span> <span data-ttu-id="63245-243">En el ejemplo se incluyen las entradas ProgID para mostrar cómo encaja todo.</span><span class="sxs-lookup"><span data-stu-id="63245-243">The example includes the ProgID entries in order to show how it all fits together.</span></span>

<span data-ttu-id="63245-244">La siguiente subclave muestra el ProgID específico de la aplicación para el tipo MIME. mp3:</span><span class="sxs-lookup"><span data-stu-id="63245-244">The following subkey shows the application-specific ProgID for the .mp3 MIME type:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

<span data-ttu-id="63245-245">A continuación se encuentra el ProgID específico de la aplicación que asocia el programa Litware a la extensión de nombre de archivo. mp3.</span><span class="sxs-lookup"><span data-stu-id="63245-245">Next is the application-specific ProgID that associates the Litware program with the .mp3 file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="63245-246">Las entradas siguientes muestran el ProgID combinado para el tipo MIME de. MPEG y la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="63245-246">The next entries show the combined ProgID for both the .mpeg MIME type and file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="63245-247">Las siguientes entradas registran el programa Litware en **programas predeterminados** y usan los ProgID previamente registrados</span><span class="sxs-lookup"><span data-stu-id="63245-247">The next entries register the Litware program in **Default Programs** and use the previously registered ProgIDs</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

<span data-ttu-id="63245-248">Por último, en este ejemplo se registra la ubicación del registro de **programas predeterminados** de Litware.</span><span class="sxs-lookup"><span data-stu-id="63245-248">Lastly, this example registers the location of the Litware **Default Programs** registration.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a><span data-ttu-id="63245-249">Convertirse en el explorador predeterminado</span><span class="sxs-lookup"><span data-stu-id="63245-249">Becoming the Default Browser</span></span>

<span data-ttu-id="63245-250">El registro del explorador debe seguir las prácticas recomendadas que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="63245-250">Browser registration must follow the best practices outlined in this topic.</span></span> <span data-ttu-id="63245-251">Cuando se instala el explorador, Windows puede presentar al usuario una notificación del sistema a través de la cual el usuario puede seleccionar el explorador como predeterminado del sistema.</span><span class="sxs-lookup"><span data-stu-id="63245-251">When the browser is installed, Windows can present the user with a system notification through which the user can select the browser as the system default.</span></span> <span data-ttu-id="63245-252">Esta notificación se muestra cuando se cumplen estas condiciones:</span><span class="sxs-lookup"><span data-stu-id="63245-252">This notification is shown when these conditions are met:</span></span>

-   <span data-ttu-id="63245-253">El instalador del explorador llama a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con la marca **SHCNE \_ ASSOCCHANGED** para indicar a Windows que se han registrado nuevos controladores de protocolo.</span><span class="sxs-lookup"><span data-stu-id="63245-253">The browser's installer calls [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the **SHCNE\_ASSOCCHANGED** flag to tell Windows that new protocol handlers have been registered.</span></span>
-   <span data-ttu-id="63245-254">Windows detecta que una o varias aplicaciones nuevas se han registrado para controlar los protocolos http://y https://, y el usuario aún no se ha notificado.</span><span class="sxs-lookup"><span data-stu-id="63245-254">Windows detects that one or more new applications have registered to handle both http:// and https:// protocols, and the user has not yet been notified.</span></span> <span data-ttu-id="63245-255">En otras palabras, no se ha mostrado nada de lo siguiente al usuario: una notificación del sistema que anuncia la aplicación, un control flotante de OpenWith que contiene la aplicación o la página del panel de control establecer valores predeterminados del usuario (SUD) para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-255">In other words, none of the following have been shown to the user: a system notification advertising the application, an OpenWith flyout that contains the application, or the Set User Defaults (SUD) Control Panel page for the application.</span></span>

<span data-ttu-id="63245-256">En el ejemplo siguiente se muestra el código de registro recomendado que el instalador del explorador debe ejecutar después de escribir sus claves del registro.</span><span class="sxs-lookup"><span data-stu-id="63245-256">The following example shows the recommended registration code that the browser's installer should run after it writes its registry keys.</span></span>

<span data-ttu-id="63245-257">[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) primero notifica al sistema que hay disponibles nuevas opciones de asociación.</span><span class="sxs-lookup"><span data-stu-id="63245-257">[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) first notifies the system that new association choices are available.</span></span> <span data-ttu-id="63245-258">La llamada a **SHChangeNotify** es necesaria para garantizar el correcto funcionamiento de los valores predeterminados del sistema.</span><span class="sxs-lookup"><span data-stu-id="63245-258">The **SHChangeNotify** call is required to ensure the proper functioning of system defaults.</span></span>

<span data-ttu-id="63245-259">Una instrucción [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) permite a los procesos del sistema controlar la notificación.</span><span class="sxs-lookup"><span data-stu-id="63245-259">A [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) statement then allows time for system processes to handle the notification.</span></span>


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



<span data-ttu-id="63245-260">Si el usuario descarta u omite la notificación o el control flotante resultante sin crear una nueva selección predeterminada del explorador, el explorador predeterminado permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="63245-260">If the user dismisses or ignores the resulting notification or flyout without making a new default browser selection, the default browser remains unchanged.</span></span> <span data-ttu-id="63245-261">Tenga en cuenta que el usuario también puede cambiar el explorador predeterminado en cualquier momento a través de otros mecanismos, incluidos los valores predeterminados establecidos por el usuario en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="63245-261">Note that the user can also change the default browser at any time through other mechanisms, including Set User Defaults in the Control Panel.</span></span>

## <a name="default-programs-ui"></a><span data-ttu-id="63245-262">Interfaz de usuario de programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="63245-262">Default Programs UI</span></span>

<span data-ttu-id="63245-263">En las ilustraciones de esta sección se muestra la interfaz de usuario de los **programas predeterminados** tal y como se muestra en el usuario.</span><span class="sxs-lookup"><span data-stu-id="63245-263">The illustrations in this section show the UI for **Default Programs** as seen by the user.</span></span>

<span data-ttu-id="63245-264">En la ilustración siguiente se muestra la ventana **programas predeterminados** principales del panel de control.</span><span class="sxs-lookup"><span data-stu-id="63245-264">The following illustration shows the main **Default Programs** window in Control Panel.</span></span>

![captura de pantalla de la página de entrada programas predeterminados](images/defaultprogramsmain.png)

<span data-ttu-id="63245-266">Cuando un usuario elige la opción **establecer programas predeterminados** , aparece la siguiente ventana.</span><span class="sxs-lookup"><span data-stu-id="63245-266">When a user chooses the **Set your default programs** option, the following window appears.</span></span> <span data-ttu-id="63245-267">Los usuarios pueden usar esta página para asignar un programa predeterminado para todos los tipos de archivos y protocolos para los que el programa sea un valor predeterminado posible.</span><span class="sxs-lookup"><span data-stu-id="63245-267">Users can use this page to assign a default program for all file types and protocols for which the program is a possible default.</span></span> <span data-ttu-id="63245-268">Como se muestra en la siguiente ilustración, todos los programas [registrados](#registering-an-application-for-use-with-default-programs) y el icono del programa aparecen en el cuadro **programas** de la izquierda.</span><span class="sxs-lookup"><span data-stu-id="63245-268">As shown in the following illustration, all [registered](#registering-an-application-for-use-with-default-programs) programs and the program icon appear in the **Programs** box on the left.</span></span>

![captura de pantalla de la página establecer programas predeterminados](images/setyourdefaultprograms.png)

<span data-ttu-id="63245-270">Cuando el usuario selecciona un programa de la lista, se muestran el icono del programa y el proveedor.</span><span class="sxs-lookup"><span data-stu-id="63245-270">When the user selects a program from the list, the program icon and provider are displayed.</span></span> <span data-ttu-id="63245-271">Si la dirección URL está incrustada en el certificado firmado digitalmente del programa, el programa también puede mostrar una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="63245-271">If the URL is embedded in the program's digitally signed certificate, the program can also display a URL.</span></span> <span data-ttu-id="63245-272">Los programas que no están firmados digitalmente no pueden mostrar una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="63245-272">Programs that are not digitally signed cannot display a URL.</span></span>

<span data-ttu-id="63245-273">También se muestra el texto descriptivo, proporcionado por el programa durante el registro.</span><span class="sxs-lookup"><span data-stu-id="63245-273">Descriptive text, which is supplied by the program during registration, is also displayed.</span></span> <span data-ttu-id="63245-274">Este texto es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="63245-274">This text is required.</span></span> <span data-ttu-id="63245-275">Debajo del cuadro Descripción se indica el número de valores predeterminados que el programa actualmente tiene asignados fuera del número completo en el que está registrado.</span><span class="sxs-lookup"><span data-stu-id="63245-275">Beneath the description box is an indication of how many defaults the program is currently assigned out of the full number it is registered to handle.</span></span>

<span data-ttu-id="63245-276">Para asignar o restaurar un programa como valor predeterminado para todos los archivos y protocolos para los que está registrado, el usuario hace clic en la opción **establecer este programa como predeterminado** .</span><span class="sxs-lookup"><span data-stu-id="63245-276">To assign or restore a program as the default for all files and protocols for which it is registered, the user clicks the **Set this program as default** option.</span></span>

<span data-ttu-id="63245-277">Para asignar tipos de archivos y protocolos individuales a un programa, el usuario hace clic en la opción **elegir valores predeterminados para este programa** , que muestra un **conjunto de asociaciones para una** ventana de programa como la que aparece en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="63245-277">To assign individual file types and protocols to a program, the user clicks the **Choose defaults for this program** option, which displays a **Set associations for a program** window like the one in the following illustration.</span></span>

> [!Note]  
> <span data-ttu-id="63245-278">Se recomienda llamar a las **asociaciones de conjuntos para un programa** mediante [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span><span class="sxs-lookup"><span data-stu-id="63245-278">We recommend you call the **Set associations for a program** by using [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span></span>

 

![captura de pantalla de la página establecer asociaciones para un programa](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a><span data-ttu-id="63245-280">Prácticas recomendadas para usar programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="63245-280">Best Practices for Using Default Programs</span></span>

<span data-ttu-id="63245-281">En esta sección se proporcionan instrucciones prácticas recomendadas para usar **programas predeterminados** al registrar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="63245-281">This section provides best practice guidelines for using **Default Programs** when you register applications.</span></span> <span data-ttu-id="63245-282">También ofrece sugerencias de diseño para crear una aplicación que proporciona a los usuarios una funcionalidad óptima de **programas predeterminados** .</span><span class="sxs-lookup"><span data-stu-id="63245-282">It also offers design suggestions for creating an application that provides users with optimal **Default Programs** functionality.</span></span>

### <a name="during-installation"></a><span data-ttu-id="63245-283">Durante la instalación</span><span class="sxs-lookup"><span data-stu-id="63245-283">During Installation</span></span>

<span data-ttu-id="63245-284">Además de los procedimientos de instalación que normalmente se usan en Windows XP, una aplicación basada en Windows Vista o posterior debe registrarse con la característica **programas predeterminados** para aprovechar su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="63245-284">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista or later based application must register with the **Default Programs** feature to take advantage of its functionality.</span></span>

<span data-ttu-id="63245-285">Realice la siguiente secuencia de pasos durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="63245-285">Perform the following sequence of steps during installation.</span></span> <span data-ttu-id="63245-286">Los pasos 1-3 coinciden con los pasos que se usaron en Windows XP; el paso 4 es nuevo en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="63245-286">Steps 1-3 match the steps that were used in Windows XP; step 4 was new in Windows Vista.</span></span>

1.  <span data-ttu-id="63245-287">Instale los archivos binarios necesarios.</span><span class="sxs-lookup"><span data-stu-id="63245-287">Install the necessary binary files.</span></span>
2.  <span data-ttu-id="63245-288">Escriba ProgIDs en el \_ equipo local HKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="63245-288">Write ProgIDs to HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="63245-289">Tenga en cuenta que las aplicaciones deben crear ProgID específicos de la aplicación para sus asociaciones.</span><span class="sxs-lookup"><span data-stu-id="63245-289">Note that applications must create application-specific ProgIDs for their associations.</span></span>
3.  <span data-ttu-id="63245-290">Registre la aplicación con los **programas predeterminados** tal como se explicó anteriormente en [el registro de una aplicación para su uso con programas predeterminados](#registering-an-application-for-use-with-default-programs).</span><span class="sxs-lookup"><span data-stu-id="63245-290">Register the application with **Default Programs** as previously explained in [Registering an Application for Use with Default Programs](#registering-an-application-for-use-with-default-programs).</span></span>

### <a name="after-installation"></a><span data-ttu-id="63245-291">Después de la instalación</span><span class="sxs-lookup"><span data-stu-id="63245-291">After Installation</span></span>

<span data-ttu-id="63245-292">En esta sección se describe cómo el mensaje de la aplicación debe presentar primero sus opciones predeterminadas a cada usuario.</span><span class="sxs-lookup"><span data-stu-id="63245-292">This section discusses how the application prompt should first present its default options to each user.</span></span> <span data-ttu-id="63245-293">También se explica cómo una aplicación puede supervisar su estado como valor predeterminado para sus posibles asociaciones y protocolos.</span><span class="sxs-lookup"><span data-stu-id="63245-293">It also discusses how an application can monitor its status as the default for its possible associations and protocols.</span></span>

### <a name="first-run-experiences"></a><span data-ttu-id="63245-294">Experiencias de primera ejecución</span><span class="sxs-lookup"><span data-stu-id="63245-294">First Run Experiences</span></span>

<span data-ttu-id="63245-295">Cuando un usuario ejecuta la aplicación por primera vez, se recomienda que la aplicación muestre la interfaz de usuario al usuario que normalmente incluye estas dos opciones:</span><span class="sxs-lookup"><span data-stu-id="63245-295">When the application is run by a user for the first time, it is recommended that the application display UI to the user that typically includes these two choices:</span></span>

-   <span data-ttu-id="63245-296">Acepte la configuración predeterminada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-296">Accept the default application settings.</span></span> <span data-ttu-id="63245-297">Esta opción está seleccionada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="63245-297">This option is selected by default.</span></span>
-   <span data-ttu-id="63245-298">Personalizar la configuración predeterminada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63245-298">Customize the default application settings.</span></span>

<span data-ttu-id="63245-299">Antes de Windows 8, si el usuario acepta la configuración predeterminada, la aplicación llama a [**IApplicationAssociationRegistration:: SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), que convierte todas las asociaciones de nivel de equipo que se declaran durante la instalación a la configuración por usuario para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="63245-299">Prior to Windows 8, if the user accepts the default settings, your application calls [**IApplicationAssociationRegistration::SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), which converts all machine-level associations that are declared during installation to per-user settings for that user.</span></span>

<span data-ttu-id="63245-300">Si el usuario decide personalizar la configuración, la aplicación llama a [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) para mostrar la interfaz de usuario de la Asociación de archivo.</span><span class="sxs-lookup"><span data-stu-id="63245-300">If the user decides to customize the settings, your application calls [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) to display the file association UI.</span></span> <span data-ttu-id="63245-301">En la ilustración siguiente se muestra esta ventana para el reproductor multimedia ficticio ficticia.</span><span class="sxs-lookup"><span data-stu-id="63245-301">The following illustration shows this window for the fictional Litware media player.</span></span>

![captura de pantalla de la página establecer asociaciones para un programa de Litware](images/setassociationsforaprogramforlitware.png)

<span data-ttu-id="63245-303">La ventana Asociación de archivos muestra los valores predeterminados que ha registrado la aplicación y también muestra el valor predeterminado actual para otras extensiones y protocolos.</span><span class="sxs-lookup"><span data-stu-id="63245-303">The file association window shows the defaults that the application registered and also shows the current default for other extensions and protocols.</span></span> <span data-ttu-id="63245-304">Una vez que el usuario termina de personalizar sus valores predeterminados, haga clic en el botón **Guardar** para confirmar los cambios.</span><span class="sxs-lookup"><span data-stu-id="63245-304">After the user finishes customizing their defaults, they click the **Save** button to commit the changes.</span></span> <span data-ttu-id="63245-305">Si el usuario hace clic en **Cancelar**, la ventana se cierra sin guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="63245-305">If the user clicks **Cancel**, the window closes without saving changes.</span></span>

<span data-ttu-id="63245-306">Debe usar esta interfaz de usuario para sus aplicaciones en lugar de crear las suyas propias.</span><span class="sxs-lookup"><span data-stu-id="63245-306">You should use this UI for your applications instead of creating your own.</span></span> <span data-ttu-id="63245-307">Al hacerlo, se guardan los recursos necesarios para desarrollar la interfaz de usuario de la Asociación de archivos.</span><span class="sxs-lookup"><span data-stu-id="63245-307">By doing so, you save the resources that were previously required to develop file association UI.</span></span> <span data-ttu-id="63245-308">También garantiza que las asociaciones se guarden correctamente.</span><span class="sxs-lookup"><span data-stu-id="63245-308">You also guarantee that associations are saved correctly.</span></span>

### <a name="set-an-application-to-check-whether-it-is-the-default"></a><span data-ttu-id="63245-309">Establecer una aplicación para comprobar si es el valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="63245-309">Set an Application to Check Whether It Is the Default</span></span>

> [!Note]  
> <span data-ttu-id="63245-310">Ya no se admite en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63245-310">This is no longer supported as of Windows 8.</span></span>

 

<span data-ttu-id="63245-311">Normalmente, las aplicaciones comprueban si están establecidas como valor predeterminado cuando se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="63245-311">Applications typically check whether they are set as the default when they are run.</span></span> <span data-ttu-id="63245-312">Establezca las aplicaciones para realizar esta comprobación mediante una llamada a [**IApplicationAssociationRegistration:: QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) o [**IApplicationAssociationRegistration:: QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span><span class="sxs-lookup"><span data-stu-id="63245-312">Set your applications to make this check by calling [**IApplicationAssociationRegistration::QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) or [**IApplicationAssociationRegistration::QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span></span>

<span data-ttu-id="63245-313">Si la aplicación determina que no es el valor predeterminado, puede presentar una interfaz de usuario que pida al usuario que acepte la situación actual o que la aplicación sea la predeterminada.</span><span class="sxs-lookup"><span data-stu-id="63245-313">If the application determines that it is not the default, it can present UI that asks the user whether to accept the current situation or to make the application the default.</span></span> <span data-ttu-id="63245-314">Incluya siempre una casilla en esta interfaz de usuario que esté seleccionada de forma predeterminada y que presente la opción no volver a preguntar.</span><span class="sxs-lookup"><span data-stu-id="63245-314">Always include a check box in this UI that is selected by default and that presents the option not to be asked again.</span></span>

> [!Note]  
> <span data-ttu-id="63245-315">La elección de default debe estar controlada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="63245-315">The choice of default should be user driven.</span></span> <span data-ttu-id="63245-316">Una aplicación nunca debe reclamar un valor predeterminado sin preguntar al usuario.</span><span class="sxs-lookup"><span data-stu-id="63245-316">An application should never reclaim a default without asking the user.</span></span>

 

<span data-ttu-id="63245-317">En la ilustración siguiente se muestra un cuadro de diálogo de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="63245-317">The following illustration shows an example dialog box.</span></span>

![captura de pantalla de un cuadro de diálogo de ejemplo](images/notthedefaultui.png)

## <a name="additional-resources"></a><span data-ttu-id="63245-319">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="63245-319">Additional Resources</span></span>

-   [<span data-ttu-id="63245-320">**IApplicationAssociationRegistration**</span><span class="sxs-lookup"><span data-stu-id="63245-320">**IApplicationAssociationRegistration**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [<span data-ttu-id="63245-321">**IApplicationAssociationRegistrationUI**</span><span class="sxs-lookup"><span data-stu-id="63245-321">**IApplicationAssociationRegistrationUI**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a><span data-ttu-id="63245-322">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63245-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63245-323">Prácticas recomendadas para asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="63245-323">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="63245-324">Escenario de ejemplo de Asociación de archivos</span><span class="sxs-lookup"><span data-stu-id="63245-324">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="63245-325">Directrices para administrar aplicaciones predeterminadas en Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="63245-325">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="63245-326">Establecer los valores predeterminados de acceso a programas y del equipo (SPAD)</span><span class="sxs-lookup"><span data-stu-id="63245-326">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
