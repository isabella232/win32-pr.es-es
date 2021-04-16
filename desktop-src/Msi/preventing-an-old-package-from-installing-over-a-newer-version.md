---
description: Windows Installer se pueden crear paquetes de actualización para que las actualizaciones principales no se instalen si un usuario ya tiene instalada una versión más reciente.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Impedir que se instale un paquete anterior en una versión más reciente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652579"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a><span data-ttu-id="d761e-103">Impedir que un paquete antiguo se instale en una versión más reciente</span><span class="sxs-lookup"><span data-stu-id="d761e-103">Preventing an Old Package from Installing Over a Newer Version</span></span>

<span data-ttu-id="d761e-104">Windows Installer se pueden crear paquetes de actualización para que las actualizaciones principales no se instalen si un usuario ya tiene instalada una versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="d761e-104">Windows Installer upgrade packages can be authored to have major upgrades not install if a user already has a newer version installed.</span></span> <span data-ttu-id="d761e-105">El procedimiento descrito en este tema solo puede impedir las degradaciones que podrían deberse a la ejecución de un paquete de actualización principal.</span><span class="sxs-lookup"><span data-stu-id="d761e-105">The procedure in this topic can only prevent downgrades that might be caused by running a major upgrade package.</span></span> <span data-ttu-id="d761e-106">Este procedimiento se basa en la [acción FindRelatedProducts](findrelatedproducts-action.md), que solo se ejecuta durante una instalación por primera vez y no se ejecuta en modo de mantenimiento (reinstalación).</span><span class="sxs-lookup"><span data-stu-id="d761e-106">This procedure relies on the [FindRelatedProducts Action](findrelatedproducts-action.md), which only runs during a first-time installation and does not run in maintenance mode (reinstallation).</span></span> <span data-ttu-id="d761e-107">Dado que las actualizaciones secundarias se realizan mediante la reinstalación, este procedimiento no se puede usar para determinar si un paquete de actualización menor está intentando degradar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="d761e-107">Because minor upgrades are performed using reinstallation, this procedure cannot be used to determine whether a minor upgrade package is attempting to downgrade an application.</span></span> <span data-ttu-id="d761e-108">Para obtener más información, consulte [preparación de una aplicación para futuras actualizaciones importantes](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="d761e-108">For more information, see [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

<span data-ttu-id="d761e-109">**Para evitar que un paquete antiguo se instale en una versión más reciente**</span><span class="sxs-lookup"><span data-stu-id="d761e-109">**To prevent an old package from installing over a newer version**</span></span>

1.  <span data-ttu-id="d761e-110">Escriba la propiedad [**UpgradeCode**](upgradecode.md) para el grupo de productos relacionados que pueden ser válidos para recibir esta actualización en la columna UpgradeCode de la [tabla de actualización](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="d761e-110">Enter the [**UpgradeCode**](upgradecode.md) Property for the group of related products that may be eligible to receive this upgrade into the UpgradeCode column of the [Upgrade Table](upgrade-table.md).</span></span>
2.  <span data-ttu-id="d761e-111">Escriba la marca de bits **msidbUpgradeAttributesOnlyDetect** en la columna atributos de la [tabla de actualización](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="d761e-111">Enter the **msidbUpgradeAttributesOnlyDetect** bit flag in the Attributes column of the [Upgrade Table](upgrade-table.md).</span></span>
3.  <span data-ttu-id="d761e-112">Escriba la versión de la actualización proporcionada por este paquete en la columna VersionMin de la [tabla de actualización](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="d761e-112">Enter the version of the upgrade provided by this package into the VersionMin column of the [Upgrade Table](upgrade-table.md).</span></span> <span data-ttu-id="d761e-113">Deje en blanco la columna VersionMax.</span><span class="sxs-lookup"><span data-stu-id="d761e-113">Leave the VersionMax column blank.</span></span>
4.  <span data-ttu-id="d761e-114">Escriba el nombre de la propiedad que va a establecer la [acción FindRelatedProducts](findrelatedproducts-action.md) en la columna ActionProperty de la tabla de [actualización](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="d761e-114">Enter the name of the property that is to be set by the [FindRelatedProducts Action](findrelatedproducts-action.md) into the ActionProperty column of the [Upgrade Table](upgrade-table.md).</span></span>
5.  <span data-ttu-id="d761e-115">Agregue la propiedad [**SecureCustomProperties**](securecustomproperties.md) y la propiedad denominada en la columna ActionProperty de la [tabla de actualización](upgrade-table.md) a la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="d761e-115">Add the [**SecureCustomProperties**](securecustomproperties.md) property and the property named in the ActionProperty column of the [Upgrade Table](upgrade-table.md) to the [Property Table](property-table.md).</span></span>
6.  <span data-ttu-id="d761e-116">Agregue un [tipo de acción personalizada 19](custom-action-type-19.md) después de la acción FindRelatedProducts en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="d761e-116">Add a [Custom Action Type 19](custom-action-type-19.md) after the FindRelatedProducts action in the [InstallExecuteSequence Table](installexecutesequence-table.md).</span></span> <span data-ttu-id="d761e-117">Incluya un registro en la [tabla CustomAction](customaction-table.md) para esta acción y escriba el texto que se mostrará en la columna de destino.</span><span class="sxs-lookup"><span data-stu-id="d761e-117">Include a record in the [CustomAction Table](customaction-table.md) for this action and enter the text to be displayed in the Target column.</span></span> <span data-ttu-id="d761e-118">La acción personalizada tipo 19 está integrada en el instalador, por lo que no hay código que escribir.</span><span class="sxs-lookup"><span data-stu-id="d761e-118">The type 19 custom action is built into the installer, so there is no code to write.</span></span>
7.  <span data-ttu-id="d761e-119">Escriba el nombre del ActionProperty en la columna condición del registro en la [tabla InstallExecuteSequence](installexecutesequence-table.md) que contiene el [tipo de acción personalizada 19](custom-action-type-19.md).</span><span class="sxs-lookup"><span data-stu-id="d761e-119">Enter the name of the ActionProperty into the Condition column of the record in [InstallExecuteSequence Table](installexecutesequence-table.md) that contains the [Custom Action Type 19](custom-action-type-19.md).</span></span> <span data-ttu-id="d761e-120">Esta acción solo se ejecuta cuando la [tabla de actualización](upgrade-table.md) detecta que ya hay instalada una versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="d761e-120">This conditions the custom action to only be executed when the [Upgrade Table](upgrade-table.md) detects that a newer version is already installed.</span></span>

    <span data-ttu-id="d761e-121">Por ejemplo, un paquete de Windows Installer que actualiza un grupo de productos relacionados con la versión 3,0 puede incluir los registros siguientes en sus tablas de [propiedades](property-table.md) de [actualización](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)y.</span><span class="sxs-lookup"><span data-stu-id="d761e-121">For example, a Windows Installer package that upgrades a group of related products to version 3.0 may include the following records in its [Upgrade](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [Property](property-table.md) tables.</span></span> <span data-ttu-id="d761e-122">Todos los productos relacionados en el grupo tienen el mismo UpgradeCode, pero el instalador no instala este paquete de actualización si ya hay instalada en el equipo una versión posterior a 3,0.</span><span class="sxs-lookup"><span data-stu-id="d761e-122">All the related products in the group have the same UpgradeCode, but the installer does not install this upgrade package if a version later than 3.0 is already installed on the computer.</span></span> <span data-ttu-id="d761e-123">En este caso, el instalador presenta un mensaje de error y se produce un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="d761e-123">In this case, the Installer presents an error message and the installation fails.</span></span> <span data-ttu-id="d761e-124">El paquete de actualización de la versión 3,0 se instala en las versiones 1,0 y 2,0.</span><span class="sxs-lookup"><span data-stu-id="d761e-124">The version 3.0 upgrade package installs over versions 1.0 and 2.0.</span></span>

    [<span data-ttu-id="d761e-125">Actualizar tabla</span><span class="sxs-lookup"><span data-stu-id="d761e-125">Upgrade Table</span></span>](upgrade-table.md)

    

    | <span data-ttu-id="d761e-126">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="d761e-126">UpgradeCode</span></span>                            | <span data-ttu-id="d761e-127">VersionMin</span><span class="sxs-lookup"><span data-stu-id="d761e-127">VersionMin</span></span> | <span data-ttu-id="d761e-128">VersionMax</span><span class="sxs-lookup"><span data-stu-id="d761e-128">VersionMax</span></span> | <span data-ttu-id="d761e-129">Idioma</span><span class="sxs-lookup"><span data-stu-id="d761e-129">Language</span></span> | <span data-ttu-id="d761e-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="d761e-130">Attributes</span></span>                                | <span data-ttu-id="d761e-131">Remove</span><span class="sxs-lookup"><span data-stu-id="d761e-131">Remove</span></span> | <span data-ttu-id="d761e-132">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="d761e-132">ActionProperty</span></span>  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | <span data-ttu-id="d761e-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="d761e-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="d761e-134">3.0</span><span class="sxs-lookup"><span data-stu-id="d761e-134">3.0</span></span>        |            |          | <span data-ttu-id="d761e-135">msidbUpgradeAttributesOnlyDetect</span><span class="sxs-lookup"><span data-stu-id="d761e-135">msidbUpgradeAttributesOnlyDetect</span></span>          |        | <span data-ttu-id="d761e-136">NEWPRODUCTFOUND</span><span class="sxs-lookup"><span data-stu-id="d761e-136">NEWPRODUCTFOUND</span></span> |
    | <span data-ttu-id="d761e-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="d761e-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="d761e-138">1,0</span><span class="sxs-lookup"><span data-stu-id="d761e-138">1.0</span></span>        | <span data-ttu-id="d761e-139">3.0</span><span class="sxs-lookup"><span data-stu-id="d761e-139">3.0</span></span>        |          | <span data-ttu-id="d761e-140">msidbUpgradeAttributesVersionMinInclusive</span><span class="sxs-lookup"><span data-stu-id="d761e-140">msidbUpgradeAttributesVersionMinInclusive</span></span> |        | <span data-ttu-id="d761e-141">UPGRADEFOUND</span><span class="sxs-lookup"><span data-stu-id="d761e-141">UPGRADEFOUND</span></span>    |

    

     

    [<span data-ttu-id="d761e-142">Tabla CustomAction</span><span class="sxs-lookup"><span data-stu-id="d761e-142">CustomAction Table</span></span>](customaction-table.md)

    

    | <span data-ttu-id="d761e-143">Acción</span><span class="sxs-lookup"><span data-stu-id="d761e-143">Action</span></span> | <span data-ttu-id="d761e-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="d761e-144">Type</span></span> | <span data-ttu-id="d761e-145">Source</span><span class="sxs-lookup"><span data-stu-id="d761e-145">Source</span></span> | <span data-ttu-id="d761e-146">Destino</span><span class="sxs-lookup"><span data-stu-id="d761e-146">Target</span></span>                                 |
    |--------|------|--------|----------------------------------------|
    | <span data-ttu-id="d761e-147">CA1</span><span class="sxs-lookup"><span data-stu-id="d761e-147">CA1</span></span>    | <span data-ttu-id="d761e-148">19</span><span class="sxs-lookup"><span data-stu-id="d761e-148">19</span></span>   |        | <span data-ttu-id="d761e-149">Ya hay instalada una actualización superior.</span><span class="sxs-lookup"><span data-stu-id="d761e-149">A higher upgrade is already installed.</span></span> |

    

     

    [<span data-ttu-id="d761e-150">Tabla InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="d761e-150">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)

    

    | <span data-ttu-id="d761e-151">Acción</span><span class="sxs-lookup"><span data-stu-id="d761e-151">Action</span></span>              | <span data-ttu-id="d761e-152">Condición</span><span class="sxs-lookup"><span data-stu-id="d761e-152">Condition</span></span>       | <span data-ttu-id="d761e-153">Secuencia</span><span class="sxs-lookup"><span data-stu-id="d761e-153">Sequence</span></span> |
    |---------------------|-----------------|----------|
    | <span data-ttu-id="d761e-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="d761e-154">FindRelatedProducts</span></span> |                 | <span data-ttu-id="d761e-155">200</span><span class="sxs-lookup"><span data-stu-id="d761e-155">200</span></span>      |
    | <span data-ttu-id="d761e-156">CA1</span><span class="sxs-lookup"><span data-stu-id="d761e-156">CA1</span></span>                 | <span data-ttu-id="d761e-157">NEWPRODUCTFOUND</span><span class="sxs-lookup"><span data-stu-id="d761e-157">NEWPRODUCTFOUND</span></span> | <span data-ttu-id="d761e-158">201</span><span class="sxs-lookup"><span data-stu-id="d761e-158">201</span></span>      |

    

     

    [<span data-ttu-id="d761e-159">Tabla de propiedades</span><span class="sxs-lookup"><span data-stu-id="d761e-159">Property Table</span></span>](property-table.md)

    

    | <span data-ttu-id="d761e-160">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d761e-160">Property</span></span>                                                 | <span data-ttu-id="d761e-161">Value</span><span class="sxs-lookup"><span data-stu-id="d761e-161">Value</span></span>                        |
    |----------------------------------------------------------|------------------------------|
    | [<span data-ttu-id="d761e-162">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="d761e-162">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="d761e-163">NEWPRODUCTFOUND; UPGRADEFOUND</span><span class="sxs-lookup"><span data-stu-id="d761e-163">NEWPRODUCTFOUND;UPGRADEFOUND</span></span> |

    

     

 

 



