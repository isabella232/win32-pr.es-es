---
description: Los elementos del panel de control que se implementan en un archivo DLL que exporta la función CPlApplet tienen distintos requisitos de registro que los archivos. exe.
title: Cómo registrar elementos del panel de control DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813699"
---
# <a name="how-to-register-dll-control-panel-items"></a><span data-ttu-id="edfda-103">Cómo registrar elementos del panel de control DLL</span><span class="sxs-lookup"><span data-stu-id="edfda-103">How to Register DLL Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="edfda-104">Instrucciones de implementación actuales indican que los nuevos elementos del panel de control deben implementarse como archivos. exe en lugar de como archivos. cpl.</span><span class="sxs-lookup"><span data-stu-id="edfda-104">Current implementation guidelines state that new Control Panel items should be implemented as .exe files rather than .cpl files.</span></span> <span data-ttu-id="edfda-105">La siguiente información se incluye principalmente para fines heredados.</span><span class="sxs-lookup"><span data-stu-id="edfda-105">The following information is included mainly for legacy purposes.</span></span>

 

<span data-ttu-id="edfda-106">Los elementos del panel de control que se implementan en un archivo DLL que exporta la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) tienen distintos requisitos de registro que los archivos. exe.</span><span class="sxs-lookup"><span data-stu-id="edfda-106">Control Panel items that are implemented in a DLL that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function have different registration requirements than .exe files.</span></span> <span data-ttu-id="edfda-107">A partir de Windows XP, los nuevos archivos dll de los elementos del panel de control deben instalarse en la carpeta de la aplicación asociada en la carpeta archivos de programa.</span><span class="sxs-lookup"><span data-stu-id="edfda-107">As of Windows XP, new Control Panel item DLLs should be installed in the associated application's folder under the Program Files folder.</span></span> <span data-ttu-id="edfda-108">No es necesario registrar los elementos que se almacenan en el directorio system32 con una extensión. cpl; se muestran automáticamente en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="edfda-108">Items that are stored in the System32 directory with a .cpl extension do not need to be registered; they are automatically shown in the Control Panel.</span></span> <span data-ttu-id="edfda-109">Todos los demás elementos del panel de control que usan **CPlApplet** deben estar registrados de una de estas dos maneras:</span><span class="sxs-lookup"><span data-stu-id="edfda-109">All other Control Panel items that use **CPlApplet** must be registered in one of two ways:</span></span>

-   <span data-ttu-id="edfda-110">Si el elemento del panel de control va a estar disponible para todos los usuarios, registre la ruta de acceso por equipo agregando un valor de **reg \_ Expand \_ SZ** a la subclave **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **control panel** \\ **CPLS** , que se establece en la ruta de acceso del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="edfda-110">If the Control Panel item is to be available to all users, register the path on a per-computer basis by adding a **REG\_EXPAND\_SZ** value to the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Control Panel**\\**Cpls** subkey, set to the DLL path.</span></span>
-   <span data-ttu-id="edfda-111">Si el elemento del panel de control va a estar disponible por usuario, use **HKEY \_ Current \_ User** como clave raíz en lugar de **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="edfda-111">If the Control Panel item is to be available on a per-user basis, use **HKEY\_CURRENT\_USER** as the root key instead of **HKEY\_LOCAL\_MACHINE**.</span></span>

<span data-ttu-id="edfda-112">Los dos ejemplos siguientes registran el elemento del panel de control *MyCplApp* .</span><span class="sxs-lookup"><span data-stu-id="edfda-112">The following two examples register the *MyCplApp* Control Panel item.</span></span> <span data-ttu-id="edfda-113">El archivo DLL se denomina MyCpl.cpl y se encuentra en el directorio de aplicación de *MiOrg \\ MyApp* .</span><span class="sxs-lookup"><span data-stu-id="edfda-113">The DLL is named MyCpl.cpl and is located in the *MyCorp\\MyApp* application directory.</span></span> <span data-ttu-id="edfda-114">En este primer ejemplo se muestra el registro por equipo.</span><span class="sxs-lookup"><span data-stu-id="edfda-114">This first example illustrates per-computer registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="edfda-115">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="edfda-115">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="edfda-116">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="edfda-116">Step 1:</span></span>

<span data-ttu-id="edfda-117">Agregue esta información al registro para registrar la existencia del archivo. cpl.</span><span class="sxs-lookup"><span data-stu-id="edfda-117">Add this information to the registry to register the existence of the .cpl file.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a><span data-ttu-id="edfda-118">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="edfda-118">Step 2:</span></span>

<span data-ttu-id="edfda-119">**Windows Vista y versiones posteriores:** Agregue esta información adicional al registro para proporcionar un GUID para el elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="edfda-119">**Windows Vista and later:** Add this additional information to the registry to provide a GUID for the Control Panel item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

