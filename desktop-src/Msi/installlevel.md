---
description: La propiedad INSTALLLEVEL es el nivel inicial en el que se seleccionan las características &\# 0034; en&\# 0034; para la instalación de de forma predeterminada.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: Propiedad INSTALLLEVEL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc0616fdf49e2c713c65017a202320fa6ea9622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690457"
---
# <a name="installlevel-property"></a><span data-ttu-id="99205-103">Propiedad INSTALLLEVEL</span><span class="sxs-lookup"><span data-stu-id="99205-103">INSTALLLEVEL property</span></span>

<span data-ttu-id="99205-104">La propiedad **INSTALLLEVEL** es el nivel inicial en el que se seleccionan las características "ON" para la instalación de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="99205-104">The **INSTALLLEVEL** property is the initial level at which features are selected "ON" for installation by default.</span></span> <span data-ttu-id="99205-105">Una característica se instala solo si el valor del campo nivel de la [tabla de características](feature-table.md) es menor o igual que el valor de INSTALLLEVEL actual.</span><span class="sxs-lookup"><span data-stu-id="99205-105">A feature is installed only if the value in the Level field of the [Feature table](feature-table.md) is less than or equal to the current INSTALLLEVEL value.</span></span> <span data-ttu-id="99205-106">El nivel de instalación de cualquier instalación se especifica mediante la propiedad **INSTALLLEVEL** y puede ser un entero comprendido entre 1 y 32.767.</span><span class="sxs-lookup"><span data-stu-id="99205-106">The installation level for any installation is specified by the **INSTALLLEVEL** property, and can be an integral from 1 to 32,767.</span></span> <span data-ttu-id="99205-107">Para obtener más información sobre los niveles de instalación, consulte [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="99205-107">For further discussion of installation levels, see [Feature Table](feature-table.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="99205-108">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="99205-108">Default Value</span></span>

<span data-ttu-id="99205-109">Si no se especifica ningún valor, el valor predeterminado del nivel de instalación es 1.</span><span class="sxs-lookup"><span data-stu-id="99205-109">If no value is specified, the install level defaults to 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="99205-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99205-110">Remarks</span></span>

<span data-ttu-id="99205-111">El nivel de instalación especificado por la propiedad **INSTALLLEVEL** se puede invalidar con las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="99205-111">The installation level specified by the **INSTALLLEVEL** property can be overridden by the following properties:</span></span>

-   [<span data-ttu-id="99205-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="99205-112">**ADDLOCAL**</span></span>](addlocal.md)
-   [<span data-ttu-id="99205-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="99205-113">**ADDSOURCE**</span></span>](addsource.md)
-   [<span data-ttu-id="99205-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="99205-114">**ADDDEFAULT**</span></span>](adddefault.md)
-   [<span data-ttu-id="99205-115">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="99205-115">**COMPADDLOCAL**</span></span>](compaddlocal.md)
-   [<span data-ttu-id="99205-116">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="99205-116">**COMPADDSOURCE**</span></span>](compaddsource.md)
-   [<span data-ttu-id="99205-117">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="99205-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="99205-118">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="99205-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="99205-119">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="99205-119">**REMOVE**</span></span>](remove.md)
-   [<span data-ttu-id="99205-120">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="99205-120">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="99205-121">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="99205-121">**ADVERTISE**</span></span>](advertise.md)

<span data-ttu-id="99205-122">Por ejemplo, al establecer ADDLOCAL = ALL se instalan todas las características localmente, independientemente del valor de la propiedad **INSTALLLEVEL** .</span><span class="sxs-lookup"><span data-stu-id="99205-122">For example, setting ADDLOCAL=ALL installs all features locally regardless of the value of the **INSTALLLEVEL** property.</span></span> <span data-ttu-id="99205-123">Si el valor de la columna LEVEL de la [tabla de características](feature-table.md) es 0, esa característica no se instala y no se muestra en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="99205-123">If the value of the Level column in the [Feature table](feature-table.md) is 0, that feature is not installed and not displayed in the UI.</span></span>

<span data-ttu-id="99205-124">Un administrador puede deshabilitar una característica de forma permanente aplicando una transformación de personalización que establezca un 0 en la columna de nivel para esa característica.</span><span class="sxs-lookup"><span data-stu-id="99205-124">An administrator can permanently disable a feature by applying a customization transform that sets a 0 in the Level column for that feature.</span></span> <span data-ttu-id="99205-125">La aplicación de la transformación de personalización evita la instalación y visualización de la característica incluso si el usuario selecciona una instalación completa mediante la interfaz de usuario o estableciendo ADDLOCAL en ALL en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="99205-125">The application of the customization transform prevents the installation and display of the feature even if the user selects a complete installation using the UI or by setting ADDLOCAL to ALL on the command line.</span></span> <span data-ttu-id="99205-126">Vea [un ejemplo de transformación de personalización](a-customization-transform-example.md).</span><span class="sxs-lookup"><span data-stu-id="99205-126">See [A Customization Transform Example](a-customization-transform-example.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99205-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99205-127">Requirements</span></span>



| <span data-ttu-id="99205-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="99205-128">Requirement</span></span> | <span data-ttu-id="99205-129">Value</span><span class="sxs-lookup"><span data-stu-id="99205-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99205-130">Versión</span><span class="sxs-lookup"><span data-stu-id="99205-130">Version</span></span><br/> | <span data-ttu-id="99205-131">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="99205-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="99205-132">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="99205-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="99205-133">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="99205-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="99205-134">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="99205-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99205-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="99205-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99205-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="99205-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




