---
description: El AdminProperties debe crearse en la tabla de propiedades.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Propiedad AdminProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671795"
---
# <a name="adminproperties-property"></a><span data-ttu-id="6a548-103">Propiedad AdminProperties</span><span class="sxs-lookup"><span data-stu-id="6a548-103">AdminProperties property</span></span>

<span data-ttu-id="6a548-104">El **AdminProperties** debe crearse en la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="6a548-104">The **AdminProperties** should be authored into the [Property Table](property-table.md).</span></span> <span data-ttu-id="6a548-105">El valor de **AdminProperties** es una lista de nombres de propiedad separados por signos de punto y coma.</span><span class="sxs-lookup"><span data-stu-id="6a548-105">The value of **AdminProperties** is a list of property names separated by semicolons.</span></span> <span data-ttu-id="6a548-106">El instalador guarda los valores de estas propiedades enumeradas en el momento de una [instalación administrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="6a548-106">The installer saves the values of these listed properties at the time of an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="6a548-107">Cuando los usuarios instalan desde la imagen administrativa, la instalación usa los valores guardados de las propiedades, en lugar de los valores del archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="6a548-107">When users install from the administrative image, the installation uses the saved values of the properties, rather than the values in the .msi file.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a548-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a548-108">Remarks</span></span>

<span data-ttu-id="6a548-109">Los nombres de propiedad de la lista pueden ser letras mayúsculas y minúsculas (propiedades privadas) o todas mayúsculas (propiedades públicas).</span><span class="sxs-lookup"><span data-stu-id="6a548-109">The property names in the list can be uppercase and lowercase letters (private properties), or all uppercase (public properties).</span></span>

<span data-ttu-id="6a548-110">Esta propiedad nunca debe terminar con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="6a548-110">This property must never end with a semicolon.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a548-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a548-111">Requirements</span></span>



| <span data-ttu-id="6a548-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a548-112">Requirement</span></span> | <span data-ttu-id="6a548-113">Value</span><span class="sxs-lookup"><span data-stu-id="6a548-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a548-114">Versión</span><span class="sxs-lookup"><span data-stu-id="6a548-114">Version</span></span><br/> | <span data-ttu-id="6a548-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6a548-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6a548-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a548-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6a548-117">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6a548-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6a548-118">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6a548-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a548-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6a548-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a548-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a548-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




