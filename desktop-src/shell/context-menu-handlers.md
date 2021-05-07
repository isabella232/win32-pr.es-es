---
description: Los controladores de menú contextual, también conocidos como controladores de menú contextual o controladores de verbos, son un tipo de controlador de tipo de archivo. Al igual que todos estos controladores, son objetos del Modelo de objetos componentes (COM) en proceso implementados como archivos DLL.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Crear controladores de menús contextuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd2611c492d517e9312ec2a4e1c95d7f1aa0fea
ms.sourcegitcommit: 05b3d7f137ef9bbddf4049215cb11d55b935997e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/06/2021
ms.locfileid: "108800976"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="62676-104">Crear controladores de menús contextuales</span><span class="sxs-lookup"><span data-stu-id="62676-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="62676-105">Los controladores de menú contextual, también conocidos como controladores de menú contextual o controladores de verbos, son un tipo de controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="62676-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="62676-106">Estos controladores pueden estar impelados de forma que se carguen en su propio proceso o en el explorador, u otros procesos de terceros.</span><span class="sxs-lookup"><span data-stu-id="62676-106">These handlers may be impelmented in a way that causes them to load in their own process or in the explorer, or other 3rd party processes.</span></span> <span data-ttu-id="62676-107">Al crear controladores en proceso, debe tener cuidado, ya que pueden causar daños en el proceso que los carga.</span><span class="sxs-lookup"><span data-stu-id="62676-107">Take care when creating in-process handlers as they can cause harm to the process that loads them.</span></span>

> [!Note]  
> <span data-ttu-id="62676-108">Hay consideraciones especiales para las versiones de Windows basadas en 64 bits al registrar controladores que funcionan en el contexto de aplicaciones de 32 bits: cuando se invoca en el contexto de una aplicación de bits diferente, el subsistema WOW64 redirige el acceso del sistema de archivos a algunas rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="62676-108">There are special considerations for 64-bit based versions of Windows when registering handlers that work in the context of 32-bit applications: when invoked in the context of an application of different bitness, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="62676-109">Si el controlador .exe se almacena en una de esas rutas de acceso, no es accesible en este contexto.</span><span class="sxs-lookup"><span data-stu-id="62676-109">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="62676-110">Por lo tanto, para evitarlo, almacene el archivo .exe en una ruta de acceso que no se redirija o almacene una versión de código auxiliar de .exe que inicie la versión real.</span><span class="sxs-lookup"><span data-stu-id="62676-110">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

<span data-ttu-id="62676-111">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="62676-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="62676-112">Verbos canónicos</span><span class="sxs-lookup"><span data-stu-id="62676-112">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="62676-113">Verbos extendidos</span><span class="sxs-lookup"><span data-stu-id="62676-113">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="62676-114">Personalizar un menú contextual mediante verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="62676-114">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="62676-115">Activación del controlador mediante la interfaz IDropTarget</span><span class="sxs-lookup"><span data-stu-id="62676-115">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="62676-116">Especificar la posición y el orden de los verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="62676-116">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="62676-117">Colocar verbos en la parte superior o inferior del menú</span><span class="sxs-lookup"><span data-stu-id="62676-117">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="62676-118">Crear menús estáticos en cascada</span><span class="sxs-lookup"><span data-stu-id="62676-118">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="62676-119">Obtención del comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada</span><span class="sxs-lookup"><span data-stu-id="62676-119">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="62676-120">En desuso: asociación de verbos Intercambio dinámico de datos comandos</span><span class="sxs-lookup"><span data-stu-id="62676-120">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="62676-121">Completar tareas de implementación de verbos</span><span class="sxs-lookup"><span data-stu-id="62676-121">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="62676-122">Personalizar el menú contextual para objetos de shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="62676-122">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="62676-123">Extensión de un submenú nuevo</span><span class="sxs-lookup"><span data-stu-id="62676-123">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="62676-124">Suprimir verbos y controlar la visibilidad</span><span class="sxs-lookup"><span data-stu-id="62676-124">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="62676-125">Empleo del modelo de selección de verbos</span><span class="sxs-lookup"><span data-stu-id="62676-125">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="62676-126">Usar atributos de elemento</span><span class="sxs-lookup"><span data-stu-id="62676-126">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="62676-127">Implementar verbos personalizados para carpetas mediante Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="62676-127">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="62676-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62676-128">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="62676-129">Verbos canónicos</span><span class="sxs-lookup"><span data-stu-id="62676-129">Canonical Verbs</span></span>

<span data-ttu-id="62676-130">Las aplicaciones suelen ser responsables de proporcionar cadenas de presentación localizadas para los verbos que definen.</span><span class="sxs-lookup"><span data-stu-id="62676-130">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="62676-131">Sin embargo, para proporcionar un grado de independencia del lenguaje, el sistema define un conjunto estándar de verbos de uso común denominados verbos canónicos.</span><span class="sxs-lookup"><span data-stu-id="62676-131">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="62676-132">Un verbo canónico nunca se muestra al usuario y se puede usar con cualquier lenguaje de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="62676-132">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="62676-133">El sistema usa el nombre canónico para generar automáticamente una cadena de presentación localizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="62676-133">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="62676-134">Por ejemplo, la cadena para mostrar del verbo abierto se establece en **Abrir** en un sistema inglés y en el equivalente en alemán en un sistema alemán.</span><span class="sxs-lookup"><span data-stu-id="62676-134">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>


