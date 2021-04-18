---
description: La propiedad PATCHNEWSUMMARYCOMMENTS actualiza la propiedad de Resumen comentarios de una instalación administrativa durante la revisión.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: Propiedad PATCHNEWSUMMARYCOMMENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe2bff9613fa5d39ae300e15c3ee816c5c6fce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653414"
---
# <a name="patchnewsummarycomments-property"></a><span data-ttu-id="c26b1-103">Propiedad PATCHNEWSUMMARYCOMMENTS</span><span class="sxs-lookup"><span data-stu-id="c26b1-103">PATCHNEWSUMMARYCOMMENTS property</span></span>

<span data-ttu-id="c26b1-104">La propiedad **PATCHNEWSUMMARYCOMMENTS** actualiza la propiedad de [**Resumen comentarios**](comments-summary.md) de una instalación administrativa durante la revisión.</span><span class="sxs-lookup"><span data-stu-id="c26b1-104">The **PATCHNEWSUMMARYCOMMENTS** property updates the [**Comments Summary**](comments-summary.md) property of an administrative installation during patching.</span></span> <span data-ttu-id="c26b1-105">Esta propiedad solo se establece mediante una transformación en un archivo. msp.</span><span class="sxs-lookup"><span data-stu-id="c26b1-105">This property is only set by a transform in a .msp file.</span></span> <span data-ttu-id="c26b1-106">El archivo. MSP debe incluir una transformación que agregue esta propiedad a la [tabla de propiedades](property-table.md) y establezca su valor.</span><span class="sxs-lookup"><span data-stu-id="c26b1-106">The .msp file must include a transform that adds this property to the [Property table](property-table.md) and sets its value.</span></span> <span data-ttu-id="c26b1-107">Después, el instalador escribe el valor de **PATCHNEWSUMMARYCOMMENTS** en la propiedad [**Summary del número de revisión**](revision-number-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="c26b1-107">The installer then writes the value of **PATCHNEWSUMMARYCOMMENTS** to the [**Revision Number Summary**](revision-number-summary.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="c26b1-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c26b1-108">Remarks</span></span>

<span data-ttu-id="c26b1-109">Las propiedades [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS** y [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) se usan para actualizar la información de resumen cuando se instala una revisión en una imagen administrativa.</span><span class="sxs-lookup"><span data-stu-id="c26b1-109">The [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS**, and [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) properties are used to update the summary information when a patch is installed to an administrative image.</span></span>

## <a name="requirements"></a><span data-ttu-id="c26b1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c26b1-110">Requirements</span></span>



| <span data-ttu-id="c26b1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c26b1-111">Requirement</span></span> | <span data-ttu-id="c26b1-112">Value</span><span class="sxs-lookup"><span data-stu-id="c26b1-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c26b1-113">Versión</span><span class="sxs-lookup"><span data-stu-id="c26b1-113">Version</span></span><br/> | <span data-ttu-id="c26b1-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c26b1-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c26b1-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c26b1-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c26b1-116">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c26b1-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c26b1-117">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c26b1-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c26b1-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c26b1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c26b1-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c26b1-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




