---
description: La tabla SelfReg contiene información sobre los módulos que deben registrarse por sí mismos.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Tabla SelfReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5895b1d23369a7c121547fed841731b5d3e76ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818550"
---
# <a name="selfreg-table"></a><span data-ttu-id="f7312-103">Tabla SelfReg</span><span class="sxs-lookup"><span data-stu-id="f7312-103">SelfReg Table</span></span>

<span data-ttu-id="f7312-104">La tabla SelfReg contiene información sobre los módulos que deben registrarse por sí mismos.</span><span class="sxs-lookup"><span data-stu-id="f7312-104">The SelfReg table contains information about modules that need to be self registered.</span></span> <span data-ttu-id="f7312-105">El instalador llama a la función [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) durante la instalación del módulo; llama a [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) durante la desinstalación del módulo.</span><span class="sxs-lookup"><span data-stu-id="f7312-105">The installer calls the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function during installation of the module; it calls [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) during uninstallation of the module.</span></span> <span data-ttu-id="f7312-106">El instalador no registra automáticamente los archivos EXE.</span><span class="sxs-lookup"><span data-stu-id="f7312-106">The installer does not self register EXE files.</span></span>

<span data-ttu-id="f7312-107">La tabla SelfReg tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f7312-107">The SelfReg table has the following columns.</span></span>



