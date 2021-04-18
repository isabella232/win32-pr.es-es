---
description: El valor de la propiedad ADDSOURCE es una lista de características que están delimitadas por comas y que se van a instalar para ejecutarse desde el origen.
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: Propiedad ADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd51d6f86060def1a7536134a0041f1e15178a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671794"
---
# <a name="addsource-property"></a><span data-ttu-id="54b94-103">Propiedad ADDSOURCE</span><span class="sxs-lookup"><span data-stu-id="54b94-103">ADDSOURCE property</span></span>

<span data-ttu-id="54b94-104">El valor de la propiedad **ADDSOURCE** es una lista de características que están delimitadas por comas y que se van a instalar para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="54b94-104">The value of the **ADDSOURCE** property is a list of features that are delimited by commas, and are to be installed to run from the source.</span></span> <span data-ttu-id="54b94-105">Las características deben estar presentes en la columna característica de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="54b94-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="54b94-106">Para instalar todas las características como ejecutar desde el origen, use ADDSOURCE = ALL en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="54b94-106">To install all features as run from source, use ADDSOURCE=ALL on the command line.</span></span> <span data-ttu-id="54b94-107">No escriba ADDSOURCE = ALL en la [tabla de propiedades](property-table.md), ya que genera un paquete de ejecución desde el origen que no se puede quitar correctamente.</span><span class="sxs-lookup"><span data-stu-id="54b94-107">Do not enter ADDSOURCE=ALL into the [Property Table](property-table.md), because this generates a run-from-source package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="54b94-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54b94-108">Remarks</span></span>

<span data-ttu-id="54b94-109">Los nombres de las características distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="54b94-109">The feature names are case sensitive.</span></span> <span data-ttu-id="54b94-110">Si se establece la marca de bits LocalOnly en la columna atributos de la [tabla componente](component-table.md) para un componente de una característica de la lista, ese componente se instala para ejecutarse localmente.</span><span class="sxs-lookup"><span data-stu-id="54b94-110">If the LocalOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed to run locally.</span></span>

<span data-ttu-id="54b94-111">El instalador siempre evalúa las siguientes propiedades en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="54b94-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="54b94-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="54b94-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="54b94-113">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="54b94-113">**REMOVE**</span></span>](remove.md)
3.  <span data-ttu-id="54b94-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="54b94-114">**ADDSOURCE**</span></span>
4.  [<span data-ttu-id="54b94-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="54b94-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="54b94-116">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="54b94-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="54b94-117">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="54b94-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="54b94-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="54b94-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="54b94-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="54b94-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="54b94-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="54b94-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="54b94-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="54b94-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="54b94-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="54b94-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="54b94-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="54b94-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="54b94-124">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="54b94-124">For example:</span></span>

-   <span data-ttu-id="54b94-125">Si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = **función**, todas las características se establecen primero en Run-local **y, a** continuación, se establece en "Run-from-Source".</span><span class="sxs-lookup"><span data-stu-id="54b94-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="54b94-126">Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL =**función**, First la **función** se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = All, todas las características **(incluidas las funciones)** se restablecen a la ejecución desde el origen.</span><span class="sxs-lookup"><span data-stu-id="54b94-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="54b94-127">El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="54b94-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="54b94-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54b94-128">Requirements</span></span>



| <span data-ttu-id="54b94-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="54b94-129">Requirement</span></span> | <span data-ttu-id="54b94-130">Value</span><span class="sxs-lookup"><span data-stu-id="54b94-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54b94-131">Versión</span><span class="sxs-lookup"><span data-stu-id="54b94-131">Version</span></span><br/> | <span data-ttu-id="54b94-132">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="54b94-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="54b94-133">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="54b94-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="54b94-134">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="54b94-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="54b94-135">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="54b94-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54b94-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="54b94-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b94-137">Propiedades</span><span class="sxs-lookup"><span data-stu-id="54b94-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




