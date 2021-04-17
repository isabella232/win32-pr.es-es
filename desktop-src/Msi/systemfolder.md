---
description: El instalador establece la propiedad Carpetadelsistema en la ruta de acceso completa de la carpeta del sistema.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: Propiedad Carpetadelsistema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680561"
---
# <a name="systemfolder-property"></a><span data-ttu-id="f9978-103">Propiedad Carpetadelsistema</span><span class="sxs-lookup"><span data-stu-id="f9978-103">SystemFolder property</span></span>

<span data-ttu-id="f9978-104">El instalador establece la propiedad **carpetadelsistema** en la ruta de acceso completa de la carpeta del sistema.</span><span class="sxs-lookup"><span data-stu-id="f9978-104">The installer sets the **SystemFolder** property to the full path of the System folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9978-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9978-105">Remarks</span></span>

<span data-ttu-id="f9978-106">El instalador establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f9978-106">The installer sets this property.</span></span> <span data-ttu-id="f9978-107">Por ejemplo, en Windows de 32 bits, el valor puede ser C: \\ Windows \\ system32.</span><span class="sxs-lookup"><span data-stu-id="f9978-107">For example, on 32-bit Windows the value may be C:\\Windows\\System32.</span></span> <span data-ttu-id="f9978-108">En Windows de 64 bits, el valor puede ser C: \\ Windows \\ SysWow64.</span><span class="sxs-lookup"><span data-stu-id="f9978-108">On 64-bit Windows, the value may be C:\\Windows\\SysWow64.</span></span>

<span data-ttu-id="f9978-109">Esta carpeta suele ser un subdirectorio de la carpeta Windows.</span><span class="sxs-lookup"><span data-stu-id="f9978-109">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="f9978-110">Sin embargo, reside en un servidor cuando se configura para las ventanas compartidas.</span><span class="sxs-lookup"><span data-stu-id="f9978-110">However, it resides on a server when configured for Shared Windows.</span></span>

<span data-ttu-id="f9978-111">Esta carpeta es local, incluso cuando está configurada para ventanas compartidas.</span><span class="sxs-lookup"><span data-stu-id="f9978-111">This folder is local, even when configured for shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9978-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9978-112">Requirements</span></span>



| <span data-ttu-id="f9978-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9978-113">Requirement</span></span> | <span data-ttu-id="f9978-114">Value</span><span class="sxs-lookup"><span data-stu-id="f9978-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9978-115">Versión</span><span class="sxs-lookup"><span data-stu-id="f9978-115">Version</span></span><br/> | <span data-ttu-id="f9978-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f9978-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f9978-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f9978-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f9978-118">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f9978-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f9978-119">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f9978-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9978-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f9978-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9978-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9978-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




