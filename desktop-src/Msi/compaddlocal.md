---
description: El valor de la propiedad COMPADDLOCAL es una lista de GUID de componentes de la columna ComponentId de la tabla de componentes, delimitado por comas, que se van a instalar localmente.
ms.assetid: 10c178c5-1eae-4191-b79c-9285810efb6a
title: Propiedad COMPADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e403459f0355c28d66da00170b9c649084afbb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671792"
---
# <a name="compaddlocal-property"></a><span data-ttu-id="509d3-103">Propiedad COMPADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="509d3-103">COMPADDLOCAL property</span></span>

<span data-ttu-id="509d3-104">El valor de la propiedad **COMPADDLOCAL** es una lista de GUID de componentes de la columna ComponentID de la [tabla de componentes](component-table.md), delimitado por comas, que se van a instalar localmente.</span><span class="sxs-lookup"><span data-stu-id="509d3-104">The value of the **COMPADDLOCAL** property is a list of component GUIDs from the ComponentId column of the [Component table](component-table.md), delimited by commas, that are to be installed locally.</span></span> <span data-ttu-id="509d3-105">El instalador usa esta lista para determinar qué características están configuradas para instalarse localmente, en función de los componentes especificados.</span><span class="sxs-lookup"><span data-stu-id="509d3-105">The installer uses this list to determine which features are set to be installed locally, based on the specified components.</span></span> <span data-ttu-id="509d3-106">Para cada identificador de componente de la lista, el instalador examina todas las características vinculadas a ese componente a través de la tabla [FeatureComponents](featurecomponents-table.md) e instala la característica que requiere la menor cantidad de espacio en disco que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="509d3-106">For each listed component ID, the installer examines all features linked to that component through the [FeatureComponents](featurecomponents-table.md) table, and installs the feature that requires the least amount of disk space to install.</span></span> <span data-ttu-id="509d3-107">Los componentes enumerados deben estar presentes en la columna componente de la tabla [componente](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="509d3-107">The components listed must be present in the Component column of the [Component](component-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="509d3-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="509d3-108">Remarks</span></span>

<span data-ttu-id="509d3-109">Tenga en cuenta que los nombres de los componentes distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="509d3-109">Note that the component names are case-sensitive.</span></span> <span data-ttu-id="509d3-110">Tenga en cuenta también que si la marca de bits SourceOnly se establece en la columna atributos de la tabla [componente](component-table.md) para un componente, el componente se instala para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="509d3-110">Also note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="509d3-111">El instalador siempre evalúa las siguientes propiedades en el orden siguiente.</span><span class="sxs-lookup"><span data-stu-id="509d3-111">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="509d3-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="509d3-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="509d3-113">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="509d3-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="509d3-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="509d3-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="509d3-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="509d3-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="509d3-116">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="509d3-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="509d3-117">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="509d3-117">**ADVERTISE**</span></span>](advertise.md)
7.  <span data-ttu-id="509d3-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="509d3-118">**COMPADDLOCAL**</span></span>
8.  [<span data-ttu-id="509d3-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="509d3-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="509d3-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="509d3-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="509d3-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="509d3-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="509d3-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="509d3-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="509d3-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="509d3-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="509d3-124">Por ejemplo, si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = función, todas las características se establecen primero en Run-local y, a continuación, se establece la función de ejecución-desde-origen.</span><span class="sxs-lookup"><span data-stu-id="509d3-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="509d3-125">Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL = función, First la función se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = ALL, todas las características (incluidas las funciones) se restablecen a la ejecución desde el origen.</span><span class="sxs-lookup"><span data-stu-id="509d3-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="509d3-126">El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="509d3-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="509d3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="509d3-127">Requirements</span></span>



| <span data-ttu-id="509d3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="509d3-128">Requirement</span></span> | <span data-ttu-id="509d3-129">Value</span><span class="sxs-lookup"><span data-stu-id="509d3-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="509d3-130">Versión</span><span class="sxs-lookup"><span data-stu-id="509d3-130">Version</span></span><br/> | <span data-ttu-id="509d3-131">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="509d3-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="509d3-132">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="509d3-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="509d3-133">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="509d3-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="509d3-134">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="509d3-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="509d3-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="509d3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="509d3-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="509d3-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




