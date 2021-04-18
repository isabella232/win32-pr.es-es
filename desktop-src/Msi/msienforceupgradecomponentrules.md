---
description: Establezca la propiedad MSIENFORCEUPGRADECOMPONENTRULES en 1 en la línea de comandos o en la tabla de propiedades para aplicar las reglas de componentes de actualización durante las actualizaciones pequeñas y las actualizaciones secundarias de un producto determinado.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: Propiedad MSIENFORCEUPGRADECOMPONENTRULES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d5946ba3a0001c988ddfe76eeaf95c008205b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671033"
---
# <a name="msienforceupgradecomponentrules-property"></a><span data-ttu-id="44268-103">Propiedad MSIENFORCEUPGRADECOMPONENTRULES</span><span class="sxs-lookup"><span data-stu-id="44268-103">MSIENFORCEUPGRADECOMPONENTRULES property</span></span>

<span data-ttu-id="44268-104">Establezca la propiedad **MSIENFORCEUPGRADECOMPONENTRULES** en 1 en la línea de comandos o en la [tabla de propiedades](property-table.md) para aplicar las reglas de componentes de actualización durante [las actualizaciones pequeñas](small-updates.md) y las actualizaciones [secundarias](minor-upgrades.md) de un producto determinado.</span><span class="sxs-lookup"><span data-stu-id="44268-104">Set the **MSIENFORCEUPGRADECOMPONENTRULES** property to 1 on the command line or in the [Property table](property-table.md) to apply the upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of a particular product.</span></span> <span data-ttu-id="44268-105">Para aplicar las reglas durante las pequeñas actualizaciones y actualizaciones secundarias de todos los productos del equipo, establezca la directiva [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) en 1.</span><span class="sxs-lookup"><span data-stu-id="44268-105">To apply the rules during small updates and minor upgrades of all products on the computer, set the [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) policy to 1.</span></span>

<span data-ttu-id="44268-106">Cuando la propiedad o la Directiva se establece en 1, se puede producir un error en [las actualizaciones pequeñas](small-updates.md) y las actualizaciones [secundarias](minor-upgrades.md) porque la actualización intenta hacer lo siguiente que infringe las reglas del componente de actualización:</span><span class="sxs-lookup"><span data-stu-id="44268-106">When the property or policy is set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update tries to do the following that violates the upgrade component rules:</span></span>

-   <span data-ttu-id="44268-107">Agregue una nueva característica a la parte superior o central de un árbol de características existente.</span><span class="sxs-lookup"><span data-stu-id="44268-107">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="44268-108">La nueva característica debe agregarse como una nueva característica hoja a un árbol de características existente.</span><span class="sxs-lookup"><span data-stu-id="44268-108">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="44268-109">En este caso, se puede cambiar el [**ProductCode**](productcode.md) del producto y la actualización se puede tratar como una [actualización principal](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="44268-109">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="44268-110">Quitar un componente de una característica.</span><span class="sxs-lookup"><span data-stu-id="44268-110">Remove a component from a feature.</span></span>

    <span data-ttu-id="44268-111">Esto también puede ocurrir si cambia el GUID de un componente.</span><span class="sxs-lookup"><span data-stu-id="44268-111">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="44268-112">El componente identificado por el GUID original parece quitarse y el componente identificado por el nuevo GUID aparece como un nuevo componente.</span><span class="sxs-lookup"><span data-stu-id="44268-112">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="44268-113">**Windows Installer 4,5 y versiones posteriores:** El componente se puede quitar correctamente con Windows Installer 4,5 y versiones posteriores estableciendo el atributo **msidbComponentAttributesUninstallOnSupersedence** en la [tabla de componentes](component-table.md) o estableciendo la propiedad [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .</span><span class="sxs-lookup"><span data-stu-id="44268-113">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 and later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component Table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="44268-114">Como alternativa, se puede cambiar el [**ProductCode**](productcode.md) del producto y la actualización se puede tratar como una [actualización principal](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="44268-114">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44268-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44268-115">Requirements</span></span>



| <span data-ttu-id="44268-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44268-116">Requirement</span></span> | <span data-ttu-id="44268-117">Value</span><span class="sxs-lookup"><span data-stu-id="44268-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44268-118">Versión</span><span class="sxs-lookup"><span data-stu-id="44268-118">Version</span></span><br/> | <span data-ttu-id="44268-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="44268-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="44268-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="44268-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="44268-121">Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="44268-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="44268-122">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="44268-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44268-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="44268-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44268-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44268-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="44268-125">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="44268-125">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




