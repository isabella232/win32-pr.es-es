---
description: La propiedad ROOTDRIVE especifica la unidad predeterminada para el directorio de destino de la instalación.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: Propiedad ROOTDRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679282"
---
# <a name="rootdrive-property"></a><span data-ttu-id="38caa-103">Propiedad ROOTDRIVE</span><span class="sxs-lookup"><span data-stu-id="38caa-103">ROOTDRIVE property</span></span>

<span data-ttu-id="38caa-104">La propiedad **ROOTDRIVE** especifica la unidad predeterminada para el directorio de destino de la instalación.</span><span class="sxs-lookup"><span data-stu-id="38caa-104">The **ROOTDRIVE** property specifies the default drive for the destination directory of the installation.</span></span> <span data-ttu-id="38caa-105">Si la columna de directorio de la [tabla de directorio](directory-table.md) indica el directorio de destino raíz mediante un nombre de propiedad que no está definido, el instalador usa el valor de la propiedad **ROOTDRIVE** para resolver la ruta de acceso al directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="38caa-105">If the Directory column of the [Directory table](directory-table.md) indicates the root destination directory by a property name that is undefined, the installer uses the value of the **ROOTDRIVE** property to resolve the path to the destination directory.</span></span>

<span data-ttu-id="38caa-106">Si **ROOTDRIVE** no se establece en una línea de comandos o se crea en la [tabla de propiedades](property-table.md), el instalador establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="38caa-106">If **ROOTDRIVE** is not set at a command line or authored into the [Property table](property-table.md), the installer sets this property.</span></span> <span data-ttu-id="38caa-107">Durante una [instalación administrativa](administrative-installation.md) , el instalador establece **ROOTDRIVE** en la primera unidad de red conectada que encuentra en la que se puede escribir.</span><span class="sxs-lookup"><span data-stu-id="38caa-107">During an [administrative installation](administrative-installation.md) the installer sets **ROOTDRIVE** to the first connected network drive it finds that can be written to.</span></span> <span data-ttu-id="38caa-108">Si no se trata de una instalación administrativa, o si el instalador no puede encontrar ninguna unidad de red, el instalador establece **ROOTDRIVE** en la unidad local que se puede escribir para que tenga más espacio libre.</span><span class="sxs-lookup"><span data-stu-id="38caa-108">If it is not an administrative installation, or if the installer can find no network drives, the installer sets **ROOTDRIVE** to the local drive that can be written to having the most free space.</span></span>

<span data-ttu-id="38caa-109">El valor de esta propiedad debe terminar en ' \\ '.</span><span class="sxs-lookup"><span data-stu-id="38caa-109">The value for this property must end with '\\'.</span></span>

## <a name="requirements"></a><span data-ttu-id="38caa-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38caa-110">Requirements</span></span>



| <span data-ttu-id="38caa-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="38caa-111">Requirement</span></span> | <span data-ttu-id="38caa-112">Value</span><span class="sxs-lookup"><span data-stu-id="38caa-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38caa-113">Versión</span><span class="sxs-lookup"><span data-stu-id="38caa-113">Version</span></span><br/> | <span data-ttu-id="38caa-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="38caa-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="38caa-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="38caa-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="38caa-116">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="38caa-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="38caa-117">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="38caa-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38caa-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38caa-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38caa-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38caa-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




