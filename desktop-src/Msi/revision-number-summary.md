---
description: Para un paquete de instalación, la propiedad Resumen del número de revisión contiene el código del paquete del instalador.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Propiedad de Resumen de número de revisión
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653907"
---
# <a name="revision-number-summary-property"></a><span data-ttu-id="62cdd-103">Propiedad de Resumen de número de revisión</span><span class="sxs-lookup"><span data-stu-id="62cdd-103">Revision Number Summary property</span></span>

<span data-ttu-id="62cdd-104">Para un paquete de instalación, la propiedad **Resumen del número de revisión** contiene el código del [*paquete*](p-gly.md) del instalador.</span><span class="sxs-lookup"><span data-stu-id="62cdd-104">For an installation package, the **Revision Number Summary** property contains the [*package code*](p-gly.md) for the installer package.</span></span> <span data-ttu-id="62cdd-105">Para obtener más información sobre los códigos de paquete, consulte [códigos de paquete](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="62cdd-105">For more information about package codes, see [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="62cdd-106">En el caso de una transformación, la propiedad **Resumen del número de revisión** muestra los GUID de código de producto y la versión de los productos nuevos y originales y el GUID del código de actualización.</span><span class="sxs-lookup"><span data-stu-id="62cdd-106">For a transform, the **Revision Number Summary** property lists the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="62cdd-107">La lista está separada por signos de punto y coma como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="62cdd-107">The list is separated with semicolons as follows.</span></span>

<span data-ttu-id="62cdd-108">"Original-Product-Code original-Product-version; New-Product Code New-Product-version; Upgrade-Code "</span><span class="sxs-lookup"><span data-stu-id="62cdd-108">"Original-Product-Code Original-Product-Version ; New-Product Code New-Product-Version; Upgrade-Code"</span></span>

<span data-ttu-id="62cdd-109">En el caso de un paquete de revisión, la propiedad **Resumen del número de revisión** especifica el código de revisión del GUID para la revisión.</span><span class="sxs-lookup"><span data-stu-id="62cdd-109">For a patch package, the **Revision Number Summary** property specifies the GUID patch code for the patch.</span></span> <span data-ttu-id="62cdd-110">Puede ir seguido de una lista de GUID de código de revisión para las revisiones obsoletas que se van a quitar cuando se aplica esta revisión.</span><span class="sxs-lookup"><span data-stu-id="62cdd-110">This can be followed by a list of patch code GUIDs for obsolete patches that are to be removed when this patch is applied.</span></span> <span data-ttu-id="62cdd-111">Los códigos de revisión se concatenan sin delimitadores que separan los GUID de la lista.</span><span class="sxs-lookup"><span data-stu-id="62cdd-111">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>

<span data-ttu-id="62cdd-112">\* \* Windows Installer 3,0: \* \* si hay información de secuenciación presente en la [tabla MsiPatchSequence](msipatchsequence-table.md), Windows Installer 3,0 usa la información de secuenciación de la tabla y omite la lista de revisiones obsoletas incluidas en la propiedad **Resumen de número de revisión** .</span><span class="sxs-lookup"><span data-stu-id="62cdd-112">\*\*Windows Installer 3.0:  \*\* If there is sequencing information present in the [MsiPatchSequence table](msipatchsequence-table.md), Windows Installer 3.0 uses the sequencing information in the table and ignores the list of obsolete patches included in the **Revision Number Summary** property.</span></span> <span data-ttu-id="62cdd-113">Windows Installer 3,0 puede seguir usando la información de revisión obsoleta en la propiedad **Resumen de número de revisión** si el paquete no contiene una tabla MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="62cdd-113">Windows Installer 3.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="62cdd-114">\* \* Windows Installer 2,0: \* \* no se admite la [tabla MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="62cdd-114">\*\*Windows Installer 2.0:  \*\* The [MsiPatchSequence table](msipatchsequence-table.md) is not supported.</span></span> <span data-ttu-id="62cdd-115">Windows Installer 2,0 puede seguir usando la información de revisión obsoleta en la propiedad **Resumen de número de revisión** si el paquete no contiene una tabla MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="62cdd-115">Windows Installer 2.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="62cdd-116">Esta propiedad de resumen es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="62cdd-116">This summary property is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="62cdd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62cdd-117">Requirements</span></span>



| <span data-ttu-id="62cdd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="62cdd-118">Requirement</span></span> | <span data-ttu-id="62cdd-119">Value</span><span class="sxs-lookup"><span data-stu-id="62cdd-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62cdd-120">Versión</span><span class="sxs-lookup"><span data-stu-id="62cdd-120">Version</span></span><br/> | <span data-ttu-id="62cdd-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="62cdd-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="62cdd-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="62cdd-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="62cdd-123">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="62cdd-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62cdd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="62cdd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62cdd-125">Descripciones de propiedades de Resumen</span><span class="sxs-lookup"><span data-stu-id="62cdd-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




