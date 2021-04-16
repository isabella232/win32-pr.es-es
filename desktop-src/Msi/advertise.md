---
description: El valor de la propiedad anunciado es una lista de características delimitadas por comas que se van a anunciar.
ms.assetid: ef97f70b-e4bf-4eb3-b643-046a9c348823
title: Propiedad de anuncio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e768f22f86dacf35009ca0e0e3ef9337ef84ab70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671245"
---
# <a name="advertise-property"></a><span data-ttu-id="fe651-103">Propiedad de anuncio</span><span class="sxs-lookup"><span data-stu-id="fe651-103">ADVERTISE property</span></span>

<span data-ttu-id="fe651-104">El valor de la propiedad **anunciado** es una lista de características delimitadas por comas que se van a anunciar.</span><span class="sxs-lookup"><span data-stu-id="fe651-104">The value of the **ADVERTISE** property is a list of features delimited by commas that are to be advertised.</span></span> <span data-ttu-id="fe651-105">Las características deben estar presentes en la columna característica de la tabla de [características](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fe651-105">The features must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="fe651-106">Para instalar todas las características como anunciadas, use ANUNCIAd = ALL en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="fe651-106">To install all features as advertised, use ADVERTISE=ALL on the command line.</span></span> <span data-ttu-id="fe651-107">No escriba ANUNCIAd = ALL en la [tabla de propiedades](property-table.md) porque genera un paquete anunciado que no se puede instalar ni quitar.</span><span class="sxs-lookup"><span data-stu-id="fe651-107">Do not enter ADVERTISE=ALL into the [Property table](property-table.md) because this generates an advertised package that cannot be installed or removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe651-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe651-108">Remarks</span></span>

<span data-ttu-id="fe651-109">Tenga en cuenta que los nombres de las características distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fe651-109">Note that feature names are case-sensitive.</span></span>

<span data-ttu-id="fe651-110">El instalador siempre evalúa las siguientes propiedades en el orden siguiente.</span><span class="sxs-lookup"><span data-stu-id="fe651-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="fe651-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="fe651-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="fe651-112">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="fe651-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="fe651-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="fe651-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="fe651-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="fe651-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="fe651-115">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="fe651-115">**REINSTALL**</span></span>](reinstall.md)
6.  <span data-ttu-id="fe651-116">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="fe651-116">**ADVERTISE**</span></span>
7.  [<span data-ttu-id="fe651-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="fe651-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="fe651-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="fe651-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="fe651-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="fe651-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="fe651-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="fe651-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="fe651-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="fe651-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="fe651-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="fe651-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="fe651-123">Por ejemplo, si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = función, todas las características se establecen primero en Run-local y, a continuación, se establece la función de ejecución-desde-origen.</span><span class="sxs-lookup"><span data-stu-id="fe651-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="fe651-124">Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL = función, First la función se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = ALL, todas las características (incluidas las funciones) se restablecen a la ejecución desde el origen.</span><span class="sxs-lookup"><span data-stu-id="fe651-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="fe651-125">El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="fe651-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe651-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe651-126">Requirements</span></span>



| <span data-ttu-id="fe651-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe651-127">Requirement</span></span> | <span data-ttu-id="fe651-128">Value</span><span class="sxs-lookup"><span data-stu-id="fe651-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe651-129">Versión</span><span class="sxs-lookup"><span data-stu-id="fe651-129">Version</span></span><br/> | <span data-ttu-id="fe651-130">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fe651-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fe651-131">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fe651-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fe651-132">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fe651-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fe651-133">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fe651-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe651-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fe651-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe651-135">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fe651-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




