---
description: Establezca la propiedad MSINODISABLEMEDIA para evitar que el instalador establezca la propiedad DISABLEMEDIA. El establecimiento de la propiedad DISABLEMEDIA evita que el instalador registre cualquier origen multimedia, como un CD-ROM, como un origen válido para el producto.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: Propiedad MSINODISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653784"
---
# <a name="msinodisablemedia-property"></a><span data-ttu-id="97376-104">Propiedad MSINODISABLEMEDIA</span><span class="sxs-lookup"><span data-stu-id="97376-104">MSINODISABLEMEDIA property</span></span>

<span data-ttu-id="97376-105">Establezca la propiedad **MSINODISABLEMEDIA** para evitar que el instalador establezca la propiedad [**DISABLEMEDIA**](-disablemedia.md) .</span><span class="sxs-lookup"><span data-stu-id="97376-105">Set the **MSINODISABLEMEDIA** property to prevent the installer from setting the [**DISABLEMEDIA**](-disablemedia.md) property.</span></span> <span data-ttu-id="97376-106">El establecimiento de la propiedad **DISABLEMEDIA** evita que el instalador registre cualquier origen multimedia, como un CD-ROM, como un origen válido para el producto.</span><span class="sxs-lookup"><span data-stu-id="97376-106">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span>

<span data-ttu-id="97376-107">Cuando no se establece **MSINODISABLEMEDIA** , el instalador puede agregar [**DISABLEMEDIA**](-disablemedia.md) al flujo de propiedades administrativas al realizar una [instalación administrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="97376-107">When **MSINODISABLEMEDIA** is not set, the installer might add [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream when performing an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="97376-108">Esto impide que los usuarios que se instalan desde la imagen administrativa se instalen desde un medio, como un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="97376-108">This prevents users who install from the administrative image from ever installing from media, such as a CD-ROM.</span></span>

-   <span data-ttu-id="97376-109">Al realizar una instalación administrativa, el instalador solo agrega [**DISABLEMEDIA**](-disablemedia.md) a la secuencia de propiedades administrativas si la propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) es inferior a 150.</span><span class="sxs-lookup"><span data-stu-id="97376-109">When performing an administrative installation, the installer only adds [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream if the [**Page Count Summary**](page-count-summary.md) Property is less than 150.</span></span>

<span data-ttu-id="97376-110">Si [**DISABLEMEDIA**](-disablemedia.md) aparece en la propiedad [**AdminProperties**](adminproperties.md) , al establecer **MSINODISABLEMEDIA** se impide que se establezca **DISABLEMEDIA** durante una instalación administrativa.</span><span class="sxs-lookup"><span data-stu-id="97376-110">If [**DISABLEMEDIA**](-disablemedia.md) is listed in the [**AdminProperties**](adminproperties.md) property, setting **MSINODISABLEMEDIA** prevents **DISABLEMEDIA** from being set during an administrative installation.</span></span> <span data-ttu-id="97376-111">En este caso, el instalador puede registrar un origen multimedia y un usuario podría tener la opción de reinstalar desde el origen de medios si la imagen de instalación administrativa original dejaba de estar disponible más adelante.</span><span class="sxs-lookup"><span data-stu-id="97376-111">In this case, the installer may register a media source and a user could then have the option to reinstall from the media source if the original administrative installation image became unavailable later.</span></span>

## <a name="requirements"></a><span data-ttu-id="97376-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97376-112">Requirements</span></span>



| <span data-ttu-id="97376-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="97376-113">Requirement</span></span> | <span data-ttu-id="97376-114">Value</span><span class="sxs-lookup"><span data-stu-id="97376-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97376-115">Versión</span><span class="sxs-lookup"><span data-stu-id="97376-115">Version</span></span><br/> | <span data-ttu-id="97376-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="97376-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="97376-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="97376-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="97376-118">Windows Installer en Windows Server 2003, Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="97376-118">Windows Installer on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="97376-119">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="97376-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97376-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="97376-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97376-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97376-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




