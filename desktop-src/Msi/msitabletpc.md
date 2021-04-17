---
description: El instalador establece la propiedad MsiTabletPC en un valor distinto de cero si el sistema operativo actual es Windows XP Tablet PC Edition.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Propiedad MsiTabletPC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680796"
---
# <a name="msitabletpc-property"></a><span data-ttu-id="a361a-103">Propiedad MsiTabletPC</span><span class="sxs-lookup"><span data-stu-id="a361a-103">MsiTabletPC property</span></span>

<span data-ttu-id="a361a-104">El instalador establece la propiedad **MsiTabletPC** en un valor distinto de cero si el sistema operativo actual es Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="a361a-104">The installer sets the **MsiTabletPC** property to a nonzero value if the current operating system is Windows XP Tablet PC Edition.</span></span> <span data-ttu-id="a361a-105">El instalador usa la función [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ TABLETPC** y la propiedad recibe el valor distinto de cero devuelto por esta función.</span><span class="sxs-lookup"><span data-stu-id="a361a-105">The installer uses the [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function with **SM\_TABLETPC**, and the property receives the nonzero value returned by this function.</span></span> <span data-ttu-id="a361a-106">Si el sistema actual no es Windows XP Tablet PC Edition, la función **GetSystemMetrics** devuelve cero y el instalador no establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a361a-106">If the current system is not Windows XP Tablet PC Edition, the **GetSystemMetrics** function returns zero and the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a361a-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a361a-107">Requirements</span></span>



| <span data-ttu-id="a361a-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="a361a-108">Requirement</span></span> | <span data-ttu-id="a361a-109">Value</span><span class="sxs-lookup"><span data-stu-id="a361a-109">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a361a-110">Versión</span><span class="sxs-lookup"><span data-stu-id="a361a-110">Version</span></span><br/> | <span data-ttu-id="a361a-111">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a361a-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a361a-112">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a361a-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a361a-113">Windows Installer 4,5 en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a361a-113">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a361a-114">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a361a-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a361a-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a361a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a361a-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a361a-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="a361a-117">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="a361a-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
