---
description: Los controladores de menú contextual, también denominados controladores de menú contextual o de verbo, son un tipo de controlador de tipo de archivo. Como todos estos controladores, se trata de objetos de modelo de objetos componentes (COM) implementados como dll.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Crear controladores de menú contextual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b7091483726c322a8ae18bace883af126d404
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "103913926"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="076f8-104">Crear controladores de menú contextual</span><span class="sxs-lookup"><span data-stu-id="076f8-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="076f8-105">Los controladores de menú contextual, también denominados controladores de menú contextual o de verbo, son un tipo de controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="076f8-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="076f8-106">Como todos estos controladores, se trata de objetos de modelo de objetos componentes (COM) implementados como dll.</span><span class="sxs-lookup"><span data-stu-id="076f8-106">Like all such handlers, they are in-process Component Object Model (COM) objects implemented as DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="076f8-107">Existen consideraciones especiales para Windows de 64 bits al registrar controladores que funcionan en el contexto de las aplicaciones de 32 bits: cuando los verbos de Shell se invocan en el contexto de una aplicación de 32 bits, el subsistema WOW64 redirige el acceso del sistema de archivos a algunas rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="076f8-107">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="076f8-108">Si el controlador. exe se almacena en una de esas rutas de acceso, no es accesible en este contexto.</span><span class="sxs-lookup"><span data-stu-id="076f8-108">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="076f8-109">Por lo tanto, como solución alternativa, almacene el archivo. exe en una ruta de acceso que no se redirija, o bien almacene una versión de código auxiliar del archivo. exe que inicia la versión real.</span><span class="sxs-lookup"><span data-stu-id="076f8-109">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

<span data-ttu-id="076f8-110">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="076f8-110">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="076f8-111">Verbos canónicos</span><span class="sxs-lookup"><span data-stu-id="076f8-111">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="076f8-112">Verbos extendidos</span><span class="sxs-lookup"><span data-stu-id="076f8-112">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="076f8-113">Personalizar un menú contextual mediante verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="076f8-113">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="076f8-114">Activar el controlador mediante la interfaz IDropTarget</span><span class="sxs-lookup"><span data-stu-id="076f8-114">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="076f8-115">Especificar la posición y el orden de los verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="076f8-115">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="076f8-116">Colocar verbos en la parte superior o inferior del menú</span><span class="sxs-lookup"><span data-stu-id="076f8-116">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="076f8-117">Crear menús en cascada estáticos</span><span class="sxs-lookup"><span data-stu-id="076f8-117">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="076f8-118">Obtener el comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada</span><span class="sxs-lookup"><span data-stu-id="076f8-118">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="076f8-119">En desuso: asociar verbos con comandos de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="076f8-119">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="076f8-120">Completar tareas de implementación de verbo</span><span class="sxs-lookup"><span data-stu-id="076f8-120">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="076f8-121">Personalización del menú contextual para objetos de Shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="076f8-121">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="076f8-122">Extender un nuevo submenú</span><span class="sxs-lookup"><span data-stu-id="076f8-122">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="076f8-123">Suprimir verbos y controlar la visibilidad</span><span class="sxs-lookup"><span data-stu-id="076f8-123">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="076f8-124">Usar el modelo de selección de verbos</span><span class="sxs-lookup"><span data-stu-id="076f8-124">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="076f8-125">Usar atributos de elemento</span><span class="sxs-lookup"><span data-stu-id="076f8-125">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="076f8-126">Implementar verbos personalizados para carpetas a través de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="076f8-126">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="076f8-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="076f8-127">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="076f8-128">Verbos canónicos</span><span class="sxs-lookup"><span data-stu-id="076f8-128">Canonical Verbs</span></span>

<span data-ttu-id="076f8-129">Las aplicaciones suelen ser responsables de proporcionar cadenas de presentación localizadas para los verbos que definen.</span><span class="sxs-lookup"><span data-stu-id="076f8-129">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="076f8-130">Sin embargo, para proporcionar un grado de independencia de lenguaje, el sistema define un conjunto estándar de verbos usados comúnmente denominados verbos canónicos.</span><span class="sxs-lookup"><span data-stu-id="076f8-130">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="076f8-131">Un verbo canónico nunca se muestra al usuario y se puede usar con cualquier idioma de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="076f8-131">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="076f8-132">El sistema utiliza el nombre canónico para generar automáticamente una cadena de presentación localizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="076f8-132">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="076f8-133">Por ejemplo, la cadena de presentación del verbo abierto está establecida en **abierto** en un sistema en inglés y en el equivalente en alemán en un sistema alemán.</span><span class="sxs-lookup"><span data-stu-id="076f8-133">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>



| <span data-ttu-id="076f8-134">Verbo canónico</span><span class="sxs-lookup"><span data-stu-id="076f8-134">Canonical verb</span></span> | <span data-ttu-id="076f8-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="076f8-135">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="076f8-136">Abrir</span><span class="sxs-lookup"><span data-stu-id="076f8-136">Open</span></span>           | <span data-ttu-id="076f8-137">Abre el archivo o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="076f8-137">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="076f8-138">Opennew</span><span class="sxs-lookup"><span data-stu-id="076f8-138">Opennew</span></span>        | <span data-ttu-id="076f8-139">Abre el archivo o la carpeta en una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="076f8-139">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="076f8-140">Impresión</span><span class="sxs-lookup"><span data-stu-id="076f8-140">Print</span></span>          | <span data-ttu-id="076f8-141">Imprime el archivo.</span><span class="sxs-lookup"><span data-stu-id="076f8-141">Prints the file.</span></span>                                                     |
| <span data-ttu-id="076f8-142">Imprimir en</span><span class="sxs-lookup"><span data-stu-id="076f8-142">Printto</span></span>        | <span data-ttu-id="076f8-143">Permite al usuario imprimir un archivo arrastrándolo a un objeto de impresora.</span><span class="sxs-lookup"><span data-stu-id="076f8-143">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="076f8-144">Explorar</span><span class="sxs-lookup"><span data-stu-id="076f8-144">Explore</span></span>        | <span data-ttu-id="076f8-145">Abre el explorador de Windows con la carpeta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="076f8-145">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="076f8-146">Propiedades</span><span class="sxs-lookup"><span data-stu-id="076f8-146">Properties</span></span>     | <span data-ttu-id="076f8-147">Abre la hoja de propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="076f8-147">Opens the object's property sheet.</span></span>                                   |



 

