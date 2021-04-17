---
description: El instalador establece la última propiedad guardada por Resumen en un valor que depende de si se trata de un paquete de instalación, una transformación o un paquete de revisión. En un paquete de instalación, el instalador establece esta propiedad en el valor de la propiedad LogonUser durante una instalación administrativa. Los desarrolladores de herramientas de edición de bases de datos pueden utilizar esta propiedad durante el proceso de desarrollo para realizar un seguimiento de la última persona que modificó la base de datos de instalación. Esta propiedad debe establecerse en null en una base de datos de envío final. El instalador nunca usa esta propiedad y un usuario nunca necesita modificarla. En una transformación, esta propiedad de Resumen contiene los IDENTIFICADOres de plataforma e idioma que debe tener una base de datos una vez transformada. La propiedad especifica en qué se debe establecer el Resumen de la plantilla en la nueva base de datos. En un paquete de revisión, esta propiedad de Resumen contiene una lista delimitada por signos de punto y coma de nombres de subalmacenamiento de transformación en el orden en que se aplican mediante esta revisión.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Última vez que se guardó la propiedad Summary
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690666"
---
# <a name="last-saved-by-summary-property"></a><span data-ttu-id="0bdcf-107">Última vez que se guardó la propiedad Summary</span><span class="sxs-lookup"><span data-stu-id="0bdcf-107">Last Saved By Summary property</span></span>

<span data-ttu-id="0bdcf-108">El instalador establece la **última propiedad guardada por Resumen** en un valor que depende de si se trata de un paquete de instalación, una transformación o un paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="0bdcf-108">The installer sets the **Last Saved by Summary** Property to a value that depends on whether this is an installation package, transform, or patch package.</span></span>

<span data-ttu-id="0bdcf-109">En un paquete de instalación, el instalador establece esta propiedad en el valor de la propiedad [**LogonUser**](logonuser.md) durante una [instalación administrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="0bdcf-109">In an installation package, the installer sets this property to the value of the [**LogonUser**](logonuser.md) property during an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="0bdcf-110">Los desarrolladores de herramientas de edición de bases de datos pueden utilizar esta propiedad durante el proceso de desarrollo para realizar un seguimiento de la última persona que modificó la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="0bdcf-110">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="0bdcf-111">Esta propiedad debe establecerse en null en una base de datos de envío final.</span><span class="sxs-lookup"><span data-stu-id="0bdcf-111">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="0bdcf-112">El instalador nunca usa esta propiedad y un usuario nunca necesita modificarla.</span><span class="sxs-lookup"><span data-stu-id="0bdcf-112">The installer never uses this property and a user never needs to modify it.</span></span>

<span data-ttu-id="0bdcf-113">En una transformación, esta propiedad de Resumen contiene los IDENTIFICADOres de plataforma e idioma que debe tener una base de datos una vez transformada.</span><span class="sxs-lookup"><span data-stu-id="0bdcf-113">In a transform, this summary property contains the platform and language ID(s) that a database should have after it has been transformed.</span></span> <span data-ttu-id="0bdcf-114">La propiedad especifica en qué se debe establecer el Resumen de la [**plantilla**](template-summary.md) en la nueva base de datos.</span><span class="sxs-lookup"><span data-stu-id="0bdcf-114">The property specifies to what the [**Template Summary**](template-summary.md) should be set in the new database.</span></span>

<span data-ttu-id="0bdcf-115">En un paquete de revisión, esta propiedad de Resumen contiene una lista delimitada por signos de punto y coma de nombres de subalmacenamiento de transformación en el orden en que se aplican mediante esta revisión.</span><span class="sxs-lookup"><span data-stu-id="0bdcf-115">In a patch package, this summary property contains a semicolon-delimited list of transform substorage names in the order they are applied by this patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bdcf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bdcf-116">Requirements</span></span>



| <span data-ttu-id="0bdcf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bdcf-117">Requirement</span></span> | <span data-ttu-id="0bdcf-118">Value</span><span class="sxs-lookup"><span data-stu-id="0bdcf-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bdcf-119">Versión</span><span class="sxs-lookup"><span data-stu-id="0bdcf-119">Version</span></span><br/> | <span data-ttu-id="0bdcf-120">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0bdcf-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0bdcf-121">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0bdcf-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0bdcf-122">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0bdcf-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0bdcf-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bdcf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bdcf-124">Descripciones de propiedades de Resumen</span><span class="sxs-lookup"><span data-stu-id="0bdcf-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




