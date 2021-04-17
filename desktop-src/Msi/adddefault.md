---
description: El valor de la propiedad ADDDEFAULT es una lista de características delimitadas por comas, que se van a instalar en su configuración predeterminada.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: Propiedad ADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43960b6d70d704337f373031ab4972bcb95dada7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653448"
---
# <a name="adddefault-property"></a><span data-ttu-id="f40fa-103">Propiedad ADDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="f40fa-103">ADDDEFAULT property</span></span>

<span data-ttu-id="f40fa-104">El valor de la propiedad **ADDDEFAULT** es una lista de características delimitadas por comas, que se van a instalar en su configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f40fa-104">The value of the **ADDDEFAULT** property is a list of features delimited by commas, which are to be installed in their default configuration.</span></span> <span data-ttu-id="f40fa-105">Las características deben estar presentes en la columna característica de la [tabla de características.](feature-table.md)</span><span class="sxs-lookup"><span data-stu-id="f40fa-105">The features must be present in the Feature column of the [Feature Table.](feature-table.md)</span></span> <span data-ttu-id="f40fa-106">Para instalar todas las características en sus configuraciones predeterminadas, use ADDDEFAULT = ALL en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f40fa-106">To install all features in their default configurations, use ADDDEFAULT=ALL on the command line.</span></span>

<span data-ttu-id="f40fa-107">Una característica enumerada en la propiedad **ADDDEFAULT** se instala en el mismo estado de instalación que si el usuario solicitara una instalación a petición de la característica.</span><span class="sxs-lookup"><span data-stu-id="f40fa-107">A feature listed in the **ADDDEFAULT** property is installed in the same installation state as if the user requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="f40fa-108">El estado viene determinado por los bits establecidos para la característica en la columna Attributes de la [tabla de características](feature-table.md), y los bits que se establecen para los componentes de características en la columna Attributes de la [tabla Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f40fa-108">The state is determined by the bits that are set for the feature in the Attributes column of the [Feature Table](feature-table.md), and which bits are set for the feature components in the Attributes column of the [Component Table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f40fa-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f40fa-109">Remarks</span></span>

<span data-ttu-id="f40fa-110">Los nombres de las características distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f40fa-110">The feature names are case sensitive.</span></span>

<span data-ttu-id="f40fa-111">El instalador siempre evalúa las siguientes propiedades en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="f40fa-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="f40fa-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="f40fa-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="f40fa-113">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="f40fa-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="f40fa-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="f40fa-114">**ADDSOURCE**</span></span>](addsource.md)
4.  <span data-ttu-id="f40fa-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f40fa-115">**ADDDEFAULT**</span></span>
5.  [<span data-ttu-id="f40fa-116">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="f40fa-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="f40fa-117">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="f40fa-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="f40fa-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="f40fa-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="f40fa-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="f40fa-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="f40fa-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f40fa-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="f40fa-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="f40fa-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="f40fa-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="f40fa-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="f40fa-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f40fa-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="f40fa-124">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f40fa-124">For example:</span></span>

-   <span data-ttu-id="f40fa-125">Si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = función, todas las características se establecen primero en Run-local **y, a** continuación, se establece en "Run-from-Source".</span><span class="sxs-lookup"><span data-stu-id="f40fa-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="f40fa-126">Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL = función, First la **función** se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = All, todas las características **(incluidas las funciones)** se restablecen a la ejecución desde el origen.</span><span class="sxs-lookup"><span data-stu-id="f40fa-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="f40fa-127">El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f40fa-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="f40fa-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f40fa-128">Requirements</span></span>



| <span data-ttu-id="f40fa-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f40fa-129">Requirement</span></span> | <span data-ttu-id="f40fa-130">Value</span><span class="sxs-lookup"><span data-stu-id="f40fa-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f40fa-131">Versión</span><span class="sxs-lookup"><span data-stu-id="f40fa-131">Version</span></span><br/> | <span data-ttu-id="f40fa-132">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f40fa-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f40fa-133">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f40fa-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f40fa-134">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f40fa-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f40fa-135">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f40fa-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f40fa-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f40fa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f40fa-137">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f40fa-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




