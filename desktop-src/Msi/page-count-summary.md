---
description: La propiedad de Resumen de recuento de páginas contiene la versión de instalador mínima que requiere el paquete de instalación.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Propiedad de Resumen de recuento de páginas
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653769"
---
# <a name="page-count-summary-property"></a><span data-ttu-id="d6cbc-103">Propiedad de Resumen de recuento de páginas</span><span class="sxs-lookup"><span data-stu-id="d6cbc-103">Page Count Summary property</span></span>

<span data-ttu-id="d6cbc-104">La propiedad de **Resumen de recuento de páginas** contiene la versión de instalador mínima que requiere el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-104">The **Page Count Summary** property contains the minimum installer version required by the installation package.</span></span> <span data-ttu-id="d6cbc-105">Para un mínimo de Windows Installer 2,0, esta propiedad se debe establecer en el entero 200.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-105">For a minimum of Windows Installer 2.0, this property must be set to the integer 200.</span></span> <span data-ttu-id="d6cbc-106">Para un mínimo de Windows Installer 3,0, esta propiedad se debe establecer en el entero 300.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-106">For a minimum of Windows Installer 3.0, this property must be set to the integer 300.</span></span> <span data-ttu-id="d6cbc-107">Para un mínimo de Windows Installer 3,1, esta propiedad debe establecerse en 301.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-107">For a minimum of Windows Installer 3.1, this property must be set to 301.</span></span> <span data-ttu-id="d6cbc-108">Para un mínimo de Windows Installer 4,5, esta propiedad debe establecerse en 405.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-108">For a minimum of Windows Installer 4.5, this property must be set to 405.</span></span> <span data-ttu-id="d6cbc-109">Para un mínimo de Windows Installer 5,0, esta propiedad debe establecerse en 500.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-109">For a minimum of Windows Installer 5.0, this property must be set to 500.</span></span>

<span data-ttu-id="d6cbc-110">En el caso de los [paquetes de Windows Installer de 64 bits](64-bit-windows-installer-packages.md), esta propiedad se debe establecer en el entero 200 o superior.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-110">For [64-bit Windows Installer Packages](64-bit-windows-installer-packages.md), this property must be set to the integer 200 or greater.</span></span> <span data-ttu-id="d6cbc-111">En el caso de los paquetes de Windows Installer de 64 bits en la plataforma Arm64, esta propiedad se debe establecer en el entero 500 o superior.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-111">For 64-bit Windows Installer Packages on the Arm64 platform, this property must be set to the integer 500 or greater.</span></span>

<span data-ttu-id="d6cbc-112">En el caso de un paquete de transformación, la propiedad de **Resumen de recuento de páginas** contiene la versión de instalador mínima necesaria para procesar la transformación.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-112">For a transform package, the **Page Count Summary** property contains the minimum installer version required to process the transform.</span></span> <span data-ttu-id="d6cbc-113">Se establece en el mayor de los dos valores de propiedad de **Resumen de recuento de páginas** que pertenecen a las bases de datos utilizadas para generar la transformación.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-113">Set to the greater of the two **Page Count Summary** property values that belong to the databases used to generate the transform.</span></span>

<span data-ttu-id="d6cbc-114">En el caso de un paquete de revisión, la propiedad de **Resumen de recuento de páginas** está establecida en NULL.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-114">For a patch package, the **Page Count Summary** property is set to Null.</span></span>

<span data-ttu-id="d6cbc-115">Esta propiedad de resumen es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-115">This summary property is required.</span></span>

<span data-ttu-id="d6cbc-116">Esta propiedad se puede usar para crear un paquete que solo pueda instalarse en la versión mínima o posterior especificada del Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-116">This property can be used to author a package that can be installed only by the specified minimum or later version of the Windows Installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6cbc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6cbc-117">Requirements</span></span>



| <span data-ttu-id="d6cbc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6cbc-118">Requirement</span></span> | <span data-ttu-id="d6cbc-119">Value</span><span class="sxs-lookup"><span data-stu-id="d6cbc-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6cbc-120">Versión</span><span class="sxs-lookup"><span data-stu-id="d6cbc-120">Version</span></span><br/> | <span data-ttu-id="d6cbc-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d6cbc-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d6cbc-123">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="d6cbc-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6cbc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6cbc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6cbc-125">Descripciones de propiedades de Resumen</span><span class="sxs-lookup"><span data-stu-id="d6cbc-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




