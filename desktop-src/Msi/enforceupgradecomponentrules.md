---
description: Se trata de una directiva del sistema por equipo que se puede usar para aplicar reglas de componentes de actualización durante pequeñas actualizaciones y actualizaciones secundarias.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002145"
---
# <a name="enforceupgradecomponentrules"></a><span data-ttu-id="6a563-103">EnforceUpgradeComponentRules</span><span class="sxs-lookup"><span data-stu-id="6a563-103">EnforceUpgradeComponentRules</span></span>

<span data-ttu-id="6a563-104">Se trata de una [Directiva del sistema](system-policy.md) por equipo que se puede usar para aplicar reglas de componentes de actualización durante [pequeñas actualizaciones](small-updates.md) y actualizaciones [secundarias](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="6a563-104">This is a per-machine [system policy](system-policy.md) that can be used to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md).</span></span>

<span data-ttu-id="6a563-105">Establezca la Directiva EnforceUpgradeComponentRules en 1 para aplicar las reglas de componentes de actualización durante [las actualizaciones pequeñas](small-updates.md) y las actualizaciones [secundarias](minor-upgrades.md) de todos los productos del equipo.</span><span class="sxs-lookup"><span data-stu-id="6a563-105">Set the EnforceUpgradeComponentRules policy to 1 to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of all products on the computer.</span></span> <span data-ttu-id="6a563-106">Para aplicar las reglas durante las actualizaciones pequeñas y las actualizaciones secundarias de un producto determinado, establezca la propiedad [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) en 1 en la línea de comandos o en la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="6a563-106">To apply the rules during small updates and minor upgrades of a particular product, set the [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) property to 1 on the command line or in the [Property table](property-table.md).</span></span>

<span data-ttu-id="6a563-107">Cuando la propiedad o la Directiva se han establecido en 1, se puede producir un error en [las actualizaciones pequeñas](small-updates.md) y las actualizaciones [secundarias](minor-upgrades.md) porque la actualización intenta hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6a563-107">When the property or policy has been set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update attempts to do the following:</span></span>

-   <span data-ttu-id="6a563-108">Agregue una nueva característica a la parte superior o central de un árbol de características existente.</span><span class="sxs-lookup"><span data-stu-id="6a563-108">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="6a563-109">La nueva característica debe agregarse como una nueva característica hoja a un árbol de características existente.</span><span class="sxs-lookup"><span data-stu-id="6a563-109">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="6a563-110">En este caso, se puede cambiar el [**ProductCode**](productcode.md) del producto y las actualizaciones se pueden tratar como una [actualización principal](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="6a563-110">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="6a563-111">Quitar un componente de una característica.</span><span class="sxs-lookup"><span data-stu-id="6a563-111">Remove a component from a feature.</span></span>

    <span data-ttu-id="6a563-112">Esto también puede ocurrir si cambia el GUID de un componente.</span><span class="sxs-lookup"><span data-stu-id="6a563-112">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="6a563-113">El componente identificado por el GUID original parece quitarse y el componente identificado por el nuevo GUID aparece como un nuevo componente.</span><span class="sxs-lookup"><span data-stu-id="6a563-113">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="6a563-114">**Windows Installer 4,5 y versiones posteriores:** El componente se puede quitar correctamente mediante Windows Installer 4,5 o posterior estableciendo el atributo **msidbComponentAttributesUninstallOnSupersedence** en la [tabla de componentes](component-table.md) o estableciendo la propiedad [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .</span><span class="sxs-lookup"><span data-stu-id="6a563-114">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 or later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="6a563-115">Como alternativa, se puede cambiar el [**ProductCode**](productcode.md) del producto y las actualizaciones se pueden tratar como una [actualización principal](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="6a563-115">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="6a563-116">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="6a563-116">Registry Key</span></span>

<span data-ttu-id="6a563-117">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="6a563-117">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="6a563-118">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6a563-118">Data Type</span></span>

<span data-ttu-id="6a563-119">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="6a563-119">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a563-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a563-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a563-121">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="6a563-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



