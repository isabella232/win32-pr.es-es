---
description: El valor de la propiedad REINSTALL es una lista de características delimitadas por comas que se van a volver a instalar. Las características enumeradas deben estar presentes en la columna característica de la tabla de características. Para reinstalar todas las características, utilice REINSTALL = ALL en la línea de comandos.
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: REINSTALL (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653660"
---
# <a name="reinstall-property"></a><span data-ttu-id="31bf3-105">REINSTALL (propiedad)</span><span class="sxs-lookup"><span data-stu-id="31bf3-105">REINSTALL property</span></span>

<span data-ttu-id="31bf3-106">El valor de la propiedad **REINSTALL** es una lista de características delimitadas por comas que se van a volver a instalar.</span><span class="sxs-lookup"><span data-stu-id="31bf3-106">The value of the **REINSTALL** property is a list of features delimited by commas that are to be reinstalled.</span></span> <span data-ttu-id="31bf3-107">Las características enumeradas deben estar presentes en la columna característica de la tabla de [características](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="31bf3-107">The features listed must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="31bf3-108">Para reinstalar todas las características, utilice REINSTALL = ALL en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="31bf3-108">To reinstall all features use REINSTALL=ALL on the command line.</span></span>

## <a name="remarks"></a><span data-ttu-id="31bf3-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31bf3-109">Remarks</span></span>

<span data-ttu-id="31bf3-110">Tenga en cuenta que los nombres de las características distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="31bf3-110">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="31bf3-111">Si se establece la propiedad **REINSTALL** , también se debe establecer la propiedad [**REINSTALLMODE**](reinstallmode.md) para indicar el tipo de reinstalación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="31bf3-111">If the **REINSTALL** property is set, the [**REINSTALLMODE**](reinstallmode.md) property should also be set, to indicate the type of reinstall to be performed.</span></span> <span data-ttu-id="31bf3-112">Si no se establece la propiedad **REINSTALLMODE** , de forma predeterminada se reinstalan todos los archivos instalados actualmente, si el archivo instalado actualmente es una versión anterior (o no está presente).</span><span class="sxs-lookup"><span data-stu-id="31bf3-112">If the **REINSTALLMODE** property is not set, then by default all files that are currently installed are reinstalled, IF the currently installed file is a lesser version (or is not present).</span></span> <span data-ttu-id="31bf3-113">De forma predeterminada, no se reescriben entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="31bf3-113">By default, no registry entries are rewritten.</span></span>

<span data-ttu-id="31bf3-114">Tenga en cuenta que incluso si **reinstalar** está establecido en todos, solo se reinstalan las características que ya se instalaron anteriormente.</span><span class="sxs-lookup"><span data-stu-id="31bf3-114">Note that even if **REINSTALL** is set to ALL, only those features that were already installed previously are reinstalled.</span></span> <span data-ttu-id="31bf3-115">Por lo tanto, si la **reinstalación** está establecida para un producto que todavía está instalado, no se realizará ninguna acción de instalación.</span><span class="sxs-lookup"><span data-stu-id="31bf3-115">Thus, if **REINSTALL** is set for a product that is yet to be installed, no installation action will take place at all.</span></span>

<span data-ttu-id="31bf3-116">El instalador siempre evalúa las siguientes propiedades en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="31bf3-116">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="31bf3-117">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="31bf3-117">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="31bf3-118">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="31bf3-118">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="31bf3-119">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="31bf3-119">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="31bf3-120">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="31bf3-120">**ADDDEFAULT**</span></span>](adddefault.md)
5.  <span data-ttu-id="31bf3-121">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="31bf3-121">**REINSTALL**</span></span>
6.  [<span data-ttu-id="31bf3-122">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="31bf3-122">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="31bf3-123">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="31bf3-123">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="31bf3-124">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="31bf3-124">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="31bf3-125">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="31bf3-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
10. [<span data-ttu-id="31bf3-126">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="31bf3-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
11. [<span data-ttu-id="31bf3-127">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="31bf3-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="31bf3-128">Por ejemplo, si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = función, todas las características se establecen primero en Run-local y, a continuación, se establece la función de ejecución-desde-origen.</span><span class="sxs-lookup"><span data-stu-id="31bf3-128">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="31bf3-129">Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL = función, First la función se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = ALL, todas las características (incluidas las funciones) se restablecen a la ejecución desde el origen.</span><span class="sxs-lookup"><span data-stu-id="31bf3-129">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="31bf3-130">El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="31bf3-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="31bf3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31bf3-131">Requirements</span></span>



| <span data-ttu-id="31bf3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="31bf3-132">Requirement</span></span> | <span data-ttu-id="31bf3-133">Value</span><span class="sxs-lookup"><span data-stu-id="31bf3-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31bf3-134">Versión</span><span class="sxs-lookup"><span data-stu-id="31bf3-134">Version</span></span><br/> | <span data-ttu-id="31bf3-135">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="31bf3-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="31bf3-136">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="31bf3-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="31bf3-137">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31bf3-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="31bf3-138">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="31bf3-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31bf3-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="31bf3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31bf3-140">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31bf3-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