> [!Note]  
> <span data-ttu-id="076f8-148">El verbo **printto** también es canónico, pero nunca se muestra.</span><span class="sxs-lookup"><span data-stu-id="076f8-148">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="076f8-149">Su inclusión permite al usuario imprimir un archivo arrastrándolo a un objeto de impresora.</span><span class="sxs-lookup"><span data-stu-id="076f8-149">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

 

<span data-ttu-id="076f8-150">Los controladores de menú contextual pueden proporcionar sus propios verbos canónicos a través de [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) con **GC \_ VERBW** o de los **catálogos globales \_**.</span><span class="sxs-lookup"><span data-stu-id="076f8-150">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="076f8-151">El sistema usará los verbos canónicos como el segundo parámetro (*lpOperation*) pasado a [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)y es [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). miembro **lpVerb** pasado al método [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="076f8-151">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="076f8-152">Verbos extendidos</span><span class="sxs-lookup"><span data-stu-id="076f8-152">Extended Verbs</span></span>

<span data-ttu-id="076f8-153">Cuando el usuario hace clic con el botón secundario en un objeto, el menú contextual muestra los verbos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="076f8-153">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="076f8-154">Es posible que desee agregar y admitir comandos en algunos menús contextuales que no se muestran en todos los menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="076f8-154">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="076f8-155">Por ejemplo, podría tener comandos que no se usan habitualmente o que están destinados a usuarios con experiencia.</span><span class="sxs-lookup"><span data-stu-id="076f8-155">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="076f8-156">Por esta razón, también puede definir uno o más verbos extendidos.</span><span class="sxs-lookup"><span data-stu-id="076f8-156">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="076f8-157">Estos verbos son similares a los verbos normales, pero se distinguen de los verbos normales por la forma en que se registran.</span><span class="sxs-lookup"><span data-stu-id="076f8-157">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="076f8-158">Para tener acceso a los verbos extendidos, el usuario debe hacer clic con el botón derecho en un objeto mientras presiona la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="076f8-158">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="076f8-159">Cuando el usuario lo hace, se muestran los verbos extendidos además de los verbos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="076f8-159">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="076f8-160">Puede utilizar el registro para definir uno o más verbos extendidos.</span><span class="sxs-lookup"><span data-stu-id="076f8-160">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="076f8-161">Los comandos asociados solo se mostrarán cuando el usuario haga clic con el botón derecho en un objeto y presione la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="076f8-161">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="076f8-162">Para definir un verbo como extendido, agregue un valor de **reg \_ SZ** "extendido" a la subclave del verbo.</span><span class="sxs-lookup"><span data-stu-id="076f8-162">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="076f8-163">El valor no debe tener ningún dato asociado.</span><span class="sxs-lookup"><span data-stu-id="076f8-163">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="076f8-164">Personalizar un menú contextual mediante verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="076f8-164">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="076f8-165">Después de [elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md) , puede extender el menú contextual de un tipo de archivo registrando un verbo estático para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="076f8-165">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="076f8-166">Para ello, agregue una subclave de **Shell** debajo de la subclave para el identificador de programa de la aplicación asociada al tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="076f8-166">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="076f8-167">Opcionalmente, puede definir un verbo predeterminado para el tipo de archivo convirtiéndolo en el valor predeterminado de la subclave del **Shell** .</span><span class="sxs-lookup"><span data-stu-id="076f8-167">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="076f8-168">En primer lugar, se muestra el verbo predeterminado en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="076f8-168">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="076f8-169">Su finalidad es proporcionar el shell con un verbo que se puede usar cuando se llama a la función [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) , pero no se especifica ningún verbo.</span><span class="sxs-lookup"><span data-stu-id="076f8-169">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="076f8-170">El shell no selecciona necesariamente el verbo predeterminado cuando se usa **ShellExecuteEx** de este modo.</span><span class="sxs-lookup"><span data-stu-id="076f8-170">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="076f8-171">El shell usa el primer verbo disponible en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="076f8-171">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="076f8-172">El verbo predeterminado</span><span class="sxs-lookup"><span data-stu-id="076f8-172">The default verb</span></span>
2.  <span data-ttu-id="076f8-173">Primer verbo del registro, si se especifica el orden del verbo</span><span class="sxs-lookup"><span data-stu-id="076f8-173">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="076f8-174">El verbo **Open**</span><span class="sxs-lookup"><span data-stu-id="076f8-174">The **Open** verb</span></span>
4.  <span data-ttu-id="076f8-175">El verbo **Open with**</span><span class="sxs-lookup"><span data-stu-id="076f8-175">The **Open With** verb</span></span>

<span data-ttu-id="076f8-176">Si ninguno de los verbos enumerados está disponible, se produce un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="076f8-176">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="076f8-177">Cree una subclave para cada verbo que desee agregar bajo la subclave del shell.</span><span class="sxs-lookup"><span data-stu-id="076f8-177">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="076f8-178">Cada una de estas subclaves debe tener un valor de **reg \_ SZ** establecido en la cadena de presentación del verbo (cadena localizada).</span><span class="sxs-lookup"><span data-stu-id="076f8-178">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="076f8-179">Para cada subclave de verbo, cree una subclave de comando con el valor predeterminado establecido en la línea de comandos para activar los elementos.</span><span class="sxs-lookup"><span data-stu-id="076f8-179">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="076f8-180">En el caso de los verbos canónicos, como **abrir** e **Imprimir**, puede omitir la cadena de presentación, ya que el sistema muestra automáticamente una cadena localizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="076f8-180">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="076f8-181">En el caso de verbos no canónicos, si se omite la cadena de presentación, se muestra la cadena de verbo.</span><span class="sxs-lookup"><span data-stu-id="076f8-181">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="076f8-182">En el siguiente ejemplo del registro, tenga en cuenta que:</span><span class="sxs-lookup"><span data-stu-id="076f8-182">In the following registry example, note that:</span></span>

-   <span data-ttu-id="076f8-183">Dado que **doit** no es un verbo canónico, se le asigna un nombre para mostrar, que se puede seleccionar presionando la tecla D.</span><span class="sxs-lookup"><span data-stu-id="076f8-183">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="076f8-184">El verbo **printto** no aparece en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="076f8-184">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="076f8-185">Sin embargo, su inclusión en el registro permite al usuario imprimir archivos colocándolos en un icono de impresora.</span><span class="sxs-lookup"><span data-stu-id="076f8-185">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="076f8-186">Se muestra una subclave para cada verbo.</span><span class="sxs-lookup"><span data-stu-id="076f8-186">One subkey is shown for each verb.</span></span> <span data-ttu-id="076f8-187">**%1** representa el nombre de archivo y **%2** el nombre de la impresora.</span><span class="sxs-lookup"><span data-stu-id="076f8-187">**%1** represents the file name and **%2** the printer name.</span></span>

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

<span data-ttu-id="076f8-188">En el diagrama siguiente se muestra la extensión del menú contextual de acuerdo con las entradas del registro anteriores.</span><span class="sxs-lookup"><span data-stu-id="076f8-188">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="076f8-189">Este menú contextual tiene los verbos **abrir**, **hacer** e **Imprimir** en su menú, con lo que lo **hace** como el verbo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="076f8-189">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![captura de pantalla del menú contextual del verbo predeterminado](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="076f8-191">Activar el controlador mediante la interfaz IDropTarget</span><span class="sxs-lookup"><span data-stu-id="076f8-191">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="076f8-192">Intercambio dinámico de datos (DDE) está en desuso; en su lugar, use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="076f8-192">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="076f8-193">**IDropTarget** es más robusto y tiene una mejor compatibilidad con la activación porque utiliza la activación com del controlador.</span><span class="sxs-lookup"><span data-stu-id="076f8-193">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="076f8-194">En el caso de la selección de varios elementos, **IDropTarget** no está sujeto a las restricciones de tamaño de búfer que se encuentran en DDE y en [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="076f8-194">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="076f8-195">Además, los elementos se pasan a la aplicación como un objeto de datos que se puede convertir en una matriz de elementos mediante la función [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="076f8-195">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="076f8-196">Hacerlo es más sencillo y no pierde información de espacio de nombres como ocurre cuando el elemento se convierte en una ruta de acceso para los protocolos de línea de comandos o DDE.</span><span class="sxs-lookup"><span data-stu-id="076f8-196">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="076f8-197">Para obtener más información sobre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y las consultas de Shell para los atributos de Asociación de archivos, consulte [tipos percibidos y registro de aplicaciones](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="076f8-197">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="076f8-198">Especificar la posición y el orden de los verbos estáticos</span><span class="sxs-lookup"><span data-stu-id="076f8-198">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="076f8-199">Normalmente, los verbos se ordenan en un menú contextual en función de cómo se enumeran; la enumeración se basa primero en el orden de la matriz de asociación y, a continuación, en el orden de los elementos de la matriz de asociación, tal y como se define en el criterio de ordenación del registro.</span><span class="sxs-lookup"><span data-stu-id="076f8-199">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="076f8-200">Los verbos se pueden ordenar especificando el valor predeterminado de la subclave de Shell para la entrada de asociación.</span><span class="sxs-lookup"><span data-stu-id="076f8-200">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="076f8-201">Este valor predeterminado puede incluir un solo elemento, que se mostrará en la parte superior del menú contextual, o una lista de elementos separados por espacios o comas.</span><span class="sxs-lookup"><span data-stu-id="076f8-201">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="076f8-202">En el último caso, el primer elemento de la lista es el elemento predeterminado y los demás verbos se muestran inmediatamente debajo de él en el orden especificado.</span><span class="sxs-lookup"><span data-stu-id="076f8-202">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="076f8-203">Por ejemplo, la siguiente entrada del registro genera verbos de menú contextual en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="076f8-203">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="076f8-204">Pantalla</span><span class="sxs-lookup"><span data-stu-id="076f8-204">Display</span></span>
2.  <span data-ttu-id="076f8-205">Gadgets</span><span class="sxs-lookup"><span data-stu-id="076f8-205">Gadgets</span></span>
3.  <span data-ttu-id="076f8-206">Personalización</span><span class="sxs-lookup"><span data-stu-id="076f8-206">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="076f8-207">Del mismo modo, la siguiente entrada del registro genera verbos de menú contextual en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="076f8-207">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="076f8-208">Personalización</span><span class="sxs-lookup"><span data-stu-id="076f8-208">Personalization</span></span>
2.  <span data-ttu-id="076f8-209">Gadgets</span><span class="sxs-lookup"><span data-stu-id="076f8-209">Gadgets</span></span>
3.  <span data-ttu-id="076f8-210">Pantalla</span><span class="sxs-lookup"><span data-stu-id="076f8-210">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="076f8-211">Colocar verbos en la parte superior o inferior del menú</span><span class="sxs-lookup"><span data-stu-id="076f8-211">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="076f8-212">El siguiente atributo del registro se puede usar para colocar un verbo en la parte superior o inferior del menú.</span><span class="sxs-lookup"><span data-stu-id="076f8-212">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="076f8-213">Si hay varios verbos que especifican este atributo, el último de ellos obtiene la prioridad:</span><span class="sxs-lookup"><span data-stu-id="076f8-213">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="076f8-214">Crear menús en cascada estáticos</span><span class="sxs-lookup"><span data-stu-id="076f8-214">Creating Static Cascading Menus</span></span>

<span data-ttu-id="076f8-215">En Windows 7 y versiones posteriores, la implementación de menús en cascada se admite a través de la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="076f8-215">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="076f8-216">Antes de Windows 7, la creación de menús en cascada solo era posible a través de la implementación de la interfaz [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="076f8-216">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="076f8-217">En Windows 7 y versiones posteriores, debe recurrir a las soluciones basadas en código COM solo cuando los métodos estáticos no sean suficientes.</span><span class="sxs-lookup"><span data-stu-id="076f8-217">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="076f8-218">La siguiente captura de pantalla proporciona un ejemplo de un menú en cascada.</span><span class="sxs-lookup"><span data-stu-id="076f8-218">The following screen shot provides an example of a cascading menu.</span></span>

![captura de pantalla que muestra un ejemplo de un menú en cascada](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="076f8-220">En Windows 7 y versiones posteriores, hay tres maneras de crear menús en cascada:</span><span class="sxs-lookup"><span data-stu-id="076f8-220">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="076f8-221">Crear menús en cascada con la entrada del registro subcomandos</span><span class="sxs-lookup"><span data-stu-id="076f8-221">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="076f8-222">Crear menús en cascada con la entrada del registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="076f8-222">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="076f8-223">Crear menús en cascada con la interfaz IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="076f8-223">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="076f8-224">Crear menús en cascada con la entrada del registro subcomandos</span><span class="sxs-lookup"><span data-stu-id="076f8-224">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="076f8-225">En Windows 7 y versiones posteriores, puede usar la entrada subcomandos para crear menús en cascada mediante el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="076f8-225">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="076f8-226">**Para crear un menú en cascada mediante la entrada subcomandos**</span><span class="sxs-lookup"><span data-stu-id="076f8-226">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="076f8-227">Cree una subclave en **HKEY \_ classes \_ raíz** \\ *ProgID* \\ **Shell** para representar el menú en cascada.</span><span class="sxs-lookup"><span data-stu-id="076f8-227">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="076f8-228">En este ejemplo, se asigna a esta subclave el nombre *CascadeTest*.</span><span class="sxs-lookup"><span data-stu-id="076f8-228">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="076f8-229">Asegúrese de que el valor predeterminado de la subclave *CascadeTest* esté vacío y se muestre como **(valor no establecido)**.</span><span class="sxs-lookup"><span data-stu-id="076f8-229">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="076f8-230">En la subclave *CascadeTest* , agregue una entrada MUIVerb de tipo **reg \_ SZ** y asígnele el texto que aparecerá como su nombre en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="076f8-230">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="076f8-231">En este ejemplo, lo asignaremos "menú en cascada de prueba".</span><span class="sxs-lookup"><span data-stu-id="076f8-231">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="076f8-232">En la subclave *CascadeTest* , agregue una entrada subcomandos de tipo **reg \_ SZ** que tenga asignada la lista, demlimited mediante punto y coma, de los verbos que deben aparecer en el menú, en el orden de aparición.</span><span class="sxs-lookup"><span data-stu-id="076f8-232">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="076f8-233">Por ejemplo, aquí se asigna un número de verbos proporcionados por el sistema:</span><span class="sxs-lookup"><span data-stu-id="076f8-233">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="076f8-234">En el caso de los verbos personalizados, se implementan mediante cualquiera de los métodos de implementación de verbos estáticos y se enumeran en la subclave **CommandStore** , tal como se muestra en este ejemplo para un verbo ficticio *VerbName*:</span><span class="sxs-lookup"><span data-stu-id="076f8-234">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

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
> <span data-ttu-id="076f8-235">Este método tiene la ventaja de que los verbos personalizados se pueden registrar una vez y reutilizarlos enumerando el nombre del verbo en la entrada subcomandos.</span><span class="sxs-lookup"><span data-stu-id="076f8-235">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="076f8-236">Sin embargo, requiere que la aplicación tenga permiso para modificar el registro en **el \_ \_ equipo local HKEY**.</span><span class="sxs-lookup"><span data-stu-id="076f8-236">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="076f8-237">Crear menús en cascada con la entrada del registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="076f8-237">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="076f8-238">En Windows 7 y versiones posteriores, puede usar la entrada ExtendedSubCommandKey para crear menús en cascada extendida: menús en cascada en menús en cascada.</span><span class="sxs-lookup"><span data-stu-id="076f8-238">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="076f8-239">La siguiente captura de pantalla es un ejemplo de un menú en cascada extendido.</span><span class="sxs-lookup"><span data-stu-id="076f8-239">The following screen shot is an example of an extended cascading menu.</span></span>

![captura de pantalla que muestra el menú en cascada ampliado para dispositivos](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="076f8-241">Dado que la **\_ \_ raíz de las clases HKEY** es una combinación de **HKEY \_ Current \_ User** y **HKEY \_ local \_ Machine**, puede registrar verbos personalizados en la subclave de clases de software de **\_ \_ usuario actual de HKEY** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="076f8-241">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="076f8-242">La principal ventaja de hacerlo es que el permiso elevado no es necesario.</span><span class="sxs-lookup"><span data-stu-id="076f8-242">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="076f8-243">Además, otras asociaciones de archivo pueden volver a usar todo el conjunto de verbos especificando la misma subclave ExtendedSubCommandsKey.</span><span class="sxs-lookup"><span data-stu-id="076f8-243">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="076f8-244">Si no necesita volver a usar este conjunto de verbos, puede enumerar los verbos en el elemento primario, pero asegúrese de que el valor predeterminado del elemento primario está vacío.</span><span class="sxs-lookup"><span data-stu-id="076f8-244">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="076f8-245">**Para crear un menú en cascada mediante una entrada ExtendedSubCommandsKey**</span><span class="sxs-lookup"><span data-stu-id="076f8-245">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="076f8-246">Cree una subclave en **HKEY \_ classes \_ raíz** \\ *ProgID* \\ **Shell** para representar el menú en cascada.</span><span class="sxs-lookup"><span data-stu-id="076f8-246">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="076f8-247">En este ejemplo, se asigna a esta subclave el nombre *CascadeTest2*.</span><span class="sxs-lookup"><span data-stu-id="076f8-247">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="076f8-248">Asegúrese de que el valor predeterminado de la subclave *CascadeTest* esté vacío y se muestre como **(valor no establecido)**.</span><span class="sxs-lookup"><span data-stu-id="076f8-248">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="076f8-249">En la subclave *CascadeTest* , agregue una entrada MUIVerb de tipo **reg \_ SZ** y asígnele el texto que aparecerá como su nombre en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="076f8-249">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="076f8-250">En este ejemplo, lo asignaremos "menú en cascada de prueba".</span><span class="sxs-lookup"><span data-stu-id="076f8-250">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="076f8-251">En la subclave *CascadeTest* que ha creado, agregue una subclave **ExtendedSubCommandsKey** y, a continuación, agregue los subcomandos de documento (of **reg \_ SZ** Type); por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="076f8-251">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

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

    <span data-ttu-id="076f8-252">Asegúrese de que el valor predeterminado de la subclave *Test Cascade Menu 2* esté vacío y se muestre como **(valor no establecido)**.</span><span class="sxs-lookup"><span data-stu-id="076f8-252">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="076f8-253">Rellene los subverbos utilizando cualquiera de las siguientes implementaciones de verbo estático.</span><span class="sxs-lookup"><span data-stu-id="076f8-253">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="076f8-254">Tenga en cuenta que la subclave CommandFlags representa los valores de EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="076f8-254">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="076f8-255">Si desea agregar un separador antes o después del elemento de menú en cascada, use ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="076f8-255">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="076f8-256">Para obtener una descripción de estas marcas de Windows 7 y versiones posteriores, vea [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="076f8-256">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="076f8-257">ECF \_ SEPARATORBEFORE solo funciona para los elementos de menú de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="076f8-257">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="076f8-258">MUIVerb es de tipo **reg \_ SZ** y CommandFlags es de tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="076f8-258">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

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

<span data-ttu-id="076f8-259">La siguiente captura de pantalla es una ilustración de los ejemplos anteriores de entradas de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="076f8-259">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![captura de pantalla que muestra un ejemplo de un menú en cascada con opciones de Bloc de notas y WordPad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="076f8-261">Crear menús en cascada con la interfaz IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="076f8-261">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="076f8-262">Otra opción para agregar verbos a un menú en cascada es a través de [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="076f8-262">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="076f8-263">Este método habilita los orígenes de datos que proporcionan los comandos del módulo de comandos a través de [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) para usar esos comandos como verbos en un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="076f8-263">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="076f8-264">En Windows 7 y versiones posteriores, puede proporcionar la misma implementación de verbo mediante [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) como se puede hacer con [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="076f8-264">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="076f8-265">En las dos capturas de pantalla siguientes se muestra el uso de menús en cascada en la carpeta **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="076f8-265">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta dispositivos.](images/file-assoc/filecascademenu.png)

<span data-ttu-id="076f8-267">En la captura de pantalla siguiente se muestra otra implementación de un menú en cascada en la carpeta **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="076f8-267">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta dispositivos](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="076f8-269">Dado que [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) solo admite la activación en proceso, se recomienda para su uso por parte de los orígenes de datos de Shell que necesitan compartir la implementación entre los comandos y los menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="076f8-269">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="076f8-270">Obtener el comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada</span><span class="sxs-lookup"><span data-stu-id="076f8-270">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="076f8-271">La sintaxis de consulta avanzada (AQS) puede expresar una condición que se evaluará mediante las propiedades del elemento para el que se crea una instancia del verbo.</span><span class="sxs-lookup"><span data-stu-id="076f8-271">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="076f8-272">Este sistema solo funciona con propiedades rápidas.</span><span class="sxs-lookup"><span data-stu-id="076f8-272">This system works only with fast properties.</span></span> <span data-ttu-id="076f8-273">Estas son las propiedades que el origen de datos de Shell informa de forma rápida al no devolver [\* \* \* \* SHCOLSTATE \_ Slow \* \* \*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) \* de [**IShellFolder2:: GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span><span class="sxs-lookup"><span data-stu-id="076f8-273">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="076f8-274">Windows 7 y versiones posteriores admiten valores canónicos que evitan problemas en las compilaciones localizadas.</span><span class="sxs-lookup"><span data-stu-id="076f8-274">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="076f8-275">La siguiente sintaxis canónica es necesaria en las compilaciones localizadas para aprovechar esta mejora de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="076f8-275">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="076f8-276">En la siguiente entrada del registro de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="076f8-276">In the following example registry entry:</span></span>

-   <span data-ttu-id="076f8-277">El valor **appliesTo** controla si el verbo se muestra u oculta.</span><span class="sxs-lookup"><span data-stu-id="076f8-277">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="076f8-278">El valor DefaultAppliesTo controla qué verbo es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="076f8-278">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="076f8-279">El valor HasLUAShield controla si se muestra un escudo de control de cuentas de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="076f8-279">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="076f8-280">En este ejemplo, el valor **DefaultAppliesTo** hace que este verbo sea el predeterminado para cualquier archivo con la palabra "exampleText1" en el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="076f8-280">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="076f8-281">El valor **appliesTo** habilita el verbo para cualquier archivo con "exampleText1" en el nombre.</span><span class="sxs-lookup"><span data-stu-id="076f8-281">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="076f8-282">El valor **HasLUAShield** muestra el escudo para los archivos con "exampleText2" en el nombre.</span><span class="sxs-lookup"><span data-stu-id="076f8-282">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="076f8-283">Agregue la subclave **Command** y un valor:</span><span class="sxs-lookup"><span data-stu-id="076f8-283">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="076f8-284">En el registro de Windows 7, consulte **HKEY \_ classes \_ root** \\ **Drive** como ejemplo de verbos de BitLocker que emplean el siguiente enfoque:</span><span class="sxs-lookup"><span data-stu-id="076f8-284">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="076f8-285">AppliesTo = System. VOLUME. BitlockerProtection: = 2</span><span class="sxs-lookup"><span data-stu-id="076f8-285">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="076f8-286">System. VOLUME. BitlockerRequiresAdmin: = System. StructuredQueryType. Boolean \# true</span><span class="sxs-lookup"><span data-stu-id="076f8-286">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="076f8-287">Para obtener más información sobre AQS, consulte [Sintaxis de consulta avanzada](../search/-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="076f8-287">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="076f8-288">En desuso: asociar verbos con comandos de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="076f8-288">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="076f8-289">DDE está en desuso; en su lugar, use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="076f8-289">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="076f8-290">DDE está en desuso porque se basa en un mensaje de ventana de difusión para detectar el servidor DDE.</span><span class="sxs-lookup"><span data-stu-id="076f8-290">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="076f8-291">Un bloqueo de servidor DDE detiene el mensaje de la ventana de difusión y, por tanto, cuelga las conversaciones DDE para otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="076f8-291">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="076f8-292">Es habitual que una sola aplicación atascada cause bloqueos posteriores en todo el proceso del usuario.</span><span class="sxs-lookup"><span data-stu-id="076f8-292">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="076f8-293">El método [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) es más sólido y tiene una mejor compatibilidad con la activación porque utiliza la activación com del controlador.</span><span class="sxs-lookup"><span data-stu-id="076f8-293">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="076f8-294">En el caso de la selección de varios elementos, **IDropTarget** no está sujeto a las restricciones de tamaño de búfer que se encuentran en DDE y en [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="076f8-294">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="076f8-295">Además, los elementos se pasan a la aplicación como un objeto de datos que se puede convertir en una matriz de elementos mediante la función [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="076f8-295">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="076f8-296">Hacerlo es más sencillo y no pierde información de espacio de nombres como ocurre cuando el elemento se convierte en una ruta de acceso para los protocolos de línea de comandos o DDE.</span><span class="sxs-lookup"><span data-stu-id="076f8-296">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="076f8-297">Para obtener más información sobre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y las consultas de Shell para los atributos de Asociación de archivos, consulte [tipos percibidos y registro de aplicaciones](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="076f8-297">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="076f8-298">Completar tareas de implementación de verbo</span><span class="sxs-lookup"><span data-stu-id="076f8-298">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="076f8-299">Las siguientes tareas para implementar verbos son relevantes para las implementaciones de verbos estáticos y dinámicos.</span><span class="sxs-lookup"><span data-stu-id="076f8-299">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="076f8-300">Para obtener más información sobre los verbos dinámicos, vea [personalizar un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="076f8-300">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="076f8-301">Personalización del menú contextual para objetos de Shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="076f8-301">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="076f8-302">Muchos objetos de Shell predefinidos tienen menús contextuales que se pueden personalizar.</span><span class="sxs-lookup"><span data-stu-id="076f8-302">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="076f8-303">Registre el comando de la misma manera que registra los tipos de archivo típicos, pero use el nombre del objeto predefinido como el nombre del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="076f8-303">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="076f8-304">Una lista de objetos predefinidos está en la sección *objetos de Shell predefinidos* de [crear controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="076f8-304">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="076f8-305">Los objetos de Shell predefinidos cuyos menús contextuales se pueden personalizar agregando verbos en el registro se marcan en la tabla con el verbo palabra.</span><span class="sxs-lookup"><span data-stu-id="076f8-305">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="076f8-306">Extender un nuevo submenú</span><span class="sxs-lookup"><span data-stu-id="076f8-306">Extending a New Submenu</span></span>

<span data-ttu-id="076f8-307">Cuando un usuario abre el menú **archivo** en el explorador de Windows, uno de los comandos que se muestran es **nuevo**.</span><span class="sxs-lookup"><span data-stu-id="076f8-307">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="076f8-308">Al seleccionar este comando se muestra un submenú.</span><span class="sxs-lookup"><span data-stu-id="076f8-308">Selecting this command displays a submenu.</span></span> <span data-ttu-id="076f8-309">De forma predeterminada, el submenú contiene dos comandos, **carpeta** y **acceso directo**, que permiten a los usuarios crear subcarpetas y accesos directos.</span><span class="sxs-lookup"><span data-stu-id="076f8-309">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="076f8-310">Este submenú se puede extender para incluir comandos de creación de archivos para cualquier tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="076f8-310">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="076f8-311">Para agregar un comando de creación de archivos al **nuevo** submenú, los archivos de la aplicación deben tener un tipo de archivo asociado.</span><span class="sxs-lookup"><span data-stu-id="076f8-311">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="076f8-312">Incluya una subclave **ShellNew** en el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="076f8-312">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="076f8-313">Cuando se selecciona el comando **nuevo** del menú **archivo** , el shell agrega el tipo de archivo al **nuevo** submenú.</span><span class="sxs-lookup"><span data-stu-id="076f8-313">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="076f8-314">La cadena de presentación del comando es la cadena descriptiva que se asigna al ProgID del programa.</span><span class="sxs-lookup"><span data-stu-id="076f8-314">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="076f8-315">Para especificar el método de creación de archivos, asigne uno o varios valores de datos a la subclave **ShellNew** .</span><span class="sxs-lookup"><span data-stu-id="076f8-315">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="076f8-316">Los valores disponibles se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="076f8-316">The available values are listed in the following table.</span></span>



| <span data-ttu-id="076f8-317">Valor de la subclave ShellNew</span><span class="sxs-lookup"><span data-stu-id="076f8-317">ShellNew subkey value</span></span> | <span data-ttu-id="076f8-318">Descripción</span><span class="sxs-lookup"><span data-stu-id="076f8-318">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="076f8-319">Comando</span><span class="sxs-lookup"><span data-stu-id="076f8-319">Command</span></span>               | <span data-ttu-id="076f8-320">Ejecuta una aplicación.</span><span class="sxs-lookup"><span data-stu-id="076f8-320">Executes an application.</span></span> <span data-ttu-id="076f8-321">Este valor **reg \_ SZ** especifica la ruta de acceso de la aplicación que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="076f8-321">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="076f8-322">Por ejemplo, puede establecerlo para iniciar un asistente.</span><span class="sxs-lookup"><span data-stu-id="076f8-322">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="076f8-323">Datos</span><span class="sxs-lookup"><span data-stu-id="076f8-323">Data</span></span>                  | <span data-ttu-id="076f8-324">Crea un archivo que contiene los datos especificados.</span><span class="sxs-lookup"><span data-stu-id="076f8-324">Creates a file containing specified data.</span></span> <span data-ttu-id="076f8-325">Este **valor \_ binario de reg** especifica los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="076f8-325">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="076f8-326">Los **datos** se omiten si se especifica **NullFile** o **filename** .</span><span class="sxs-lookup"><span data-stu-id="076f8-326">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="076f8-327">FileName</span><span class="sxs-lookup"><span data-stu-id="076f8-327">FileName</span></span>              | <span data-ttu-id="076f8-328">Crea un archivo que es una copia de un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="076f8-328">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="076f8-329">Este valor **reg \_ SZ** especifica la ruta de acceso completa del archivo que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="076f8-329">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="076f8-330">NullFile</span><span class="sxs-lookup"><span data-stu-id="076f8-330">NullFile</span></span>              | <span data-ttu-id="076f8-331">Crea un archivo vacío.</span><span class="sxs-lookup"><span data-stu-id="076f8-331">Creates an empty file.</span></span> <span data-ttu-id="076f8-332">**NullFile** no tiene asignado un valor.</span><span class="sxs-lookup"><span data-stu-id="076f8-332">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="076f8-333">Si se especifica **NullFile** , se omiten los valores de registro de los **datos** y del **nombre de archivo** .</span><span class="sxs-lookup"><span data-stu-id="076f8-333">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="076f8-334">El siguiente ejemplo de clave del registro y captura de pantalla ilustran el **nuevo** submenú para el tipo de archivo. MYP-ms.</span><span class="sxs-lookup"><span data-stu-id="076f8-334">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="076f8-335">Tiene un comando, **aplicación de programa**.</span><span class="sxs-lookup"><span data-stu-id="076f8-335">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="076f8-336">En la captura de pantalla se muestra el **nuevo** submenú.</span><span class="sxs-lookup"><span data-stu-id="076f8-336">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="076f8-337">Cuando un usuario selecciona mi **aplicación** en el submenú **nuevo** , el shell crea un archivo denominado **nueva aplicación de MYP-ms** y lo pasa a **MyProgram.exe**.</span><span class="sxs-lookup"><span data-stu-id="076f8-337">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![captura de pantalla del explorador de Windows que muestra un nuevo comando "mi aplicación" en el submenú "nuevo"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="076f8-339">Crear controladores de arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="076f8-339">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="076f8-340">El procedimiento básico para implementar un controlador de arrastrar y colocar es el mismo que el de los controladores de menú contextuales convencionales.</span><span class="sxs-lookup"><span data-stu-id="076f8-340">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="076f8-341">Sin embargo, los controladores de menús contextuales normalmente usan solo el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) que se pasa al método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del controlador para extraer el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="076f8-341">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="076f8-342">Un controlador de arrastrar y colocar podría implementar un controlador de datos más sofisticado para modificar el comportamiento del objeto arrastrado.</span><span class="sxs-lookup"><span data-stu-id="076f8-342">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="076f8-343">Cuando un usuario hace clic con el botón secundario en un objeto de Shell para arrastrar un objeto, se muestra un menú contextual cuando el usuario intenta quitar el objeto.</span><span class="sxs-lookup"><span data-stu-id="076f8-343">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="076f8-344">En la captura de pantalla siguiente se muestra un menú contextual típico de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="076f8-344">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![captura de pantalla del menú contextual de arrastrar y colocar](images/context-menu/context-dragdrop.png)

<span data-ttu-id="076f8-346">Un controlador de arrastrar y colocar es un controlador de menú contextual que puede agregar elementos a este menú contextual.</span><span class="sxs-lookup"><span data-stu-id="076f8-346">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="076f8-347">Los controladores de arrastrar y colocar se registran normalmente en la subclave siguiente.</span><span class="sxs-lookup"><span data-stu-id="076f8-347">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="076f8-348">Agregue una subclave en la subclave **DragDropHandlers** denominada para el controlador de arrastrar y colocar, y establezca el valor predeterminado de la subclave en el formato de cadena del GUID del identificador de clase (CLSID) del controlador.</span><span class="sxs-lookup"><span data-stu-id="076f8-348">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="076f8-349">En el ejemplo siguiente se habilita el controlador de arrastrar y colocar de **MyDD** .</span><span class="sxs-lookup"><span data-stu-id="076f8-349">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="076f8-350">Suprimir verbos y controlar la visibilidad</span><span class="sxs-lookup"><span data-stu-id="076f8-350">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="076f8-351">Puede usar la configuración de directiva de Windows para controlar la visibilidad de los verbos.</span><span class="sxs-lookup"><span data-stu-id="076f8-351">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="076f8-352">Los verbos se pueden suprimir a través de la configuración de la Directiva agregando un valor de **SuppressionPolicy** o un valor de GUID de **SuppressionPolicyEx** a la subclave del registro del verbo.</span><span class="sxs-lookup"><span data-stu-id="076f8-352">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="076f8-353">Establezca el valor de la subclave **SuppressionPolicy** en el identificador de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="076f8-353">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="076f8-354">Si la Directiva está activada, se suprimen el verbo y su entrada de menú contextual asociada.</span><span class="sxs-lookup"><span data-stu-id="076f8-354">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="076f8-355">Para ver los posibles valores de ID. de Directiva, consulte la enumeración [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="076f8-355">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="076f8-356">Usar el modelo de selección de verbos</span><span class="sxs-lookup"><span data-stu-id="076f8-356">Employing the Verb Selection Model</span></span>

<span data-ttu-id="076f8-357">Los valores del registro se deben establecer para que los verbos controlen las situaciones en las que un usuario puede seleccionar un solo elemento, varios elementos o una selección de un elemento.</span><span class="sxs-lookup"><span data-stu-id="076f8-357">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="076f8-358">Un verbo requiere valores de registro independientes para cada una de estas tres situaciones que admite el verbo.</span><span class="sxs-lookup"><span data-stu-id="076f8-358">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="076f8-359">Los valores posibles para el modelo de selección de verbos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="076f8-359">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="076f8-360">Especifique el valor de MultiSelectModel para todos los verbos.</span><span class="sxs-lookup"><span data-stu-id="076f8-360">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="076f8-361">Si no se especifica el valor MultiSelectModel, se deduce del tipo de implementación de verbo que ha elegido.</span><span class="sxs-lookup"><span data-stu-id="076f8-361">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="076f8-362">En el caso de los métodos basados en COM (como DropTarget y ExecuteCommand), se supone que el **jugador** y para el resto **de métodos se** supone.</span><span class="sxs-lookup"><span data-stu-id="076f8-362">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="076f8-363">Especifique **Single** para los verbos que solo admiten una sola selección.</span><span class="sxs-lookup"><span data-stu-id="076f8-363">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="076f8-364">Especifique **Player** para los verbos que admiten cualquier número de elementos.</span><span class="sxs-lookup"><span data-stu-id="076f8-364">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="076f8-365">Especifique el **documento** para los verbos que crean una ventana de nivel superior para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="076f8-365">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="076f8-366">Esto limita el número de elementos activados y ayuda a evitar quedarse sin recursos del sistema si el usuario abre demasiadas ventanas.</span><span class="sxs-lookup"><span data-stu-id="076f8-366">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="076f8-367">Cuando el número de elementos seleccionados no coincide con el modelo de selección de verbos o es mayor que los límites predeterminados que se describen en la tabla siguiente, el verbo no aparece.</span><span class="sxs-lookup"><span data-stu-id="076f8-367">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="076f8-368">Tipo de implementación de verbo</span><span class="sxs-lookup"><span data-stu-id="076f8-368">Type of verb implementation</span></span> | <span data-ttu-id="076f8-369">Documento</span><span class="sxs-lookup"><span data-stu-id="076f8-369">Document</span></span> | <span data-ttu-id="076f8-370">Reproductor</span><span class="sxs-lookup"><span data-stu-id="076f8-370">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="076f8-371">Heredado</span><span class="sxs-lookup"><span data-stu-id="076f8-371">Legacy</span></span>                      | <span data-ttu-id="076f8-372">15 elementos</span><span class="sxs-lookup"><span data-stu-id="076f8-372">15 items</span></span> | <span data-ttu-id="076f8-373">100 elementos</span><span class="sxs-lookup"><span data-stu-id="076f8-373">100 items</span></span> |
| <span data-ttu-id="076f8-374">COM</span><span class="sxs-lookup"><span data-stu-id="076f8-374">COM</span></span>                         | <span data-ttu-id="076f8-375">15 elementos</span><span class="sxs-lookup"><span data-stu-id="076f8-375">15 items</span></span> | <span data-ttu-id="076f8-376">Sin límite</span><span class="sxs-lookup"><span data-stu-id="076f8-376">No limit</span></span>  |



 

<span data-ttu-id="076f8-377">A continuación se muestran las entradas del registro de ejemplo con el valor MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="076f8-377">The following are example registry entries using the MultiSelectModel value.</span></span>

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

### <a name="using-item-attributes"></a><span data-ttu-id="076f8-378">Usar atributos de elemento</span><span class="sxs-lookup"><span data-stu-id="076f8-378">Using Item Attributes</span></span>

<span data-ttu-id="076f8-379">Los valores de marca [**SFGAO**](sfgao.md) de los atributos de Shell para un elemento pueden probarse para determinar si el verbo debe estar habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="076f8-379">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="076f8-380">Para usar esta característica de atributo, agregue los siguientes valores de **reg \_ DWORD** en el verbo:</span><span class="sxs-lookup"><span data-stu-id="076f8-380">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="076f8-381">El valor AttributeMask especifica el valor de [**SFGAO**](sfgao.md) de los valores de bit de la máscara que se va a probar con.</span><span class="sxs-lookup"><span data-stu-id="076f8-381">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="076f8-382">El valor AttributeValue especifica el valor de [**SFGAO**](sfgao.md) de los bits que se prueban.</span><span class="sxs-lookup"><span data-stu-id="076f8-382">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="076f8-383">ImpliedSelectionModel especifica cero para los verbos de elemento o un valor distinto de cero para los verbos en el menú contextual del fondo.</span><span class="sxs-lookup"><span data-stu-id="076f8-383">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="076f8-384">En la siguiente entrada del registro de ejemplo, AttributeMask se establece en [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="076f8-384">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

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

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="076f8-385">Implementar verbos personalizados para carpetas a través de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="076f8-385">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="076f8-386">En Windows 7 y versiones posteriores, puede Agregar verbos a una carpeta a través de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="076f8-386">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="076f8-387">Para obtener más información acerca de los archivos de Desktop.ini, consulte [Cómo personalizar carpetas con Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="076f8-387">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="076f8-388">Desktop.ini archivos siempre deben estar marcados como **sistema**  +  **oculto** para que no se muestren a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="076f8-388">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="076f8-389">**Para agregar verbos personalizados para carpetas a través de un archivo de Desktop.ini, realice los pasos siguientes:**</span><span class="sxs-lookup"><span data-stu-id="076f8-389">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="076f8-390">Cree una carpeta marcada como **de solo lectura** o **sistema**.</span><span class="sxs-lookup"><span data-stu-id="076f8-390">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="076f8-391">Cree un archivo de Desktop.ini que incluya un \[ . ShellClassInfo \] DirectoryClass = ProgID.</span><span class="sxs-lookup"><span data-stu-id="076f8-391">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="076f8-392">En el registro, cree **HKEY \_ classes \_ raíz** \\ **ProgID** con un valor de CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="076f8-392">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="076f8-393">El valor CanUseForDirectory evita el uso incorrecto de los ProgID que se establecen para no participar en la implementación de verbos personalizados para carpetas a través de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="076f8-393">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="076f8-394">Agregue verbos en la subclave ProgID de la **carpeta**, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="076f8-394">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="076f8-395">Estos verbos pueden ser el verbo predeterminado, en cuyo caso al hacer doble clic en la carpeta se activa el verbo.</span><span class="sxs-lookup"><span data-stu-id="076f8-395">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="076f8-396">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="076f8-396">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="076f8-397">Prácticas recomendadas para los controladores de menú contextual y varios verbos de selección</span><span class="sxs-lookup"><span data-stu-id="076f8-397">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="076f8-398">Elegir un verbo estático o dinámico para el menú contextual</span><span class="sxs-lookup"><span data-stu-id="076f8-398">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="076f8-399">Personalización de un menú contextual mediante verbos dinámicos</span><span class="sxs-lookup"><span data-stu-id="076f8-399">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="076f8-400">Menús contextuales y controladores de menú contextual</span><span class="sxs-lookup"><span data-stu-id="076f8-400">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="076f8-401">Verbos y asociaciones de archivo</span><span class="sxs-lookup"><span data-stu-id="076f8-401">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="076f8-402">Referencia del menú contextual</span><span class="sxs-lookup"><span data-stu-id="076f8-402">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
