---
description: La tabla de accesos directos contiene la información que la aplicación necesita para crear accesos directos en el equipo del usuario.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Tabla de acceso directo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56482f1d2d5521bede54c781c91d2de2bc39e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910901"
---
# <a name="shortcut-table"></a><span data-ttu-id="19d9b-103">Tabla de acceso directo</span><span class="sxs-lookup"><span data-stu-id="19d9b-103">Shortcut Table</span></span>

<span data-ttu-id="19d9b-104">La tabla de accesos directos contiene la información que la aplicación necesita para crear accesos directos en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="19d9b-104">The Shortcut table holds the information the application needs to create shortcuts on the user's computer.</span></span>

<span data-ttu-id="19d9b-105">La tabla de acceso directo tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="19d9b-105">The Shortcut table has the following columns.</span></span>



| <span data-ttu-id="19d9b-106">Columna</span><span class="sxs-lookup"><span data-stu-id="19d9b-106">Column</span></span>                 | <span data-ttu-id="19d9b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="19d9b-107">Type</span></span>                         | <span data-ttu-id="19d9b-108">Clave</span><span class="sxs-lookup"><span data-stu-id="19d9b-108">Key</span></span> | <span data-ttu-id="19d9b-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="19d9b-109">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="19d9b-110">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="19d9b-110">Shortcut</span></span>               | [<span data-ttu-id="19d9b-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="19d9b-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="19d9b-112">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-112">Y</span></span>   | <span data-ttu-id="19d9b-113">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-113">N</span></span>        |
| <span data-ttu-id="19d9b-114">Directorio\_</span><span class="sxs-lookup"><span data-stu-id="19d9b-114">Directory\_</span></span>            | [<span data-ttu-id="19d9b-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="19d9b-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="19d9b-116">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-116">N</span></span>   | <span data-ttu-id="19d9b-117">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-117">N</span></span>        |
| <span data-ttu-id="19d9b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="19d9b-118">Name</span></span>                   | [<span data-ttu-id="19d9b-119">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="19d9b-119">Filename</span></span>](filename.md)     | <span data-ttu-id="19d9b-120">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-120">N</span></span>   | <span data-ttu-id="19d9b-121">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-121">N</span></span>        |
| <span data-ttu-id="19d9b-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="19d9b-122">Component\_</span></span>            | [<span data-ttu-id="19d9b-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="19d9b-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="19d9b-124">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-124">N</span></span>   | <span data-ttu-id="19d9b-125">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-125">N</span></span>        |
| <span data-ttu-id="19d9b-126">Destino</span><span class="sxs-lookup"><span data-stu-id="19d9b-126">Target</span></span>                 | [<span data-ttu-id="19d9b-127">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="19d9b-127">Shortcut</span></span>](shortcut.md)     | <span data-ttu-id="19d9b-128">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-128">N</span></span>   | <span data-ttu-id="19d9b-129">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-129">N</span></span>        |
| <span data-ttu-id="19d9b-130">Argumentos</span><span class="sxs-lookup"><span data-stu-id="19d9b-130">Arguments</span></span>              | [<span data-ttu-id="19d9b-131">Formatea</span><span class="sxs-lookup"><span data-stu-id="19d9b-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="19d9b-132">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-132">N</span></span>   | <span data-ttu-id="19d9b-133">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-133">Y</span></span>        |
| <span data-ttu-id="19d9b-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="19d9b-134">Description</span></span>            | [<span data-ttu-id="19d9b-135">Texto</span><span class="sxs-lookup"><span data-stu-id="19d9b-135">Text</span></span>](text.md)             | <span data-ttu-id="19d9b-136">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-136">N</span></span>   | <span data-ttu-id="19d9b-137">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-137">Y</span></span>        |
| <span data-ttu-id="19d9b-138">Tecla de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="19d9b-138">Hotkey</span></span>                 | [<span data-ttu-id="19d9b-139">Entero</span><span class="sxs-lookup"><span data-stu-id="19d9b-139">Integer</span></span>](integer.md)       | <span data-ttu-id="19d9b-140">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-140">N</span></span>   | <span data-ttu-id="19d9b-141">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-141">Y</span></span>        |
| <span data-ttu-id="19d9b-142">Icono\_</span><span class="sxs-lookup"><span data-stu-id="19d9b-142">Icon\_</span></span>                 | [<span data-ttu-id="19d9b-143">Identificador</span><span class="sxs-lookup"><span data-stu-id="19d9b-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="19d9b-144">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-144">N</span></span>   | <span data-ttu-id="19d9b-145">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-145">Y</span></span>        |
| <span data-ttu-id="19d9b-146">IconIndex</span><span class="sxs-lookup"><span data-stu-id="19d9b-146">IconIndex</span></span>              | [<span data-ttu-id="19d9b-147">Entero</span><span class="sxs-lookup"><span data-stu-id="19d9b-147">Integer</span></span>](integer.md)       | <span data-ttu-id="19d9b-148">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-148">N</span></span>   | <span data-ttu-id="19d9b-149">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-149">Y</span></span>        |
| <span data-ttu-id="19d9b-150">ShowCmd</span><span class="sxs-lookup"><span data-stu-id="19d9b-150">ShowCmd</span></span>                | [<span data-ttu-id="19d9b-151">Entero</span><span class="sxs-lookup"><span data-stu-id="19d9b-151">Integer</span></span>](integer.md)       | <span data-ttu-id="19d9b-152">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-152">N</span></span>   | <span data-ttu-id="19d9b-153">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-153">Y</span></span>        |
| <span data-ttu-id="19d9b-154">WkDir</span><span class="sxs-lookup"><span data-stu-id="19d9b-154">WkDir</span></span>                  | [<span data-ttu-id="19d9b-155">Identificador</span><span class="sxs-lookup"><span data-stu-id="19d9b-155">Identifier</span></span>](identifier.md) | <span data-ttu-id="19d9b-156">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-156">N</span></span>   | <span data-ttu-id="19d9b-157">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-157">Y</span></span>        |
| <span data-ttu-id="19d9b-158">DisplayResourceDLL</span><span class="sxs-lookup"><span data-stu-id="19d9b-158">DisplayResourceDLL</span></span>     | [<span data-ttu-id="19d9b-159">Formatea</span><span class="sxs-lookup"><span data-stu-id="19d9b-159">Formatted</span></span>](formatted.md)   | <span data-ttu-id="19d9b-160">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-160">N</span></span>   | <span data-ttu-id="19d9b-161">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-161">Y</span></span>        |
| <span data-ttu-id="19d9b-162">DisplayResourceId</span><span class="sxs-lookup"><span data-stu-id="19d9b-162">DisplayResourceId</span></span>      | [<span data-ttu-id="19d9b-163">Entero</span><span class="sxs-lookup"><span data-stu-id="19d9b-163">Integer</span></span>](integer.md)       | <span data-ttu-id="19d9b-164">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-164">N</span></span>   | <span data-ttu-id="19d9b-165">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-165">Y</span></span>        |
| <span data-ttu-id="19d9b-166">DescriptionResourceDLL</span><span class="sxs-lookup"><span data-stu-id="19d9b-166">DescriptionResourceDLL</span></span> | [<span data-ttu-id="19d9b-167">Formatea</span><span class="sxs-lookup"><span data-stu-id="19d9b-167">Formatted</span></span>](formatted.md)   | <span data-ttu-id="19d9b-168">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-168">N</span></span>   | <span data-ttu-id="19d9b-169">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-169">Y</span></span>        |
| <span data-ttu-id="19d9b-170">DescriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="19d9b-170">DescriptionResourceId</span></span>  | [<span data-ttu-id="19d9b-171">Entero</span><span class="sxs-lookup"><span data-stu-id="19d9b-171">Integer</span></span>](integer.md)       | <span data-ttu-id="19d9b-172">N</span><span class="sxs-lookup"><span data-stu-id="19d9b-172">N</span></span>   | <span data-ttu-id="19d9b-173">Y</span><span class="sxs-lookup"><span data-stu-id="19d9b-173">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="19d9b-174">Columnas</span><span class="sxs-lookup"><span data-stu-id="19d9b-174">Columns</span></span>

<dl> <dt>

<span data-ttu-id="19d9b-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Contextual</span><span class="sxs-lookup"><span data-stu-id="19d9b-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Shortcut</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-176">Valor de clave de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="19d9b-176">The key value for this table.</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_</span><span class="sxs-lookup"><span data-stu-id="19d9b-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-178">La clave externa en la primera columna de la [tabla de directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="19d9b-178">The external key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="19d9b-179">Esta columna especifica el directorio en el que se crea el archivo de acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-179">This column specifies the directory in which the Shortcut file is created.</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="19d9b-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-181">Nombre traducible del acceso directo que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="19d9b-181">The localizable name of the shortcut to be created.</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="19d9b-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-183">La clave externa en la primera columna de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="19d9b-183">The external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="19d9b-184">El instalador usa el estado de instalación del componente especificado en esta columna para determinar si se crea o se elimina el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-184">The installer uses the installation state of the component specified in this column to determine whether the shortcut is created or deleted.</span></span> <span data-ttu-id="19d9b-185">Este componente debe tener una ruta de acceso de clave válida para que se instale el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-185">This component must have a valid key path for the shortcut to be installed.</span></span> <span data-ttu-id="19d9b-186">Si la columna de destino contiene el nombre de una característica, el archivo Iniciado por el acceso directo es el archivo de clave del componente que se muestra en esta columna.</span><span class="sxs-lookup"><span data-stu-id="19d9b-186">If the Target column contains the name of a feature, the file launched by the shortcut is the key file of the component listed in this column.</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Dirigir</span><span class="sxs-lookup"><span data-stu-id="19d9b-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-188">El destino del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-188">The shortcut target.</span></span>

<span data-ttu-id="19d9b-189">En el caso de un acceso directo anunciado, esta columna debe ser una clave externa en la primera columna de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="19d9b-189">For an advertised shortcut, this column must be an external key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="19d9b-190">El instalador evalúa la entrada en el campo de destino como un [identificador](identifier.md) y la entrada debe ser una clave externa válida en la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="19d9b-190">The installer evaluates the entry in the Target field as an [Identifier](identifier.md) and the entry must be a valid foreign key into the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="19d9b-191">El archivo Iniciado por el acceso directo en este caso es el archivo de clave del componente que aparece en la \_ columna componente.</span><span class="sxs-lookup"><span data-stu-id="19d9b-191">The file launched by the shortcut in this case is the key file of the component listed in the Component\_ column.</span></span> <span data-ttu-id="19d9b-192">Cuando se activa el acceso directo, el instalador comprueba que todos los componentes de la característica se instalan antes de iniciar este archivo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-192">When the shortcut is activated, the installer verifies that all the components in the feature are installed before launching this file.</span></span>

<span data-ttu-id="19d9b-193">En el caso de un acceso directo no anunciado, el instalador evalúa este campo como una cadena [con formato](formatted.md) .</span><span class="sxs-lookup"><span data-stu-id="19d9b-193">For a non-advertised shortcut, the installer evaluates this field as a [Formatted](formatted.md) string.</span></span> <span data-ttu-id="19d9b-194">El campo debe contener un identificador de propiedad entre corchetes ( \[ \] ), que se expande en el archivo o en una carpeta a la que apunta el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-194">The field should contains a property identifier enclosed by square brackets (\[ \]), that is expanded into the file or a folder pointed to by the shortcut.</span></span> <span data-ttu-id="19d9b-195">Para obtener más información, consulte la [acción CreateShortcuts](createshortcuts-action.md).</span><span class="sxs-lookup"><span data-stu-id="19d9b-195">For more information, see the [CreateShortcuts action](createshortcuts-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos</span><span class="sxs-lookup"><span data-stu-id="19d9b-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-197">Argumentos de la línea de comandos para el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-197">The command-line arguments for the shortcut.</span></span>

<span data-ttu-id="19d9b-198">Tenga en cuenta que la resolución de propiedades en el campo arguments es limitada.</span><span class="sxs-lookup"><span data-stu-id="19d9b-198">Note that the resolution of properties in the Arguments field is limited.</span></span> <span data-ttu-id="19d9b-199">Una propiedad con formato \[  \] de propiedad en este campo solo se puede resolver si la propiedad ya tiene el valor previsto cuando se instala el componente que posee el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-199">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component that owns the shortcut is installed.</span></span> <span data-ttu-id="19d9b-200">Por ejemplo, para resolver el valor correcto para el argumento " \[ \#MyDoc.doc\] ", el mismo proceso debe instalar el archivo MyDoc.doc y el componente al que pertenece el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-200">For example, to resolve to the correct value for the argument "\[\#MyDoc.doc\]", the same process must be installing the file MyDoc.doc and the component that owns the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="19d9b-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-202">La descripción localizable del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-202">The localizable description of the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Directa</span><span class="sxs-lookup"><span data-stu-id="19d9b-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-204">Tecla de acceso rápido para el método abreviado.</span><span class="sxs-lookup"><span data-stu-id="19d9b-204">The hotkey for the shortcut.</span></span> <span data-ttu-id="19d9b-205">El byte de orden inferior contiene el código de clave virtual para la clave y el byte de orden superior contiene marcas de modificador.</span><span class="sxs-lookup"><span data-stu-id="19d9b-205">The low-order byte contains the virtual-key code for the key, and the high-order byte contains modifier flags.</span></span> <span data-ttu-id="19d9b-206">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-206">This must be a non-negative number.</span></span> <span data-ttu-id="19d9b-207">Por lo general, se recomienda que los autores de los paquetes de instalación no establezcan esta opción, ya que la configuración de esta opción puede Agregar teclas de error duplicadas al escritorio de un usuario.</span><span class="sxs-lookup"><span data-stu-id="19d9b-207">Authors of installation packages are generally recommended not to set this option, because the setting of this option can add duplicate hotkeys to a user's desktop.</span></span> <span data-ttu-id="19d9b-208">Además, la práctica de asignar teclas de acceso rápido a los accesos directos puede ser problemática para los usuarios que usan teclas de acceso directo para la [accesibilidad](accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="19d9b-208">In addition, the practice of assigning hotkeys to shortcuts can be problematic for users using hotkeys for [accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icono\_</span><span class="sxs-lookup"><span data-stu-id="19d9b-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-210">La clave externa para la columna uno de la [tabla de iconos](icon-table.md).</span><span class="sxs-lookup"><span data-stu-id="19d9b-210">The external key to column one of the [Icon table](icon-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span><span class="sxs-lookup"><span data-stu-id="19d9b-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-212">Índice del icono para el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-212">The icon index for the shortcut.</span></span> <span data-ttu-id="19d9b-213">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-213">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span><span class="sxs-lookup"><span data-stu-id="19d9b-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-215">El comando show para la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="19d9b-215">The Show command for the application window.</span></span>

<span data-ttu-id="19d9b-216">Se pueden usar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="19d9b-216">The following values may be used.</span></span> <span data-ttu-id="19d9b-217">Los valores son los definidos para la función de la API de Windows ShowWindow.</span><span class="sxs-lookup"><span data-stu-id="19d9b-217">The values are as defined for the Windows API function ShowWindow.</span></span>



| <span data-ttu-id="19d9b-218">Value</span><span class="sxs-lookup"><span data-stu-id="19d9b-218">Value</span></span> | <span data-ttu-id="19d9b-219">Significado</span><span class="sxs-lookup"><span data-stu-id="19d9b-219">Meaning</span></span>             |
|-------|---------------------|
| <span data-ttu-id="19d9b-220">1</span><span class="sxs-lookup"><span data-stu-id="19d9b-220">1</span></span>     | <span data-ttu-id="19d9b-221">\_SHOWNORMAL SW</span><span class="sxs-lookup"><span data-stu-id="19d9b-221">SW\_SHOWNORMAL</span></span>      |
| <span data-ttu-id="19d9b-222">3</span><span class="sxs-lookup"><span data-stu-id="19d9b-222">3</span></span>     | <span data-ttu-id="19d9b-223">\_SHOWMAXIMIZED SW</span><span class="sxs-lookup"><span data-stu-id="19d9b-223">SW\_SHOWMAXIMIZED</span></span>   |
| <span data-ttu-id="19d9b-224">7</span><span class="sxs-lookup"><span data-stu-id="19d9b-224">7</span></span>     | <span data-ttu-id="19d9b-225">\_SHOWMINNOACTIVE SW</span><span class="sxs-lookup"><span data-stu-id="19d9b-225">SW\_SHOWMINNOACTIVE</span></span> |



 

</dd> <dt>

<span data-ttu-id="19d9b-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir</span><span class="sxs-lookup"><span data-stu-id="19d9b-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-227">Nombre de la propiedad que tiene la ruta de acceso del directorio de trabajo para el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-227">The name of the property that has the path of the working directory for the shortcut.</span></span> <span data-ttu-id="19d9b-228">El valor puede utilizar el formato de Windows para hacer referencia a las variables de entorno, por ejemplo,% USERPROFILE%.</span><span class="sxs-lookup"><span data-stu-id="19d9b-228">The value can use the Windows format to reference environment variables, for example %USERPROFILE%.</span></span> <span data-ttu-id="19d9b-229">Las referencias se resuelven en una ruta de acceso real cuando el instalador resuelve el directorio de trabajo para crear el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-229">The references are resolved to an actual path when the installer resolves the working directory to create the shortcut.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="19d9b-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL</span><span class="sxs-lookup"><span data-stu-id="19d9b-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-231">Este campo contiene un valor de cadena [con formato](formatted.md) para la ruta de acceso completa al archivo ejecutable portable (LN) independiente del idioma que contiene los datos de la configuración de recursos (RC config).</span><span class="sxs-lookup"><span data-stu-id="19d9b-231">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="19d9b-232">La cadena con formato puede usar la \[ \# \] Convención filekey.</span><span class="sxs-lookup"><span data-stu-id="19d9b-232">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="19d9b-233">Si este campo contiene un valor, se omite la columna Name.</span><span class="sxs-lookup"><span data-stu-id="19d9b-233">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="19d9b-234">Si este campo está vacío, el instalador usa el valor de la columna nombre.</span><span class="sxs-lookup"><span data-stu-id="19d9b-234">If this field is empty, the installer uses the value in the Name column.</span></span> <span data-ttu-id="19d9b-235">Cuando este campo contiene un valor, el campo **DisplayResourceId** también es necesario para contener un valor o se produce un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="19d9b-235">When this field contains a value, the **DisplayResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="19d9b-236">Esta columna de la tabla de acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite.</span><span class="sxs-lookup"><span data-stu-id="19d9b-236">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="19d9b-237">Esta columna está disponible con versiones de anteriores a Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="19d9b-237">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="19d9b-238">Para obtener información sobre cómo agregar accesos directos a la tabla de acceso directo para su uso con recursos de MUI, vea [un ejemplo de acceso directo de MUI](a-mui-shortcut-example.md).</span><span class="sxs-lookup"><span data-stu-id="19d9b-238">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId</span><span class="sxs-lookup"><span data-stu-id="19d9b-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-240">Índice del nombre para mostrar del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-240">The display name index for the shortcut.</span></span> <span data-ttu-id="19d9b-241">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-241">This must be a non-negative number.</span></span> <span data-ttu-id="19d9b-242">Cuando este campo contiene un valor, el campo **DisplayResourceDLL** también es necesario para contener un valor o se produce un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="19d9b-242">When this field contains a value, the **DisplayResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="19d9b-243">Esta columna de la tabla de acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite.</span><span class="sxs-lookup"><span data-stu-id="19d9b-243">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="19d9b-244">Esta columna está disponible con versiones de anteriores a Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="19d9b-244">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL</span><span class="sxs-lookup"><span data-stu-id="19d9b-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-246">Este campo contiene un valor de cadena [con formato](formatted.md) para la ruta de acceso completa al archivo ejecutable portable (LN) independiente del idioma que contiene los datos de la configuración de recursos (RC config).</span><span class="sxs-lookup"><span data-stu-id="19d9b-246">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="19d9b-247">La cadena con formato puede usar la \[ \# \] Convención filekey.</span><span class="sxs-lookup"><span data-stu-id="19d9b-247">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="19d9b-248">Si este campo contiene un valor, se omite la columna Name.</span><span class="sxs-lookup"><span data-stu-id="19d9b-248">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="19d9b-249">Si este campo está vacío, el instalador usa el valor de la columna Description.</span><span class="sxs-lookup"><span data-stu-id="19d9b-249">If this field is empty, the installer uses the value in the Description column.</span></span> <span data-ttu-id="19d9b-250">Cuando este campo contiene un valor, el campo **DescriptionResourceId** también es necesario para contener un valor o se produce un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="19d9b-250">When this field contains a value, the **DescriptionResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="19d9b-251">Esta columna de la tabla de acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite.</span><span class="sxs-lookup"><span data-stu-id="19d9b-251">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="19d9b-252">Esta columna está disponible con versiones de anteriores a Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="19d9b-252">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="19d9b-253">Para obtener información sobre cómo agregar accesos directos a la tabla de acceso directo para su uso con recursos de MUI, vea [un ejemplo de acceso directo de MUI](a-mui-shortcut-example.md).</span><span class="sxs-lookup"><span data-stu-id="19d9b-253">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="19d9b-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="19d9b-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId</span></span>
</dt> <dd>

<span data-ttu-id="19d9b-255">Índice del nombre de la descripción del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-255">The description name index for the shortcut.</span></span> <span data-ttu-id="19d9b-256">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="19d9b-256">This must be a non-negative number.</span></span> <span data-ttu-id="19d9b-257">Cuando este campo contiene un valor, el campo **DescriptionResourceDLL** también es necesario para contener un valor o se produce un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="19d9b-257">When this field contains a value, the **DescriptionResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="19d9b-258">Esta columna de la tabla de acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite.</span><span class="sxs-lookup"><span data-stu-id="19d9b-258">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="19d9b-259">Esta columna está disponible con versiones de anteriores a Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="19d9b-259">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19d9b-260">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19d9b-260">Remarks</span></span>

<span data-ttu-id="19d9b-261">La habilitación de una característica crea un acceso directo anunciado solo si la interfaz IShellLink del sistema admite la resolución de descriptores de instalador.</span><span class="sxs-lookup"><span data-stu-id="19d9b-261">The enabling of a feature creates an advertised shortcut only if the system's IShellLink interface supports installer descriptor resolution.</span></span> <span data-ttu-id="19d9b-262">Es compatible con Microsoft Windows 2000 y los sistemas que ejecutan Microsoft Internet Explorer 4,01.</span><span class="sxs-lookup"><span data-stu-id="19d9b-262">This is supported by Microsoft Windows 2000 and systems running Microsoft Internet Explorer 4.01.</span></span> <span data-ttu-id="19d9b-263">Si no se admite, el instalador crea un acceso directo no anunciado al instalar el componente de la característica, ya sea de forma local o se ejecuta desde el origen.</span><span class="sxs-lookup"><span data-stu-id="19d9b-263">If unsupported, the installer creates a non-advertised shortcut upon the installation of the feature's component, either locally or run from source.</span></span>

<span data-ttu-id="19d9b-264">Tenga en cuenta que los accesos directos anunciados siempre apuntan a una aplicación determinada, identificada por un [**ProductCode**](productcode.md), y no deben compartirse entre aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="19d9b-264">Note that advertised shortcuts always point at a particular application, identified by a [**ProductCode**](productcode.md), and should not be shared between applications.</span></span> <span data-ttu-id="19d9b-265">Los métodos abreviados anunciados solo funcionan en la aplicación instalada más recientemente y se quitan cuando se quita la aplicación.</span><span class="sxs-lookup"><span data-stu-id="19d9b-265">Advertised shortcuts only work for the most recently installed application, and are removed when that application is removed.</span></span>

<span data-ttu-id="19d9b-266">Se hace referencia a esta tabla cuando se ejecuta la acción [CreateShortcuts](createshortcuts-action.md) y la [acción RemoveShortcuts](removeshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="19d9b-266">This table is referred to when the [CreateShortcuts action](createshortcuts-action.md) and the [RemoveShortcuts action](removeshortcuts-action.md) is executed.</span></span>

<span data-ttu-id="19d9b-267">Vea también la propiedad [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) .</span><span class="sxs-lookup"><span data-stu-id="19d9b-267">See also the [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="19d9b-268">Validación</span><span class="sxs-lookup"><span data-stu-id="19d9b-268">Validation</span></span>

<dl>

[<span data-ttu-id="19d9b-269">ICE03</span><span class="sxs-lookup"><span data-stu-id="19d9b-269">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="19d9b-270">ICE06</span><span class="sxs-lookup"><span data-stu-id="19d9b-270">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="19d9b-271">ICE19</span><span class="sxs-lookup"><span data-stu-id="19d9b-271">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="19d9b-272">ICE32</span><span class="sxs-lookup"><span data-stu-id="19d9b-272">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="19d9b-273">ICE36</span><span class="sxs-lookup"><span data-stu-id="19d9b-273">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="19d9b-274">ICE46</span><span class="sxs-lookup"><span data-stu-id="19d9b-274">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="19d9b-275">ICE50</span><span class="sxs-lookup"><span data-stu-id="19d9b-275">ICE50</span></span>](ice50.md)  
[<span data-ttu-id="19d9b-276">ICE57</span><span class="sxs-lookup"><span data-stu-id="19d9b-276">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="19d9b-277">ICE59</span><span class="sxs-lookup"><span data-stu-id="19d9b-277">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="19d9b-278">ICE67</span><span class="sxs-lookup"><span data-stu-id="19d9b-278">ICE67</span></span>](ice67.md)  
[<span data-ttu-id="19d9b-279">ICE69</span><span class="sxs-lookup"><span data-stu-id="19d9b-279">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="19d9b-280">ICE80</span><span class="sxs-lookup"><span data-stu-id="19d9b-280">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="19d9b-281">ICE90</span><span class="sxs-lookup"><span data-stu-id="19d9b-281">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="19d9b-282">ICE91</span><span class="sxs-lookup"><span data-stu-id="19d9b-282">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="19d9b-283">ICE94</span><span class="sxs-lookup"><span data-stu-id="19d9b-283">ICE94</span></span>](ice94.md)  
</dl>

 

 



