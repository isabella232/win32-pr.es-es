---
description: La propiedad MSIPATCHREMOVE especifica la lista de revisiones que se van a quitar durante una instalación.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: Propiedad MSIPATCHREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670643"
---
# <a name="msipatchremove-property"></a><span data-ttu-id="1c4ac-103">Propiedad MSIPATCHREMOVE</span><span class="sxs-lookup"><span data-stu-id="1c4ac-103">MSIPATCHREMOVE property</span></span>

<span data-ttu-id="1c4ac-104">La propiedad **MSIPATCHREMOVE** especifica la lista de revisiones que se van a quitar durante una instalación.</span><span class="sxs-lookup"><span data-stu-id="1c4ac-104">The **MSIPATCHREMOVE** property specifies the list of patches to remove during an installation.</span></span> <span data-ttu-id="1c4ac-105">Las revisiones individuales de la lista se separan mediante signos de punto y coma y se pueden representar mediante el GUID del código de revisión o la ruta de acceso completa a la revisión.</span><span class="sxs-lookup"><span data-stu-id="1c4ac-105">Individual patches in the list are separated by semicolons and can be represented by patch code GUID or the full path to the patch.</span></span> <span data-ttu-id="1c4ac-106">La función [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) y el método [**RemovePatches**](installer-removepatches.md) del objeto [instalador](installer-object.md) establecen la propiedad **MSIPATCHREMOVE** .</span><span class="sxs-lookup"><span data-stu-id="1c4ac-106">The [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function and the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object set the **MSIPATCHREMOVE** property.</span></span>

<span data-ttu-id="1c4ac-107">La propiedad **MSIPATCHREMOVE** se puede establecer en la línea de comandos como se indica a continuación para quitar una revisión.</span><span class="sxs-lookup"><span data-stu-id="1c4ac-107">The **MSIPATCHREMOVE** property can be set on the command line as follows to remove a patch.</span></span>

<span data-ttu-id="1c4ac-108">**msiexec/i A: \\Example.msi MSIPATCHREMOVE = c: \\ patches \\ qfe1. MSP; { 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/QB**</span><span class="sxs-lookup"><span data-stu-id="1c4ac-108">**msiexec /i A:\\Example.msi MSIPATCHREMOVE=c:\\patches\\qfe1.msp;{0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0};{A86B443B-E3BF-4009-ADED-F716FC735858}/qb**</span></span>

## <a name="requirements"></a><span data-ttu-id="1c4ac-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c4ac-109">Requirements</span></span>



| <span data-ttu-id="1c4ac-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c4ac-110">Requirement</span></span> | <span data-ttu-id="1c4ac-111">Value</span><span class="sxs-lookup"><span data-stu-id="1c4ac-111">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4ac-112">Versión</span><span class="sxs-lookup"><span data-stu-id="1c4ac-112">Version</span></span><br/> | <span data-ttu-id="1c4ac-113">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1c4ac-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1c4ac-114">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1c4ac-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1c4ac-115">Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c4ac-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1c4ac-116">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1c4ac-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c4ac-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1c4ac-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c4ac-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c4ac-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="1c4ac-119">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="1c4ac-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




