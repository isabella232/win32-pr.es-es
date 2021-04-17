---
description: El valor de la propiedad Resumen de asunto transmite el nombre del producto, la transformación o el parche que instala el paquete.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Propiedad de Resumen de asunto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653564"
---
# <a name="subject-summary-property"></a><span data-ttu-id="f19ed-103">Propiedad de Resumen de asunto</span><span class="sxs-lookup"><span data-stu-id="f19ed-103">Subject Summary property</span></span>

<span data-ttu-id="f19ed-104">El valor de la propiedad **Resumen de asunto** transmite el nombre del producto, la transformación o el parche que instala el paquete.</span><span class="sxs-lookup"><span data-stu-id="f19ed-104">The value of the **Subject Summary** property conveys the name of the product, transform, or patch that is installed by the package.</span></span>

<span data-ttu-id="f19ed-105">Es el autor de una base de datos de instalación, una transformación o un paquete de revisión que proporcione el valor de esta propiedad en la información de resumen.</span><span class="sxs-lookup"><span data-stu-id="f19ed-105">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="f19ed-106">Los autores deben hacer lo siguiente para determinar el valor correcto.</span><span class="sxs-lookup"><span data-stu-id="f19ed-106">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="f19ed-107">Establezca la propiedad **Resumen de asunto** de un paquete de instalación en el mismo valor que la propiedad [**ProductName**](productname.md) .</span><span class="sxs-lookup"><span data-stu-id="f19ed-107">Set the **Subject Summary** property in an installation package to the same value as the [**ProductName**](productname.md) property.</span></span>
-   <span data-ttu-id="f19ed-108">Establezca la propiedad **Resumen del asunto** en una transformación en el mismo valor que la propiedad Resumen del **firmante** en el paquete de instalación original.</span><span class="sxs-lookup"><span data-stu-id="f19ed-108">Set the **Subject Summary** property in a transform to the same value as the **Subject Summary** property in the original installation package.</span></span>
-   <span data-ttu-id="f19ed-109">Establezca la propiedad **Resumen del asunto** en la información de Resumen de un paquete de revisión en una breve descripción de la revisión que incluye el nombre del producto.</span><span class="sxs-lookup"><span data-stu-id="f19ed-109">Set the **Subject Summary** property in the summary information of a patch package to a short description of the patch that includes the name of the product.</span></span>

## <a name="requirements"></a><span data-ttu-id="f19ed-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f19ed-110">Requirements</span></span>



| <span data-ttu-id="f19ed-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f19ed-111">Requirement</span></span> | <span data-ttu-id="f19ed-112">Value</span><span class="sxs-lookup"><span data-stu-id="f19ed-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f19ed-113">Versión</span><span class="sxs-lookup"><span data-stu-id="f19ed-113">Version</span></span><br/> | <span data-ttu-id="f19ed-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f19ed-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f19ed-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f19ed-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f19ed-116">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="f19ed-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f19ed-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="f19ed-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f19ed-118">**PATCHNEWSUMMARYSUBJECT**</span><span class="sxs-lookup"><span data-stu-id="f19ed-118">**PATCHNEWSUMMARYSUBJECT**</span></span>](patchnewsummarysubject.md)
</dt> <dt>

[<span data-ttu-id="f19ed-119">Descripciones de propiedades de Resumen</span><span class="sxs-lookup"><span data-stu-id="f19ed-119">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




