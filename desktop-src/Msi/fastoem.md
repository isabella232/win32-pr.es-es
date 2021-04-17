---
description: La propiedad FASTOEM está diseñada para permitir a los OEM reducir el tiempo necesario para instalar Windows Installer aplicaciones para un escenario específico.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: propiedad FASTOEM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690988"
---
# <a name="fastoem-property"></a><span data-ttu-id="271eb-103">propiedad FASTOEM</span><span class="sxs-lookup"><span data-stu-id="271eb-103">FASTOEM property</span></span>

<span data-ttu-id="271eb-104">La propiedad **FASTOEM** está diseñada para permitir a los OEM reducir el tiempo necesario para instalar Windows Installer aplicaciones para un escenario específico.</span><span class="sxs-lookup"><span data-stu-id="271eb-104">The **FASTOEM** property is designed to enable OEMs to reduce the time it takes to install Windows Installer applications for a specific scenario.</span></span> <span data-ttu-id="271eb-105">No cree la propiedad **FASTOEM** en la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="271eb-105">Do not author the **FASTOEM** property into the [Property Table](property-table.md).</span></span>

<span data-ttu-id="271eb-106">La propiedad **FASTOEM** solo es aplicable si se cumplen todas estas condiciones:</span><span class="sxs-lookup"><span data-stu-id="271eb-106">The **FASTOEM** property is only applicable if all of these conditions are true:</span></span>

