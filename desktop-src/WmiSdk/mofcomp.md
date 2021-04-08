---
description: El compilador de Managed Object Format (MOF) analiza un archivo que contiene instrucciones MOF y agrega las clases y las instancias de clase definidas en el archivo al repositorio WMI.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: MOFCOMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908328"
---
# <a name="mofcomp"></a><span data-ttu-id="e3a20-103">MOFCOMP</span><span class="sxs-lookup"><span data-stu-id="e3a20-103">mofcomp</span></span>

<span data-ttu-id="e3a20-104">El compilador de [*Managed Object Format (MOF)*](gloss-m.md) analiza un archivo que contiene instrucciones MOF y agrega las clases y las instancias de clase definidas en el archivo al repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="e3a20-104">The [*Managed Object Format (MOF)*](gloss-m.md) compiler parses a file containing MOF statements and adds the classes and class instances defined in the file to the WMI repository.</span></span> <span data-ttu-id="e3a20-105">Normalmente, los archivos MOF se compilan automáticamente durante la instalación de los sistemas con los que se proporcionan, pero también puede compilar archivos MOF con esta herramienta.</span><span class="sxs-lookup"><span data-stu-id="e3a20-105">MOF files are usually automatically compiled during the installation of the systems with which they are provided, but you can also compile MOF files by using this tool.</span></span>

