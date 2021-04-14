---
description: El valor de la propiedad REMOVE es una lista de características delimitadas por comas que se van a quitar.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE, propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653913"
---
# <a name="remove-property"></a><span data-ttu-id="cd317-103">REMOVE, propiedad</span><span class="sxs-lookup"><span data-stu-id="cd317-103">REMOVE property</span></span>

<span data-ttu-id="cd317-104">El valor de la propiedad **Remove** es una lista de características delimitadas por comas que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="cd317-104">The value of the **REMOVE** property is a list of features delimited by commas that are to be removed.</span></span> <span data-ttu-id="cd317-105">Las características deben estar presentes en la columna característica de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="cd317-105">The features must be present in the Feature column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="cd317-106">Tenga en cuenta que si usa REMOVE = ALL en la línea de comandos, el instalador quita todas las características que tengan un nivel de instalación superior a 0.</span><span class="sxs-lookup"><span data-stu-id="cd317-106">Note that if you use REMOVE=ALL on the command line, the installer removes all features having an install level greater than 0.</span></span> <span data-ttu-id="cd317-107">En este caso, el instalador no quita las características que tienen un nivel de instalación de 0.</span><span class="sxs-lookup"><span data-stu-id="cd317-107">In this case, the installer does not remove features having an install level of 0.</span></span> <span data-ttu-id="cd317-108">Para obtener más información sobre el nivel de instalación de características, vea [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="cd317-108">For more information about the install level of features see [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd317-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd317-109">Remarks</span></span>

<span data-ttu-id="cd317-110">Para determinar si se ha configurado un producto para que se desinstale por completo, el autor de un paquete puede usar una expresión condicional para comprobar si se quita = ALL.</span><span class="sxs-lookup"><span data-stu-id="cd317-110">To determine whether a product has been set to be completely uninstalled, a package author may use a conditional expression to check whether REMOVE=ALL.</span></span> <span data-ttu-id="cd317-111">Tenga en cuenta que si el producto se quita estableciendo su característica superior en ausente, es posible que la propiedad **Remove** no sea igual a toda hasta después de la [acción InstallValidate](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="cd317-111">Note that if the product is removed by setting its top feature to absent, the **REMOVE** property may not equal ALL until after the [InstallValidate action](installvalidate-action.md).</span></span> <span data-ttu-id="cd317-112">Esto significa que cualquier acción personalizada que dependa de REMOVE = ALL se debe secuenciar después de InstallValidate.</span><span class="sxs-lookup"><span data-stu-id="cd317-112">This means that any custom action that depends upon REMOVE=ALL must be sequenced after the InstallValidate.</span></span> <span data-ttu-id="cd317-113">Para obtener más información, consulte también [acciones de acondicionamiento para ejecutarse durante la eliminación](conditioning-actions-to-run-during-removal.md).</span><span class="sxs-lookup"><span data-stu-id="cd317-113">For more information see also [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span> <span data-ttu-id="cd317-114">Tenga en cuenta que los nombres de las características distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cd317-114">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="cd317-115">El instalador siempre evalúa las siguientes propiedades en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="cd317-115">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="cd317-116">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="cd317-116">**ADDLOCAL**</span></span>](addlocal.md)
2.  <span data-ttu-id="cd317-117">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="cd317-117">**REMOVE**</span></span>
3.  [<span data-ttu-id="cd317-118">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="cd317-118">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="cd317-119">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cd317-119">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="cd317-120">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="cd317-120">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="cd317-121">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="cd317-121">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="cd317-122">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="cd317-122">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="cd317-123">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="cd317-123">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="cd317-124">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cd317-124">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="cd317-125">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="cd317-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="cd317-126">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="cd317-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="cd317-127">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cd317-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="cd317-128">Por ejemplo, si la línea de comandos especifica ADDLOCAL = ALL, ADDSOURCE = función, todas las características se establecen primero en Run-local y, a continuación, se establece la función de ejecución-desde-origen.</span><span class="sxs-lookup"><span data-stu-id="cd317-128">For example, if the command line specifies ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="cd317-129">Si la línea de comandos es ADDSOURCE = ALL, ADDLOCAL = función, First la función se establece en Run-local y, cuando se evalúa ADDSOURCE = ALL, todas las características (incluidas las funciones) se restablecen en Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="cd317-129">If the command line is ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="cd317-130">El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="cd317-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd317-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd317-131">Requirements</span></span>



| <span data-ttu-id="cd317-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd317-132">Requirement</span></span> | <span data-ttu-id="cd317-133">Value</span><span class="sxs-lookup"><span data-stu-id="cd317-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd317-134">Versión</span><span class="sxs-lookup"><span data-stu-id="cd317-134">Version</span></span><br/> | <span data-ttu-id="cd317-135">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cd317-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cd317-136">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cd317-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cd317-137">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd317-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cd317-138">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cd317-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd317-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cd317-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd317-140">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd317-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