| <span data-ttu-id="f7312-108">Columna</span><span class="sxs-lookup"><span data-stu-id="f7312-108">Column</span></span> | <span data-ttu-id="f7312-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f7312-109">Type</span></span>                         | <span data-ttu-id="f7312-110">Clave</span><span class="sxs-lookup"><span data-stu-id="f7312-110">Key</span></span> | <span data-ttu-id="f7312-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="f7312-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="f7312-112">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="f7312-112">File\_</span></span> | [<span data-ttu-id="f7312-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="f7312-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="f7312-114">Y</span><span class="sxs-lookup"><span data-stu-id="f7312-114">Y</span></span>   | <span data-ttu-id="f7312-115">N</span><span class="sxs-lookup"><span data-stu-id="f7312-115">N</span></span>        |
| <span data-ttu-id="f7312-116">Costos</span><span class="sxs-lookup"><span data-stu-id="f7312-116">Cost</span></span>   | [<span data-ttu-id="f7312-117">Entero</span><span class="sxs-lookup"><span data-stu-id="f7312-117">Integer</span></span>](integer.md)       | <span data-ttu-id="f7312-118">N</span><span class="sxs-lookup"><span data-stu-id="f7312-118">N</span></span>   | <span data-ttu-id="f7312-119">Y</span><span class="sxs-lookup"><span data-stu-id="f7312-119">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f7312-120">Columnas</span><span class="sxs-lookup"><span data-stu-id="f7312-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f7312-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_</span><span class="sxs-lookup"><span data-stu-id="f7312-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="f7312-122">Clave externa en la primera columna de la [tabla de archivos](file-table.md) que indica el módulo que se debe registrar.</span><span class="sxs-lookup"><span data-stu-id="f7312-122">External key into the first column of the [File table](file-table.md) indicating the module that needs to be registered.</span></span>

</dd> <dt>

<span data-ttu-id="f7312-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Costará</span><span class="sxs-lookup"><span data-stu-id="f7312-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="f7312-124">Costo de registrar el módulo en bytes.</span><span class="sxs-lookup"><span data-stu-id="f7312-124">The cost of registering the module in bytes.</span></span> <span data-ttu-id="f7312-125">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="f7312-125">This must be a non-negative number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7312-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7312-126">Remarks</span></span>

<span data-ttu-id="f7312-127">Se recomienda encarecidamente el uso del registro automático a los autores de paquetes de instalación.</span><span class="sxs-lookup"><span data-stu-id="f7312-127">Installation package authors are strongly advised against using self registration.</span></span> <span data-ttu-id="f7312-128">En su lugar, deben registrar los módulos mediante la creación de una o varias tablas proporcionadas por el instalador para este fin.</span><span class="sxs-lookup"><span data-stu-id="f7312-128">Instead they should register modules by authoring one or more tables provided by the installer for this purpose.</span></span> <span data-ttu-id="f7312-129">Para obtener más información, consulte [grupo de tablas del registro](registry-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="f7312-129">For more information, see [Registry Tables Group](registry-tables-group.md).</span></span> <span data-ttu-id="f7312-130">Muchas de las ventajas de tener un servicio de instalador central se pierden con el registro automático porque las rutinas de registro automático suelen ocultar la información de configuración crítica.</span><span class="sxs-lookup"><span data-stu-id="f7312-130">Many of the benefits of having a central installer service are lost with self registration because self-registration routines tend to hide critical configuration information.</span></span> <span data-ttu-id="f7312-131">Entre los motivos para evitar el registro propio se incluyen:</span><span class="sxs-lookup"><span data-stu-id="f7312-131">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="f7312-132">La reversión de una instalación con módulos autoregistrados no puede realizarse de forma segura con [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) porque no hay ninguna manera de indicar si otras características o aplicaciones usan las claves registradas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f7312-132">Rollback of an installation with self-registered modules cannot be safely done using [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) because there is no way of telling if the self-registered keys are used by another feature or application.</span></span>
-   <span data-ttu-id="f7312-133">La capacidad de usar el anuncio se reduce si el registro de la clase o del servidor de extensiones se realiza en rutinas de registro automático.</span><span class="sxs-lookup"><span data-stu-id="f7312-133">The ability to use advertisement is reduced if Class or extension server registration is performed within self-registration routines.</span></span>
-   <span data-ttu-id="f7312-134">El instalador controla automáticamente las claves HKCR en las tablas del registro para las instalaciones por usuario o por equipo.</span><span class="sxs-lookup"><span data-stu-id="f7312-134">The installer automatically handles HKCR keys in the registry tables for both per-user or per-machine installations.</span></span> <span data-ttu-id="f7312-135">Actualmente, las rutinas de [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) no admiten la noción de una clave HKCR por usuario.</span><span class="sxs-lookup"><span data-stu-id="f7312-135">[**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) routines currently do not support the notion of a per-user HKCR key.</span></span>
-   <span data-ttu-id="f7312-136">Si varios usuarios utilizan una aplicación autoregistrada en el mismo equipo, cada usuario debe instalar la aplicación la primera vez que la ejecuta.</span><span class="sxs-lookup"><span data-stu-id="f7312-136">If multiple users are using a self-registered application on the same computer, each user must install the application the first time they run it.</span></span> <span data-ttu-id="f7312-137">En caso contrario, el instalador no puede determinar fácilmente que existen las claves del registro HKCU apropiadas.</span><span class="sxs-lookup"><span data-stu-id="f7312-137">Otherwise the installer cannot easily determine that the proper HKCU registry keys exist.</span></span>
-   <span data-ttu-id="f7312-138">Se puede denegar el acceso a la red [**a los recursos**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) de red, como las bibliotecas de tipos, si un componente se especifica como Run-from-Source y aparece en la tabla SelfReg.</span><span class="sxs-lookup"><span data-stu-id="f7312-138">The [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) can be denied access to network resources such as type libraries if a component is both specified as run-from-source and is listed in the SelfReg table.</span></span> <span data-ttu-id="f7312-139">Esto puede hacer que se produzca un error en la instalación del componente durante una instalación administrativa.</span><span class="sxs-lookup"><span data-stu-id="f7312-139">This can cause the installation of the component to fail to during an administrative installation.</span></span>
-   <span data-ttu-id="f7312-140">Los archivos dll de registro automático son más susceptibles a errores de codificación porque el nuevo código necesario para [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) es normalmente diferente para cada archivo dll.</span><span class="sxs-lookup"><span data-stu-id="f7312-140">Self-registering DLLs are more susceptible to coding errors because the new code required for [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) is commonly different for each DLL.</span></span> <span data-ttu-id="f7312-141">En su lugar, use las tablas del registro en la base de datos para aprovechar el código existente proporcionado por el instalador.</span><span class="sxs-lookup"><span data-stu-id="f7312-141">Instead use the registry tables in the database to take advantage of existing code provided by the installer.</span></span>
-   <span data-ttu-id="f7312-142">A veces, los archivos dll de registro automático pueden vincularse a archivos dll auxiliares que no estén presentes o que tengan una versión incorrecta.</span><span class="sxs-lookup"><span data-stu-id="f7312-142">Self-registering DLLs can sometimes link to auxiliary DLLs that are not present or are the wrong version.</span></span> <span data-ttu-id="f7312-143">En cambio, el instalador puede registrar los archivos DLL mediante las tablas del registro sin depender del estado actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="f7312-143">In contrast, the installer can register the DLLs using the registry tables with no dependency on the current state of the system.</span></span>

> [!Note]  
> <span data-ttu-id="f7312-144">No se puede especificar el orden en el que el instalador registra o anula el registro de los archivos dll de registro automático mediante las acciones [SelfRegModules](selfregmodules-action.md) y [SelfUnRegModules](selfunregmodules-action.md) .</span><span class="sxs-lookup"><span data-stu-id="f7312-144">You cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="f7312-145">Vea [especificar el orden de registro automático](specifying-the-order-of-self-registration.md).</span><span class="sxs-lookup"><span data-stu-id="f7312-145">See [Specifying the Order of Self Registration](specifying-the-order-of-self-registration.md).</span></span>

 

## <a name="validation"></a><span data-ttu-id="f7312-146">Validación</span><span class="sxs-lookup"><span data-stu-id="f7312-146">Validation</span></span>

<dl>

[<span data-ttu-id="f7312-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="f7312-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f7312-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="f7312-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f7312-149">ICE32</span><span class="sxs-lookup"><span data-stu-id="f7312-149">ICE32</span></span>](ice32.md)  
</dl>

 

 