| <span data-ttu-id="62676-135">Verbo canónico</span><span class="sxs-lookup"><span data-stu-id="62676-135">Canonical verb</span></span> | <span data-ttu-id="62676-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="62676-136">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="62676-137">Abrir</span><span class="sxs-lookup"><span data-stu-id="62676-137">Open</span></span>           | <span data-ttu-id="62676-138">Abre el archivo o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="62676-138">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="62676-139">Abrirnuevo</span><span class="sxs-lookup"><span data-stu-id="62676-139">Opennew</span></span>        | <span data-ttu-id="62676-140">Abre el archivo o la carpeta en una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="62676-140">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="62676-141">Impresión</span><span class="sxs-lookup"><span data-stu-id="62676-141">Print</span></span>          | <span data-ttu-id="62676-142">Imprime el archivo.</span><span class="sxs-lookup"><span data-stu-id="62676-142">Prints the file.</span></span>                                                     |
| <span data-ttu-id="62676-143">Printto</span><span class="sxs-lookup"><span data-stu-id="62676-143">Printto</span></span>        | <span data-ttu-id="62676-144">Permite al usuario imprimir un archivo arrastrándolo a un objeto de impresora.</span><span class="sxs-lookup"><span data-stu-id="62676-144">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="62676-145">Explorar</span><span class="sxs-lookup"><span data-stu-id="62676-145">Explore</span></span>        | <span data-ttu-id="62676-146">Abre Explorador de Windows con la carpeta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="62676-146">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="62676-147">Propiedades</span><span class="sxs-lookup"><span data-stu-id="62676-147">Properties</span></span>     | <span data-ttu-id="62676-148">Abre la hoja de propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="62676-148">Opens the object's property sheet.</span></span>                                   |

> [!Note]  
> <span data-ttu-id="62676-149">El **verbo Printto** también es canónico, pero nunca se muestra.</span><span class="sxs-lookup"><span data-stu-id="62676-149">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="62676-150">Su inclusión permite al usuario imprimir un archivo arrastrándolo a un objeto de impresora.</span><span class="sxs-lookup"><span data-stu-id="62676-150">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

<span data-ttu-id="62676-151">Los controladores de menús contextuales pueden proporcionar sus propios verbos canónicos a través de [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) con **\_ GCS VERBW** o **GCS \_ VERBA.**</span><span class="sxs-lookup"><span data-stu-id="62676-151">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="62676-152">El sistema usará los verbos canónicos como segundo parámetro (*lpOperation*) pasado a [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)y [**es CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). **Miembro lpVerb** pasado al [**método IContextMenu::InvokeCommand.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)</span><span class="sxs-lookup"><span data-stu-id="62676-152">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="62676-153">Verbos extendidos</span><span class="sxs-lookup"><span data-stu-id="62676-153">Extended Verbs</span></span>