<span data-ttu-id="e3a20-106">Para obtener más información acerca de la búsqueda y el uso de mofcomp.exe, consulte [uso de las herramientas de administración de WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="e3a20-106">For more information about locating and using mofcomp.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span> <span data-ttu-id="e3a20-107">Para obtener información acerca de cómo quitar clases e instancias del repositorio WMI, vea el comando de preprocesador [**pragma deleteclass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="e3a20-107">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="e3a20-108">En el ejemplo de código siguiente se muestra cómo ejecutar el compilador MOF en un archivo.</span><span class="sxs-lookup"><span data-stu-id="e3a20-108">The following code example shows how to run the MOF compiler on a file.</span></span>

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a><span data-ttu-id="e3a20-109">Conmutadores</span><span class="sxs-lookup"><span data-stu-id="e3a20-109">Switches</span></span>

<dl> <dt>

<span data-ttu-id="e3a20-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-Autorrecuperación**</span><span class="sxs-lookup"><span data-stu-id="e3a20-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-autorecover**</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-111">Agrega el archivo MOF con nombre a la lista de archivos compilados durante la recuperación del repositorio.</span><span class="sxs-lookup"><span data-stu-id="e3a20-111">Adds the named MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="e3a20-112">La lista de archivos MOF de Autorrecuperación se almacena en la clave del registro:</span><span class="sxs-lookup"><span data-stu-id="e3a20-112">The list of autorecover MOF files is stored in the registry key:</span></span>

<span data-ttu-id="e3a20-113">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**</span><span class="sxs-lookup"><span data-stu-id="e3a20-113">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM\\**</span></span>

<span data-ttu-id="e3a20-114">Los archivos MOF que aparecen en esta entrada del registro deben residir en el equipo local, ya que los archivos MOF que utilizan el comando **Autorrecuperación** no pueden recuperar archivos MOF ubicados en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="e3a20-114">The MOF files listed in this registry entry must reside on the local computer because MOF files that use the **autorecover** command cannot recover MOF files located on a remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="e3a20-115">Para asegurarse de que todas las definiciones de clase WMI para objetos administrados se restauran en el [*repositorio WMI*](gloss-w.md) si WMI tiene un error y se reinician, use la instrucción de preprocesador [**\# pragma autocover**](pragma-autorecover.md) en el archivo [*Managed Object Format*](gloss-m.md) (MOF).</span><span class="sxs-lookup"><span data-stu-id="e3a20-115">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format*](gloss-m.md) (MOF) file.</span></span>

 

</dd> <dt>

<span data-ttu-id="e3a20-116"><span id="-check"></span><span id="-CHECK"></span>**-comprobar**</span><span class="sxs-lookup"><span data-stu-id="e3a20-116"><span id="-check"></span><span id="-CHECK"></span>**-check**</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-117">Solicita que el compilador realice una comprobación de sintaxis únicamente e imprima los mensajes de error correspondientes.</span><span class="sxs-lookup"><span data-stu-id="e3a20-117">Requests that the compiler perform a syntax check only and print appropriate error messages.</span></span> <span data-ttu-id="e3a20-118">No se puede usar ningún otro conmutador con este modificador.</span><span class="sxs-lookup"><span data-stu-id="e3a20-118">No other switch can be used with this switch.</span></span> <span data-ttu-id="e3a20-119">Cuando se utiliza este modificador, no se establece ninguna conexión a Instrumental de administración de Windows (WMI) y no se realiza ninguna modificación en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="e3a20-119">When this switch is used, no connection to Windows Management Instrumentation (WMI) is established and no modifications to the WMI repository are made.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N: <** _namespacepath_*_>_*</span><span class="sxs-lookup"><span data-stu-id="e3a20-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N:<**_namespacepath_*_>_*</span></span>
</dt> <dd><span data-ttu-id="e3a20-121">Solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como *namespacepath*.</span><span class="sxs-lookup"><span data-stu-id="e3a20-121">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="e3a20-122">El MOF compilado se carga en el espacio de nombres de MOFCOMP predeterminado, raíz \\ predeterminado, a menos que se use este modificador.</span><span class="sxs-lookup"><span data-stu-id="e3a20-122">The compiled MOF is loaded into the default Mofcomp namespace, root\\default, unless this switch is used.</span></span> <span data-ttu-id="e3a20-123">También puede insertar el comando de preprocesador **\# pragma ("**_ruta de acceso de espacio de nombres_*_")_* en el archivo MOF para lograr el mismo efecto.</span><span class="sxs-lookup"><span data-stu-id="e3a20-123">You can also insert the preprocessor command **\#pragma namespace ("**_namespace path_*_")_* in the MOF file to achieve the same effect.</span></span> <span data-ttu-id="e3a20-124">Si se usan el modificador **-N:** y el comando de \# <a href="pragma-namespace.md">espacio de nombres pragma</a> , la Autorrecuperación del \# **espacio de nombres de pragma**  tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="e3a20-124">If both the **-N:** switch and the \#<a href="pragma-namespace.md">pragma namespace</a> command are used, \#**pragma namespace** **autorecover** takes priority.</span></span> <span data-ttu-id="e3a20-125">En este caso, la única manera de compilar el MOF en otro espacio de nombres es editar el archivo MOF y cambiar el \# comando **pragma namespace** .</span><span class="sxs-lookup"><span data-stu-id="e3a20-125">In this case, the only way to compile the MOF into another namespace is to edit the MOF file and change the \#**pragma namespace** command.</span></span> <span data-ttu-id="e3a20-126">Se puede especificar un equipo remoto mediante el \\ \\ valor predeterminado de MachineName \\ raíz \\ .</span><span class="sxs-lookup"><span data-stu-id="e3a20-126">A remote computer can be specified using \\\\machinename\\root\\default.</span></span></dd> <dt>

<span data-ttu-id="e3a20-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-clase: createonly**</span><span class="sxs-lookup"><span data-stu-id="e3a20-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-class:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-128">Solicita que el compilador no realice ningún cambio en las clases existentes.</span><span class="sxs-lookup"><span data-stu-id="e3a20-128">Requests that the compiler not make any changes to existing classes.</span></span> <span data-ttu-id="e3a20-129">Cuando se utiliza este modificador, la operación de compilación finaliza si ya existe una clase especificada en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="e3a20-129">When this switch is used, the compile operation terminates if a class specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-Class: ForceUpdate**</span><span class="sxs-lookup"><span data-stu-id="e3a20-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-class:forceupdate**</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-131">Fuerza la actualización de las clases cuando existen clases secundarias en conflicto.</span><span class="sxs-lookup"><span data-stu-id="e3a20-131">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="e3a20-132">Por ejemplo, supongamos que se define un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador.</span><span class="sxs-lookup"><span data-stu-id="e3a20-132">For example, suppose a class qualifier is defined in a child class and the base class tries to add the same qualifier.</span></span> <span data-ttu-id="e3a20-133">En el modo de **clase: ForceUpdate** , el compilador MOF resuelve este conflicto eliminando el calificador en conflicto de la clase secundaria.</span><span class="sxs-lookup"><span data-stu-id="e3a20-133">In **-class:forceupdate** mode, the MOF compiler resolves this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="e3a20-134">Si la clase secundaria tiene instancias, se produce un error en la actualización forzada.</span><span class="sxs-lookup"><span data-stu-id="e3a20-134">If the child class has instances, the forced update fails.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-clase: safeupdate**</span><span class="sxs-lookup"><span data-stu-id="e3a20-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-class:safeupdate**</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-136">Permite actualizaciones de clases aunque haya clases secundarias, siempre y cuando el cambio no cause conflictos con las clases secundarias.</span><span class="sxs-lookup"><span data-stu-id="e3a20-136">Allows updates of classes even if there are child classes, as long as the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="e3a20-137">Por ejemplo, esta marca permite agregar una nueva propiedad a la clase base que no se mencionó anteriormente en las clases secundarias.</span><span class="sxs-lookup"><span data-stu-id="e3a20-137">For example, this flag allows adding a new property to the base class that was not previously mentioned in child classes.</span></span> <span data-ttu-id="e3a20-138">Si las clases secundarias tienen instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="e3a20-138">If the child classes have instances, the update fails.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-clase: updateonly**</span><span class="sxs-lookup"><span data-stu-id="e3a20-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-class:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-140">Solicita que el compilador no cree nuevas clases.</span><span class="sxs-lookup"><span data-stu-id="e3a20-140">Requests that the compiler not create any new classes.</span></span> <span data-ttu-id="e3a20-141">Cuando se utiliza este modificador, la operación de compilación finaliza si no existe una clase especificada en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="e3a20-141">When this switch is used, the compile operation terminates if a class specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instancia: updateonly**</span><span class="sxs-lookup"><span data-stu-id="e3a20-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-143">Solicita que el compilador no cree instancias nuevas.</span><span class="sxs-lookup"><span data-stu-id="e3a20-143">Requests that the compiler not create any new instances.</span></span> <span data-ttu-id="e3a20-144">Cuando se utiliza este modificador, la operación de compilación finaliza si no existe una instancia especificada en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="e3a20-144">When this switch is used, the compile operation terminates if an instance specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instancia: createonly**</span><span class="sxs-lookup"><span data-stu-id="e3a20-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-146">Solicita que el compilador no realice ningún cambio en las instancias existentes.</span><span class="sxs-lookup"><span data-stu-id="e3a20-146">Requests that the compiler not make any changes to existing instances.</span></span> <span data-ttu-id="e3a20-147">Cuando se utiliza este modificador, la operación de compilación finaliza si ya existe una instancia especificada en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="e3a20-147">When this switch is used, the compile operation terminates if an instance specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B: <** _nombre de archivo_*_>_*</span><span class="sxs-lookup"><span data-stu-id="e3a20-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B:<**_filename_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-149">Solicita que el compilador cree una versión binaria del archivo MOF con el nombre *filename* sin realizar ninguna modificación en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="e3a20-149">Requests that the compiler create a binary version of the MOF file with the name *filename* without making any modifications to the WMI repository.</span></span>

<span data-ttu-id="e3a20-150">Si usa la opción **-B: <** _nombre_ de *_>_* archivo para crear un archivo MOF binario, solo se almacenan los tipos de calificador predeterminados en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="e3a20-150">If you use the **-B:<**_filename_*_>_* option to create a binary MOF file, only default qualifier flavors are stored in the WMI repository.</span></span>

<span data-ttu-id="e3a20-151">El formato MOF binario es el formato intermedio para combinar un controlador WDM con el MOF como un recurso.</span><span class="sxs-lookup"><span data-stu-id="e3a20-151">Binary MOF format is the intermediate format for combining a WDM-driver with the MOF as a resource.</span></span> <span data-ttu-id="e3a20-152">MOF binario representa las clases y las instancias de la misma forma que un archivo MOF de texto y se comprimen antes de almacenarse en el disco.</span><span class="sxs-lookup"><span data-stu-id="e3a20-152">The binary MOF represents classes and instances just as a text MOF file does and is compressed before it is stored on disk.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span><span class="sxs-lookup"><span data-stu-id="e3a20-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-154">Solicita que el compilador realice una comprobación de la sintaxis de WMI.</span><span class="sxs-lookup"><span data-stu-id="e3a20-154">Requests that the compiler perform a WMI syntax check.</span></span> <span data-ttu-id="e3a20-155">El modificador **-B:** debe usarse con este modificador.</span><span class="sxs-lookup"><span data-stu-id="e3a20-155">The **-B:** switch must be used with this switch.</span></span> <span data-ttu-id="e3a20-156">El modificador **-WMI** solo se usa para compilar archivos MOF binarios para su uso por parte de controladores de dispositivos WDM.</span><span class="sxs-lookup"><span data-stu-id="e3a20-156">The **-WMI** switch is only used for building binary MOF files for use by WDM device drivers.</span></span> <span data-ttu-id="e3a20-157">Este modificador invoca un comprobador de archivos MOF binario independiente, que se ejecuta después de crear el archivo MOF binario.</span><span class="sxs-lookup"><span data-stu-id="e3a20-157">This switch invokes a separate binary MOF file checker, which runs after the binary MOF file is created.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P: contraseña de <** *_>_*</span><span class="sxs-lookup"><span data-stu-id="e3a20-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P:<**_Password_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-159">Especifica la *contraseña* que el usuario del equipo debe especificar al iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="e3a20-159">Specifies *Password* as the password for the computer user to enter when logging on.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U: <** _nombre de usuario_*_>_*</span><span class="sxs-lookup"><span data-stu-id="e3a20-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U:<**_UserName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-161">Especifica *username* como el nombre del usuario que inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="e3a20-161">Specifies *UserName* as the name of the user logging on.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A: entidad de <** *_>_*</span><span class="sxs-lookup"><span data-stu-id="e3a20-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A:<**_Authority_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-163">Especifica la *autoridad* como la entidad (nombre de dominio) que se va a usar al iniciar sesión en WMI.</span><span class="sxs-lookup"><span data-stu-id="e3a20-163">Specifies *Authority* as the authority (domain name) to use when logging on to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF: <** _ruta de acceso_*_>_*</span><span class="sxs-lookup"><span data-stu-id="e3a20-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-165">Nombre de la salida independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="e3a20-165">Name of the language neutral output.</span></span> <span data-ttu-id="e3a20-166">Se usa con el modificador **-enmiendas** para especificar el nombre del archivo MOF independiente del idioma que se generará.</span><span class="sxs-lookup"><span data-stu-id="e3a20-166">Used with the **-AMENDMENT** switch to specify the name of the language-neutral MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL: ruta de acceso de <** *_>_*</span><span class="sxs-lookup"><span data-stu-id="e3a20-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-168">Nombre de la salida específica del idioma.</span><span class="sxs-lookup"><span data-stu-id="e3a20-168">Name of the language specific output.</span></span> <span data-ttu-id="e3a20-169">Se usa con el modificador **-enmiendas** para especificar el nombre del archivo MOF específico del idioma que se generará.</span><span class="sxs-lookup"><span data-stu-id="e3a20-169">Used with the **-AMENDMENT** switch to specify the name of the language-specific MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-Enmienda:** _configuración regional_ de <*_>_*</span><span class="sxs-lookup"><span data-stu-id="e3a20-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-AMENDMENT:<**_Locale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-171">Divide el archivo MOF en versiones independientes del lenguaje y específicas.</span><span class="sxs-lookup"><span data-stu-id="e3a20-171">Splits the MOF file into language-neutral and -specific versions.</span></span> <span data-ttu-id="e3a20-172">El compilador MOF crea una forma independiente del idioma del archivo MOF que tiene todos los calificadores modificados que se han quitado.</span><span class="sxs-lookup"><span data-stu-id="e3a20-172">The MOF compiler creates a language-neutral form of the MOF file that has all amended qualifiers removed.</span></span> <span data-ttu-id="e3a20-173">También se crea una versión localizada del archivo MOF con una extensión de nombre de archivo MFL.</span><span class="sxs-lookup"><span data-stu-id="e3a20-173">A localized version of the MOF file is also created with an MFL file name extension.</span></span> <span data-ttu-id="e3a20-174">El parámetro *locale* especifica el nombre del espacio de nombres secundario que contiene las definiciones de clase localizadas.</span><span class="sxs-lookup"><span data-stu-id="e3a20-174">The *Locale* parameter specifies the name of the child namespace that contains the localized class definitions.</span></span> <span data-ttu-id="e3a20-175">El formato del parámetro de *configuración regional* es ms \_ xxx, donde xxx es el valor hexadecimal del LCID de Windows.</span><span class="sxs-lookup"><span data-stu-id="e3a20-175">The format of the *Locale* parameter is MS\_xxx where xxx is the hexadecimal value of the Windows LCID.</span></span> <span data-ttu-id="e3a20-176">Por ejemplo, la configuración regional de inglés americano es MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="e3a20-176">For example, the locale for American English is MS\_409.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <** _ResourceName_*_>_*</span><span class="sxs-lookup"><span data-stu-id="e3a20-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <**_ResourceName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-178">Extrae MOF binario de un recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="e3a20-178">Extracts binary MOF from a named resource.</span></span> <span data-ttu-id="e3a20-179">Este modificador obtiene el MOF binario de la clase en el repositorio WMI, mientras que el modificador-B crea el formato MOF binario a partir de un archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="e3a20-179">This switch gets the binary MOF from the class in the WMI repository while the -B switch creates the binary MOF format from a MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L: <** _ResourceLocale_*_>_*</span><span class="sxs-lookup"><span data-stu-id="e3a20-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L:<**_ResourceLocale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-181">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e3a20-181">Optional.</span></span> <span data-ttu-id="e3a20-182">Extrae las descripciones de MOF localizadas del MOF binario cuando se usa con el modificador-ER.</span><span class="sxs-lookup"><span data-stu-id="e3a20-182">Extracts the localized MOF descriptions from the binary MOF when used with -ER switch.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span><span class="sxs-lookup"><span data-stu-id="e3a20-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-184">Nombre del archivo que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="e3a20-184">Name of the file to parse.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="e3a20-185">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="e3a20-185">Return Values</span></span>

<span data-ttu-id="e3a20-186">Como primera operación, el compilador MOF realiza una comprobación de sintaxis en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="e3a20-186">As its first operation, the MOF compiler performs a syntax check on the MOF file.</span></span> <span data-ttu-id="e3a20-187">Si el compilador encuentra algún error, imprime un mensaje de error y finaliza el proceso.</span><span class="sxs-lookup"><span data-stu-id="e3a20-187">If the compiler finds any errors, it prints an error message and the process terminates.</span></span>

<span data-ttu-id="e3a20-188">El compilador MOF puede devolver los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="e3a20-188">The MOF compiler can return the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e3a20-189"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="e3a20-189"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-190">Operación de compilación de MOF realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="e3a20-190">MOF compile operation was successful.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-191"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="e3a20-191"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-192">El compilador MOF no se pudo conectar con el servidor WMI.</span><span class="sxs-lookup"><span data-stu-id="e3a20-192">The MOF compiler could not connect with the WMI server.</span></span> <span data-ttu-id="e3a20-193">Esto se debe a un error semántico, como una incompatibilidad con el repositorio WMI existente o un error real, como el error del servidor WMI en iniciarse.</span><span class="sxs-lookup"><span data-stu-id="e3a20-193">This is either because of a semantic error such as an incompatibility with the existing WMI repository or an actual error such as the failure of the WMI server to start.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-194"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="e3a20-194"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-195">Uno o varios modificadores de la línea de comandos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="e3a20-195">One or more command-line switches were not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e3a20-196"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="e3a20-196"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="e3a20-197">Error de sintaxis de MOF.</span><span class="sxs-lookup"><span data-stu-id="e3a20-197">A MOF syntax error occurred.</span></span>

</dd> </dl>

<span data-ttu-id="e3a20-198">Si el archivo MOF se analiza correctamente, pero se realiza un intento de realizar una operación prohibida por un modificador de la línea de comandos, el compilador devuelve un código de error generado por WMI en lugar de cualquiera de los códigos de retorno que aparecen en la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="e3a20-198">If the MOF file is parsed correctly, but an attempt is made to perform an operation that is forbidden by a command-line switch, the compiler returns an error code generated by WMI instead of any of the return codes listed in the list preceding.</span></span> <span data-ttu-id="e3a20-199">Por ejemplo, se devuelve un código de error de WMI cuando se especifica el modificador **-Instance: updateonly** y el archivo MOF intenta crear una instancia.</span><span class="sxs-lookup"><span data-stu-id="e3a20-199">For example, a WMI error code is returned when the **-instance:updateonly** switch is specified and the MOF file attempts to create an instance.</span></span>

<span data-ttu-id="e3a20-200">Si la instrucción [**\# pragma autorecover**](pragma-autorecover.md) preprocesser no está en el archivo, se devuelve la siguiente ADVERTENCIA:</span><span class="sxs-lookup"><span data-stu-id="e3a20-200">If the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement is not in the file, then the following warning is returned:</span></span>

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a><span data-ttu-id="e3a20-201">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3a20-201">Remarks</span></span>

<span data-ttu-id="e3a20-202">El compilador MOF está disponible en el directorio% WINDIR% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="e3a20-202">The MOF Compiler is available in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="e3a20-203">Debe especificar el archivo MOF como el parámetro del compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="e3a20-203">You must specify the MOF file as the parameter of the MOF Compiler.</span></span> <span data-ttu-id="e3a20-204">También puede especificar un modificador de Autorrecuperación si desea que el archivo MOF se vuelva a compilar automáticamente si alguna vez el repositorio CIM tiene que recuperarse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e3a20-204">You can also specify an Autorecover switch if you want the MOF file to be automatically recompiled if the CIM Repository ever has to be automatically recovered.</span></span> <span data-ttu-id="e3a20-205">Para obtener más información, escriba **MOFCOMP/?**</span><span class="sxs-lookup"><span data-stu-id="e3a20-205">For more information, type **Mofcomp /?**</span></span> <span data-ttu-id="e3a20-206">en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="e3a20-206">at the command prompt.</span></span>

<span data-ttu-id="e3a20-207">Un archivo MOF que utiliza el juego de caracteres Unicode contiene una firma como los dos primeros bytes del archivo.</span><span class="sxs-lookup"><span data-stu-id="e3a20-207">A MOF file that uses the Unicode character set contains a signature as the first two bytes of the file.</span></span> <span data-ttu-id="e3a20-208">Esta firma es U + FFFE o U + FEFF, dependiendo del orden de bytes del archivo.</span><span class="sxs-lookup"><span data-stu-id="e3a20-208">This signature is either U+FFFE or U+FEFF, depending on the byte ordering of the file.</span></span>

<span data-ttu-id="e3a20-209">Cuando no se producen errores en el proceso de análisis, el compilador MOF se conecta al servidor WMI que se ejecuta en el equipo local, a menos que se especifique el modificador **-check** .</span><span class="sxs-lookup"><span data-stu-id="e3a20-209">When no errors occur in the parsing process, the MOF compiler connects to the WMI server running on the local computer unless the **-check** switch is specified.</span></span> <span data-ttu-id="e3a20-210">Las clases e instancias definidas en el archivo MOF se agregan al repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="e3a20-210">Classes and instances defined in the MOF file are added to the WMI repository.</span></span>

<span data-ttu-id="e3a20-211">Cuando se produce un error al actualizar el repositorio WMI, el compilador no intenta devolver el repositorio a su estado anterior a que el compilador comenzó el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="e3a20-211">When an error occurs in updating the WMI repository, the compiler makes no attempt to return the repository to its state before the compiler began processing.</span></span>

<span data-ttu-id="e3a20-212">**Windows 8:** Al instalar un proveedor, MOFCOMP trata los \[ \] calificadores de clave y \[ estáticos \] como true si están presentes, independientemente de sus valores reales.</span><span class="sxs-lookup"><span data-stu-id="e3a20-212">**Windows 8:** When installing a provider, mofcomp treats the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="e3a20-213">Otros calificadores se tratan como false si están presentes pero no se establecen explícitamente en true.</span><span class="sxs-lookup"><span data-stu-id="e3a20-213">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a20-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3a20-214">Requirements</span></span>



| <span data-ttu-id="e3a20-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a20-215">Requirement</span></span> | <span data-ttu-id="e3a20-216">Value</span><span class="sxs-lookup"><span data-stu-id="e3a20-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e3a20-217">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3a20-217">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a20-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3a20-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e3a20-219">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3a20-219">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a20-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3a20-220">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3a20-221">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3a20-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a20-222">**pragma (espacio de nombres)**</span><span class="sxs-lookup"><span data-stu-id="e3a20-222">**pragma namespace**</span></span>](pragma-namespace.md)
</dt> <dt>

[<span data-ttu-id="e3a20-223">Compilar archivos MOF</span><span class="sxs-lookup"><span data-stu-id="e3a20-223">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="e3a20-224">Compilar archivos MOF localizados</span><span class="sxs-lookup"><span data-stu-id="e3a20-224">Compiling Localized MOF Files</span></span>](compiling-localized-mof-files.md)
</dt> <dt>

[<span data-ttu-id="e3a20-225">Registrar un proveedor</span><span class="sxs-lookup"><span data-stu-id="e3a20-225">Registering a Provider</span></span>](registering-a-provider.md)
</dt> <dt>

[<span data-ttu-id="e3a20-226">**IMOFCompiler::CompileFile**</span><span class="sxs-lookup"><span data-stu-id="e3a20-226">**IMOFCompiler::CompileFile**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

