---
description: El valor de la propiedad FILEADDDEFAULT es una lista de claves de archivo delimitadas por comas que se instalan en su configuración predeterminada.
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: Propiedad FILEADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c1afc9658c58b048c4e75232d7e550acb36e57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690014"
---
# <a name="fileadddefault-property"></a><span data-ttu-id="c429d-103">Propiedad FILEADDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="c429d-103">FILEADDDEFAULT property</span></span>

<span data-ttu-id="c429d-104">El valor de la propiedad **FILEADDDEFAULT** es una lista de claves de archivo delimitadas por comas que se instalan en su configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c429d-104">The value of the **FILEADDDEFAULT** property is a list of file keys delimited by commas that are installed in their default configuration.</span></span> <span data-ttu-id="c429d-105">Para cada clave de archivo de la lista, el instalador determina el componente que controla ese archivo e instala la característica que requiere menos espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="c429d-105">For each file key in the list, the installer determines the component that controls that file and installs the feature that requires the least disk space.</span></span> <span data-ttu-id="c429d-106">Las claves de archivo de la lista deben estar presentes en la columna archivo de la tabla [archivo](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c429d-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="c429d-107">Una característica se instala en el mismo estado de instalación que si el usuario hubiera solicitado una instalación a petición de la característica.</span><span class="sxs-lookup"><span data-stu-id="c429d-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="c429d-108">El estado se determina por qué bits se establecen para la característica en la columna Attributes de la [tabla de características](feature-table.md)y qué bits se establecen para los componentes de la característica en la columna Attributes de la [tabla Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c429d-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c429d-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c429d-109">Remarks</span></span>

<span data-ttu-id="c429d-110">Tenga en cuenta que los nombres de clave de archivo distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c429d-110">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="c429d-111">Tenga en cuenta también que si la marca de bits SourceOnly se establece en la columna atributos de la tabla [componente](component-table.md) para un componente, el componente se instala para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="c429d-111">Also note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="c429d-112">El instalador siempre evalúa las siguientes propiedades en el orden siguiente.</span><span class="sxs-lookup"><span data-stu-id="c429d-112">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="c429d-113">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="c429d-113">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="c429d-114">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="c429d-114">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="c429d-115">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="c429d-115">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="c429d-116">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c429d-116">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="c429d-117">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="c429d-117">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="c429d-118">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="c429d-118">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="c429d-119">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="c429d-119">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="c429d-120">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="c429d-120">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="c429d-121">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c429d-121">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="c429d-122">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="c429d-122">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="c429d-123">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="c429d-123">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. <span data-ttu-id="c429d-124">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c429d-124">**FILEADDDEFAULT**</span></span>

<span data-ttu-id="c429d-125">Por ejemplo, si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = función, todas las características se establecen primero en Run-local y, a continuación, se establece la función de ejecución-desde-origen.</span><span class="sxs-lookup"><span data-stu-id="c429d-125">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="c429d-126">Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL = función, First la función se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = ALL, todas las características (incluidas las funciones) se restablecen a la ejecución desde el origen.</span><span class="sxs-lookup"><span data-stu-id="c429d-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="c429d-127">El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="c429d-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="c429d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c429d-128">Requirements</span></span>



| <span data-ttu-id="c429d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c429d-129">Requirement</span></span> | <span data-ttu-id="c429d-130">Value</span><span class="sxs-lookup"><span data-stu-id="c429d-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c429d-131">Versión</span><span class="sxs-lookup"><span data-stu-id="c429d-131">Version</span></span><br/> | <span data-ttu-id="c429d-132">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c429d-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c429d-133">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c429d-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c429d-134">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c429d-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c429d-135">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c429d-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c429d-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c429d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c429d-137">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c429d-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




