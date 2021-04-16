---
description: El valor de la propiedad ADDLOCAL es una lista de características que están delimitadas por comas y que se van a instalar localmente.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: ADDLOCAL (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9618389d6e409829dce1eb7bb3a38c1269a2e06d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671796"
---
# <a name="addlocal-property"></a><span data-ttu-id="fc545-103">ADDLOCAL (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fc545-103">ADDLOCAL property</span></span>

<span data-ttu-id="fc545-104">El valor de la propiedad **AddLocal** es una lista de características que están delimitadas por comas y que se van a instalar localmente.</span><span class="sxs-lookup"><span data-stu-id="fc545-104">The value of the **ADDLOCAL** property is a list of features that are delimited by commas, and are to be installed locally.</span></span> <span data-ttu-id="fc545-105">Las características deben estar presentes en la columna característica de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="fc545-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="fc545-106">Para instalar todas las características localmente, utilice ADDLOCAL = ALL en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="fc545-106">To install all features locally, use ADDLOCAL=ALL on the command line.</span></span> <span data-ttu-id="fc545-107">No escriba ADDLOCAL = ALL en la [tabla de propiedades](property-table.md), ya que esto genera un paquete instalado localmente que no se puede quitar correctamente.</span><span class="sxs-lookup"><span data-stu-id="fc545-107">Do not enter ADDLOCAL=ALL into the [Property Table](property-table.md), because this generates a locally installed package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc545-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc545-108">Remarks</span></span>

<span data-ttu-id="fc545-109">Los nombres de las características distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fc545-109">Feature names are case sensitive.</span></span> <span data-ttu-id="fc545-110">Si la marca de bits SourceOnly se establece en la columna atributos de la [tabla componente](component-table.md) para un componente de una característica de la lista, ese componente se instala como ejecutar desde el origen.</span><span class="sxs-lookup"><span data-stu-id="fc545-110">If the SourceOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed as run from source.</span></span>

<span data-ttu-id="fc545-111">El instalador siempre evalúa las siguientes propiedades en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="fc545-111">The installer always evaluates the following properties in the following order:</span></span>

1.  <span data-ttu-id="fc545-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="fc545-112">**ADDLOCAL**</span></span>
2.  [<span data-ttu-id="fc545-113">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="fc545-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="fc545-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="fc545-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="fc545-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="fc545-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="fc545-116">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="fc545-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="fc545-117">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="fc545-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="fc545-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="fc545-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="fc545-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="fc545-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="fc545-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="fc545-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="fc545-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="fc545-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="fc545-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="fc545-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="fc545-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="fc545-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="fc545-124">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="fc545-124">For example:</span></span>

-   <span data-ttu-id="fc545-125">Si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = **función**, todas las características se establecen primero en Run-local **y, a** continuación, se establece en "Run-from-Source".</span><span class="sxs-lookup"><span data-stu-id="fc545-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="fc545-126">Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL =**función**, First la **función** se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = All, todas las características **(incluidas las funciones)** se restablecen a la ejecución desde el origen.</span><span class="sxs-lookup"><span data-stu-id="fc545-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="fc545-127">El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="fc545-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the previous properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc545-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc545-128">Requirements</span></span>



| <span data-ttu-id="fc545-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc545-129">Requirement</span></span> | <span data-ttu-id="fc545-130">Value</span><span class="sxs-lookup"><span data-stu-id="fc545-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc545-131">Versión</span><span class="sxs-lookup"><span data-stu-id="fc545-131">Version</span></span><br/> | <span data-ttu-id="fc545-132">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fc545-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fc545-133">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc545-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fc545-134">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc545-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fc545-135">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fc545-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc545-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fc545-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc545-137">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc545-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




