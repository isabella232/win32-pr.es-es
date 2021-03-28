---
description: El menú Inicio de Windows XP y Windows vista contiene ranuras reservadas para los clientes Internet (explorador) y correo electrónico (correo electrónico) predeterminados, que suelen denominarse aplicaciones de Internet del menú Inicio.
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279856"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a><span data-ttu-id="3f3c1-103">Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows</span><span class="sxs-lookup"><span data-stu-id="3f3c1-103">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>

> [!Note]  
> <span data-ttu-id="3f3c1-104">Este tema se aplica a Windows XP, Windows Vista y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-104">This topic applies to Windows XP, Windows Vista, and Windows 7.</span></span>

 

<span data-ttu-id="3f3c1-105">El menú Inicio de Windows XP y Windows vista contiene ranuras reservadas para los clientes **Internet** (explorador) y **correo electrónico** (correo electrónico) predeterminados, que suelen denominarse aplicaciones de Internet del *menú Inicio*.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-105">The Start menu in Windows XP and Windows Vista contains reserved slots for the default **Internet** (browser) and **E-mail** (mail) clients, together commonly known as *Start Menu Internet Applications*.</span></span> <span data-ttu-id="3f3c1-106">Las aplicaciones que se registran como aplicaciones de Internet del menú Inicio lo hacen en todo el sistema (por equipo).</span><span class="sxs-lookup"><span data-stu-id="3f3c1-106">Applications which register as Start Menu Internet Applications do so across the entire system (per-machine).</span></span> <span data-ttu-id="3f3c1-107">En Windows Vista, el usuario puede usar la característica **programas predeterminados** para establecer un valor predeterminado por usuario.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-107">In Windows Vista, the user may use the **Default Programs** feature to set a per-user default.</span></span>

<span data-ttu-id="3f3c1-108">Cuando las aplicaciones se registran como menú Inicio aplicaciones de Internet, Windows XP y Windows Vista, cree iconos de **Internet** y **correo electrónico** en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-108">When applications register as Start Menu Internet Applications, Windows XP and Windows Vista create **Internet** and **E-mail** icons on the Start menu.</span></span> <span data-ttu-id="3f3c1-109">Al hacer clic en estos iconos, el menú Inicio comprueba el subárbol del registro por usuario (**HKEY \_ Current \_ User**).</span><span class="sxs-lookup"><span data-stu-id="3f3c1-109">Clicking these icons causes the Start menu to check the per-user registry subtree (**HKEY\_CURRENT\_USER**).</span></span> <span data-ttu-id="3f3c1-110">Si no se encuentra ninguna configuración predeterminada por usuario, el menú Inicio busca la subclave predeterminada por equipo en el subárbol de la **\_ \_ máquina local HKEY** .</span><span class="sxs-lookup"><span data-stu-id="3f3c1-110">If no per-user default setting is found, the Start menu looks for the per-machine default subkey in the **HKEY\_LOCAL\_MACHINE** subtree.</span></span>

> [!Note]  
> <span data-ttu-id="3f3c1-111">La instalación predeterminada de Windows no registra un programa de correo electrónico o Internet predeterminado por usuario, solo un valor predeterminado para todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-111">The default installation of Windows does not register a per-user default Internet or email program, only a system-wide default.</span></span> <span data-ttu-id="3f3c1-112">Esto proporciona una ruta de acceso de actualización sin problemas de las versiones anteriores del sistema operativo, en la que solo \_ \_ se admite el subárbol de la máquina local HKEY para los registros de cliente.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-112">This provides a smooth upgrade path from previous versions of the operating system, in which only the HKEY\_LOCAL\_MACHINE subtree is supported for client registrations.</span></span>

 

<span data-ttu-id="3f3c1-113">En este tema se describen los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="3f3c1-113">This topic discusses the following items:</span></span>

