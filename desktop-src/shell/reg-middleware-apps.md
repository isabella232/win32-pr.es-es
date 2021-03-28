---
description: 'En este tema se explica cómo registrar un programa en el registro de Windows como uno de los siguientes tipos de cliente: explorador, correo electrónico, reproducción multimedia, mensajería instantánea o máquina virtual para Java.'
title: Registrar programas con tipos de cliente
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 71dd4e3192dc75821fd0a3e8c0d4742e1a8d571a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914245"
---
# <a name="registering-programs-with-client-types"></a><span data-ttu-id="20904-103">Registrar programas con tipos de cliente</span><span class="sxs-lookup"><span data-stu-id="20904-103">Registering Programs with Client Types</span></span>

<span data-ttu-id="20904-104">En este tema se explica cómo registrar un programa en el registro de Windows como uno de los siguientes tipos de cliente: explorador, correo electrónico, reproducción multimedia, mensajería instantánea o máquina virtual para Java.</span><span class="sxs-lookup"><span data-stu-id="20904-104">This topic explains how to register a program in the Windows registry as one of the following client types: browser, email, media playback, instant messaging, or virtual machine for Java.</span></span>

> [!Note]  
> <span data-ttu-id="20904-105">Esta información se aplica a los siguientes sistemas operativos:</span><span class="sxs-lookup"><span data-stu-id="20904-105">This information applies to the following operating systems:</span></span>
> 
> -   <span data-ttu-id="20904-106">Windows 2000 Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="20904-106">Windows 2000 Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="20904-107">Windows 2000 Service Pack 4 (SP4)</span><span class="sxs-lookup"><span data-stu-id="20904-107">Windows 2000 Service Pack 4 (SP4)</span></span>
> -   <span data-ttu-id="20904-108">Windows XP Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="20904-108">Windows XP Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="20904-109">Windows XP Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="20904-109">Windows XP Service Pack 2 (SP2)</span></span>
> -   <span data-ttu-id="20904-110">Windows XP Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="20904-110">Windows XP Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="20904-111">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="20904-111">Windows Server 2003</span></span>
> -   <span data-ttu-id="20904-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20904-112">Windows Vista</span></span>
> -   <span data-ttu-id="20904-113">Windows Vista Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="20904-113">Windows Vista Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="20904-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="20904-114">Windows 8</span></span>

 

