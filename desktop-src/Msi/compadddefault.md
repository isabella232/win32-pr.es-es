---
description: El valor de la propiedad COMPADDDEFAULT es una lista de GUID de componentes de la columna ComponentId de la tabla de componentes, delimitado por comas, que se instalan en su configuración predeterminada.
ms.assetid: 1bf05680-fcba-4fbb-8f8c-4203a90346ce
title: Propiedad COMPADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e96d2259f0610a3030e79f8685c498a0fb2d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653531"
---
# <a name="compadddefault-property"></a><span data-ttu-id="be5da-103">Propiedad COMPADDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="be5da-103">COMPADDDEFAULT property</span></span>

<span data-ttu-id="be5da-104">El valor de la propiedad **COMPADDDEFAULT** es una lista de GUID de componentes de la columna ComponentID de la [tabla de componentes](component-table.md), delimitado por comas, que se instalan en su configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="be5da-104">The value of the **COMPADDDEFAULT** property is a list of component GUIDs from the ComponentId column of the [Component table](component-table.md), delimited by commas, that are installed in their default configuration.</span></span> <span data-ttu-id="be5da-105">Para cada identificador de componente de la lista, el instalador instala la característica que requiere el menor espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="be5da-105">For each component ID in the list, the installer installs the feature that requires the least disk space.</span></span> <span data-ttu-id="be5da-106">Los identificadores de componente de la lista deben estar presentes en la columna ComponentId de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="be5da-106">The component IDs in the list must be present in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="be5da-107">Una característica se instala en el mismo estado de instalación que si el usuario hubiera solicitado una instalación a petición de la característica.</span><span class="sxs-lookup"><span data-stu-id="be5da-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="be5da-108">El estado se determina por qué bits se establecen para la característica en la columna Attributes de la [tabla de características](feature-table.md)y qué bits se establecen para los componentes de la característica en la columna Attributes de la tabla Component.</span><span class="sxs-lookup"><span data-stu-id="be5da-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="be5da-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be5da-109">Remarks</span></span>

<span data-ttu-id="be5da-110">Tenga en cuenta que si la marca de bits SourceOnly se establece en la columna Attributes de la tabla de [componentes](component-table.md) para un componente, el componente se instala para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="be5da-110">Note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="be5da-111">El instalador siempre evalúa las siguientes propiedades en el orden siguiente.</span><span class="sxs-lookup"><span data-stu-id="be5da-111">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="be5da-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="be5da-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="be5da-113">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="be5da-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="be5da-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="be5da-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="be5da-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="be5da-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="be5da-116">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="be5da-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="be5da-117">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="be5da-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="be5da-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="be5da-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="be5da-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="be5da-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  <span data-ttu-id="be5da-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="be5da-120">**COMPADDDEFAULT**</span></span>
10. [<span data-ttu-id="be5da-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="be5da-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="be5da-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="be5da-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="be5da-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="be5da-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="be5da-124">Por ejemplo, si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = función, todas las características se establecen primero en Run-local y, a continuación, se establece la función de ejecución-desde-origen.</span><span class="sxs-lookup"><span data-stu-id="be5da-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="be5da-125">Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL = función, First la función se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = ALL, todas las características (incluidas las funciones) se restablecen a la ejecución desde el origen.</span><span class="sxs-lookup"><span data-stu-id="be5da-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="be5da-126">El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="be5da-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="be5da-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be5da-127">Requirements</span></span>



| <span data-ttu-id="be5da-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="be5da-128">Requirement</span></span> | <span data-ttu-id="be5da-129">Value</span><span class="sxs-lookup"><span data-stu-id="be5da-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be5da-130">Versión</span><span class="sxs-lookup"><span data-stu-id="be5da-130">Version</span></span><br/> | <span data-ttu-id="be5da-131">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="be5da-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="be5da-132">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be5da-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="be5da-133">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="be5da-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="be5da-134">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="be5da-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be5da-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="be5da-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be5da-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="be5da-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