-   [<span data-ttu-id="3f3c1-114">Registro para el vínculo a Internet del menú Inicio</span><span class="sxs-lookup"><span data-stu-id="3f3c1-114">Registering for the Start Menu Internet Link</span></span>](#registering-for-the-start-menu-internet-link)
    -   [<span data-ttu-id="3f3c1-115">Cómo registrarse como el cliente de Internet predeterminado</span><span class="sxs-lookup"><span data-stu-id="3f3c1-115">How to Register as the Default Internet Client</span></span>](#how-to-register-as-the-default-internet-client)
-   [<span data-ttu-id="3f3c1-116">Registro para el vínculo de correo electrónico del menú Inicio</span><span class="sxs-lookup"><span data-stu-id="3f3c1-116">Registering for the Start Menu Email Link</span></span>](#registering-for-the-start-menu-email-link)
    -   [<span data-ttu-id="3f3c1-117">Cómo el menú Inicio muestra el cliente de correo electrónico predeterminado</span><span class="sxs-lookup"><span data-stu-id="3f3c1-117">How the Start Menu Displays the Default Email Client</span></span>](#how-the-start-menu-displays-the-default-email-client)
    -   [<span data-ttu-id="3f3c1-118">Cómo registrarse como cliente de correo electrónico predeterminado</span><span class="sxs-lookup"><span data-stu-id="3f3c1-118">How to Register as the Default EMail Client</span></span>](#how-to-register-as-the-default-email-client)
-   [<span data-ttu-id="3f3c1-119">Personalización del menú contextual</span><span class="sxs-lookup"><span data-stu-id="3f3c1-119">Customizing the Context Menu</span></span>](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a><span data-ttu-id="3f3c1-120">Registro para el vínculo a Internet del menú Inicio</span><span class="sxs-lookup"><span data-stu-id="3f3c1-120">Registering for the Start Menu Internet Link</span></span>

> [!Note]  
> <span data-ttu-id="3f3c1-121">Este registro está en desuso a partir de Windows 7, que ya no proporciona un vínculo a Internet del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-121">This registration is deprecated as of Windows 7, which no longer provides a Start menu Internet link.</span></span> <span data-ttu-id="3f3c1-122">Los registros existentes se omiten en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-122">Existing registrations are ignored in Windows 7 and later.</span></span> <span data-ttu-id="3f3c1-123">Si se registra como la aplicación de Internet predeterminada del menú Inicio, no se registrará como el explorador Web predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-123">Being registered as the default Start menu Internet application is not the same as being registered as the default web browser.</span></span> <span data-ttu-id="3f3c1-124">El explorador Web predeterminado se utiliza para iniciar direcciones URL arbitrarias desde cualquier parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-124">The default web browser is used for launching arbitrary URLs from anywhere in the system.</span></span> <span data-ttu-id="3f3c1-125">La aplicación de Internet del menú Inicio simplemente controla el programa que se inicia cuando el usuario hace clic en el icono de Internet del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-125">The Start menu Internet application merely controls the program that is started when the user clicks the Internet icon on the Start menu.</span></span>

 

<span data-ttu-id="3f3c1-126">Cualquier aplicación de explorador Web puede registrarse para aparecer como un cliente de Internet en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-126">Any web browser application can register to appear as an Internet client on the Start menu.</span></span> <span data-ttu-id="3f3c1-127">Esta visibilidad, junto con el registro adecuado para los tipos de [protocolos](/previous-versions//aa767743(v=vs.85)) y [archivos](fa-intro.md) de una aplicación, proporciona un estado de explorador predeterminado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-127">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default browser status.</span></span>

<span data-ttu-id="3f3c1-128">Los registros realizados en el subárbol de **\_ \_ usuario de HKEY Current** tienen mayor prioridad para el usuario de la consola que los registros correspondientes realizados en el **\_ \_ equipo local HKEY**.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-128">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="3f3c1-129">En el caso de los nuevos usuarios del sistema, se usan las opciones almacenadas en **HKEY \_ local \_ Machine** .</span><span class="sxs-lookup"><span data-stu-id="3f3c1-129">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="3f3c1-130">A partir de Windows XP, la configuración de Internet del menú Inicio se mantiene en las entradas predeterminadas de dos ubicaciones del registro:</span><span class="sxs-lookup"><span data-stu-id="3f3c1-130">As of Windows XP, Start menu Internet settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="3f3c1-131">**HKEY \_ \_** Clientes de \\ **software** de usuario actual \\  \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="3f3c1-131">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>
-   <span data-ttu-id="3f3c1-132">**HKEY \_ \_** Clientes de \\ **software** de equipo local \\  \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="3f3c1-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>

<span data-ttu-id="3f3c1-133">La subclave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **StartMenuInternet** describe el explorador de Internet que se inicia cuando el usuario hace clic en el icono de **Internet** del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-133">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** describes the Internet browser that is started when the user clicks the **Internet** icon on the Start menu.</span></span> <span data-ttu-id="3f3c1-134">Si esa subclave está en blanco o falta, el icono de **Internet** del menú Inicio se establece en el valor predeterminado del sistema almacenado en la segunda ubicación en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** , que describe todas las aplicaciones de explorador de Internet instaladas en el sistema.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-134">If that subkey is blank or missing, then the **Internet** icon on the Start menu is set to the system default stored in the second location at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** , which describes all Internet browser applications that are installed on the system.</span></span>

<span data-ttu-id="3f3c1-135">Cuando un usuario nuevo inicia sesión en el sistema, el menú Inicio usa el valor predeterminado de la subclave en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** para mostrar el cliente de Internet predeterminado e inicia la aplicación registrada cuando se hace clic en ese icono.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-135">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** to display the default Internet client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-internet-client"></a><span data-ttu-id="3f3c1-136">Cómo registrarse como el cliente de Internet predeterminado</span><span class="sxs-lookup"><span data-stu-id="3f3c1-136">How to Register as the Default Internet Client</span></span>

<span data-ttu-id="3f3c1-137">Debajo de la subclave **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** puede haber cero o más subclaves, una para cada aplicación de explorador de Internet registrada.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-137">Below the subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** there can be zero or more subkeys, one for each registered Internet browser application.</span></span> <span data-ttu-id="3f3c1-138">Por ejemplo, un sistema hipotético podría tener esta disposición:</span><span class="sxs-lookup"><span data-stu-id="3f3c1-138">For example, a hypothetical system might have this arrangement:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

<span data-ttu-id="3f3c1-139">Se mostrarán las entradas del registro con un explorador hipotético denominado "Lit View" desde una empresa ficticia denominada Litware Inc. Supongamos que el nombre del archivo ejecutable para la vista Lit es Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-139">We will demonstrate registry entries with a hypothetical browser called "Lit View" from a fictional company called Litware Inc. Suppose that the executable name for Lit View is Litview.exe.</span></span> <span data-ttu-id="3f3c1-140">El registro de la vista Lit se produce como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="3f3c1-140">The registration of Lit View occurs as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="3f3c1-141">Los datos de LocalizedString son del tipo REG \_ SZ o REG \_ Expand \_ SZ si se usan variables de ruta de acceso como `%programfiles%` .</span><span class="sxs-lookup"><span data-stu-id="3f3c1-141">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="3f3c1-142">LocalizedString proporciona la ruta de acceso a un archivo ejecutable (. exe) o de biblioteca (. dll).</span><span class="sxs-lookup"><span data-stu-id="3f3c1-142">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="3f3c1-143">Tenga en cuenta que la cadena de ruta de acceso comienza con un signo "arroba" (@) y que no se requieren comillas alrededor de la ruta de acceso, independientemente de los espacios que contiene.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-143">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="3f3c1-144">El entero decimal es el identificador de un recurso de cadena, incluido en el archivo DLL especificado, cuyo valor se va a mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-144">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="3f3c1-145">Esto permite usar el mismo registro para varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-145">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="3f3c1-146">Cada lenguaje proporciona una ResourceDLL.dll diferente.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-146">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="3f3c1-147">Esto permite que el sistema muestre la cadena correcta según el idioma seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-147">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="3f3c1-148">Los siguientes valores de REG \_ SZ o REG \_ Expand, indican al \_ menú Inicio del icono predeterminado que se muestre cuando el usuario selecciona Lit View como el explorador de Internet del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-148">The following REG\_SZ or REG\_EXPAND\_SZ value informs the Start menu of the default icon to display when the user selects Lit View as the Start menu Internet browser.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

<span data-ttu-id="3f3c1-149">La siguiente subclave del registro especifica una línea de comandos que se ejecuta cuando el usuario hace clic en el comando de menú de Internet en el menú Inicio, suponiendo que Lit View es el explorador de Internet seleccionado del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-149">The following registry subkey specifies a command line to run when the user clicks the Internet menu command on the Start menu, assuming that Lit View is the selected Start menu Internet browser.</span></span> <span data-ttu-id="3f3c1-150">Por ejemplo, el comando podría abrir el explorador con la Página principal del usuario o el comando podría iniciar una interfaz de usuario introductoria que el fabricante de software independiente (ISV) cree que es adecuado.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-150">For example, the command might open the browser with the user's home page or the command could launch an introductory user interface that the independent software vendor (ISV) feels is appropriate.</span></span> <span data-ttu-id="3f3c1-151">Los datos son de tipo REG \_ SZ o REG \_ Expand \_ , pero Observe que, dado que hay un espacio en la ruta de acceso de la línea de comandos, la ruta de acceso del archivo ejecutable está entre comillas.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-151">The data is of type REG\_SZ or REG\_EXPAND\_SZ, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

<span data-ttu-id="3f3c1-152">Cuando el usuario especifica [establecer el acceso y los valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md) que Lit View debe usar como explorador Web predeterminado de nivel de equipo, la aplicación debe establecer la siguiente \_ entrada reg SZ.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-152">When the user specifies through [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) that Lit View should be used as the computer-level default web browser, the application should set the following REG\_SZ entry.</span></span> <span data-ttu-id="3f3c1-153">Tenga en cuenta que, dado que SPAD se ejecuta con privilegios de administrador, se permite el acceso a esta subclave.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-153">Note that because SPAD runs with Administrator privileges, access to this subkey is allowed.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> <span data-ttu-id="3f3c1-154">En Windows Vista, el explorador Web predeterminado de nivel de usuario debe establecerse con la herramienta **programas predeterminados** , no con [SPAD](cpl-setprogramaccess.md).</span><span class="sxs-lookup"><span data-stu-id="3f3c1-154">In Windows Vista, the user-level default web browser should be set using the **Default Programs** tool, not [SPAD](cpl-setprogramaccess.md).</span></span>
> 
> <span data-ttu-id="3f3c1-155">**La siguiente información solo se aplica a Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="3f3c1-155">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="3f3c1-156">Si el registro del explorador Web predeterminado de nivel de equipo en HKEY \_ local \_ Machine, tal como se mostró anteriormente, es correcto, la aplicación debe eliminar la entrada predeterminada en la siguiente subclave:</span><span class="sxs-lookup"><span data-stu-id="3f3c1-156">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> <span data-ttu-id="3f3c1-157">Si se produce un error en el registro del explorador Web predeterminado de nivel de equipo en HKEY \_ local \_ Machine, la aplicación debe establecer los datos de reg \_ SZ tal como se muestra en este ejemplo para la aplicación Lit View:</span><span class="sxs-lookup"><span data-stu-id="3f3c1-157">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE fails, the application should set the REG\_SZ data as shown in this example for the Lit View application:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

<span data-ttu-id="3f3c1-158">Después de actualizar las subclaves adecuadas, la aplicación difunde el mensaje de [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con el parámetro *wParam* establecido en 0 y su parámetro *lParam* que apunta a la cadena terminada en NULL `"Software\Clients\StartMenuInternet"` .</span><span class="sxs-lookup"><span data-stu-id="3f3c1-158">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\StartMenuInternet"`.</span></span> <span data-ttu-id="3f3c1-159">Esto notifica al sistema operativo que el cliente predeterminado ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-159">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="3f3c1-160">La configuración de estas subclaves para el explorador de Internet predeterminado es necesaria para mantener la compatibilidad con versiones anteriores de los exploradores Web que no admiten registros por usuario.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-160">Setting these subkeys for the default Start menu Internet browser is necessary to preserve backward compatibility with old web browsers that do not support per-user registrations.</span></span>

## <a name="registering-for-the-start-menu-email-link"></a><span data-ttu-id="3f3c1-161">Registro para el vínculo de correo electrónico del menú Inicio</span><span class="sxs-lookup"><span data-stu-id="3f3c1-161">Registering for the Start Menu Email Link</span></span>

> [!Note]  
> <span data-ttu-id="3f3c1-162">El vínculo de correo electrónico del menú Inicio se ha quitado de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-162">The Start menu Email link has been removed as of Windows 7.</span></span> <span data-ttu-id="3f3c1-163">Sin embargo, este registro que se trata en esta sección todavía debe realizarse para su efecto en la asignación del cliente MAPI predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-163">However, this registration discussed in this section should still be performed for its effect in assigning the default MAPI client.</span></span>

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a><span data-ttu-id="3f3c1-164">Cómo el menú Inicio muestra el cliente de correo electrónico predeterminado</span><span class="sxs-lookup"><span data-stu-id="3f3c1-164">How the Start Menu Displays the Default Email Client</span></span>

<span data-ttu-id="3f3c1-165">Cualquier aplicación de correo electrónico puede registrarse para aparecer como un cliente de correo electrónico en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-165">Any email application can register to appear as an email client on the Start menu.</span></span> <span data-ttu-id="3f3c1-166">Esta visibilidad, junto con el registro adecuado para los tipos de [protocolos](/previous-versions//aa767743(v=vs.85)) y [archivos](fa-intro.md) de una aplicación, proporciona un estado de correo predeterminado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-166">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default mail status.</span></span>

<span data-ttu-id="3f3c1-167">Los registros realizados en el subárbol de **\_ \_ usuario de HKEY Current** tienen mayor prioridad para el usuario de la consola que los registros correspondientes realizados en el **\_ \_ equipo local HKEY**.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-167">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="3f3c1-168">En el caso de los nuevos usuarios del sistema, se usan las opciones almacenadas en **HKEY \_ local \_ Machine** .</span><span class="sxs-lookup"><span data-stu-id="3f3c1-168">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="3f3c1-169">A partir de Windows XP, la configuración de correo electrónico del menú Inicio se mantiene en las entradas predeterminadas de dos ubicaciones del registro:</span><span class="sxs-lookup"><span data-stu-id="3f3c1-169">As of Windows XP, Start menu Email settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="3f3c1-170">**HKEY \_ \_** \\  \\  \\ **Correo electrónico** de clientes de software del usuario actual</span><span class="sxs-lookup"><span data-stu-id="3f3c1-170">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>
-   <span data-ttu-id="3f3c1-171">**HKEY \_ \_** \\  \\  \\ **Correo electrónico** de clientes de software de máquina local</span><span class="sxs-lookup"><span data-stu-id="3f3c1-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>

<span data-ttu-id="3f3c1-172">La subclave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **mail** describe el cliente de correo electrónico que se inicia cuando el usuario hace clic en el icono de **correo electrónico** del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-172">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email client that is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="3f3c1-173">La subclave **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** describe las aplicaciones de correo electrónico instaladas en el sistema, así como la aplicación de correo electrónico predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-173">The subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email applications that are installed on the system, as well as the default email application.</span></span>

<span data-ttu-id="3f3c1-174">Si el correo de los clientes de software del **\_ \_ usuario actual de HKEY** \\  \\  \\  está en blanco o falta, se utiliza el valor predeterminado definido en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** para seleccionar la aplicación de correo electrónico que aparece en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-174">If the **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** is blank or missing, the default value defined in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** is used to select the email application that appears on the Start menu.</span></span>

<span data-ttu-id="3f3c1-175">Cuando un usuario nuevo inicia sesión en el sistema, el menú Inicio usa el valor predeterminado de la subclave en **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** para mostrar el cliente de correo electrónico predeterminado e inicia la aplicación registrada cuando se hace clic en ese icono.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-175">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** to display the default email client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-email-client"></a><span data-ttu-id="3f3c1-176">Cómo registrarse como cliente de correo electrónico predeterminado</span><span class="sxs-lookup"><span data-stu-id="3f3c1-176">How to Register as the Default EMail Client</span></span>

<span data-ttu-id="3f3c1-177">**HKEY \_ El \_** \\  \\ correo electrónico de **los clientes** \\  de software de máquina local puede contener cero o más subclaves, una para cada aplicación de correo electrónico registrada.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-177">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** can contain zero or more subkeys, one for each registered email application.</span></span> <span data-ttu-id="3f3c1-178">Por ejemplo, un sistema hipotético podría definir las subclaves siguientes:</span><span class="sxs-lookup"><span data-stu-id="3f3c1-178">For example, a hypothetical system might define the following subkeys:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

<span data-ttu-id="3f3c1-179">Se mostrarán las entradas del registro con un cliente de correo electrónico hipotético llamado "Lit mail" de la empresa ficticia denominada Litware Inc. Litware Inc. decide registrar este cliente de correo electrónico con el nombre interno "LitMail".</span><span class="sxs-lookup"><span data-stu-id="3f3c1-179">We will demonstrate registry entries with a hypothetical email client called "Lit Mail" from the fictional company called Litware Inc. Litware Inc. decides to register this email client under the internal name "LitMail".</span></span> <span data-ttu-id="3f3c1-180">Al igual que con un explorador, el nombre interno es una cadena única que se usa como nombre de la subclave, pero nunca se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-180">As with a browser, the internal name is a unique string used as the subkey name, but it is never shown to the user.</span></span>

<span data-ttu-id="3f3c1-181">Para instalar el cliente de correo electrónico de lit mail como predeterminado, usan la siguiente subclave y sus entradas:</span><span class="sxs-lookup"><span data-stu-id="3f3c1-181">To install the Lit Mail email client as the default, they use the following subkey and its entries:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

<span data-ttu-id="3f3c1-182">Los datos de LocalizedString son del tipo REG \_ SZ o REG \_ Expand \_ SZ si se usan variables de ruta de acceso como `%programfiles%` .</span><span class="sxs-lookup"><span data-stu-id="3f3c1-182">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="3f3c1-183">LocalizedString proporciona la ruta de acceso a un archivo ejecutable (. exe) o de biblioteca (. dll).</span><span class="sxs-lookup"><span data-stu-id="3f3c1-183">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="3f3c1-184">Tenga en cuenta que la cadena de ruta de acceso comienza con un signo "arroba" (@) y que no se requieren comillas alrededor de la ruta de acceso, independientemente de los espacios que contiene.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-184">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="3f3c1-185">El entero decimal es el identificador de un recurso de cadena, incluido en el archivo DLL especificado, cuyo valor se va a mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-185">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="3f3c1-186">Esto permite usar el mismo registro para varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-186">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="3f3c1-187">Cada lenguaje proporciona una ResourceDLL.dll diferente.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-187">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="3f3c1-188">Esto permite que el sistema muestre la cadena correcta según el idioma seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-188">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="3f3c1-189">Después de actualizar las subclaves adecuadas, la aplicación difunde el mensaje de [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con el parámetro *wParam* establecido en 0 y su parámetro *lParam* que apunta a la cadena terminada en NULL `"Software\Clients\Mail"` .</span><span class="sxs-lookup"><span data-stu-id="3f3c1-189">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\Mail"`.</span></span> <span data-ttu-id="3f3c1-190">Esto notifica al sistema operativo que el cliente predeterminado ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-190">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="3f3c1-191">Para mantener la compatibilidad con las aplicaciones que no admiten cadenas localizadas, el nombre de la aplicación en el idioma instalado también debe establecerse como el valor predeterminado de la subclave.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-191">For backward compatibility with applications that do not support localized strings, the name of the application in the installed language should also be set as the default value for the subkey.</span></span>

<span data-ttu-id="3f3c1-192">Los siguientes valores de **reg \_ SZ** o **reg \_ Expand \_** se muestran en el menú Inicio del icono predeterminado para que se muestren cuando el usuario selecciona Lit mail como programa de correo del menú Inicio:</span><span class="sxs-lookup"><span data-stu-id="3f3c1-192">The following **REG\_SZ** or **REG\_EXPAND\_SZ** value informs the Start menu of the default icon to display when the user selects Lit Mail as the Start menu mail program:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

<span data-ttu-id="3f3c1-193">La entrada siguiente especifica una línea de comandos que se ejecutará cuando el usuario haga clic en el elemento de menú **correo electrónico** en el menú Inicio, suponiendo que Lit mail es el programa de correo electrónico seleccionado del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-193">The following entry specifies a command line to run when the user clicks the **E-mail** menu item on the Start menu, assuming that Lit Mail is the selected Start menu email program.</span></span> <span data-ttu-id="3f3c1-194">Esta línea de comandos también se ejecuta si el usuario selecciona **leer correo electrónico** en el menú **herramientas** de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-194">This command line is also run if the user selects **Read email** from the Windows Internet Explorer **Tools** menu.</span></span> <span data-ttu-id="3f3c1-195">Los datos son de tipo **reg \_ SZ** o **reg \_ Expand \_**, pero Observe que, dado que hay un espacio en la ruta de acceso de la línea de comandos, la ruta de acceso del archivo ejecutable está entre comillas.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-195">The data is of type **REG\_SZ** or **REG\_EXPAND\_SZ**, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

<span data-ttu-id="3f3c1-196">Si (y solo si) *el usuario* especifica que Lit mail sea la aplicación de correo electrónico predeterminada del menú Inicio, la aplicación Lit mail puede escribir su nombre interno en el siguiente valor **reg \_ SZ** :</span><span class="sxs-lookup"><span data-stu-id="3f3c1-196">If (and only if) *the user* specifies Lit Mail to be the default Start menu email application, the Lit Mail application may write its internal name to the following **REG\_SZ** value:</span></span>

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="3f3c1-197">Si (y solo si) *el usuario* especifica que Lit mail sea la aplicación de correo electrónico predeterminada para todo el sistema, la aplicación Lit mail puede escribir su nombre interno en el valor **reg \_ SZ** que se especifica a continuación.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-197">If (and only if) *the user* specifies Lit Mail to be the system-wide default email application, the Lit Mail application may write its internal name to the **REG\_SZ** value specified below.</span></span> <span data-ttu-id="3f3c1-198">Tenga en cuenta que el acceso a esta subclave podría estar restringido.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-198">Note that access to this subkey might be restricted.</span></span> <span data-ttu-id="3f3c1-199">Las aplicaciones no deben suponer que todos los usuarios tienen permiso para cambiar la aplicación de correo electrónico predeterminada para todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-199">Applications should not assume that all users have permission to change the system-wide default email application.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="3f3c1-200">El registro como la aplicación de correo electrónico predeterminada del menú Inicio no es equivalente al registro como el cliente de correo electrónico predeterminado del sistema o el controlador *mailto* registrado.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-200">Registration as the default Start menu email application is not equivalent to registration as the system default email client or the registered *mailto* handler.</span></span>

-   <span data-ttu-id="3f3c1-201">El cliente de correo electrónico predeterminado del sistema se inicia cuando el usuario hace clic en **leer correo electrónico** en el menú **herramientas** de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-201">The system default email client is started when the user clicks **Read email** from the Internet Explorer **Tools** menu.</span></span>
-   <span data-ttu-id="3f3c1-202">El controlador *mailto* registrado se inicia cuando el usuario hace clic en una dirección URL del formulario `mailto:someone@example.com` .</span><span class="sxs-lookup"><span data-stu-id="3f3c1-202">The registered *mailto* handler is started when the user clicks a URL of the form `mailto:someone@example.com`.</span></span>
-   <span data-ttu-id="3f3c1-203">La aplicación de correo electrónico del menú Inicio se inicia cuando el usuario hace clic en el icono de **correo electrónico** del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-203">The Start menu email application is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="3f3c1-204">Si no se especifica ninguna aplicación de correo electrónico predeterminada del menú Inicio, el icono de correo electrónico del menú Inicio inicia el cliente de correo electrónico predeterminado del sistema.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-204">If no default Start menu email application is specified, the Email icon on the Start menu launches the system default email client.</span></span>

<span data-ttu-id="3f3c1-205">En este tema no se trata el registro de la aplicación como el controlador de protocolo *mailto* predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-205">This topic does not cover registration of the application as the default *mailto* protocol handler.</span></span> <span data-ttu-id="3f3c1-206">Las aplicaciones que desean registrarse de este modo deben seguir las especificaciones existentes sobre este asunto.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-206">Applications that want to register in such a manner should continue to follow existing specifications on this subject.</span></span>

## <a name="customizing-the-context-menu"></a><span data-ttu-id="3f3c1-207">Personalización del menú contextual</span><span class="sxs-lookup"><span data-stu-id="3f3c1-207">Customizing the Context Menu</span></span>

<span data-ttu-id="3f3c1-208">Una aplicación puede personalizar las páginas de propiedades que se muestran cuando el usuario selecciona **propiedades** en el menú contextual del icono de **correo electrónico** (o **Internet**).</span><span class="sxs-lookup"><span data-stu-id="3f3c1-208">An application can customize the property pages that are displayed when the user selects **Properties** from the **E-mail** (or **Internet**) icon's shortcut menu.</span></span> <span data-ttu-id="3f3c1-209">Por ejemplo, la aplicación de correo electrónico Litware agrega los siguientes datos de **reg \_ SZ** o **reg \_ Expand \_ SZ** para mostrar una hoja de propiedades personalizada para el icono de **correo electrónico** en lugar de su hoja de propiedades predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-209">For example, the Litware email application adds the following **REG\_SZ** or **REG\_EXPAND\_SZ** data to display a custom property sheet for the **E-mail** icon rather than its default property sheet.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

<span data-ttu-id="3f3c1-210">El elemento de datos MUIVerb se construye a partir de un signo "arroba" (@), seguido de la ruta de acceso completa al archivo DLL de recursos, una coma, un signo menos (-) y, a continuación, el identificador de recursos de cadena decimal que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-210">The MUIVerb data item is constructed beginning with an "at" sign (@), followed by the full path to the resource DLL, a comma, a minus sign (-), and then the decimal string resource identifier to display.</span></span> <span data-ttu-id="3f3c1-211">Tenga en cuenta que la ruta de acceso al LitMail.exe programa contiene espacios, por lo que la cadena de ruta de acceso se coloca entre comillas.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-211">Note that the path to the LitMail.exe program contains spaces, so the path string is placed inside quotation marks.</span></span>

<span data-ttu-id="3f3c1-212">Una aplicación también puede Agregar comandos adicionales al menú contextual.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-212">An application can also add additional commands to the context menu.</span></span> <span data-ttu-id="3f3c1-213">Por ejemplo, la aplicación de correo electrónico de Litware agrega un comando de **búsqueda** con los siguientes datos de **reg \_ SZ** :</span><span class="sxs-lookup"><span data-stu-id="3f3c1-213">For example, the Litware email application adds a **find** command with the following **REG\_SZ** data:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

<span data-ttu-id="3f3c1-214">El nombre de la subclave que se encuentra debajo del **Shell** (en este caso, "Find") es un nombre arbitrario no traducido.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-214">The subkey name below **shell** (in this case, "find") is an arbitrary, nonlocalized name.</span></span> <span data-ttu-id="3f3c1-215">Una vez más, los datos de MUIVerb contienen un signo de arroba (@) como primer elemento, seguido de la ruta de acceso a un archivo DLL de recursos, un separador de coma y, a continuación, un signo menos que precede al identificador de recursos de cadena decimal.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-215">Once again the MUIVerb data contains an "at" sign (@) as the first element, followed by the path to a resource DLL, a comma separator, and then a minus sign preceding the decimal string resource identifier.</span></span> <span data-ttu-id="3f3c1-216">Por ejemplo, ese recurso de cadena podría ser "Abrir libreta de direcciones".</span><span class="sxs-lookup"><span data-stu-id="3f3c1-216">For example, that string resource might be "Open Address Book".</span></span> <span data-ttu-id="3f3c1-217">Por último, tenga en cuenta que la cadena de la línea de comandos contiene espacios, por lo que está entre comillas.</span><span class="sxs-lookup"><span data-stu-id="3f3c1-217">Finally, note that the command-line string contains spaces, so it is enclosed in quotation marks.</span></span>

 

 
