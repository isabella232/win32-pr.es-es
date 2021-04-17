---
description: La propiedad PATCHNEWPACKAGECODE actualiza la propiedad de resumen del número de revisión de una imagen administrativa durante la revisión.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: Propiedad PATCHNEWPACKAGECODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7c1c70c91ede5788258c67626cdf429df74e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670427"
---
# <a name="patchnewpackagecode-property"></a><span data-ttu-id="115a0-103">Propiedad PATCHNEWPACKAGECODE</span><span class="sxs-lookup"><span data-stu-id="115a0-103">PATCHNEWPACKAGECODE property</span></span>

<span data-ttu-id="115a0-104">La propiedad **PATCHNEWPACKAGECODE** actualiza la propiedad de [**Resumen del número de revisión**](revision-number-summary.md) de una imagen administrativa durante la revisión.</span><span class="sxs-lookup"><span data-stu-id="115a0-104">The **PATCHNEWPACKAGECODE** property updates the [**Revision Number Summary**](revision-number-summary.md) property of an administrative image during patching.</span></span> <span data-ttu-id="115a0-105">Esta propiedad solo se establece mediante una transformación en un archivo. msp.</span><span class="sxs-lookup"><span data-stu-id="115a0-105">This property is only set by a transform in a .msp file.</span></span> <span data-ttu-id="115a0-106">El archivo. MSP debe incluir una transformación que agregue esta propiedad a la [tabla de propiedades](property-table.md) y establezca su valor.</span><span class="sxs-lookup"><span data-stu-id="115a0-106">The .msp file must include a transform that adds this property to the [Property table](property-table.md) and sets its value.</span></span> <span data-ttu-id="115a0-107">Después, el instalador escribe el valor de **PATCHNEWPACKAGECODE** en la propiedad **Summary del número de revisión** .</span><span class="sxs-lookup"><span data-stu-id="115a0-107">The installer then writes the value of **PATCHNEWPACKAGECODE** to the **Revision Number Summary** property.</span></span>

## <a name="remarks"></a><span data-ttu-id="115a0-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="115a0-108">Remarks</span></span>

<span data-ttu-id="115a0-109">Las propiedades **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)y [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) se usan para actualizar la información de resumen cuando se instala una revisión en una imagen administrativa.</span><span class="sxs-lookup"><span data-stu-id="115a0-109">The **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md), and [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) properties are used to update the summary information when a patch is installed to an administrative image.</span></span>

## <a name="requirements"></a><span data-ttu-id="115a0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="115a0-110">Requirements</span></span>



| <span data-ttu-id="115a0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="115a0-111">Requirement</span></span> | <span data-ttu-id="115a0-112">Value</span><span class="sxs-lookup"><span data-stu-id="115a0-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="115a0-113">Versión</span><span class="sxs-lookup"><span data-stu-id="115a0-113">Version</span></span><br/> | <span data-ttu-id="115a0-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="115a0-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="115a0-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="115a0-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="115a0-116">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="115a0-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="115a0-117">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="115a0-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="115a0-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="115a0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="115a0-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="115a0-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




