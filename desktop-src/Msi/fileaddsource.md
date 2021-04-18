---
description: El valor de la propiedad FILEADDSOURCE denota una lista de claves de archivo delimitadas por comas que se instalarán para ejecutarse desde el medio de origen.
ms.assetid: 52e328e7-7a98-4762-86a1-48e52fd55882
title: Propiedad FILEADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b99ea1d9f4d6e212b74d6c4ee54655dce98c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690012"
---
# <a name="fileaddsource-property"></a><span data-ttu-id="28691-103">Propiedad FILEADDSOURCE</span><span class="sxs-lookup"><span data-stu-id="28691-103">FILEADDSOURCE property</span></span>

<span data-ttu-id="28691-104">El valor de la propiedad **FILEADDSOURCE** denota una lista de claves de archivo delimitadas por comas que se instalarán para ejecutarse desde el medio de origen.</span><span class="sxs-lookup"><span data-stu-id="28691-104">The value of the **FILEADDSOURCE** property denotes a list of file keys delimited by commas that are to be installed to run from the source media.</span></span> <span data-ttu-id="28691-105">Para cada clave de archivo de la lista, el instalador determina el componente que controla ese archivo y, a continuación, examina todas las características vinculadas a ese componente por la tabla [FeatureComponents](featurecomponents-table.md) e instala la característica que requiere la menor cantidad de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="28691-105">For each file key in the list, the installer determines the component that controls that file, then examines all features linked to that component by the [FeatureComponents](featurecomponents-table.md) table and installs the feature that requires the least amount of disk space.</span></span> <span data-ttu-id="28691-106">Las claves de archivo de la lista deben estar presentes en la columna archivo de la tabla [archivo](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="28691-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="28691-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28691-107">Remarks</span></span>

<span data-ttu-id="28691-108">Tenga en cuenta que los nombres de clave de archivo distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="28691-108">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="28691-109">Tenga en cuenta también que si la marca de bits de LocalOnly está establecida en la columna atributos de la tabla [componente](component-table.md) para un componente, el componente se instala para ejecutarse localmente.</span><span class="sxs-lookup"><span data-stu-id="28691-109">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="28691-110">El instalador siempre evalúa las siguientes propiedades en el orden siguiente.</span><span class="sxs-lookup"><span data-stu-id="28691-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="28691-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="28691-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="28691-112">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="28691-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="28691-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="28691-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="28691-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="28691-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="28691-115">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="28691-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="28691-116">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="28691-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="28691-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="28691-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="28691-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="28691-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="28691-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="28691-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="28691-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="28691-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. <span data-ttu-id="28691-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="28691-121">**FILEADDSOURCE**</span></span>
12. [<span data-ttu-id="28691-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="28691-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="28691-123">Por ejemplo, si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = función, todas las características se establecen primero en Run-local y, a continuación, se establece la función de ejecución-desde-origen.</span><span class="sxs-lookup"><span data-stu-id="28691-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="28691-124">Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL = función, First la función se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = ALL, todas las características (incluidas las funciones) se restablecen a la ejecución desde el origen.</span><span class="sxs-lookup"><span data-stu-id="28691-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="28691-125">El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="28691-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="28691-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28691-126">Requirements</span></span>



| <span data-ttu-id="28691-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="28691-127">Requirement</span></span> | <span data-ttu-id="28691-128">Value</span><span class="sxs-lookup"><span data-stu-id="28691-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28691-129">Versión</span><span class="sxs-lookup"><span data-stu-id="28691-129">Version</span></span><br/> | <span data-ttu-id="28691-130">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="28691-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="28691-131">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="28691-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="28691-132">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="28691-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="28691-133">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="28691-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28691-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="28691-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28691-135">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28691-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