<span data-ttu-id="62676-154">Cuando el usuario hace clic con el botón derecho en un objeto, el menú contextual muestra los verbos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="62676-154">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="62676-155">Es posible que quiera agregar y admitir comandos en algunos menús contextuales que no se muestran en todos los menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="62676-155">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="62676-156">Por ejemplo, podría tener comandos que no se usan normalmente o que están pensados para usuarios experimentados.</span><span class="sxs-lookup"><span data-stu-id="62676-156">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="62676-157">Por esta razón, también puede definir uno o varios verbos extendidos.</span><span class="sxs-lookup"><span data-stu-id="62676-157">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="62676-158">Estos verbos son similares a los verbos normales, pero se distinguen de los verbos normales por la forma en que se registran.</span><span class="sxs-lookup"><span data-stu-id="62676-158">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="62676-159">Para tener acceso a verbos extendidos, el usuario debe hacer clic con el botón derecho en un objeto mientras presiona la tecla MAYÚS.</span><span class="sxs-lookup"><span data-stu-id="62676-159">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="62676-160">Cuando el usuario lo hace, se muestran los verbos extendidos además de los verbos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="62676-160">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="62676-161">Puede usar el Registro para definir uno o varios verbos extendidos.</span><span class="sxs-lookup"><span data-stu-id="62676-161">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="62676-162">Los comandos asociados solo se mostrarán cuando el usuario haga clic con el botón derecho en un objeto mientras también presiona la tecla MAYÚS.</span><span class="sxs-lookup"><span data-stu-id="62676-162">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="62676-163">Para definir un verbo como extendido, agregue un valor **REG \_ SZ** "extendido" a la subclave del verbo.</span><span class="sxs-lookup"><span data-stu-id="62676-163">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="62676-164">El valor no debe tener ningún dato asociado.</span><span class="sxs-lookup"><span data-stu-id="62676-164">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="62676-165">Personalizar un menú contextual mediante verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="62676-165">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="62676-166">Después [de elegir un verbo estático](shortcut-choose-method.md) o dinámico para el menú contextual, puede ampliar el menú contextual de un tipo de archivo registrando un verbo estático para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="62676-166">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="62676-167">Para ello, agregue una **subclave shell** debajo de la subclave para el ProgID de la aplicación asociada al tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="62676-167">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="62676-168">Opcionalmente, puede definir un verbo predeterminado para el tipo de archivo si lo hace el valor predeterminado de la **subclave Shell.**</span><span class="sxs-lookup"><span data-stu-id="62676-168">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="62676-169">El verbo predeterminado se muestra primero en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="62676-169">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="62676-170">Su finalidad es proporcionar al Shell un verbo que puede usar cuando se llama a la función [**ShellExecuteEx,**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pero no se especifica ningún verbo.</span><span class="sxs-lookup"><span data-stu-id="62676-170">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="62676-171">El shell no selecciona necesariamente el verbo predeterminado cuando **se usa ShellExecuteEx** de este modo.</span><span class="sxs-lookup"><span data-stu-id="62676-171">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="62676-172">El Shell usa el primer verbo disponible en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="62676-172">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="62676-173">Verbo predeterminado</span><span class="sxs-lookup"><span data-stu-id="62676-173">The default verb</span></span>
2.  <span data-ttu-id="62676-174">Primer verbo del Registro, si se especifica el orden verbal</span><span class="sxs-lookup"><span data-stu-id="62676-174">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="62676-175">Verbo  abierto</span><span class="sxs-lookup"><span data-stu-id="62676-175">The **Open** verb</span></span>
4.  <span data-ttu-id="62676-176">Verbo **Abrir con**</span><span class="sxs-lookup"><span data-stu-id="62676-176">The **Open With** verb</span></span>

<span data-ttu-id="62676-177">Si ninguno de los verbos enumerados está disponible, se produce un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="62676-177">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="62676-178">Cree una subclave para cada verbo que quiera agregar en la subclave Shell.</span><span class="sxs-lookup"><span data-stu-id="62676-178">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="62676-179">Cada una de estas subclaves debe tener un **valor REG \_ SZ** establecido en la cadena de presentación del verbo (cadena localizada).</span><span class="sxs-lookup"><span data-stu-id="62676-179">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="62676-180">Para cada subclave de verbo, cree una subclave de comando con el valor predeterminado establecido en la línea de comandos para activar los elementos.</span><span class="sxs-lookup"><span data-stu-id="62676-180">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="62676-181">Para verbos canónicos, como **Abrir** e Imprimir **,** puede omitir la cadena de presentación porque el sistema muestra automáticamente una cadena localizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="62676-181">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="62676-182">En el caso de los verbos no éticos, si se omite la cadena para mostrar, se muestra la cadena de verbo.</span><span class="sxs-lookup"><span data-stu-id="62676-182">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="62676-183">En el siguiente ejemplo del Registro, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="62676-183">In the following registry example, note that:</span></span>

-   <span data-ttu-id="62676-184">Dado **que Doit** no es un verbo canónico, se le asigna un nombre para mostrar, que se puede seleccionar presionando la tecla D.</span><span class="sxs-lookup"><span data-stu-id="62676-184">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="62676-185">El **verbo Printto** no aparece en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="62676-185">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="62676-186">Sin embargo, su inclusión en el Registro permite al usuario imprimir archivos al colocarlos en un icono de impresora.</span><span class="sxs-lookup"><span data-stu-id="62676-186">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="62676-187">Se muestra una subclave para cada verbo.</span><span class="sxs-lookup"><span data-stu-id="62676-187">One subkey is shown for each verb.</span></span> <span data-ttu-id="62676-188">**%1 representa** el nombre de archivo y **%2 el** nombre de impresora.</span><span class="sxs-lookup"><span data-stu-id="62676-188">**%1** represents the file name and **%2** the printer name.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

<span data-ttu-id="62676-189">En el diagrama siguiente se muestra la extensión del menú contextual de acuerdo con las entradas del Registro anteriores.</span><span class="sxs-lookup"><span data-stu-id="62676-189">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="62676-190">Este menú contextual tiene los  **verbos** **Abrir,** Hacerlo e Imprimir en su menú, con Do **It (Hacerlo)** como verbo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="62676-190">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![captura de pantalla del menú contextual de verbo predeterminado](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="62676-192">Activación del controlador mediante la interfaz IDropTarget</span><span class="sxs-lookup"><span data-stu-id="62676-192">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="62676-193">Intercambio dinámico de datos (DDE) está en desuso; use [**IDropTarget en su**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) lugar.</span><span class="sxs-lookup"><span data-stu-id="62676-193">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="62676-194">**IDropTarget es** más sólido y tiene una mejor compatibilidad con la activación porque usa la activación COM del controlador.</span><span class="sxs-lookup"><span data-stu-id="62676-194">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="62676-195">En el caso de la selección de varios elementos, **IDropTarget** no está sujeto a las restricciones de tamaño de búfer que se encuentran en DDE y [**CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)</span><span class="sxs-lookup"><span data-stu-id="62676-195">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="62676-196">Además, los elementos se pasan a la aplicación como un objeto de datos que se puede convertir en una matriz de elementos mediante la [**función SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)</span><span class="sxs-lookup"><span data-stu-id="62676-196">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="62676-197">Esto es más sencillo y no pierde la información del espacio de nombres, como sucede cuando el elemento se convierte en una ruta de acceso para los protocolos DDE o de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="62676-197">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="62676-198">Para obtener más información sobre [**las consultas IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y Shell para los atributos de asociación de archivos, vea [Perceived Types and Application Registration](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="62676-198">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="62676-199">Especificar la posición y el orden de los verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="62676-199">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="62676-200">Normalmente, los verbos se ordenan en un menú contextual en función de cómo se enumeran; La enumeración se basa primero en el orden de la matriz de asociación y, a continuación, en el orden de los elementos de la matriz de asociación, tal y como se define en el criterio de ordenación del registro.</span><span class="sxs-lookup"><span data-stu-id="62676-200">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="62676-201">Los verbos se pueden ordenar especificando el valor predeterminado de la subclave Shell para la entrada de asociación.</span><span class="sxs-lookup"><span data-stu-id="62676-201">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="62676-202">Este valor predeterminado puede incluir un solo elemento, que se mostrará en la posición superior del menú contextual, o una lista de elementos separados por espacios o comas.</span><span class="sxs-lookup"><span data-stu-id="62676-202">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="62676-203">En el último caso, el primer elemento de la lista es el elemento predeterminado y los demás verbos se muestran inmediatamente debajo de él en el orden especificado.</span><span class="sxs-lookup"><span data-stu-id="62676-203">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="62676-204">Por ejemplo, la siguiente entrada del Registro genera verbos de menú contextual en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="62676-204">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="62676-205">Mostrar</span><span class="sxs-lookup"><span data-stu-id="62676-205">Display</span></span>
2.  <span data-ttu-id="62676-206">Gadgets</span><span class="sxs-lookup"><span data-stu-id="62676-206">Gadgets</span></span>
3.  <span data-ttu-id="62676-207">Personalización</span><span class="sxs-lookup"><span data-stu-id="62676-207">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="62676-208">De forma similar, la siguiente entrada del Registro genera verbos de menú contextual en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="62676-208">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="62676-209">Personalización</span><span class="sxs-lookup"><span data-stu-id="62676-209">Personalization</span></span>
2.  <span data-ttu-id="62676-210">Gadgets</span><span class="sxs-lookup"><span data-stu-id="62676-210">Gadgets</span></span>
3.  <span data-ttu-id="62676-211">Mostrar</span><span class="sxs-lookup"><span data-stu-id="62676-211">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="62676-212">Colocar verbos en la parte superior o inferior del menú</span><span class="sxs-lookup"><span data-stu-id="62676-212">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="62676-213">El siguiente atributo del Registro se puede usar para colocar un verbo en la parte superior o inferior del menú.</span><span class="sxs-lookup"><span data-stu-id="62676-213">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="62676-214">Si hay varios verbos que especifican este atributo, el último en hacerlo obtiene prioridad:</span><span class="sxs-lookup"><span data-stu-id="62676-214">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="62676-215">Crear menús estáticos en cascada</span><span class="sxs-lookup"><span data-stu-id="62676-215">Creating Static Cascading Menus</span></span>

<span data-ttu-id="62676-216">En Windows 7 y versiones posteriores, la implementación del menú en cascada se admite a través de la configuración del Registro.</span><span class="sxs-lookup"><span data-stu-id="62676-216">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="62676-217">Antes de Windows 7, la creación de menús en cascada solo era posible mediante la implementación de la [**interfaz IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)</span><span class="sxs-lookup"><span data-stu-id="62676-217">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="62676-218">En Windows 7 y versiones posteriores, debe recurrir a soluciones basadas en código COM solo cuando los métodos estáticos no son suficientes.</span><span class="sxs-lookup"><span data-stu-id="62676-218">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="62676-219">En la captura de pantalla siguiente se proporciona un ejemplo de un menú en cascada.</span><span class="sxs-lookup"><span data-stu-id="62676-219">The following screen shot provides an example of a cascading menu.</span></span>

![captura de pantalla que muestra un ejemplo de un menú en cascada](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="62676-221">En Windows 7 y versiones posteriores, hay tres maneras de crear menús en cascada:</span><span class="sxs-lookup"><span data-stu-id="62676-221">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="62676-222">Crear menús en cascada con la entrada del Registro SubCommands</span><span class="sxs-lookup"><span data-stu-id="62676-222">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="62676-223">Crear menús en cascada con la entrada del Registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="62676-223">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="62676-224">Crear menús en cascada con la interfaz IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="62676-224">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="62676-225">Crear menús en cascada con la entrada del Registro SubCommands</span><span class="sxs-lookup"><span data-stu-id="62676-225">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="62676-226">En Windows 7 y versiones posteriores, puede usar la entrada SubCommands para crear menús en cascada mediante el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="62676-226">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="62676-227">**Para crear un menú en cascada mediante la entrada SubCommands**</span><span class="sxs-lookup"><span data-stu-id="62676-227">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="62676-228">Cree una subclave en el shell **de ProgID \_ \_ raíz de HKEY CLASSES** para representar el menú en \\  \\  cascada.</span><span class="sxs-lookup"><span data-stu-id="62676-228">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="62676-229">En este ejemplo, se le da a esta subclave el nombre *CascadeTest.*</span><span class="sxs-lookup"><span data-stu-id="62676-229">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="62676-230">Asegúrese de que el valor predeterminado de la subclave *CascadeTest* está vacío y se muestra **como (valor no establecido).**</span><span class="sxs-lookup"><span data-stu-id="62676-230">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="62676-231">A la subclave *CascadeTest,* agregue una entrada DE TIPO **INVERB de tipo REG \_ SZ** y asígnele el texto que aparecerá como su nombre en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="62676-231">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="62676-232">En este ejemplo, le asignamos "Test Cascade Menu".</span><span class="sxs-lookup"><span data-stu-id="62676-232">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="62676-233">A la subclave *CascadeTest,* agregue una entrada SubCommands de tipo **REG \_ SZ** que esté asignada a una lista, delimitada por punto y coma, de los verbos que deben aparecer en el menú, en el orden de apariencia.</span><span class="sxs-lookup"><span data-stu-id="62676-233">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="62676-234">Por ejemplo, aquí asignamos una serie de verbos proporcionados por el sistema:</span><span class="sxs-lookup"><span data-stu-id="62676-234">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="62676-235">En el caso de verbos personalizados, implemente mediante cualquiera de los métodos de implementación de verbo estáticos y enumérrelos en la subclave **CommandStore** como se muestra en este ejemplo para un *verbo ficticio VerbName*:</span><span class="sxs-lookup"><span data-stu-id="62676-235">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> <span data-ttu-id="62676-236">Este método tiene la ventaja de que los verbos personalizados se pueden registrar una vez y reutilizarse enumerando el nombre del verbo en la entrada SubCommands.</span><span class="sxs-lookup"><span data-stu-id="62676-236">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="62676-237">Sin embargo, requiere que la aplicación tenga permiso para modificar el Registro en **HKEY \_ LOCAL \_ MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="62676-237">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="62676-238">Creación de menús en cascada con la entrada del Registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="62676-238">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="62676-239">En Windows 7 y versiones posteriores, puede usar la entrada ExtendedSubCommandKey para crear menús en cascada extendidos: menús en cascada dentro de menús en cascada.</span><span class="sxs-lookup"><span data-stu-id="62676-239">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="62676-240">La siguiente captura de pantalla es un ejemplo de un menú en cascada extendido.</span><span class="sxs-lookup"><span data-stu-id="62676-240">The following screen shot is an example of an extended cascading menu.</span></span>

![captura de pantalla que muestra el menú en cascada extendido para dispositivos](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="62676-242">Dado **que HKEY \_ CLASSES ROOT \_ es** una combinación de **HKEY CURRENT \_ \_ USER** y **HKEY LOCAL \_ \_ MACHINE,** puede registrar los verbos personalizados en la subclave clases de software **HKEY CURRENT \_ \_ USER.** \\  \\ </span><span class="sxs-lookup"><span data-stu-id="62676-242">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="62676-243">La principal ventaja de hacerlo es que no se requiere el permiso con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="62676-243">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="62676-244">Además, otras asociaciones de archivo pueden reutilizar todo este conjunto de verbos especificando la misma subclave ExtendedSubCommandsKey.</span><span class="sxs-lookup"><span data-stu-id="62676-244">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="62676-245">Si no necesita volver a usar este conjunto de verbos, puede enumerar los verbos del elemento primario, pero asegúrese de que el valor Predeterminado del elemento primario esté vacío.</span><span class="sxs-lookup"><span data-stu-id="62676-245">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="62676-246">**Para crear un menú en cascada mediante una entrada ExtendedSubCommandsKey**</span><span class="sxs-lookup"><span data-stu-id="62676-246">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="62676-247">Cree una subclave en el shell **de ProgID \_ \_ raíz de HKEY CLASSES** para representar el menú en \\  \\  cascada.</span><span class="sxs-lookup"><span data-stu-id="62676-247">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="62676-248">En este ejemplo, se le da a esta subclave el nombre *CascadeTest2*.</span><span class="sxs-lookup"><span data-stu-id="62676-248">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="62676-249">Asegúrese de que el valor predeterminado de la subclave *CascadeTest* está vacío y se muestra como **(valor no establecido).**</span><span class="sxs-lookup"><span data-stu-id="62676-249">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="62676-250">A la subclave *CascadeTest,* agregue una entrada DE TIPO MUIVerb de tipo **REG \_ SZ** y asígnele el texto que aparecerá como su nombre en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="62676-250">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="62676-251">En este ejemplo, le asignamos "Test Cascade Menu".</span><span class="sxs-lookup"><span data-stu-id="62676-251">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="62676-252">En la subclave *CascadeTest* que ha creado, agregue una subclave **ExtendedSubCommandsKey** y, a continuación, agregue los subcomandos del documento (del tipo **REG \_ SZ);** por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="62676-252">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    <span data-ttu-id="62676-253">Asegúrese de que el valor predeterminado de la subclave *Test Cascade Menu 2* está vacío y se muestra **como (valor no establecido).**</span><span class="sxs-lookup"><span data-stu-id="62676-253">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="62676-254">Rellene los subverberos mediante cualquiera de las siguientes implementaciones de verbo estático.</span><span class="sxs-lookup"><span data-stu-id="62676-254">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="62676-255">Tenga en cuenta que la subclave CommandFlags representa valores EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="62676-255">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="62676-256">Si desea agregar un separador antes o después del elemento de menú en cascada, use ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="62676-256">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="62676-257">Para obtener una descripción de estas marcas de Windows 7 y versiones posteriores, vea [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="62676-257">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="62676-258">ECF \_ SEPARATORBEFORE solo funciona para los elementos de menú de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="62676-258">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="62676-259">MUIVerb es de tipo **REG \_ SZ** y CommandFlags es de tipo **REG \_ DWORD.**</span><span class="sxs-lookup"><span data-stu-id="62676-259">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

<span data-ttu-id="62676-260">La siguiente captura de pantalla es una ilustración de los ejemplos de entrada de clave del Registro anteriores.</span><span class="sxs-lookup"><span data-stu-id="62676-260">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![captura de pantalla que muestra un ejemplo de un menú en cascada que muestra las opciones del Bloc de notas y el Bloc de palabras](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="62676-262">Crear menús en cascada con la interfaz IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="62676-262">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="62676-263">Otra opción para agregar verbos a un menú en cascada es a través de [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="62676-263">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="62676-264">Este método permite que los orígenes de datos que proporcionan sus comandos de módulo de comandos a través de [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) usen esos comandos como verbos en un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="62676-264">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="62676-265">En Windows 7 y versiones posteriores, puede proporcionar la misma implementación de verbo mediante [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) que con [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="62676-265">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="62676-266">Las dos capturas de pantalla siguientes muestran el uso de menús en cascada en la **carpeta Dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="62676-266">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta devices.](images/file-assoc/filecascademenu.png)

<span data-ttu-id="62676-268">En la siguiente captura de pantalla se muestra otra implementación de un menú en cascada en la **carpeta** Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="62676-268">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta devices](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="62676-270">Dado [**que IExplorerCommand solo**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) admite la activación en proceso, se recomienda su uso por parte de orígenes de datos de Shell que necesitan compartir la implementación entre comandos y menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="62676-270">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="62676-271">Obtención del comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada</span><span class="sxs-lookup"><span data-stu-id="62676-271">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="62676-272">La sintaxis de consulta avanzada (AQS) puede expresar una condición que se evaluará mediante las propiedades del elemento para el que se crea una instancia del verbo.</span><span class="sxs-lookup"><span data-stu-id="62676-272">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="62676-273">Este sistema solo funciona con propiedades rápidas.</span><span class="sxs-lookup"><span data-stu-id="62676-273">This system works only with fast properties.</span></span> <span data-ttu-id="62676-274">Estas son propiedades que el origen de datos del shell notifica como rápidas al no devolver [\*\**SHCOLSTATE \_ SLOW*%](/windows/win32/api/shtypes/ne-shtypes-shcolstate) desde [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span><span class="sxs-lookup"><span data-stu-id="62676-274">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="62676-275">Windows 7 y versiones posteriores admiten valores canónicos que evitan problemas en las compilaciones localizadas.</span><span class="sxs-lookup"><span data-stu-id="62676-275">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="62676-276">La siguiente sintaxis canónica es necesaria en las compilaciones localizadas para aprovechar esta mejora de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="62676-276">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="62676-277">En la siguiente entrada del Registro de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="62676-277">In the following example registry entry:</span></span>

-   <span data-ttu-id="62676-278">El **valor AppliesTo** controla si el verbo se muestra u oculta.</span><span class="sxs-lookup"><span data-stu-id="62676-278">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="62676-279">El valor DefaultAppliesTo controla qué verbo es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="62676-279">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="62676-280">El valor HasLUAShield controla si se muestra un escudo de control de cuentas de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="62676-280">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="62676-281">En este ejemplo, **el valor DefaultAppliesTo** convierte este verbo en el valor predeterminado para cualquier archivo con la palabra "exampleText1" en su nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="62676-281">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="62676-282">El **valor AppliesTo** habilita el verbo para cualquier archivo con "exampleText1" en el nombre.</span><span class="sxs-lookup"><span data-stu-id="62676-282">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="62676-283">El **valor HasLUAShield** muestra el escudo de los archivos con "exampleText2" en el nombre.</span><span class="sxs-lookup"><span data-stu-id="62676-283">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="62676-284">Agregue **la** subclave Command y un valor:</span><span class="sxs-lookup"><span data-stu-id="62676-284">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="62676-285">En el Registro de Windows 7, vea HKEY CLASSES ROOT drive **(Unidad RAÍZ HKEY \_ CLASSES) \_** como ejemplo de \\  verbos de BitLocker que emplean el enfoque siguiente:</span><span class="sxs-lookup"><span data-stu-id="62676-285">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="62676-286">AppliesTo = System.Volume.BitlockerProtection:=2</span><span class="sxs-lookup"><span data-stu-id="62676-286">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="62676-287">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean \# True</span><span class="sxs-lookup"><span data-stu-id="62676-287">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="62676-288">Para obtener más información sobre AQS, vea [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="62676-288">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="62676-289">En desuso: Asociación de verbos Intercambio dinámico de datos comandos</span><span class="sxs-lookup"><span data-stu-id="62676-289">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="62676-290">DDE está en desuso; use [**IDropTarget en su**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) lugar.</span><span class="sxs-lookup"><span data-stu-id="62676-290">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="62676-291">DDE está en desuso porque se basa en un mensaje de ventana de difusión para detectar el servidor DDE.</span><span class="sxs-lookup"><span data-stu-id="62676-291">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="62676-292">Un servidor DDE detiene el mensaje de la ventana de difusión y, por tanto, se detienen las conversaciones de DDE para otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="62676-292">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="62676-293">Es habitual que una sola aplicación bloqueada cause errores posteriores en toda la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="62676-293">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="62676-294">El [**método IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) es más sólido y tiene una mejor compatibilidad con la activación porque usa la activación COM del controlador.</span><span class="sxs-lookup"><span data-stu-id="62676-294">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="62676-295">En el caso de la selección de varios elementos, **IDropTarget** no está sujeto a las restricciones de tamaño de búfer que se encuentran en DDE y [**CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)</span><span class="sxs-lookup"><span data-stu-id="62676-295">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="62676-296">Además, los elementos se pasan a la aplicación como un objeto de datos que se puede convertir en una matriz de elementos mediante la función [**SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)</span><span class="sxs-lookup"><span data-stu-id="62676-296">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="62676-297">Esto es más sencillo y no pierde la información del espacio de nombres como ocurre cuando el elemento se convierte en una ruta de acceso para los protocolos DDE o de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="62676-297">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="62676-298">Para obtener más información sobre [**las consultas IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y Shell para los atributos de asociación de archivos, vea [Perceived Types and Application Registration](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="62676-298">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="62676-299">Completar tareas de implementación de verbos</span><span class="sxs-lookup"><span data-stu-id="62676-299">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="62676-300">Las siguientes tareas para implementar verbos son relevantes para las implementaciones de verbos estáticos y dinámicos.</span><span class="sxs-lookup"><span data-stu-id="62676-300">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="62676-301">Para obtener más información sobre los verbos dinámicos, vea Personalización de un [menú contextual mediante verbos dinámicos.](shortcut-menu-using-dynamic-verbs.md)</span><span class="sxs-lookup"><span data-stu-id="62676-301">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="62676-302">Personalizar el menú contextual para objetos de shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="62676-302">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="62676-303">Muchos objetos predefinidos de Shell tienen menús contextuales que se pueden personalizar.</span><span class="sxs-lookup"><span data-stu-id="62676-303">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="62676-304">Registre el comando de la misma manera que registra los tipos de archivo típicos, pero use el nombre del objeto predefinido como nombre del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="62676-304">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="62676-305">Una lista de objetos predefinidos se encuentra en la *sección Objetos de shell predefinidos* de Crear controladores de extensión de [shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="62676-305">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="62676-306">Los objetos predefinidos de Shell cuyos menús contextuales se pueden personalizar agregando verbos en el Registro se marcan en la tabla con la palabra Verbo.</span><span class="sxs-lookup"><span data-stu-id="62676-306">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="62676-307">Extender un nuevo submenú</span><span class="sxs-lookup"><span data-stu-id="62676-307">Extending a New Submenu</span></span>

<span data-ttu-id="62676-308">Cuando un usuario abre el **menú** Archivo Explorador de Windows, uno de los comandos que se muestran es **Nuevo.**</span><span class="sxs-lookup"><span data-stu-id="62676-308">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="62676-309">Al seleccionar este comando se muestra un submenú.</span><span class="sxs-lookup"><span data-stu-id="62676-309">Selecting this command displays a submenu.</span></span> <span data-ttu-id="62676-310">De forma predeterminada, el submenú contiene dos comandos, **Carpeta** y **Acceso** directo, que permiten a los usuarios crear subcarpetas y accesos directos.</span><span class="sxs-lookup"><span data-stu-id="62676-310">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="62676-311">Este submenú se puede extender para incluir comandos de creación de archivos para cualquier tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="62676-311">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="62676-312">Para agregar un comando de creación de archivos al submenú **Nuevo,** los archivos de la aplicación deben tener un tipo de archivo asociado.</span><span class="sxs-lookup"><span data-stu-id="62676-312">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="62676-313">Incluya una **subclave ShellNew** en el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="62676-313">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="62676-314">Cuando se **selecciona** el comando **Nuevo** del menú Archivo, el shell agrega el tipo de archivo al submenú **Nuevo.**</span><span class="sxs-lookup"><span data-stu-id="62676-314">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="62676-315">La cadena para mostrar del comando es la cadena descriptiva que se asigna al ProgID del programa.</span><span class="sxs-lookup"><span data-stu-id="62676-315">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="62676-316">Para especificar el método de creación de archivos, asigne uno o varios valores de datos a la **subclave ShellNew.**</span><span class="sxs-lookup"><span data-stu-id="62676-316">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="62676-317">Los valores disponibles se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="62676-317">The available values are listed in the following table.</span></span>



| <span data-ttu-id="62676-318">ShellNuevo valor de subclave</span><span class="sxs-lookup"><span data-stu-id="62676-318">ShellNew subkey value</span></span> | <span data-ttu-id="62676-319">Descripción</span><span class="sxs-lookup"><span data-stu-id="62676-319">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62676-320">Comando</span><span class="sxs-lookup"><span data-stu-id="62676-320">Command</span></span>               | <span data-ttu-id="62676-321">Ejecuta una aplicación.</span><span class="sxs-lookup"><span data-stu-id="62676-321">Executes an application.</span></span> <span data-ttu-id="62676-322">Este **valor DE REG \_ SZ** especifica la ruta de acceso de la aplicación que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="62676-322">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="62676-323">Por ejemplo, podría establecerlo para iniciar un asistente.</span><span class="sxs-lookup"><span data-stu-id="62676-323">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="62676-324">data</span><span class="sxs-lookup"><span data-stu-id="62676-324">Data</span></span>                  | <span data-ttu-id="62676-325">Crea un archivo que contiene los datos especificados.</span><span class="sxs-lookup"><span data-stu-id="62676-325">Creates a file containing specified data.</span></span> <span data-ttu-id="62676-326">Este **valor \_ REG BINARY** especifica los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="62676-326">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="62676-327">**Los** datos se omiten **si se especifica NullFile** o **FileName.**</span><span class="sxs-lookup"><span data-stu-id="62676-327">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="62676-328">FileName</span><span class="sxs-lookup"><span data-stu-id="62676-328">FileName</span></span>              | <span data-ttu-id="62676-329">Crea un archivo que es una copia de un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="62676-329">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="62676-330">Este **valor \_ REG SZ** especifica la ruta de acceso completa del archivo que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="62676-330">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="62676-331">NullFile</span><span class="sxs-lookup"><span data-stu-id="62676-331">NullFile</span></span>              | <span data-ttu-id="62676-332">Crea un archivo vacío.</span><span class="sxs-lookup"><span data-stu-id="62676-332">Creates an empty file.</span></span> <span data-ttu-id="62676-333">**NullFile** no tiene ningún valor asignado.</span><span class="sxs-lookup"><span data-stu-id="62676-333">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="62676-334">Si **se especifica NullFile,** se omiten los valores del Registro **Data** y **FileName.**</span><span class="sxs-lookup"><span data-stu-id="62676-334">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="62676-335">En el siguiente ejemplo de clave del Registro y la captura de pantalla se muestra el submenú **Nuevo** para el tipo de archivo .myp-ms.</span><span class="sxs-lookup"><span data-stu-id="62676-335">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="62676-336">Tiene un comando, **MyProgram Application**.</span><span class="sxs-lookup"><span data-stu-id="62676-336">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="62676-337">La captura de pantalla muestra el **submenú Nuevo.**</span><span class="sxs-lookup"><span data-stu-id="62676-337">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="62676-338">Cuando un usuario selecciona **MyProgram Application** en el **submenú** New (Nuevo), shell crea un archivo denominado New **MyProgram Application.myp-ms** y lo pasa a **MyProgram.exe**.</span><span class="sxs-lookup"><span data-stu-id="62676-338">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![captura de pantalla del Explorador de Windows que muestra un nuevo comando "myprogram application" en el submenú "new"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="62676-340">Crear controladores de arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="62676-340">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="62676-341">El procedimiento básico para implementar un controlador de arrastrar y colocar es el mismo que para los controladores de menús contextuales convencionales.</span><span class="sxs-lookup"><span data-stu-id="62676-341">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="62676-342">Sin embargo, los controladores de menús contextuales normalmente solo usan el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pasado al método [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del controlador para extraer el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="62676-342">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="62676-343">Un controlador de arrastrar y colocar podría implementar un controlador de datos más sofisticado para modificar el comportamiento del objeto arrastrado.</span><span class="sxs-lookup"><span data-stu-id="62676-343">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="62676-344">Cuando un usuario hace clic con el botón derecho en un objeto shell para arrastrar un objeto, se muestra un menú contextual cuando el usuario intenta colocar el objeto.</span><span class="sxs-lookup"><span data-stu-id="62676-344">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="62676-345">En la siguiente captura de pantalla se muestra un menú contextual típico de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="62676-345">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![captura de pantalla del menú contextual de arrastrar y colocar](images/context-menu/context-dragdrop.png)

<span data-ttu-id="62676-347">Un controlador de arrastrar y colocar es un controlador de menú contextual que puede agregar elementos a este menú contextual.</span><span class="sxs-lookup"><span data-stu-id="62676-347">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="62676-348">Los controladores de arrastrar y colocar normalmente se registran en la subclave siguiente.</span><span class="sxs-lookup"><span data-stu-id="62676-348">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="62676-349">Agregue una subclave bajo la subclave **DragDropHandlers** denominada para el controlador de arrastrar y colocar y establezca el valor predeterminado de la subclave en el formato de cadena del GUID del identificador de clase (CLSID) del controlador.</span><span class="sxs-lookup"><span data-stu-id="62676-349">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="62676-350">En el ejemplo siguiente se habilita el controlador de arrastrar y colocar **MyDD.**</span><span class="sxs-lookup"><span data-stu-id="62676-350">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="62676-351">Suprimir verbos y controlar la visibilidad</span><span class="sxs-lookup"><span data-stu-id="62676-351">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="62676-352">Puede usar la configuración de directivas de Windows para controlar la visibilidad de verbos.</span><span class="sxs-lookup"><span data-stu-id="62676-352">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="62676-353">Los verbos se pueden suprimir mediante la configuración de directiva agregando un valor **SuppressionPolicy** o un valor GUID **SuppressionPolicyEx** a la subclave del Registro del verbo.</span><span class="sxs-lookup"><span data-stu-id="62676-353">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="62676-354">Establezca el valor de la subclave **SuppressionPolicy** en el identificador de directiva.</span><span class="sxs-lookup"><span data-stu-id="62676-354">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="62676-355">Si la directiva está activada, se suprimen el verbo y su entrada de menú contextual asociada.</span><span class="sxs-lookup"><span data-stu-id="62676-355">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="62676-356">Para ver los posibles valores de identificador de directiva, consulte la [**enumeración RESTRICTIONS.**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions)</span><span class="sxs-lookup"><span data-stu-id="62676-356">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="62676-357">Empleo del modelo de selección de verbos</span><span class="sxs-lookup"><span data-stu-id="62676-357">Employing the Verb Selection Model</span></span>

<span data-ttu-id="62676-358">Los valores del Registro deben establecerse para que los verbos controle situaciones en las que un usuario puede seleccionar un solo elemento, varios elementos o una selección de un elemento.</span><span class="sxs-lookup"><span data-stu-id="62676-358">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="62676-359">Un verbo requiere valores del Registro independientes para cada una de estas tres situaciones que admite el verbo.</span><span class="sxs-lookup"><span data-stu-id="62676-359">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="62676-360">Los valores posibles para el modelo de selección de verbos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="62676-360">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="62676-361">Especifique el valor MultiSelectModel para todos los verbos.</span><span class="sxs-lookup"><span data-stu-id="62676-361">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="62676-362">Si no se especifica el valor MultiSelectModel, se deduce del tipo de implementación de verbo que ha elegido.</span><span class="sxs-lookup"><span data-stu-id="62676-362">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="62676-363">En el caso de los métodos basados en COM (como DropTarget y **ExecuteCommand),** se da por supuesto el reproductor y, para los demás métodos, se supone que **Document.**</span><span class="sxs-lookup"><span data-stu-id="62676-363">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="62676-364">Especifique **Single** para los verbos que solo admiten una selección única.</span><span class="sxs-lookup"><span data-stu-id="62676-364">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="62676-365">Especifique **Player** para los verbos que admiten cualquier número de elementos.</span><span class="sxs-lookup"><span data-stu-id="62676-365">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="62676-366">Especifique **Document** para los verbos que crean una ventana de nivel superior para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="62676-366">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="62676-367">Esto limita el número de elementos activados y ayuda a evitar que se quedándose sin recursos del sistema si el usuario abre demasiadas ventanas.</span><span class="sxs-lookup"><span data-stu-id="62676-367">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="62676-368">Cuando el número de elementos seleccionados no coincide con el modelo de selección de verbos o es mayor que los límites predeterminados descritos en la tabla siguiente, el verbo no aparece.</span><span class="sxs-lookup"><span data-stu-id="62676-368">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="62676-369">Tipo de implementación de verbo</span><span class="sxs-lookup"><span data-stu-id="62676-369">Type of verb implementation</span></span> | <span data-ttu-id="62676-370">Documento</span><span class="sxs-lookup"><span data-stu-id="62676-370">Document</span></span> | <span data-ttu-id="62676-371">Reproductor</span><span class="sxs-lookup"><span data-stu-id="62676-371">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="62676-372">Heredado</span><span class="sxs-lookup"><span data-stu-id="62676-372">Legacy</span></span>                      | <span data-ttu-id="62676-373">15 elementos</span><span class="sxs-lookup"><span data-stu-id="62676-373">15 items</span></span> | <span data-ttu-id="62676-374">100 elementos</span><span class="sxs-lookup"><span data-stu-id="62676-374">100 items</span></span> |
| <span data-ttu-id="62676-375">COM</span><span class="sxs-lookup"><span data-stu-id="62676-375">COM</span></span>                         | <span data-ttu-id="62676-376">15 elementos</span><span class="sxs-lookup"><span data-stu-id="62676-376">15 items</span></span> | <span data-ttu-id="62676-377">Sin límite</span><span class="sxs-lookup"><span data-stu-id="62676-377">No limit</span></span>  |



 

<span data-ttu-id="62676-378">A continuación se incluyen entradas del Registro de ejemplo que usan el valor MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="62676-378">The following are example registry entries using the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a><span data-ttu-id="62676-379">Usar atributos de elemento</span><span class="sxs-lookup"><span data-stu-id="62676-379">Using Item Attributes</span></span>

<span data-ttu-id="62676-380">Los [**valores de marca SFGAO**](sfgao.md) de los atributos de Shell para un elemento se pueden probar para determinar si el verbo debe habilitarse o deshabilitarse.</span><span class="sxs-lookup"><span data-stu-id="62676-380">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="62676-381">Para usar esta característica de atributo, agregue los siguientes valores **REG \_ DWORD** en el verbo :</span><span class="sxs-lookup"><span data-stu-id="62676-381">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="62676-382">El valor attributeMask especifica el valor [**SFGAO**](sfgao.md) de los valores de bits de la máscara con la que se probará.</span><span class="sxs-lookup"><span data-stu-id="62676-382">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="62676-383">El valor AttributeValue especifica el valor [**SFGAO**](sfgao.md) de los bits que se prueban.</span><span class="sxs-lookup"><span data-stu-id="62676-383">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="62676-384">ImpliedSelectionModel especifica cero para verbos de elemento o distinto de cero para verbos en el menú contextual de fondo.</span><span class="sxs-lookup"><span data-stu-id="62676-384">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="62676-385">En la siguiente entrada del Registro de ejemplo, AttributeMask se establece en [**SFGAO \_ READONLY**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="62676-385">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="62676-386">Implementar verbos personalizados para carpetas mediante Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="62676-386">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="62676-387">En Windows 7 y versiones posteriores, puede agregar verbos a una carpeta mediante Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="62676-387">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="62676-388">Para obtener más información sobre Desktop.ini, [vea How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="62676-388">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="62676-389">Desktop.ini archivos deben marcarse siempre como **Sistema** oculto para que no se  +   muestren a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="62676-389">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="62676-390">**Para agregar verbos personalizados para carpetas mediante un Desktop.ini, realice los pasos siguientes:**</span><span class="sxs-lookup"><span data-stu-id="62676-390">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="62676-391">Cree una carpeta que esté marcada como **De solo lectura** o **Sistema.**</span><span class="sxs-lookup"><span data-stu-id="62676-391">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="62676-392">Cree un Desktop.ini que incluya \[ un . ShellClassInfo \] DirectoryClass=Folder ProgID.</span><span class="sxs-lookup"><span data-stu-id="62676-392">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="62676-393">En el Registro, cree **HKEY \_ CLASSES \_ ROOT** \\ **Folder ProgID** con un valor de CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="62676-393">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="62676-394">El valor CanUseForDirectory evita el uso incorrecto de progID que se establecen para no participar en la implementación de verbos personalizados para carpetas a través de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="62676-394">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="62676-395">Agregue verbos en la **subclave Folder** ProgID, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="62676-395">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="62676-396">Estos verbos pueden ser el verbo predeterminado, en cuyo caso hacer doble clic en la carpeta activa el verbo.</span><span class="sxs-lookup"><span data-stu-id="62676-396">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="62676-397">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62676-397">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62676-398">Procedimientos recomendados para controladores de menús contextuales y verbos de selección múltiple</span><span class="sxs-lookup"><span data-stu-id="62676-398">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="62676-399">Elegir un verbo estático o dinámico para el menú contextual</span><span class="sxs-lookup"><span data-stu-id="62676-399">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="62676-400">Personalizar un menú contextual mediante verbos dinámicos</span><span class="sxs-lookup"><span data-stu-id="62676-400">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="62676-401">Menús contextuales y controladores de menús contextuales</span><span class="sxs-lookup"><span data-stu-id="62676-401">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="62676-402">Verbos y asociaciones de archivo</span><span class="sxs-lookup"><span data-stu-id="62676-402">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="62676-403">Referencia del menú contextual</span><span class="sxs-lookup"><span data-stu-id="62676-403">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
