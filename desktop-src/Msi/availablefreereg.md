---
description: La propiedad AVAILABLEFREEREG especifica en kilobytes el espacio libre total disponible en el registro después de llamar a la acción AllocateRegistrySpace. El valor máximo de la propiedad AVAILABLEFREEREG es 2 millones kilobytes. Esta propiedad se establece únicamente en Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: Propiedad AVAILABLEFREEREG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 517073748195c47ee27b68adbe70d6c69f3f585b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653817"
---
# <a name="availablefreereg-property"></a><span data-ttu-id="ee5fa-103">Propiedad AVAILABLEFREEREG</span><span class="sxs-lookup"><span data-stu-id="ee5fa-103">AVAILABLEFREEREG property</span></span>

<span data-ttu-id="ee5fa-104">La propiedad **AVAILABLEFREEREG** especifica en kilobytes el espacio libre total disponible en el registro después de llamar a la [acción AllocateRegistrySpace](allocateregistryspace-action.md).</span><span class="sxs-lookup"><span data-stu-id="ee5fa-104">The **AVAILABLEFREEREG** property specifies in kilobytes the total free space available in the registry after calling the [AllocateRegistrySpace action](allocateregistryspace-action.md).</span></span>

<span data-ttu-id="ee5fa-105">El valor máximo de la propiedad **AVAILABLEFREEREG** es 2 millones kilobytes.</span><span class="sxs-lookup"><span data-stu-id="ee5fa-105">The maximum value of the **AVAILABLEFREEREG** property is 2000000 kilobytes.</span></span>

<span data-ttu-id="ee5fa-106">Esta propiedad se establece únicamente en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ee5fa-106">This property is set only on Windows 2000.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee5fa-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee5fa-107">Remarks</span></span>

<span data-ttu-id="ee5fa-108">La propiedad **AVAILABLEFREEREG** debe establecerse en un valor lo suficientemente grande como para garantizar espacio suficiente en el registro para toda la información de registro agregada por la instalación.</span><span class="sxs-lookup"><span data-stu-id="ee5fa-108">The **AVAILABLEFREEREG** property must be set to a value large enough to ensure sufficient space in the registry for all registration information added by the installation.</span></span> <span data-ttu-id="ee5fa-109">El valor mínimo necesario para garantizar que el espacio sea suficiente depende de dónde se encuentre la [acción AllocateRegistrySpace](allocateregistryspace-action.md) en la secuencia de acción porque el instalador aumenta automáticamente el espacio según sea necesario al registrar la información en las tablas [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md)y [Verb](verb-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ee5fa-109">The minimum value required to ensure sufficient space depends on where the [AllocateRegistrySpace action](allocateregistryspace-action.md) is located in the action sequence because the installer automatically increases the space as needed when registering information in the [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md), and [Verb](verb-table.md) tables.</span></span> <span data-ttu-id="ee5fa-110">El instalador no aumenta el espacio total del registro hasta la cantidad especificada por **AVAILABLEFREEREG** hasta llegar a AllocateRegistrySpace en la secuencia de acción.</span><span class="sxs-lookup"><span data-stu-id="ee5fa-110">The installer does not increase the total registry space to the amount specified by **AVAILABLEFREEREG** until reaching AllocateRegistrySpace in the action sequence.</span></span>

<span data-ttu-id="ee5fa-111">Si AllocateRegistrySpace es una de las primeras acciones de la secuencia de acciones, **AVAILABLEFREEREG** debe establecerse en el espacio total requerido por la información de registro en la tabla del registro, la tabla de clases, la tabla typelib, la tabla SelfReg, la tabla de extensión, la tabla MIME, la tabla de verbos, el registro de [acciones personalizadas](custom-actions.md) , el registro propio y cualquier otra información del registro escrita durante la instalación</span><span class="sxs-lookup"><span data-stu-id="ee5fa-111">If AllocateRegistrySpace is one of the first actions in the action sequence, **AVAILABLEFREEREG** should be set to the total space required by the registration information in the Registry table, Class table, TypeLib table, SelfReg table, Extension table, MIME table, Verb table, [custom actions](custom-actions.md) registration, self registration, and any other registry information written during the installation.</span></span> <span data-ttu-id="ee5fa-112">El valor de **AVAILABLEFREEREG** es la cantidad total de información agregada por la instalación y garantiza suficiente espacio en todos los casos.</span><span class="sxs-lookup"><span data-stu-id="ee5fa-112">The value of **AVAILABLEFREEREG** is the total amount of information added by the installation and ensures sufficient space in all cases.</span></span> <span data-ttu-id="ee5fa-113">Este es también el caso más común.</span><span class="sxs-lookup"><span data-stu-id="ee5fa-113">This is also the most common case.</span></span>

<span data-ttu-id="ee5fa-114">Si la acción AllocateRegistrySpace se puede crear en la secuencia de acciones después de todas [las acciones estándar](standard-actions.md) que escriben los datos de registro, como [WriteRegistryValues](writeregistryvalues-action.md) y [RegisterClassInfo](registerclassinfo-action.md), el valor de **AVAILABLEFREEREG** solo debe establecerse en el espacio necesario para registrar las acciones personalizadas, registrar bibliotecas de tipos y cualquier otra información que no se haya registrado a través de las tablas.</span><span class="sxs-lookup"><span data-stu-id="ee5fa-114">If the AllocateRegistrySpace action can be authored into the action sequence after all [standard actions](standard-actions.md) that write registration data, such as [WriteRegistryValues](writeregistryvalues-action.md) and [RegisterClassInfo](registerclassinfo-action.md), the value of **AVAILABLEFREEREG** needs only be set to the space needed to register custom actions, register type libraries, and any other information not yet registered through the tables.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee5fa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee5fa-115">Requirements</span></span>



| <span data-ttu-id="ee5fa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee5fa-116">Requirement</span></span> | <span data-ttu-id="ee5fa-117">Value</span><span class="sxs-lookup"><span data-stu-id="ee5fa-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee5fa-118">Versión</span><span class="sxs-lookup"><span data-stu-id="ee5fa-118">Version</span></span><br/> | <span data-ttu-id="ee5fa-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ee5fa-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ee5fa-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ee5fa-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ee5fa-121">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ee5fa-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ee5fa-122">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ee5fa-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee5fa-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ee5fa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee5fa-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee5fa-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




