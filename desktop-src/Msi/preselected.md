---
description: La propiedad preseleccionada indica que las características ya se han seleccionado y que no es necesario mostrar el cuadro de diálogo de selección. Las expresiones condicionales que dependen de si las características ya están instaladas usan este valor.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Propiedad preseleccionada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653861"
---
# <a name="preselected-property"></a><span data-ttu-id="0e665-103">Propiedad preseleccionada</span><span class="sxs-lookup"><span data-stu-id="0e665-103">Preselected property</span></span>

<span data-ttu-id="0e665-104">La propiedad **preseleccionada** indica que las características ya se han seleccionado y que no es necesario mostrar el cuadro de diálogo de selección.</span><span class="sxs-lookup"><span data-stu-id="0e665-104">The **Preselected** property indicates that features have already been selected and that the selection dialog need not be shown.</span></span>

<span data-ttu-id="0e665-105">Las expresiones condicionales que dependen de si las características ya están instaladas usan este valor.</span><span class="sxs-lookup"><span data-stu-id="0e665-105">Conditional expressions which depend on whether features are already installed use this value.</span></span> <span data-ttu-id="0e665-106">Por ejemplo, la propiedad se puede utilizar para suprimir los cuadros de diálogo que impliquen selecciones de características durante la reanudación de una instalación suspendida.</span><span class="sxs-lookup"><span data-stu-id="0e665-106">For example, the property can be used to suppress any dialogs involving feature selections during the resumption of a suspended installation.</span></span>

<span data-ttu-id="0e665-107">El instalador establece la propiedad **preseleccionada** en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las siguientes propiedades en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0e665-107">The installer sets the **Preselected** property to a value of "1" during the resumption of a suspended installation or when any of the following properties are specified on the command line.</span></span> <span data-ttu-id="0e665-108">Si la propiedad **preseleccionada** se ha establecido en 1, el instalador no utiliza la [tabla de condiciones](condition-table.md) para evaluar la selección de características.</span><span class="sxs-lookup"><span data-stu-id="0e665-108">If the **Preselected** property has been set to 1, the installer does not use the [Condition table](condition-table.md) to evaluate the selection of features.</span></span> <span data-ttu-id="0e665-109">Las características se instalan en función de las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="0e665-109">Features are installed based upon the following properties.</span></span> <span data-ttu-id="0e665-110">El instalador siempre evalúa estas propiedades en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="0e665-110">The installer always evaluates these properties in the following order:</span></span>

1.  [<span data-ttu-id="0e665-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="0e665-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="0e665-112">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="0e665-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="0e665-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="0e665-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="0e665-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0e665-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="0e665-115">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="0e665-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="0e665-116">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="0e665-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="0e665-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="0e665-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="0e665-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="0e665-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="0e665-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0e665-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="0e665-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="0e665-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="0e665-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="0e665-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="0e665-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0e665-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

## <a name="requirements"></a><span data-ttu-id="0e665-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e665-123">Requirements</span></span>



| <span data-ttu-id="0e665-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e665-124">Requirement</span></span> | <span data-ttu-id="0e665-125">Value</span><span class="sxs-lookup"><span data-stu-id="0e665-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e665-126">Versión</span><span class="sxs-lookup"><span data-stu-id="0e665-126">Version</span></span><br/> | <span data-ttu-id="0e665-127">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0e665-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0e665-128">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0e665-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0e665-129">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e665-129">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="0e665-130">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0e665-130">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e665-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0e665-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e665-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e665-132">Properties</span></span>](properties.md)
</dt> </dl>

 

 




