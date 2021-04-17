---
description: El instalador establece la propiedad MediaSourceDir en 1 cuando la instalación utiliza un origen ubicado en un medio, como un CD-ROM.
ms.assetid: 79c7c5eb-b212-4dbf-943a-00ebd6037ce1
title: Propiedad MediaSourceDir
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ae8ec79d11f8aaf5027ae0e68003532449c52ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670744"
---
# <a name="mediasourcedir-property"></a><span data-ttu-id="deea1-103">Propiedad MediaSourceDir</span><span class="sxs-lookup"><span data-stu-id="deea1-103">MediaSourceDir property</span></span>

<span data-ttu-id="deea1-104">El instalador establece la propiedad **MediaSourceDir** en 1 cuando la instalación utiliza un origen ubicado en un medio, como un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="deea1-104">The installer sets the **MediaSourceDir** property to 1 when the installation uses a source located on media, such as a CD-ROM.</span></span> <span data-ttu-id="deea1-105">Esta propiedad no se establece cuando la instalación utiliza un origen ubicado en una ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="deea1-105">This property is not set when the installation uses a source located at a network location.</span></span> <span data-ttu-id="deea1-106">Por ejemplo, el [control SelectionTree](selectiontree-control.md) usa **MediaSourceDir** para determinar si la instalación se ejecuta desde el origen o se ejecuta desde una ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="deea1-106">For example, the [SelectionTree Control](selectiontree-control.md) uses **MediaSourceDir** to determine whether the installation is being run from source or run from a network location.</span></span>

## <a name="requirements"></a><span data-ttu-id="deea1-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deea1-107">Requirements</span></span>



| <span data-ttu-id="deea1-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="deea1-108">Requirement</span></span> | <span data-ttu-id="deea1-109">Value</span><span class="sxs-lookup"><span data-stu-id="deea1-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deea1-110">Versión</span><span class="sxs-lookup"><span data-stu-id="deea1-110">Version</span></span><br/> | <span data-ttu-id="deea1-111">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="deea1-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="deea1-112">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="deea1-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="deea1-113">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="deea1-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="deea1-114">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="deea1-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="deea1-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="deea1-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deea1-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="deea1-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