-   <span data-ttu-id="271eb-107">La aplicación se está instalando en el mismo volumen que la carpeta que contiene los archivos de origen.</span><span class="sxs-lookup"><span data-stu-id="271eb-107">The application is being installed on the same volume as the folder containing the source files.</span></span>
-   <span data-ttu-id="271eb-108">Los archivos de origen se eliminan después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="271eb-108">The source files are deleted after the installation.</span></span>
-   <span data-ttu-id="271eb-109">No se muestra ninguna interfaz de usuario durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="271eb-109">No user interface is displayed during the installation.</span></span> <span data-ttu-id="271eb-110">El [nivel](user-interface-levels.md) de la interfaz de usuario es None.</span><span class="sxs-lookup"><span data-stu-id="271eb-110">The [user interface level](user-interface-levels.md) is none.</span></span>
-   <span data-ttu-id="271eb-111">La instalación se realiza en el [contexto de instalación](installation-context.md)por máquina.</span><span class="sxs-lookup"><span data-stu-id="271eb-111">The installation is performed in the per-machine [installation context](installation-context.md).</span></span>
-   <span data-ttu-id="271eb-112">Hay suficiente espacio en el equipo para una instalación correcta.</span><span class="sxs-lookup"><span data-stu-id="271eb-112">There is enough space on the computer for a successful installation.</span></span>
-   <span data-ttu-id="271eb-113">Esta es la primera vez que se instala.</span><span class="sxs-lookup"><span data-stu-id="271eb-113">This is first time installation.</span></span> <span data-ttu-id="271eb-114">La instalación no está anunciando, reinstalando, quitando o realizando una instalación administrativa.</span><span class="sxs-lookup"><span data-stu-id="271eb-114">The installation is not advertising, reinstalling, removing, or doing an administrative installation.</span></span>
-   <span data-ttu-id="271eb-115">No hay características instaladas para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="271eb-115">No features are installed to run from source.</span></span>
-   <span data-ttu-id="271eb-116">El paquete de instalación no contiene ningún [componente aislado](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="271eb-116">The installation package contains no [isolated components](isolated-components.md).</span></span> <span data-ttu-id="271eb-117">Dado que los componentes aislados requieren que los archivos de código fuente permanezcan ubicados en el origen, la propiedad **FASTOEM** no se puede usar actualmente con componentes aislados.</span><span class="sxs-lookup"><span data-stu-id="271eb-117">Because isolated components require source files to remain located at the source, the **FASTOEM** property cannot currently be used with isolated components.</span></span>

<span data-ttu-id="271eb-118">Si se cumplen todas las condiciones anteriores, el establecimiento de la propiedad **FASTOEM** permite a Windows Installer mejorar el rendimiento haciendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="271eb-118">If all of the previous conditions are true, setting the **FASTOEM** property enables Windows Installer to improve performance by doing the following:</span></span>

-   <span data-ttu-id="271eb-119">Mueva en lugar de copiar archivos en el mismo volumen.</span><span class="sxs-lookup"><span data-stu-id="271eb-119">Move rather than copy files on the same volume.</span></span> <span data-ttu-id="271eb-120">Esto no garantiza que todos los archivos se muevan en lugar de copiarse.</span><span class="sxs-lookup"><span data-stu-id="271eb-120">This does not guarantee that all files are moved rather than copied.</span></span> <span data-ttu-id="271eb-121">Tenga en cuenta que si el equipo tiene varias unidades de disco duro, debe inicializar la propiedad [**ROOTDRIVE**](rootdrive.md) en la línea de comandos en la misma unidad que contiene el origen de instalación.</span><span class="sxs-lookup"><span data-stu-id="271eb-121">Note that if the computer has multiple hard drives, you must initialize the [**ROOTDRIVE**](rootdrive.md) property on the command line to the same drive containing the installation source.</span></span>
-   <span data-ttu-id="271eb-122">Omita este origen de la lista de origen de la aplicación para que las instalaciones de reinstalación o mantenimiento posteriores tengan como valor predeterminado los orígenes de CD-ROM especificados en la [tabla de medios](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="271eb-122">Omit this source from the application's source list so that subsequent reinstallation or maintenance installations default to the CD-ROM sources specified in the [Media Table](media-table.md).</span></span>
-   <span data-ttu-id="271eb-123">Optimice el costo de los [archivos](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="271eb-123">Streamline [file costing](file-costing.md).</span></span>
-   <span data-ttu-id="271eb-124">Suprime los mensajes de progreso enviados desde Windows Installer al cliente.</span><span class="sxs-lookup"><span data-stu-id="271eb-124">Suppress progress messages sent from Windows Installer to the client.</span></span>

## <a name="remarks"></a><span data-ttu-id="271eb-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="271eb-125">Remarks</span></span>

<span data-ttu-id="271eb-126">Dado que no se envía ningún mensaje de progreso cuando se establece **FASTOEM** , se recomienda que los autores escriban manualmente un valor de 1800 para el tiempo de espera en la clave.</span><span class="sxs-lookup"><span data-stu-id="271eb-126">Because no progress messages are sent when **FASTOEM** is set, it is recommended that authors manually write a value of 1800 for Timeout into the key</span></span>

<span data-ttu-id="271eb-127">**HKLM** \\ **Software** \\ de **Directivas** \\ de **Microsoft** \\ **Windows** \\ **Instalador** \\ de **Tiempo de espera**</span><span class="sxs-lookup"><span data-stu-id="271eb-127">**HKLM**\\**SoftWare**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**Timeout**</span></span>

<span data-ttu-id="271eb-128">Timeout es un tipo de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="271eb-128">Timeout is a **REG\_DWORD** type.</span></span>

<span data-ttu-id="271eb-129">Para mostrar el tamaño de la aplicación en Agregar o quitar programas en el panel de control de Windows 2000, debe escribir manualmente el valor de EstimatedSize en la clave.</span><span class="sxs-lookup"><span data-stu-id="271eb-129">To display the size of the application in Add or Remove Programs in the Windows 2000 Control Panel, you must manually write the value of EstimatedSize into the key</span></span>

<span data-ttu-id="271eb-130">**HKLM** \\ **Software** \\ de **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ **<  Código > de producto**</span><span class="sxs-lookup"><span data-stu-id="271eb-130">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\**<*Product Code*>**</span></span>

<span data-ttu-id="271eb-131">Se trata de un tipo de **Registro \_ DWORD** y es igual al tamaño de la aplicación en Kbytes.</span><span class="sxs-lookup"><span data-stu-id="271eb-131">This is a **REG\_DWORD** type and equals to the size of the application in Kbytes.</span></span> <span data-ttu-id="271eb-132">El instalador no escribe este valor automáticamente.</span><span class="sxs-lookup"><span data-stu-id="271eb-132">The installer does not automatically write this value.</span></span>

<span data-ttu-id="271eb-133">Utilice la siguiente línea de comandos de ejemplo si el CD-ROM enviado a los usuarios finales almacena el paquete de instalación de la aplicación en la raíz del CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="271eb-133">Use the following example command line if the CD-ROM shipped to end users stores the application's installation package at the root of the CD-ROM.</span></span> <span data-ttu-id="271eb-134">Tenga en cuenta que la etiqueta de volumen de la [tabla de medios](media-table.md) del archivo. msi debe coincidir con la etiqueta de volumen del CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="271eb-134">Note that the volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span>

<span data-ttu-id="271eb-135">**Msiexec/I C: \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 ROOTDRIVE = C:\\**</span><span class="sxs-lookup"><span data-stu-id="271eb-135">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 ROOTDRIVE=C:\\**</span></span>

<span data-ttu-id="271eb-136">Utilice la siguiente línea de comandos de ejemplo si el paquete de instalación no se encuentra en la raíz del CD-ROM enviado a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="271eb-136">Use the following example command line if the installation package is not located at the root of the CD-ROM shipped to end users.</span></span> <span data-ttu-id="271eb-137">Debe establecer la propiedad [**MEDIAPACKAGEPATH**](mediapackagepath.md) en este caso en la ruta de acceso al paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="271eb-137">You must set the [**MEDIAPACKAGEPATH**](mediapackagepath.md) property in this case to the path to the installation package.</span></span> <span data-ttu-id="271eb-138">La etiqueta de volumen de la [tabla de medios](media-table.md) del archivo. msi debe coincidir con la etiqueta de volumen del CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="271eb-138">The volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span> <span data-ttu-id="271eb-139">En este caso, siga este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="271eb-139">In this case follow this example.</span></span>

<span data-ttu-id="271eb-140">**Msiexec/I C: \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 MEDIAPACKAGEPATH = C: \\ TempImage \\package.msi ROOTDRIVE = c:\\**</span><span class="sxs-lookup"><span data-stu-id="271eb-140">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 MEDIAPACKAGEPATH=C:\\TempImage\\package.msi ROOTDRIVE=C:\\**</span></span>

## <a name="requirements"></a><span data-ttu-id="271eb-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="271eb-141">Requirements</span></span>



| <span data-ttu-id="271eb-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="271eb-142">Requirement</span></span> | <span data-ttu-id="271eb-143">Value</span><span class="sxs-lookup"><span data-stu-id="271eb-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="271eb-144">Versión</span><span class="sxs-lookup"><span data-stu-id="271eb-144">Version</span></span><br/> | <span data-ttu-id="271eb-145">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="271eb-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="271eb-146">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="271eb-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="271eb-147">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="271eb-147">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="271eb-148">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="271eb-148">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="271eb-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="271eb-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="271eb-150">Propiedades</span><span class="sxs-lookup"><span data-stu-id="271eb-150">Properties</span></span>](properties.md)
</dt> </dl>

 

 




