---
description: El valor de la propiedad ProductVersion es la versión del producto en formato de cadena.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: Propiedad ProductVersion
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653794"
---
# <a name="productversion-property"></a><span data-ttu-id="528b5-103">Propiedad ProductVersion</span><span class="sxs-lookup"><span data-stu-id="528b5-103">ProductVersion property</span></span>

<span data-ttu-id="528b5-104">El valor de la propiedad **ProductVersion** es la versión del producto en formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="528b5-104">The value of the **ProductVersion** property is the version of the product in string format.</span></span> <span data-ttu-id="528b5-105">Esta propiedad es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="528b5-105">This property is REQUIRED.</span></span>

<span data-ttu-id="528b5-106">El formato de la cadena es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="528b5-106">The format of the string is as follows:</span></span>

<dl> <span data-ttu-id="528b5-107">principal.secundario.de compilación</span><span class="sxs-lookup"><span data-stu-id="528b5-107">major.minor.build</span></span>  
</dl>

<span data-ttu-id="528b5-108">El primer campo es la versión principal y tiene un valor máximo de 255.</span><span class="sxs-lookup"><span data-stu-id="528b5-108">The first field is the major version and has a maximum value of 255.</span></span> <span data-ttu-id="528b5-109">El segundo campo es la versión secundaria y tiene un valor máximo de 255.</span><span class="sxs-lookup"><span data-stu-id="528b5-109">The second field is the minor version and has a maximum value of 255.</span></span> <span data-ttu-id="528b5-110">El tercer campo se denomina versión de compilación o versión de actualización y tiene un valor máximo de 65.535.</span><span class="sxs-lookup"><span data-stu-id="528b5-110">The third field is called the build version or the update version and has a maximum value of 65,535.</span></span>

## <a name="remarks"></a><span data-ttu-id="528b5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="528b5-111">Remarks</span></span>

<span data-ttu-id="528b5-112">Al menos uno de los tres campos de **ProductVersion** debe cambiar para una actualización mediante la [tabla de actualización](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="528b5-112">At least one of the three fields of **ProductVersion** must change for an upgrade using the [Upgrade table](upgrade-table.md).</span></span> <span data-ttu-id="528b5-113">Cualquier actualización que solo cambie el código de paquete, pero deja **ProductVersion** y [**ProductCode**](productcode.md) sin modificar se denomina una [actualización pequeña](small-updates.md).</span><span class="sxs-lookup"><span data-stu-id="528b5-113">Any update that changes only the package code, but leaves **ProductVersion** and [**ProductCode**](productcode.md) unchanged is called a [small update](small-updates.md).</span></span> <span data-ttu-id="528b5-114">Los campos de tres versiones se proporcionan principalmente para mayor comodidad.</span><span class="sxs-lookup"><span data-stu-id="528b5-114">The three versions fields are provided primarily for convenience.</span></span> <span data-ttu-id="528b5-115">Por ejemplo, si desea cambiar el **ProductVersion** pero no desea cambiar la versión principal o secundaria, puede cambiar la versión de compilación.</span><span class="sxs-lookup"><span data-stu-id="528b5-115">For example, if you want to change **ProductVersion**, but do not want to change either the major or minor versions, you can change the build version.</span></span>

<span data-ttu-id="528b5-116">Tenga en cuenta que Windows Installer solo utiliza los tres primeros campos de la versión del producto.</span><span class="sxs-lookup"><span data-stu-id="528b5-116">Note that Windows Installer uses only the first three fields of the product version.</span></span> <span data-ttu-id="528b5-117">Si incluye un cuarto campo en la versión del producto, el instalador omite el cuarto campo.</span><span class="sxs-lookup"><span data-stu-id="528b5-117">If you include a fourth field in your product version, the installer ignores the fourth field.</span></span>

## <a name="requirements"></a><span data-ttu-id="528b5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="528b5-118">Requirements</span></span>



| <span data-ttu-id="528b5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="528b5-119">Requirement</span></span> | <span data-ttu-id="528b5-120">Value</span><span class="sxs-lookup"><span data-stu-id="528b5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="528b5-121">Versión</span><span class="sxs-lookup"><span data-stu-id="528b5-121">Version</span></span><br/> | <span data-ttu-id="528b5-122">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="528b5-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="528b5-123">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="528b5-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="528b5-124">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="528b5-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="528b5-125">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="528b5-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="528b5-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="528b5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="528b5-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="528b5-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="528b5-128">Revisiones y actualizaciones</span><span class="sxs-lookup"><span data-stu-id="528b5-128">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="528b5-129">actualización pequeña</span><span class="sxs-lookup"><span data-stu-id="528b5-129">small update</span></span>](small-updates.md)
</dt> </dl>

 

 




