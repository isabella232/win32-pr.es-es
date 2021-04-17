---
description: La propiedad de Resumen de recuento de caracteres solo se usa en transformaciones.
ms.assetid: d26d24a5-558e-4333-ae39-ffba1bbc5247
title: Propiedad de Resumen de recuento de caracteres
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afc99c065721f0f0b94691a12e00204305940efd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670899"
---
# <a name="character-count-summary-property"></a><span data-ttu-id="db789-103">Propiedad de Resumen de recuento de caracteres</span><span class="sxs-lookup"><span data-stu-id="db789-103">Character Count Summary property</span></span>

<span data-ttu-id="db789-104">La propiedad de **Resumen de recuento de caracteres** solo se usa en transformaciones.</span><span class="sxs-lookup"><span data-stu-id="db789-104">The **Character Count Summary** property is only used in transforms.</span></span> <span data-ttu-id="db789-105">Esta parte de la secuencia de información de resumen se divide en palabras de 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="db789-105">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="db789-106">La palabra superior contiene las [*marcas de validación de transformación*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="db789-106">The upper word contains the [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="db789-107">La palabra inferior contiene las [*marcas de condición de error de transformación*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="db789-107">The lower word contains the [*transform error condition flags*](t-gly.md).</span></span>

<span data-ttu-id="db789-108">Esta propiedad debe ser null en un paquete de instalación o un paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="db789-108">This property should be Null in an installation package or patch package.</span></span>

## <a name="requirements"></a><span data-ttu-id="db789-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db789-109">Requirements</span></span>



| <span data-ttu-id="db789-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="db789-110">Requirement</span></span> | <span data-ttu-id="db789-111">Value</span><span class="sxs-lookup"><span data-stu-id="db789-111">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db789-112">Versión</span><span class="sxs-lookup"><span data-stu-id="db789-112">Version</span></span><br/> | <span data-ttu-id="db789-113">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="db789-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="db789-114">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="db789-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="db789-115">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="db789-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db789-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="db789-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db789-117">Descripciones de propiedades de Resumen</span><span class="sxs-lookup"><span data-stu-id="db789-117">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