<span data-ttu-id="edfda-120">Al generar un GUID para identificar de forma única el elemento del panel de control, puede Agregar vínculos de tarea al panel de control.</span><span class="sxs-lookup"><span data-stu-id="edfda-120">By generating a GUID to uniquely identify the Control Panel item, you can add task links to the Control Panel.</span></span> <span data-ttu-id="edfda-121">Sin este GUID, no hay ninguna manera de asociar los vínculos de tarea con el elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="edfda-121">Without this GUID, there is no way for the task links to be associated with the Control Panel item.</span></span> <span data-ttu-id="edfda-122">Consulte [crear vínculos de tarea que se pueden buscar para un elemento del panel de control](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="edfda-122">See [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="edfda-123">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="edfda-123">Step 3:</span></span>

<span data-ttu-id="edfda-124">**Windows Vista y versiones posteriores:** Agregue la siguiente información al registro para crear un nombre canónico para el elemento.</span><span class="sxs-lookup"><span data-stu-id="edfda-124">**Windows Vista and later:** Add the following information to the registry to create a canonical name for the item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

<span data-ttu-id="edfda-125">Al agregar un nombre canónico, los usuarios pueden iniciar el elemento del panel de control desde una línea de comandos escribiendo `control.exe /name MyCorporation.MyCpl` .</span><span class="sxs-lookup"><span data-stu-id="edfda-125">By adding a canonical name, users can launch the Control Panel item from a command line by entering `control.exe /name MyCorporation.MyCpl`.</span></span> <span data-ttu-id="edfda-126">Esto también permite cambiar una implementación de un archivo. cpl a un archivo. exe más adelante, sin necesidad de que los programas que llaman realicen cambios, ya que pueden continuar abriendo el elemento a través de su nombre canónico.</span><span class="sxs-lookup"><span data-stu-id="edfda-126">This also makes it possible to change an implementation from a .cpl file to a .exe file later, without requiring calling programs to make any changes since they can continue opening the item through its canonical name.</span></span> <span data-ttu-id="edfda-127">Para obtener más información sobre los nombres canónicos, vea [Ejecutar elementos del panel de control](executing-control-panel-items.md).</span><span class="sxs-lookup"><span data-stu-id="edfda-127">For more information on canonical names, see [Executing Control Panel Items](executing-control-panel-items.md).</span></span>

### <a name="step-4"></a><span data-ttu-id="edfda-128">Paso 4:</span><span class="sxs-lookup"><span data-stu-id="edfda-128">Step 4:</span></span>

<span data-ttu-id="edfda-129">**Windows Vista y versiones posteriores:** Agregue la siguiente información al registro para asignar un elemento del panel de control a una o varias categorías.</span><span class="sxs-lookup"><span data-stu-id="edfda-129">**Windows Vista and later:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="edfda-130">**Windows XP:** Agregue la siguiente información al registro para asignar un elemento del panel de control a una o varias categorías.</span><span class="sxs-lookup"><span data-stu-id="edfda-130">**Windows XP:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="edfda-131">En este ejemplo se asigna el elemento a la categoría 3, que es red e Internet.</span><span class="sxs-lookup"><span data-stu-id="edfda-131">This example assigns the item to category 3, which is Network and Internet.</span></span> <span data-ttu-id="edfda-132">Para agregar un elemento a varias categorías, proporcione la lista como un valor de REG \_ SZ separado por comas, como "3, 8".</span><span class="sxs-lookup"><span data-stu-id="edfda-132">To add an item to multiple categories, provide the list as a REG\_SZ value separated by commas, such as "3,8".</span></span> <span data-ttu-id="edfda-133">Los valores se pueden proporcionar en formato decimal o hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="edfda-133">Values can be provided as either decimal or hexadecimal.</span></span> <span data-ttu-id="edfda-134">Tenga en cuenta que la capacidad de agregar un elemento a varias categorías solo es posible en Windows XP Service Pack 2 (SP2) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="edfda-134">Note that the ability to add an item to multiple categories is only possible in Windows XP Service Pack 2 (SP2) and later.</span></span> <span data-ttu-id="edfda-135">Vea [asignar categorías del panel de control](assigning-control-panel-categories.md) para todos los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="edfda-135">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for all possible values.</span></span>

### <a name="step-5"></a><span data-ttu-id="edfda-136">Paso 5:</span><span class="sxs-lookup"><span data-stu-id="edfda-136">Step 5:</span></span>

<span data-ttu-id="edfda-137">**Windows Vista y versiones posteriores:** Agregue la siguiente información al registro para crear y apuntar a un archivo XML que contenga vínculos de tareas para el elemento.</span><span class="sxs-lookup"><span data-stu-id="edfda-137">**Windows Vista and later:** Add the following information to the registry to create and point to an XML file to hold task links for the item.</span></span> <span data-ttu-id="edfda-138">El valor debe ser una \_ ruta de acceso reg SZ como se muestra aquí o un identificador de módulo y de recurso (por ejemplo, "C: \\ archivos de programa \\ Corp \\ \\MyApp.exe,-31") si es un recurso incrustado.</span><span class="sxs-lookup"><span data-stu-id="edfda-138">The value must be a REG\_SZ path as shown here or a module and resource ID (for example, "C:\\Program Files\\MyCorp\\MyApp\\MyApp.exe,-31") if it is an embedded resource.</span></span> <span data-ttu-id="edfda-139">La ubicación del archivo XML debe especificarse por completo.</span><span class="sxs-lookup"><span data-stu-id="edfda-139">The location of the XML file should be fully specified.</span></span> <span data-ttu-id="edfda-140">No puede usar una variable de entorno como% ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="edfda-140">It cannot use an environment variable such as %ProgramFiles%.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

<span data-ttu-id="edfda-141">Para obtener más información sobre los vínculos de tarea y cómo crear el archivo XML que los contiene, vea [crear vínculos de tarea que se pueden buscar para un elemento del panel de control](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="edfda-141">For more details on task links and how to create the XML file to hold them, see [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="edfda-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edfda-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edfda-143">Registrar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="edfda-143">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="edfda-144">Cómo registrar elementos del panel de control ejecutable</span><span class="sxs-lookup"><span data-stu-id="edfda-144">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
