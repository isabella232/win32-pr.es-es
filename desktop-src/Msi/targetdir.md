---
description: La propiedad TARGETDIR especifica el directorio de destino raíz de la instalación.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: Propiedad TARGETDIR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680527"
---
# <a name="targetdir-property"></a><span data-ttu-id="bb5c5-103">Propiedad TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="bb5c5-103">TARGETDIR property</span></span>

<span data-ttu-id="bb5c5-104">La propiedad **targetDir** especifica el directorio de destino raíz de la instalación.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-104">The **TARGETDIR** property specifies the root destination directory for the installation.</span></span> <span data-ttu-id="bb5c5-105">**TargetDir** debe ser el nombre de una raíz en la tabla del [directorio](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bb5c5-105">**TARGETDIR** must be the name of one root in the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="bb5c5-106">Puede haber un único directorio de destino raíz.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-106">There may be only a single root destination directory.</span></span> <span data-ttu-id="bb5c5-107">Durante una [instalación administrativa](administrative-installation.md) , esta propiedad especifica la ubicación en la que se va a copiar el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-107">During an [administrative installation](administrative-installation.md) this property specifies the location to copy the installation package.</span></span> <span data-ttu-id="bb5c5-108">Durante una instalación no administrativa, esta propiedad especifica el directorio de destino raíz.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-108">During a non-administrative installation this property specifies the root destination directory.</span></span>

<span data-ttu-id="bb5c5-109">Para especificar el directorio raíz de destino, establezca la columna directorio de la tabla directorio en la propiedad **targetDir** y la columna DefaultDir en la propiedad [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="bb5c5-109">To specify the root destination directory, set the Directory column of the Directory table to the **TARGETDIR** property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="bb5c5-110">Si se define la propiedad **targetDir** , el directorio de destino se resuelve en el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-110">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="bb5c5-111">Si la propiedad **targetDir** es undefined, la propiedad [**ROOTDRIVE**](rootdrive.md) se utiliza para resolver la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-111">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span> <span data-ttu-id="bb5c5-112">Para obtener más información sobre el uso de la propiedad **targetDir** , vea [usar la tabla de directorio](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="bb5c5-112">For more information about using the **TARGETDIR** property, see [Using the Directory Table](using-the-directory-table.md).</span></span>

<span data-ttu-id="bb5c5-113">Tenga en cuenta que el valor de la propiedad **targetDir** se establece normalmente en la línea de comandos o a través de una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-113">Note that the value of the **TARGETDIR** property is typically set at the command line or through a user interface.</span></span> <span data-ttu-id="bb5c5-114">No se recomienda establecer **targetDir** mediante la creación de una ruta de acceso en la [tabla de propiedades](property-table.md) porque los equipos difieren en la configuración de la unidad local.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-114">Setting **TARGETDIR** by authoring a path into the [Property table](property-table.md) is not recommended because computers differ in the set up of the local drive.</span></span>

<span data-ttu-id="bb5c5-115">Para obtener más información sobre cómo cambiar el TARGETDIR durante una instalación, consulte [cambiar la ubicación de destino de un directorio](changing-the-target-location-for-a-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="bb5c5-115">For more information on how to change TARGETDIR during an installation see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="bb5c5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb5c5-116">Requirements</span></span>



| <span data-ttu-id="bb5c5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb5c5-117">Requirement</span></span> | <span data-ttu-id="bb5c5-118">Value</span><span class="sxs-lookup"><span data-stu-id="bb5c5-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5c5-119">Versión</span><span class="sxs-lookup"><span data-stu-id="bb5c5-119">Version</span></span><br/> | <span data-ttu-id="bb5c5-120">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bb5c5-121">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bb5c5-122">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bb5c5-123">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bb5c5-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb5c5-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bb5c5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb5c5-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb5c5-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