<span data-ttu-id="20904-115">En este tema se incluyen las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="20904-115">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="20904-116">Elementos comunes de registro para todos los tipos de cliente</span><span class="sxs-lookup"><span data-stu-id="20904-116">Common Registration Elements for All Client Types</span></span>](#common-registration-elements-for-all-client-types)
    -   [<span data-ttu-id="20904-117">Seleccionar un nombre canónico</span><span class="sxs-lookup"><span data-stu-id="20904-117">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
    -   [<span data-ttu-id="20904-118">Registrar el nombre para mostrar de un programa</span><span class="sxs-lookup"><span data-stu-id="20904-118">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
    -   [<span data-ttu-id="20904-119">Registrar el icono de un programa</span><span class="sxs-lookup"><span data-stu-id="20904-119">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
    -   [<span data-ttu-id="20904-120">Registrar un verbo abierto</span><span class="sxs-lookup"><span data-stu-id="20904-120">Registering an Open Verb</span></span>](#registering-an-open-verb)
    -   [<span data-ttu-id="20904-121">Registrar información de instalación</span><span class="sxs-lookup"><span data-stu-id="20904-121">Registering Installation Information</span></span>](#registering-installation-information)
-   [<span data-ttu-id="20904-122">Elementos de registro para tipos de cliente específicos</span><span class="sxs-lookup"><span data-stu-id="20904-122">Registration Elements for Specific Client Types</span></span>](#registration-elements-for-specific-client-types)
    -   [<span data-ttu-id="20904-123">Registro del menú Inicio</span><span class="sxs-lookup"><span data-stu-id="20904-123">Start Menu Registration</span></span>](#start-menu-registration)
    -   [<span data-ttu-id="20904-124">Registro del cliente de correo</span><span class="sxs-lookup"><span data-stu-id="20904-124">Mail Client Registration</span></span>](#mail-client-registration)
-   [<span data-ttu-id="20904-125">Completar registros de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-125">Complete Sample Registrations</span></span>](#complete-sample-registrations)
    -   [<span data-ttu-id="20904-126">Un explorador de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-126">A Sample Browser</span></span>](#a-sample-browser)
    -   [<span data-ttu-id="20904-127">Un explorador de correo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-127">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
    -   [<span data-ttu-id="20904-128">Media Player de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-128">A Sample Media Player</span></span>](#a-sample-media-player)
    -   [<span data-ttu-id="20904-129">Un programa de mensajería instantánea de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-129">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
    -   [<span data-ttu-id="20904-130">Una máquina virtual de ejemplo para Java</span><span class="sxs-lookup"><span data-stu-id="20904-130">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)
-   [<span data-ttu-id="20904-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20904-131">Related topics</span></span>](#related-topics)

<span data-ttu-id="20904-132">En este tema se amplía la documentación existente sobre el registro de un programa como un tipo de cliente determinado.</span><span class="sxs-lookup"><span data-stu-id="20904-132">This topic extends existing documentation about registering a program as a particular client type.</span></span> <span data-ttu-id="20904-133">Para obtener vínculos a esa documentación, consulte la sección temas relacionados.</span><span class="sxs-lookup"><span data-stu-id="20904-133">For links to that documentation, see the Related Topics section.</span></span>

## <a name="common-registration-elements-for-all-client-types"></a><span data-ttu-id="20904-134">Elementos comunes de registro para todos los tipos de cliente</span><span class="sxs-lookup"><span data-stu-id="20904-134">Common Registration Elements for All Client Types</span></span>

<span data-ttu-id="20904-135">Al registrar un programa como un tipo de cliente, la mayoría de las entradas del registro son las mismas independientemente del tipo de cliente.</span><span class="sxs-lookup"><span data-stu-id="20904-135">When registering a program as a client type, most of the registry entries are the same regardless of the client type.</span></span> <span data-ttu-id="20904-136">Sin embargo, algunas entradas del registro son específicas del tipo de cliente y se indican en la sección [elementos de registro para tipos de cliente específicos](#registration-elements-for-specific-client-types) .</span><span class="sxs-lookup"><span data-stu-id="20904-136">Some registry entries, however, are specific to the client type and these are noted in the [Registration Elements for Specific Client Types](#registration-elements-for-specific-client-types) section.</span></span>

<span data-ttu-id="20904-137">En esta sección se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="20904-137">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="20904-138">Seleccionar un nombre canónico</span><span class="sxs-lookup"><span data-stu-id="20904-138">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
-   [<span data-ttu-id="20904-139">Registrar el nombre para mostrar de un programa</span><span class="sxs-lookup"><span data-stu-id="20904-139">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
-   [<span data-ttu-id="20904-140">Registrar el icono de un programa</span><span class="sxs-lookup"><span data-stu-id="20904-140">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
-   [<span data-ttu-id="20904-141">Registrar un verbo abierto</span><span class="sxs-lookup"><span data-stu-id="20904-141">Registering an Open Verb</span></span>](#registering-an-open-verb)
-   [<span data-ttu-id="20904-142">Registrar información de instalación</span><span class="sxs-lookup"><span data-stu-id="20904-142">Registering Installation Information</span></span>](#registering-installation-information)

> [!Note]  
> <span data-ttu-id="20904-143">Los nombres de subclaves que se indican en cursiva en este tema son marcadores de posición para nombres de subclaves definidos por el usuario o un conjunto de valores posibles.</span><span class="sxs-lookup"><span data-stu-id="20904-143">Subkey names given in italics throughout this topic are placeholders for user-defined subkey names or a set of possible values.</span></span> <span data-ttu-id="20904-144">En la sección [registros de ejemplo completos](#complete-sample-registrations) se proporcionan ejemplos completos con nombres de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="20904-144">Full examples with example names in place are provided in the [Complete Sample Registrations](#complete-sample-registrations) section.</span></span>

 

<span data-ttu-id="20904-145">Toda la información de registro de tipos de cliente se almacena en la subclave siguiente:</span><span class="sxs-lookup"><span data-stu-id="20904-145">All client type registration information is stored under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

<span data-ttu-id="20904-146">*ClientTypeName* es uno de los siguientes nombres de subclave:</span><span class="sxs-lookup"><span data-stu-id="20904-146">*ClientTypeName* is one of the following subkey names:</span></span>

-   <span data-ttu-id="20904-147">StartMenuInternet (para exploradores)</span><span class="sxs-lookup"><span data-stu-id="20904-147">StartMenuInternet (for browsers)</span></span>
-   <span data-ttu-id="20904-148">Correo (por correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="20904-148">Mail (for email)</span></span>
-   <span data-ttu-id="20904-149">Medios (para la reproducción multimedia)</span><span class="sxs-lookup"><span data-stu-id="20904-149">Media (for media playback)</span></span>
-   <span data-ttu-id="20904-150">IM (para mensajería instantánea)</span><span class="sxs-lookup"><span data-stu-id="20904-150">IM (for instant messaging)</span></span>
-   <span data-ttu-id="20904-151">JavaVM (para la máquina virtual para Java)</span><span class="sxs-lookup"><span data-stu-id="20904-151">JavaVM (for virtual machine for Java)</span></span>

<span data-ttu-id="20904-152">En este tema, se anotarán las referencias a un programa de equipo ficticio denominado "Lit View" de Litware Inc., con un archivo ejecutable denominado Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="20904-152">Throughout this topic, you will note references to a fictional computer program named "Lit View" by Litware Inc., with an executable file named Litview.exe.</span></span> <span data-ttu-id="20904-153">Este programa hipotético se usa indistintamente como una mensajería instantánea, un explorador u otro tipo de programa cliente según sea necesario con fines ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="20904-153">This hypothetical program is used interchangeably as an instant messenger, a browser, or another type of client program as needed for illustrative purposes.</span></span>

### <a name="selecting-a-canonical-name"></a><span data-ttu-id="20904-154">Seleccionar un nombre canónico</span><span class="sxs-lookup"><span data-stu-id="20904-154">Selecting a Canonical Name</span></span>

<span data-ttu-id="20904-155">El proveedor debe elegir un *nombre canónico* para el programa.</span><span class="sxs-lookup"><span data-stu-id="20904-155">The vendor must choose a *canonical name* for the program.</span></span> <span data-ttu-id="20904-156">El nombre canónico nunca se muestra al usuario, por lo que no es necesario localizarlo.</span><span class="sxs-lookup"><span data-stu-id="20904-156">The canonical name is never shown to the user, so it does not need to be localized.</span></span> <span data-ttu-id="20904-157">Su única finalidad es proporcionar una cadena única que se pueda usar para identificar el programa.</span><span class="sxs-lookup"><span data-stu-id="20904-157">Its only purpose is to provide a unique string that can be used to identify the program.</span></span> <span data-ttu-id="20904-158">Normalmente es el mismo que el nombre en inglés del programa, pero esto es simplemente una Convención.</span><span class="sxs-lookup"><span data-stu-id="20904-158">It is typically the same as the English name of the program, but this is merely a convention.</span></span>

<span data-ttu-id="20904-159">En el caso de tipos de cliente distintos de los exploradores, el nombre canónico puede ser cualquier cadena.</span><span class="sxs-lookup"><span data-stu-id="20904-159">For client types other than browsers, the canonical name can be any string.</span></span> <span data-ttu-id="20904-160">Elija un nombre único, uno que no es probable que sea utilizado por otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="20904-160">Choose a unique name, one that is not likely to be used by another vendor.</span></span>

<span data-ttu-id="20904-161">En el caso de los clientes del explorador, el nombre canónico debe ser el nombre, incluida la extensión, del ejecutable asociado; por ejemplo, "Litview.exe".</span><span class="sxs-lookup"><span data-stu-id="20904-161">For browser clients, the canonical name must be the name—including the extension—of the associated executable; for instance, "Litview.exe".</span></span>

<span data-ttu-id="20904-162">Estos son algunos ejemplos de nombres canónicos.</span><span class="sxs-lookup"><span data-stu-id="20904-162">Here are some examples of canonical names.</span></span>

-   <span data-ttu-id="20904-163">Iexplore.exe (explorador)</span><span class="sxs-lookup"><span data-stu-id="20904-163">Iexplore.exe (browser)</span></span>
-   <span data-ttu-id="20904-164">Correo de Windows (correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="20904-164">Windows Mail (email)</span></span>
-   <span data-ttu-id="20904-165">Windows Media Player (multimedia)</span><span class="sxs-lookup"><span data-stu-id="20904-165">Windows Media Player (media)</span></span>
-   <span data-ttu-id="20904-166">Windows Messenger (mensajería instantánea)</span><span class="sxs-lookup"><span data-stu-id="20904-166">Windows Messenger (instant messaging)</span></span>

<span data-ttu-id="20904-167">Registre el nombre canónico mediante la creación de una subclave, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="20904-167">Register the canonical name by creating a subkey as shown here.</span></span> <span data-ttu-id="20904-168">El nombre de la subclave es el nombre canónico.</span><span class="sxs-lookup"><span data-stu-id="20904-168">The name of the subkey is the canonical name.</span></span> <span data-ttu-id="20904-169">Toda la información relacionada con el registro de ese programa existirá en esta subclave.</span><span class="sxs-lookup"><span data-stu-id="20904-169">All information relating to that program's registration will exist under this subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a><span data-ttu-id="20904-170">Registrar el nombre para mostrar de un programa</span><span class="sxs-lookup"><span data-stu-id="20904-170">Registering a Program's Display Name</span></span>

<span data-ttu-id="20904-171">El siguiente paso del registro consiste en especificar el nombre para mostrar del programa.</span><span class="sxs-lookup"><span data-stu-id="20904-171">The next step in registration is to specify the program's display name.</span></span> <span data-ttu-id="20904-172">Se proporciona como un valor en la clave de nombre canónico, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="20904-172">It is given as a value under the canonical name key as shown here.</span></span> <span data-ttu-id="20904-173">Tenga en cuenta de nuevo que *CanonicalName* y *ClientTypeName* no son los nombres reales de las claves, sino solo los marcadores de posición para los nombres verdaderos, como *Lit View*.</span><span class="sxs-lookup"><span data-stu-id="20904-173">Note again that *CanonicalName* and *ClientTypeName* are not the actual names of the keys, but only placeholders for the true names, such as *Lit View*.</span></span>

> [!Note]  
> <span data-ttu-id="20904-174">A partir de Windows 8, el nombre que se usa para registrar para [configurar el acceso a programas y los valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md) y para los [programas predeterminados](default-programs.md) debe coincidir para que los cambios de SPAD desencadenen los registros de programas predeterminados.</span><span class="sxs-lookup"><span data-stu-id="20904-174">As of Windows 8, the name used to register for [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) and for [Default Programs](default-programs.md) should match in order for SPAD changes to trigger Default Programs registrations.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

<span data-ttu-id="20904-175">El valor de **LocalizedString** es una \_ cadena de reg SZ y consta de un signo de arroba (@), la ruta de acceso completa a un archivo. dll o. exe, una coma, un signo menos y un entero decimal.</span><span class="sxs-lookup"><span data-stu-id="20904-175">The **LocalizedString** value is a REG\_SZ string and consists of an "at" sign (@), the full path to a .dll or .exe file, a comma, a minus sign, and a decimal integer.</span></span> <span data-ttu-id="20904-176">El entero decimal es el identificador de un recurso de cadena, incluido en el archivo. dll o. exe, cuyo valor se va a mostrar al usuario como el nombre de este cliente.</span><span class="sxs-lookup"><span data-stu-id="20904-176">The decimal integer is the ID of a string resource—contained within the .dll or .exe file—whose value is to be displayed to the user as the name of this client.</span></span> <span data-ttu-id="20904-177">Tenga en cuenta que la ruta de acceso del archivo no requiere comillas, aunque contenga espacios.</span><span class="sxs-lookup"><span data-stu-id="20904-177">Note that the file path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="20904-178">El registro de la cadena del nombre para mostrar de esta manera permite usar el mismo registro para varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="20904-178">Registering the display name string in this manner allows the same registration to be used for multiple languages.</span></span> <span data-ttu-id="20904-179">Cada instalación de idioma proporciona un archivo de recursos diferente con el nombre para mostrar almacenado en el mismo identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="20904-179">Each language installation provides a different resource file with the display name stored at the same resource ID.</span></span>

<span data-ttu-id="20904-180">En el ejemplo siguiente se muestra el registro de un programa de mensajería instantánea de la vista ficticia Lit.</span><span class="sxs-lookup"><span data-stu-id="20904-180">The following example shows the registration for a fictional Lit View instant messaging program.</span></span> <span data-ttu-id="20904-181">Dado que se trata de un programa de mensajería instantánea, la subclave *CanonicalName* (en este caso, la *vista Lit*) se almacena en la subclave **im** .</span><span class="sxs-lookup"><span data-stu-id="20904-181">Because it is an instant messaging program, the *CanonicalName* subkey (in this case *Lit View*) is stored under the **IM** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="20904-182">Tenga en cuenta el uso de la entrada (valor predeterminado) como una declaración secundaria del nombre para mostrar del cliente.</span><span class="sxs-lookup"><span data-stu-id="20904-182">Note the use of the (Default) entry as a secondary declaration of the client's display name.</span></span> <span data-ttu-id="20904-183">Si **LocalizedString** no está presente, se utiliza en su lugar el valor (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="20904-183">If the **LocalizedString** is not present, the (Default) value is used instead.</span></span> <span data-ttu-id="20904-184">Esto funciona con todos los tipos de cliente (exploradores de Internet, exploradores de correo electrónico, mensajería instantánea y reproductores multimedia).</span><span class="sxs-lookup"><span data-stu-id="20904-184">This works with all client types (Internet browsers, email browsers, instant messengers, and media players).</span></span> <span data-ttu-id="20904-185">Para mantener la compatibilidad con el [diseño del registro del cliente de Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), los programas de correo electrónico deben establecer el valor (predeterminado) de la subclave *CanonicalName* en el nombre para mostrar del cliente en el idioma instalado actualmente.</span><span class="sxs-lookup"><span data-stu-id="20904-185">For backward compatibility with the [Internet Explorer Client Registry Layout](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), email programs should set the (Default) value of the *CanonicalName* subkey to the client's display name in the currently installed language.</span></span>

### <a name="registering-a-programs-icon"></a><span data-ttu-id="20904-186">Registrar el icono de un programa</span><span class="sxs-lookup"><span data-stu-id="20904-186">Registering a Program's Icon</span></span>

> [!Note]  
> <span data-ttu-id="20904-187">Esta sección no se aplica a Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="20904-187">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="20904-188">De forma predeterminada, la sección superior del menú **Inicio** de Windows XP y Windows vista contiene iconos de **Internet** y **correo electrónico** .</span><span class="sxs-lookup"><span data-stu-id="20904-188">By default, the upper section of the Windows XP and Windows Vista **Start** menu contains **Internet** and **E-mail** icons.</span></span> <span data-ttu-id="20904-189">Estos iconos no están presentes en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="20904-189">These icons are not present in Windows 7 and later.</span></span> <span data-ttu-id="20904-190">En el caso de los clientes de explorador y de correo electrónico, cuando se asigna un programa como valor predeterminado para su tipo de cliente, se muestra el icono registrado de ese programa para dichas entradas en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="20904-190">For browser and email clients, when a program is assigned as the default for their client type, that program's registered icon is displayed for those **Start** menu entries.</span></span>

<span data-ttu-id="20904-191">El registro del icono de un programa es obligatorio para los clientes de explorador y de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="20904-191">Registering a program's icon is mandatory for browser and email clients.</span></span> <span data-ttu-id="20904-192">El registro de un icono para la reproducción multimedia, mensajería instantánea o máquina virtual para tipos de cliente Java es opcional, y los iconos registrados para esos tipos de cliente no se usan actualmente en Windows y no se muestran en la sección superior de los menús **Inicio** de Windows XP o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20904-192">Registering an icon for the media playback, instant messaging, or virtual machine for Java client types is optional, and registered icons for those client types are not currently used by Windows and are not displayed in the upper section of the Windows XP or Windows Vista **Start** menus.</span></span>

<span data-ttu-id="20904-193">Para registrar un icono para un programa cliente, agregue una subclave **DefaultIcon** con un valor predeterminado, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="20904-193">To register an icon for a client program, add a **DefaultIcon** subkey with a default value as shown here.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

<span data-ttu-id="20904-194">El valor **filePath** es la ruta de acceso completa al archivo que contiene el icono.</span><span class="sxs-lookup"><span data-stu-id="20904-194">The **FilePath** value is the full path to the file that contains the icon.</span></span> <span data-ttu-id="20904-195">Esta ruta de acceso no requiere comillas, aunque contenga espacios.</span><span class="sxs-lookup"><span data-stu-id="20904-195">This path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="20904-196">El valor de **IconIndex** se interpreta de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="20904-196">The **IconIndex** value is interpreted as follows:</span></span>

-   <span data-ttu-id="20904-197">Si **IconIndex** es un número positivo, el número se utiliza como el índice de la matriz de los iconos de *base cero* que se almacena en el archivo.</span><span class="sxs-lookup"><span data-stu-id="20904-197">If **IconIndex** is a positive number, the number is used as the index of the *zero-based* array of icons stored in the file.</span></span> <span data-ttu-id="20904-198">Por ejemplo, si **IconIndex** es 1, el segundo icono se carga desde el archivo.</span><span class="sxs-lookup"><span data-stu-id="20904-198">For example, if **IconIndex** is 1, the second icon is loaded from the file.</span></span>
-   <span data-ttu-id="20904-199">Si **IconIndex** es un número negativo, el valor absoluto de **iconindex** se utiliza como identificador de recursos (en lugar del índice) para el icono.</span><span class="sxs-lookup"><span data-stu-id="20904-199">If **IconIndex** is a negative number, the absolute value of **IconIndex** is used as the resource identifier (rather than the index) for the icon.</span></span> <span data-ttu-id="20904-200">Por ejemplo, si **IconIndex** es-3, el icono cuyo identificador de recurso es 3 se carga desde el archivo.</span><span class="sxs-lookup"><span data-stu-id="20904-200">For example, if **IconIndex** is -3, the icon whose resource identifier is 3 is loaded from the file.</span></span>

<span data-ttu-id="20904-201">En el ejemplo siguiente se muestra el registro de un explorador hipotético de lit View.</span><span class="sxs-lookup"><span data-stu-id="20904-201">The following example shows the registration of a hypothetical Lit View browser.</span></span> <span data-ttu-id="20904-202">El segundo icono almacenado en el archivo Litview.exe se utiliza como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="20904-202">The second icon stored in the Litview.exe file is used as the default.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a><span data-ttu-id="20904-203">Registrar un verbo abierto</span><span class="sxs-lookup"><span data-stu-id="20904-203">Registering an Open Verb</span></span>

> [!Note]  
> <span data-ttu-id="20904-204">Esta sección no se aplica a Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="20904-204">This section does not apply to Windows 2000.</span></span> <span data-ttu-id="20904-205">El siguiente paso solo es necesario para los clientes del explorador y de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="20904-205">The following step is necessary only for browser and email clients.</span></span>

 

<span data-ttu-id="20904-206">Supongamos que un usuario ha seleccionado el programa como el programa de Internet o de correo electrónico predeterminado.</span><span class="sxs-lookup"><span data-stu-id="20904-206">Assume that a user has selected your program as the default Internet or email program.</span></span> <span data-ttu-id="20904-207">Ese usuario hace clic en el icono de **Internet** o **correo electrónico** en el menú **Inicio** de Windows XP o Windows Vista para abrir el programa.</span><span class="sxs-lookup"><span data-stu-id="20904-207">That user clicks the **Internet** or **E-mail** icon in the Windows XP or Windows Vista **Start** menu to open the program.</span></span> <span data-ttu-id="20904-208">En ese momento, se ejecuta la línea de comandos registrada tal y como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="20904-208">At that point, the command line registered as shown here is executed.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

<span data-ttu-id="20904-209">La línea de comandos debe especificar una ruta de acceso absoluta completa al archivo, seguida de opciones de línea de comandos opcionales.</span><span class="sxs-lookup"><span data-stu-id="20904-209">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="20904-210">Si el tipo de entrada es REG \_ Expand \_ SZ, se pueden usar variables de entorno en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="20904-210">If the entry type is REG\_EXPAND\_SZ, environment variables can be used in the path.</span></span> <span data-ttu-id="20904-211">Use las comillas correctamente para asegurarse de que no se interpreten erróneamente los espacios de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="20904-211">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span> <span data-ttu-id="20904-212">La línea de comandos debe ejecutar el programa con los valores predeterminados adecuados.</span><span class="sxs-lookup"><span data-stu-id="20904-212">The command line should execute the program with appropriate defaults.</span></span> <span data-ttu-id="20904-213">Los exploradores suelen tener como valor predeterminado la Página principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="20904-213">Browsers generally default to the user's home page.</span></span> <span data-ttu-id="20904-214">Los programas de correo electrónico suelen abrir la **bandeja de entrada** del usuario.</span><span class="sxs-lookup"><span data-stu-id="20904-214">Email programs generally open the user's **Inbox**.</span></span>

<span data-ttu-id="20904-215">En el ejemplo siguiente se muestra el registro de un `open` verbo para un explorador hipotético de lit View.</span><span class="sxs-lookup"><span data-stu-id="20904-215">The following example shows the registration of an `open` verb for a hypothetical Lit View browser.</span></span> <span data-ttu-id="20904-216">No especifica ninguna opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="20904-216">It specifies no command-line options.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

<span data-ttu-id="20904-217">Tenga en cuenta que, en este valor, las comillas se colocan alrededor de la ruta de acceso porque contiene espacios incrustados.</span><span class="sxs-lookup"><span data-stu-id="20904-217">Note that in this value, quotation marks are placed around the path because it contains embedded spaces.</span></span> <span data-ttu-id="20904-218">Si se omiten estas comillas, puede que la línea de comandos se interprete erróneamente.</span><span class="sxs-lookup"><span data-stu-id="20904-218">Omitting these quotation marks could cause the command line to be misinterpreted.</span></span>

### <a name="registering-installation-information"></a><span data-ttu-id="20904-219">Registrar información de instalación</span><span class="sxs-lookup"><span data-stu-id="20904-219">Registering Installation Information</span></span>

> [!Note]  
> <span data-ttu-id="20904-220">Esta sección no se aplica a Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="20904-220">This section does not apply to Windows Server 2003.</span></span>

 

-   [<span data-ttu-id="20904-221">El comando REINSTALL</span><span class="sxs-lookup"><span data-stu-id="20904-221">The Reinstall Command</span></span>](#the-reinstall-command)
-   [<span data-ttu-id="20904-222">Comando Ocultar iconos</span><span class="sxs-lookup"><span data-stu-id="20904-222">The Hide Icons Command</span></span>](#the-hide-icons-command)
-   [<span data-ttu-id="20904-223">Comando Mostrar iconos</span><span class="sxs-lookup"><span data-stu-id="20904-223">The Show Icons Command</span></span>](#the-show-icons-command)
-   [<span data-ttu-id="20904-224">Configuración del programa de grupo</span><span class="sxs-lookup"><span data-stu-id="20904-224">Group Program Configuration</span></span>](#group-program-configuration)
-   [<span data-ttu-id="20904-225">Ejemplo de registro del explorador</span><span class="sxs-lookup"><span data-stu-id="20904-225">Browser Registration Example</span></span>](#browser-registration-example)

<span data-ttu-id="20904-226">La característica por la que el usuario selecciona programas predeterminados por equipo se denomina y se obtiene acceso a ella, tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="20904-226">The feature by which the user selects per-machine default programs is named and accessed as shown in the following table.</span></span> <span data-ttu-id="20904-227">(Windows Vista presentó una nueva característica, **establece los programas predeterminados**, mediante los cuales un usuario puede establecer los valores predeterminados por usuario).</span><span class="sxs-lookup"><span data-stu-id="20904-227">(Windows Vista introduced a new feature, **Set your default programs**, by which a user can set per-user defaults.)</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20904-228">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="20904-228">Operating System</span></span></th>
<th><span data-ttu-id="20904-229">Title</span><span class="sxs-lookup"><span data-stu-id="20904-229">Title</span></span></th>
<th><span data-ttu-id="20904-230">Ubicación de acceso</span><span class="sxs-lookup"><span data-stu-id="20904-230">Access Location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20904-231">Windows 7</span><span class="sxs-lookup"><span data-stu-id="20904-231">Windows 7</span></span></td>
<td><span data-ttu-id="20904-232">Establecer los valores predeterminados de acceso a programas y del equipo</span><span class="sxs-lookup"><span data-stu-id="20904-232">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="20904-233">Opción <strong>programas predeterminados</strong> del menú <strong>Inicio</strong></span><span class="sxs-lookup"><span data-stu-id="20904-233"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="20904-234"><strong>Programas predeterminados</strong> Elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="20904-234"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20904-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20904-235">Windows Vista</span></span></td>
<td><span data-ttu-id="20904-236">Establecer los valores predeterminados de acceso a programas y del equipo</span><span class="sxs-lookup"><span data-stu-id="20904-236">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="20904-237">Opción <strong>programas predeterminados</strong> del menú <strong>Inicio</strong></span><span class="sxs-lookup"><span data-stu-id="20904-237"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="20904-238"><strong>Programas predeterminados</strong> Elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="20904-238"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20904-239">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="20904-239">Windows XP SP2</span></span></td>
<td><span data-ttu-id="20904-240">Establecer acceso y valores predeterminados de programas</span><span class="sxs-lookup"><span data-stu-id="20904-240">Set Program Access and Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="20904-241">Menú <strong>Inicio</strong></span><span class="sxs-lookup"><span data-stu-id="20904-241"><strong>Start</strong> menu</span></span></li>
<li><span data-ttu-id="20904-242"><strong>Agregar o quitar programas</strong> Elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="20904-242"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20904-243">Windows XP SP1</span><span class="sxs-lookup"><span data-stu-id="20904-243">Windows XP SP1</span></span></td>
<td><span data-ttu-id="20904-244">Configurar programas</span><span class="sxs-lookup"><span data-stu-id="20904-244">Configure Programs</span></span></td>
<td><ul>
<li><span data-ttu-id="20904-245"><strong>Agregar o quitar programas</strong> Elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="20904-245"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="20904-246">Para simplificar, en este tema se usa el título de Windows 7 de la característica.</span><span class="sxs-lookup"><span data-stu-id="20904-246">For simplicity, this topic uses the Windows 7 title of the feature.</span></span> <span data-ttu-id="20904-247">A todas las versiones de la característica se les conoce comúnmente como SPAD.</span><span class="sxs-lookup"><span data-stu-id="20904-247">All versions of the feature are popularly referred to as SPAD.</span></span>

> [!Note]  
> <span data-ttu-id="20904-248">Si ejecuta Windows 2000 o Windows XP, debe tener al menos Windows 2000 SP3 o Windows XP SP1 instalado para ver la página **establecer acceso y valores predeterminados del programa** .</span><span class="sxs-lookup"><span data-stu-id="20904-248">If you are running Windows 2000 or Windows XP, you must have at least Windows 2000 SP3 or Windows XP SP1 installed to see the **Set Program Access and Defaults** page.</span></span> <span data-ttu-id="20904-249">En Windows Vista y versiones posteriores, el acceso a la página **establecer los valores predeterminados de acceso a programas y equipos** requiere privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="20904-249">In Windows Vista and later, access to the **Set Program Access and Computer Defaults** page requires Administrator privileges.</span></span> <span data-ttu-id="20904-250">Por esta razón, se recomienda que los desarrolladores se registren en el elemento configurar el panel de control [programas predeterminados](default-programs.md) para que cualquier usuario pueda administrar los valores predeterminados de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20904-250">For this reason, developers are encouraged to register for the [Set your default programs](default-programs.md) Control Panel item so that any user can manage application defaults.</span></span>

 

<span data-ttu-id="20904-251">En el árbol del Registro siguiente se muestra la variedad de información que se debe registrar en la clave **InstallInfo** del programa para que el programa aparezca en la página **establecer los valores predeterminados de acceso a programas y del equipo** como opción para su tipo de cliente.</span><span class="sxs-lookup"><span data-stu-id="20904-251">The following registry tree shows the variety of information that must be registered in the program's **InstallInfo** key in order for the program to appear on the **Set Program Access and Computer Defaults** page as an option for its client type.</span></span> <span data-ttu-id="20904-252">Cada uno de estos valores se describe en detalle en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="20904-252">Each of these values is discussed in detail in the following sections.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

<span data-ttu-id="20904-253">La línea de comandos debe especificar una ruta de acceso absoluta completa al archivo, seguida de opciones de línea de comandos opcionales.</span><span class="sxs-lookup"><span data-stu-id="20904-253">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="20904-254">Use las comillas correctamente para asegurarse de que no se interpreten erróneamente los espacios de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="20904-254">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span>

### <a name="the-reinstall-command"></a><span data-ttu-id="20904-255">El comando REINSTALL</span><span class="sxs-lookup"><span data-stu-id="20904-255">The Reinstall Command</span></span>

<span data-ttu-id="20904-256">La línea de comandos de reinstalación declarada en el valor ReinstallCommand se ejecuta cuando el usuario utiliza la página **establecer los valores predeterminados de acceso a programas y del equipo** para seleccionar el programa como predeterminado para su tipo de cliente.</span><span class="sxs-lookup"><span data-stu-id="20904-256">The reinstall command line declared in the ReinstallCommand value is executed when the user uses the **Set Program Access and Computer Defaults** page to select your program as the default for its client type.</span></span> <span data-ttu-id="20904-257">En Windows Vista y versiones posteriores, el acceso a esta página requiere un nivel de privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="20904-257">In Windows Vista and later, access to this page requires an Administrator privilege level.</span></span> <span data-ttu-id="20904-258">En Windows 8, si ha registrado la aplicación con el mismo nombre para establecer el **acceso a programas y los valores** predeterminados del equipo y **programas predeterminados**, los valores predeterminados especificados en **programas** predeterminados para esa aplicación se aplicarán para el usuario actual, así como para ejecutar el comando reinstalar.</span><span class="sxs-lookup"><span data-stu-id="20904-258">In Windows 8, if you have registered your application using the same name for both **Set Program Access and Computer Defaults** and **Default Programs**, the defaults specified in **Default Programs** for that application will be applied for the current user as well as running the reinstall command.</span></span>

<span data-ttu-id="20904-259">El programa iniciado por la línea de comandos de reinstalación debe asociar la aplicación con el conjunto completo de tipos de [archivos](fa-intro.md) y [protocolos](/previous-versions//aa767743(v=vs.85)) que la aplicación puede controlar.</span><span class="sxs-lookup"><span data-stu-id="20904-259">The program launched by the reinstall command line must associate the application with the complete set of [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types the application can handle.</span></span> <span data-ttu-id="20904-260">Todas las aplicaciones deben establecer la capacidad del controlador en el comando de reinstalación.</span><span class="sxs-lookup"><span data-stu-id="20904-260">All applications must establish handler capability in the reinstall command.</span></span> <span data-ttu-id="20904-261">Las aplicaciones pueden usar el comando REINSTALL para registrar la funcionalidad y, opcionalmente, establecer el estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="20904-261">Applications can use the reinstall command to register capability as well as optionally establish default status.</span></span> <span data-ttu-id="20904-262">Cuando una aplicación elige implementar el estado de la capacidad y del controlador predeterminado en el comando de reinstalación, también debe restablecer los vínculos o accesos directos visibles que desee.</span><span class="sxs-lookup"><span data-stu-id="20904-262">When an application chooses to implement both capability and default handler status in the reinstall command, it should also reinstate any visible links or shortcuts desired.</span></span> <span data-ttu-id="20904-263">Los puntos de entrada visibles que la mayoría de las aplicaciones elija aparecen en [el comando Ocultar iconos](#the-hide-icons-command).</span><span class="sxs-lookup"><span data-stu-id="20904-263">The visible entry points most applications choose are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span>

> [!Note]  
> <span data-ttu-id="20904-264">Se recomienda encarecidamente que las aplicaciones implementen la funcionalidad de administración en el comando de reinstalación.</span><span class="sxs-lookup"><span data-stu-id="20904-264">It is highly recommended that applications implement handling capability in the reinstall command.</span></span>

 

<span data-ttu-id="20904-265">Una vez completado el proceso de reinstalación, el programa iniciado por la línea de comandos de reinstalación debe salir.</span><span class="sxs-lookup"><span data-stu-id="20904-265">Once the reinstall process is complete, the program launched by the reinstall command line should exit.</span></span> <span data-ttu-id="20904-266">No debe iniciar el programa correspondiente; simplemente debe registrar los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="20904-266">It should not launch the corresponding program; it should merely register defaults.</span></span> <span data-ttu-id="20904-267">Por ejemplo, el comando reinstalar de un explorador no debe abrir la Página principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="20904-267">For example, the reinstall command for a browser should not open the user's home page.</span></span>

> [!Note]  
> <span data-ttu-id="20904-268">En el caso de los clientes de explorador y de correo electrónico en Windows XP y Windows Vista, las aplicaciones que optan por establecer la capacidad de control y el estado predeterminado en el comando de reinstalación deben registrarse para el icono correspondiente en la parte superior del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="20904-268">For browser and email clients in Windows XP and Windows Vista, applications that choose to establish both handling capability and default status in the reinstall command should register for the corresponding icon at the top of the Start menu.</span></span> <span data-ttu-id="20904-269">Consulte [registro del menú Inicio](#start-menu-registration) para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="20904-269">See [Start Menu Registration](#start-menu-registration) for additional information.</span></span>

 

### <a name="the-hide-icons-command"></a><span data-ttu-id="20904-270">Comando Ocultar iconos</span><span class="sxs-lookup"><span data-stu-id="20904-270">The Hide Icons Command</span></span>

<span data-ttu-id="20904-271">La línea de comandos declarada en el valor HideIconsCommand se ejecuta cuando el usuario desactiva el cuadro **Habilitar acceso a este programa** de la página **establecer los valores predeterminados de acceso a programas y del equipo** .</span><span class="sxs-lookup"><span data-stu-id="20904-271">The command line declared in the HideIconsCommand value is executed when the user clears the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="20904-272">Esta línea de comandos debe ocultar todos los puntos de acceso del programa que estén visibles en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="20904-272">This command line must hide all of your program's access points that are visible in the user interface.</span></span> <span data-ttu-id="20904-273">Las instrucciones específicas son para quitar accesos directos e iconos de las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="20904-273">The specific guidelines are to remove shortcuts and icons from the following locations:</span></span>

-   <span data-ttu-id="20904-274">Iconos de escritorio</span><span class="sxs-lookup"><span data-stu-id="20904-274">Desktop icons</span></span>
-   <span data-ttu-id="20904-275">Vínculos del menú Inicio, incluido el grupo **Inicio**</span><span class="sxs-lookup"><span data-stu-id="20904-275">Start menu links, including the **Startup** group</span></span>
-   <span data-ttu-id="20904-276">Vínculos de la barra de inicio rápido</span><span class="sxs-lookup"><span data-stu-id="20904-276">Quick Launch bar links</span></span>
-   <span data-ttu-id="20904-277">Área de notificaciones</span><span class="sxs-lookup"><span data-stu-id="20904-277">Notification area</span></span>
-   <span data-ttu-id="20904-278">Menús contextuales</span><span class="sxs-lookup"><span data-stu-id="20904-278">Shortcut menus</span></span>
-   <span data-ttu-id="20904-279">Banda de tareas de carpeta</span><span class="sxs-lookup"><span data-stu-id="20904-279">Folder task band</span></span>

<span data-ttu-id="20904-280">Esta línea de comandos también debe evitar las invocaciones automáticas del programa, como las especificadas en la clave **Ejecutar** registro.</span><span class="sxs-lookup"><span data-stu-id="20904-280">This command line must also prevent automatic invocations of the program, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="20904-281">Se recomienda a los proveedores que implementen estas instrucciones en la devolución de llamada de ocultación de acceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20904-281">Vendors are encouraged to implement these guidelines in the application's Hide Access callback.</span></span>

<span data-ttu-id="20904-282">No es necesario renunciar al registro (capacidad de aplicación) de los tipos de archivo cuando se ocultan los iconos.</span><span class="sxs-lookup"><span data-stu-id="20904-282">You do not need to relinquish registration (application capability) of file types when icons are hidden.</span></span> <span data-ttu-id="20904-283">Tampoco es necesario ceder el estado predeterminado de la aplicación para los tipos de protocolo y archivo.</span><span class="sxs-lookup"><span data-stu-id="20904-283">You also do not need to relinquish the application's default status for file and protocol types.</span></span> <span data-ttu-id="20904-284">Esto puede dar lugar a una experiencia de usuario incorrecta cuando estos tipos se encuentran en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="20904-284">Doing so can lead to a bad user experience when these types are encountered in the UI.</span></span>

<span data-ttu-id="20904-285">Después de ocultar correctamente los iconos, debe actualizar el valor del registro IconsVisible a 0, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="20904-285">After successfully hiding icons, you must update the IconsVisible registry value to 0 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

<span data-ttu-id="20904-286">La entrada IconsVisible es de tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="20904-286">The IconsVisible entry is of type **REG\_DWORD**.</span></span>

### <a name="an-alternate-hide-icons-method-in-spad"></a><span data-ttu-id="20904-287">Un método de ocultar iconos alternativo en SPAD</span><span class="sxs-lookup"><span data-stu-id="20904-287">An Alternate Hide Icons Method in SPAD</span></span>

<span data-ttu-id="20904-288">En el caso de algunas aplicaciones heredadas, es posible que una implementación completa de ocultar acceso no sea práctica.</span><span class="sxs-lookup"><span data-stu-id="20904-288">For some legacy applications, a full implementation of Hide Access may not be practical.</span></span> <span data-ttu-id="20904-289">Un método alternativo que logra el mismo efecto es desinstalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20904-289">An alternative method that achieves the same effect is to uninstall the application.</span></span> <span data-ttu-id="20904-290">En la sección siguiente se muestra el comportamiento de ejemplo y el código de ejemplo para implementar esta alternativa.</span><span class="sxs-lookup"><span data-stu-id="20904-290">The section below shows example behavior and sample code to implement this alternative.</span></span> <span data-ttu-id="20904-291">En general, los fabricantes de software independientes (ISV) deben evitar esta alternativa, ya que lo hará:</span><span class="sxs-lookup"><span data-stu-id="20904-291">In general, independent software vendors (ISVs) should avoid this alternative since it will:</span></span>

-   <span data-ttu-id="20904-292">Desinstale la aplicación por completo del sistema.</span><span class="sxs-lookup"><span data-stu-id="20904-292">Uninstall the application completely from the system.</span></span>
-   <span data-ttu-id="20904-293">Quitar los valores predeterminados previamente seleccionados.</span><span class="sxs-lookup"><span data-stu-id="20904-293">Remove previously selected defaults.</span></span>
-   <span data-ttu-id="20904-294">No deje la opción de interfaz de usuario para volver a instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20904-294">Leave no UI option to reinstall the application.</span></span>
-   <span data-ttu-id="20904-295">Haga que la característica habilitar acceso deje de estar disponible, ya que una desinstalación quita la aplicación completamente de SPAD.</span><span class="sxs-lookup"><span data-stu-id="20904-295">Make the enable access feature no longer available, since an uninstallation removes the application completely from SPAD.</span></span>

<span data-ttu-id="20904-296">La experiencia de usuario recomendada es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="20904-296">The recommended user experience is as follows:</span></span>

-   <span data-ttu-id="20904-297">Cuando el usuario desactive la casilla **Habilitar el acceso a este programa** en SPAD, se presenta la siguiente interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="20904-297">When the user unchecks the **Enable access to this program** box in SPAD, the following UI is presented.</span></span>

    ![cuadro de diálogo sobre cómo ocultar el acceso al programa](images/hideaccessvista.png)

-   <span data-ttu-id="20904-299">Cuando el usuario selecciona **Aceptar**, se inicia el elemento **programas y características** del panel de control para permitir que el usuario desinstale la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20904-299">When the user selects **OK**, the **Programs and Features** Control Panel item launches to allow the user to uninstall the application.</span></span>
-   <span data-ttu-id="20904-300">Los usuarios de Windows XP deben aparecer con este cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="20904-300">Windows XP users should be presented with this dialog box.</span></span>

    ![cuadro de diálogo equivalente de Windows XP](images/hideaccessxp.png)

-   <span data-ttu-id="20904-302">Cuando el usuario de Windows XP selecciona **Aceptar**, se inicia el elemento **Agregar o quitar programas** del panel de control para permitir que el usuario desinstale la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20904-302">When the Windows XP user selects **OK**, the **Add or Remove Programs** Control Panel item launches to allow the user to uninstall the application.</span></span>

<span data-ttu-id="20904-303">El código siguiente proporciona una implementación reutilizable para la característica de ocultación de acceso, como se describe anteriormente.</span><span class="sxs-lookup"><span data-stu-id="20904-303">The following code provides a reusable implementation for the Hide Access feature as outlined above.</span></span> <span data-ttu-id="20904-304">Se puede usar en Windows XP, Windows Vista y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="20904-304">It can be used on Windows XP, Windows Vista, and Windows 7.</span></span>


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a><span data-ttu-id="20904-305">Comando Mostrar iconos</span><span class="sxs-lookup"><span data-stu-id="20904-305">The Show Icons Command</span></span>

<span data-ttu-id="20904-306">La línea de comandos declarada en la entrada ShowIconsCommand se ejecuta cuando el usuario activa la casilla **Habilitar el acceso a este programa** en la página **establecer los valores predeterminados de acceso a programas y del equipo** .</span><span class="sxs-lookup"><span data-stu-id="20904-306">The command line declared in the ShowIconsCommand entry is executed when the user checks the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="20904-307">Esta línea de comandos puede restaurar los puntos de acceso de su programa, incluidos los que están en el menú **Inicio** , en el escritorio y en el grupo **Inicio** , así como las invocaciones automáticas normales, como las especificadas en la clave **Ejecutar** registro.</span><span class="sxs-lookup"><span data-stu-id="20904-307">This command line may restore your program's access points, including those in the **Start** menu, on the desktop, and in the **Startup** group, as well as normal automatic invocations, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="20904-308">Los puntos de acceso visibles de interés para la mayoría de las aplicaciones se muestran en [el comando Ocultar iconos](#the-hide-icons-command).</span><span class="sxs-lookup"><span data-stu-id="20904-308">The visible access points of interest to most applications are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span> <span data-ttu-id="20904-309">La aplicación no debe cambiar los valores predeterminados por usuario; el usuario debe realizar ese cambio a través de los **programas predeterminados**.</span><span class="sxs-lookup"><span data-stu-id="20904-309">The application should not change per-user defaults; that change should be done by the user through **Default Programs**.</span></span>

<span data-ttu-id="20904-310">Después de mostrar correctamente los iconos, debe actualizar el valor del registro IconsVisible en 1, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="20904-310">After successfully showing your icons, you must update the IconsVisible registry value to 1 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

<span data-ttu-id="20904-311">Tenga en cuenta que si ha usado la entrada HideIconsCommand para solicitar una desinstalación de la aplicación, la entrada ShowIconsCommand no tiene ningún uso.</span><span class="sxs-lookup"><span data-stu-id="20904-311">Note that if you have used the HideIconsCommand entry to prompt an uninstall of the application, the ShowIconsCommand entry is of no use.</span></span> <span data-ttu-id="20904-312">Se debe quitar del registro con el resto de la información de la aplicación durante el proceso de desinstalación.</span><span class="sxs-lookup"><span data-stu-id="20904-312">It should be removed from the registry with the rest of the application's information during the uninstall process.</span></span>

### <a name="group-program-configuration"></a><span data-ttu-id="20904-313">Configuración del programa de grupo</span><span class="sxs-lookup"><span data-stu-id="20904-313">Group Program Configuration</span></span>

> [!Note]  
> <span data-ttu-id="20904-314">Esta sección no se aplica a Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="20904-314">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="20904-315">Como parte de la preparación del sistema, un OEM puede establecer una configuración que oculte los puntos de acceso para el explorador de Microsoft, el correo electrónico, la reproducción multimedia, la mensajería instantánea o la máquina virtual para los programas cliente de Java y especifique sus propios programas predeterminados.</span><span class="sxs-lookup"><span data-stu-id="20904-315">As part of system preparation, an OEM can establish a configuration that hides access points for the Microsoft browser, email, media playback, instant messaging, or virtual machine for Java client programs and specifies their own default programs.</span></span> <span data-ttu-id="20904-316">Los OEM pueden permitir que los usuarios restablezcan sus equipos en cualquier momento a esta configuración predeterminada mediante el establecimiento de los siguientes valores del registro.</span><span class="sxs-lookup"><span data-stu-id="20904-316">OEMs can enable users to reset their computers at any time to this default configuration by setting the following registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

<span data-ttu-id="20904-317">Si estas claves están configuradas, los usuarios pueden restaurar la configuración de OEM seleccionando la opción **fabricante del equipo** en la página establecer los **valores predeterminados de acceso a programas y del equipo** .</span><span class="sxs-lookup"><span data-stu-id="20904-317">If these keys are set, users can restore the OEM configuration by selecting the **Computer Manufacturer** option on the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="20904-318">Si no se establecen estas claves, no se muestra la opción **fabricante del equipo** .</span><span class="sxs-lookup"><span data-stu-id="20904-318">If these keys are not set, the **Computer Manufacturer** option is not shown.</span></span>

<span data-ttu-id="20904-319">La entrada **OEMShowIcons** , si está presente, establece el icono mostrar el estado del cliente especificado que se aplica si el usuario selecciona **fabricante del equipo**.</span><span class="sxs-lookup"><span data-stu-id="20904-319">The **OEMShowIcons** entry, if present, sets the icon show state for the specified client that is applied if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="20904-320">Un valor de 1 hace que se muestren los iconos y un valor de 0 hace que no se muestren los iconos.</span><span class="sxs-lookup"><span data-stu-id="20904-320">A value of 1 causes icons to be shown, and a value of 0 causes icons to not be shown.</span></span> <span data-ttu-id="20904-321">Si **OEMShowIcons** no está presente, la selección **del fabricante del equipo** no tiene ningún efecto en el icono Mostrar configuración.</span><span class="sxs-lookup"><span data-stu-id="20904-321">If **OEMShowIcons** is absent, selecting **Computer Manufacturer** has no effect on the icon show setting.</span></span> <span data-ttu-id="20904-322">**OEMShowIcons** es de tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="20904-322">**OEMShowIcons** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="20904-323">La entrada **OEMDefault** , si está presente y está establecida en 1, establece la preferencia del OEM para el cliente predeterminado del tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="20904-323">The **OEMDefault** entry, if present and set to 1, establishes the OEM preference for the default client of the indicated type.</span></span> <span data-ttu-id="20904-324">Solo un cliente de un tipo determinado se puede marcar como el valor predeterminado del OEM.</span><span class="sxs-lookup"><span data-stu-id="20904-324">Only one client of a particular type can be marked as the OEM default.</span></span> <span data-ttu-id="20904-325">Si más de un registro de un cliente contiene la entrada **OEMDefault** , se omiten todos los valores y el cliente actual se sigue usando como cliente predeterminado.</span><span class="sxs-lookup"><span data-stu-id="20904-325">If more then one client's registration contains the **OEMDefault** entry, then all are ignored and the current client continues to be used as default client.</span></span> <span data-ttu-id="20904-326">Si la entrada **OEMDefault** no está presente o está presente y está establecida en 0, ese cliente concreto no se utiliza como el cliente predeterminado si el usuario selecciona **fabricante del equipo**.</span><span class="sxs-lookup"><span data-stu-id="20904-326">If the **OEMDefault** entry is not present or is present and set to 0, then that particular client is not used as the default client if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="20904-327">**OEMDefault** es de tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="20904-327">**OEMDefault** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="20904-328">Además de la opción de restablecer los equipos a la configuración predeterminada establecida por el OEM, los usuarios tienen otras tres opciones de configuración:</span><span class="sxs-lookup"><span data-stu-id="20904-328">In addition to the option to reset their computers to the default configuration established by the OEM, users have three other configuration options:</span></span>

-   <span data-ttu-id="20904-329">Establezca su equipo en una configuración de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="20904-329">Set their computer to a Microsoft Windows configuration.</span></span> <span data-ttu-id="20904-330">En este caso, la página **establecer los valores predeterminados de acceso a programas y del equipo** permite el acceso a todo el software de Microsoft y que no sea de Microsoft en el equipo registrado en las categorías de productos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="20904-330">In this case, the **Set Program Access and Computer Defaults** page enables access to all Microsoft and non-Microsoft software on the computer registered in the relevant product categories.</span></span> <span data-ttu-id="20904-331">Los programas de Microsoft Windows se seleccionan como la opción predeterminada para cada categoría.</span><span class="sxs-lookup"><span data-stu-id="20904-331">Microsoft Windows programs are selected as the default option for each category.</span></span>
-   <span data-ttu-id="20904-332">Establezca su equipo en una configuración que no sea de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20904-332">Set their computer to a non-Microsoft configuration.</span></span> <span data-ttu-id="20904-333">Esta configuración oculta los puntos de acceso (por ejemplo, el menú **Inicio** ) en Windows Internet Explorer, Windows Media Player, Windows Messenger y Microsoft Outlook Express.</span><span class="sxs-lookup"><span data-stu-id="20904-333">This configuration hides access points (such as the **Start** menu) to Windows Internet Explorer, Windows Media Player, Windows Messenger, and Microsoft Outlook Express.</span></span> <span data-ttu-id="20904-334">Permite el acceso al software que no es de Microsoft en el equipo en estas categorías.</span><span class="sxs-lookup"><span data-stu-id="20904-334">It enables access to the non-Microsoft software on the computer in these categories.</span></span> <span data-ttu-id="20904-335">Además, si un programa que no es de Microsoft está disponible en una categoría, se establece como el valor predeterminado para esa categoría.</span><span class="sxs-lookup"><span data-stu-id="20904-335">Furthermore, if a non-Microsoft program is available in a category, it is set as the default for that category.</span></span> <span data-ttu-id="20904-336">Si hay más de un programa que no es de Microsoft disponible en una categoría, se pide al usuario que elija el programa que no es de Microsoft que se debe usar como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="20904-336">If more than one non-Microsoft program is available in a category, the user is asked to choose which non-Microsoft program should be used as the default.</span></span>
-   <span data-ttu-id="20904-337">Establezca una configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="20904-337">Establish a custom configuration.</span></span> <span data-ttu-id="20904-338">Los usuarios realizan sus propias selecciones para habilitar o quitar el acceso, y mezclar programas de Microsoft y que no sean de Microsoft tal y como se ven.</span><span class="sxs-lookup"><span data-stu-id="20904-338">Users make their own selections for enabling or removing access, mixing Microsoft and non-Microsoft programs as they see fit.</span></span> <span data-ttu-id="20904-339">Los usuarios establecen las opciones predeterminadas categoría por categoría.</span><span class="sxs-lookup"><span data-stu-id="20904-339">Users establish default options on a category-by-category basis.</span></span>

<span data-ttu-id="20904-340">Los usuarios pueden cambiar cualquiera de estas opciones en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="20904-340">Users are free to change any of these options at any time.</span></span>

### <a name="browser-registration-example"></a><span data-ttu-id="20904-341">Ejemplo de registro del explorador</span><span class="sxs-lookup"><span data-stu-id="20904-341">Browser Registration Example</span></span>

<span data-ttu-id="20904-342">En el ejemplo siguiente se muestra el registro completo de **InstallInfo** para un explorador ficticio de vista de Lit.</span><span class="sxs-lookup"><span data-stu-id="20904-342">The following example shows the full **InstallInfo** registration for a fictional Lit View browser.</span></span> <span data-ttu-id="20904-343">En este caso, los modificadores de la línea de comandos permiten al archivo Litview.exe realizar las acciones necesarias para cada valor.</span><span class="sxs-lookup"><span data-stu-id="20904-343">In this case the command line switches allow the Litview.exe file to perform whatever actions are necessary for each value.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="20904-344">Tenga en cuenta que las comillas se colocan alrededor de las rutas de acceso porque contienen espacios incrustados.</span><span class="sxs-lookup"><span data-stu-id="20904-344">Note that quotation marks are placed around the paths because they contain embedded spaces.</span></span>

## <a name="registration-elements-for-specific-client-types"></a><span data-ttu-id="20904-345">Elementos de registro para tipos de cliente específicos</span><span class="sxs-lookup"><span data-stu-id="20904-345">Registration Elements for Specific Client Types</span></span>

<span data-ttu-id="20904-346">La siguiente información también se puede encontrar en los recursos que aparecen en la sección temas relacionados al final de este tema.</span><span class="sxs-lookup"><span data-stu-id="20904-346">The following information also can be found in the resources listed in the Related Topics section at the end of this topic.</span></span>

-   [<span data-ttu-id="20904-347">Registro del menú Inicio</span><span class="sxs-lookup"><span data-stu-id="20904-347">Start Menu Registration</span></span>](#start-menu-registration)
-   [<span data-ttu-id="20904-348">Registro del cliente de correo</span><span class="sxs-lookup"><span data-stu-id="20904-348">Mail Client Registration</span></span>](#mail-client-registration)

### <a name="start-menu-registration"></a><span data-ttu-id="20904-349">Registro del menú Inicio</span><span class="sxs-lookup"><span data-stu-id="20904-349">Start Menu Registration</span></span>

<span data-ttu-id="20904-350">En Windows XP, las aplicaciones suelen registrar los valores predeterminados en una máquina (**HKEY \_ local \_ Machine**) en lugar de un ámbito de usuario (**HKEY \_ Current \_ User**).</span><span class="sxs-lookup"><span data-stu-id="20904-350">Under Windows XP, applications typically registered defaults on a machine-wide (**HKEY\_LOCAL\_MACHINE**) rather than a user (**HKEY\_CURRENT\_USER**) scope.</span></span> <span data-ttu-id="20904-351">Con la introducción de Windows Vista del control de cuentas de usuario (UAC), las aplicaciones que reclaman las ranuras de **Internet** y de **correo electrónico** en el menú **Inicio** deben implementar el comando REINSTALL en el contexto de ejecución correcto.</span><span class="sxs-lookup"><span data-stu-id="20904-351">With the Windows Vista introduction of the User Account Control (UAC), applications that claim the **Internet** and **E-mail** slots in the **Start** menu must implement the reinstall command within the correct execution context.</span></span>

> [!Note]  
> <span data-ttu-id="20904-352">El vínculo de **correo electrónico** del menú Inicio se ha quitado de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="20904-352">The Start menu **E-mail** link has been removed as of Windows 7.</span></span> <span data-ttu-id="20904-353">Sin embargo, el registro descrito en esta sección se debe seguir realizando porque asigna el cliente MAPI predeterminado.</span><span class="sxs-lookup"><span data-stu-id="20904-353">However, the registration discussed in this section should still be performed because it assigns the default MAPI client.</span></span>

 

<span data-ttu-id="20904-354">Un usuario limitado en Windows XP, Windows Vista o Windows 7 no puede tener acceso a SPAD.</span><span class="sxs-lookup"><span data-stu-id="20904-354">A limited user on Windows XP, Windows Vista, or Windows 7 cannot access SPAD.</span></span> <span data-ttu-id="20904-355">Por esta razón, se recomienda que los desarrolladores se registren en el elemento configurar el panel de control de **programas predeterminados** para que cualquier usuario pueda administrar los valores predeterminados de la aplicación por usuario.</span><span class="sxs-lookup"><span data-stu-id="20904-355">For this reason, developers are encouraged to register for the **Set your default programs** Control Panel item so that any user can manage per-user application defaults.</span></span>

<span data-ttu-id="20904-356">Las selecciones realizadas en SPAD solo deben afectar a la configuración de cada máquina.</span><span class="sxs-lookup"><span data-stu-id="20904-356">Selections made in SPAD should only affect per-machine settings.</span></span>

<span data-ttu-id="20904-357">Establezca el valor del registro como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="20904-357">Set the registry value as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> <span data-ttu-id="20904-358">**La siguiente información solo se aplica a Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="20904-358">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="20904-359">Si el registro del valor predeterminado de nivel de equipo en HKEY \_ local \_ Machine como se mostró anteriormente es correcto, la aplicación debe eliminar el valor asignado a la entrada predeterminada en la siguiente subclave:</span><span class="sxs-lookup"><span data-stu-id="20904-359">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the value assigned to the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> <span data-ttu-id="20904-360">Si se produce un error en el registro del valor predeterminado de nivel de equipo en HKEY \_ local \_ Machine como se mostró anteriormente, normalmente porque el usuario no tiene permiso de escritura en la subclave, la aplicación debe establecer el siguiente valor:</span><span class="sxs-lookup"><span data-stu-id="20904-360">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above fails, usually because the user does not have write permission to the subkey, the application should set the following value:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> <span data-ttu-id="20904-361">Esto registra el nombre canónico solo para el usuario actual, no para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="20904-361">This registers the canonical name only for the current user, not for all users.</span></span>

 

<span data-ttu-id="20904-362">Después de actualizar las claves del registro, el programa debe difundir el mensaje de [**\_ SETTINGCHANGE de WM**](../winmsg/wm-settingchange.md) con **wParam** = 0 y **lParam** que apunta a la cadena terminada en NULL "software \\ clients \\ **ClientTypeName**" para notificar al sistema operativo que el cliente predeterminado ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="20904-362">After updating the registry keys, the program should broadcast the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with **wParam** = 0 and **lParam** pointing to the null-terminated string "Software\\Clients\\**ClientTypeName**" to notify the operating system that the default client has changed.</span></span>

### <a name="mail-client-registration"></a><span data-ttu-id="20904-363">Registro del cliente de correo</span><span class="sxs-lookup"><span data-stu-id="20904-363">Mail Client Registration</span></span>

<span data-ttu-id="20904-364">Para un cliente de correo, el programa debe tener la configuración registrada en la clave correo electrónico **\_ \_ raíz de las clases HKEY** \\  para poder atender las direcciones URL que utilizan el `mailto` Protocolo.</span><span class="sxs-lookup"><span data-stu-id="20904-364">For a mail client, the program needs to have registered settings under the **HKEY\_CLASSES\_ROOT**\\**mailto** key in order to service URLs that use the `mailto` protocol.</span></span> <span data-ttu-id="20904-365">Establezca valores y claves que reflejen la configuración de la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="20904-365">Set values and keys that mirror those settings under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

<span data-ttu-id="20904-366">Esta jerarquía del registro reemplaza `mailto` a la jerarquía del registro existente que se encuentra en **HKEY \_ classes \_ root** \\ **mailto**.</span><span class="sxs-lookup"><span data-stu-id="20904-366">This registry hierarchy replaces the existing `mailto` registry hierarchy found at **HKEY\_CLASSES\_ROOT**\\**mailto**.</span></span> <span data-ttu-id="20904-367">La jerarquía sigue siendo la misma, solo la ubicación ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="20904-367">The hierarchy remains the same, only the location has changed.</span></span> <span data-ttu-id="20904-368">El formato de esta jerarquía se documenta en MSDN en [información general y tutoriales del protocolo conectable asincrónico](/previous-versions//aa767913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="20904-368">The format of this hierarchy is documented on MSDN under [Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85)).</span></span> <span data-ttu-id="20904-369">Normalmente, el `mailto` Protocolo se registra en un programa en lugar de un Protocolo asincrónico, en cuyo caso se aplica la documentación sobre el [registro de una aplicación en un esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="20904-369">Typically, the `mailto` protocol is registered to a program rather than an asynchronous protocol, in which case the documentation on [Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) applies.</span></span>

<span data-ttu-id="20904-370">En el ejemplo siguiente se muestra la `mailto` sección del registro de un `mailto` controlador registrado en un programa.</span><span class="sxs-lookup"><span data-stu-id="20904-370">The following example shows the `mailto` section of the registration for a `mailto` handler registered to a program.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

<span data-ttu-id="20904-371">El valor del registro marcas se documenta en [tipos de archivo](fa-file-types.md) en la sección titulada "definir los atributos de tipo de archivo".</span><span class="sxs-lookup"><span data-stu-id="20904-371">The EditFlags registry value is documented in [File Types](fa-file-types.md) in the section titled "Defining File Type Attributes."</span></span>

## <a name="complete-sample-registrations"></a><span data-ttu-id="20904-372">Completar registros de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-372">Complete Sample Registrations</span></span>

<span data-ttu-id="20904-373">Los ejemplos siguientes se proporcionan para mostrar los requisitos de registro completos para los distintos tipos de cliente.</span><span class="sxs-lookup"><span data-stu-id="20904-373">The following examples are provided to show the complete registration requirements for the various client types.</span></span>

-   [<span data-ttu-id="20904-374">Un explorador de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-374">A Sample Browser</span></span>](#a-sample-browser)
-   [<span data-ttu-id="20904-375">Un explorador de correo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-375">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
-   [<span data-ttu-id="20904-376">Media Player de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-376">A Sample Media Player</span></span>](#a-sample-media-player)
-   [<span data-ttu-id="20904-377">Un programa de mensajería instantánea de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-377">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
-   [<span data-ttu-id="20904-378">Una máquina virtual de ejemplo para Java</span><span class="sxs-lookup"><span data-stu-id="20904-378">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a><span data-ttu-id="20904-379">Un explorador de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-379">A Sample Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a><span data-ttu-id="20904-380">Un explorador de correo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-380">A Sample Mail Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a><span data-ttu-id="20904-381">Media Player de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-381">A Sample Media Player</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a><span data-ttu-id="20904-382">Un programa de mensajería instantánea de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20904-382">A Sample Instant Messenger Program</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a><span data-ttu-id="20904-383">Una máquina virtual de ejemplo para Java</span><span class="sxs-lookup"><span data-stu-id="20904-383">A Sample Virtual Machine for Java</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="20904-384">*Las compañías, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares y eventos que se describen aquí son ficticios. No se pretende ni se debe inferir ninguna asociación con compañías, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares o eventos reales.*</span><span class="sxs-lookup"><span data-stu-id="20904-384">*The example companies, organizations, products, domain names, email addresses, logos, people, places, and events depicted herein are fictitious. No association with any real company, organization, product, domain name, email address, logo, person, place, or event is intended or should be inferred.*</span></span>

## <a name="related-topics"></a><span data-ttu-id="20904-385">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20904-385">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20904-386">Programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="20904-386">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="20904-387">Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows</span><span class="sxs-lookup"><span data-stu-id="20904-387">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
</dt> <dt>

<span data-ttu-id="20904-388">[Diseño del registro del cliente de Internet Explorer (consulte la sección "definiciones de clave del registro de cliente")](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20904-388">[Internet Explorer Client Registry Layout (see the "Client Registry Key Definitions" section)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="20904-389">[Información general y tutoriales del protocolo acoplable asincrónico](/previous-versions//aa767913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20904-389">[Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="20904-390">[Registrar una aplicación en un esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20904-390">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>
</dt> </dl>

 

 
