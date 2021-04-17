---
description: En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad MsiNTSuiteSmallBusinessRestricted en 1 si Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor.
ms.assetid: a7100df4-6fe4-4159-ba94-9b5bd1803107
title: Propiedad MsiNTSuiteSmallBusinessRestricted
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d85fa7fe83c0c8c7cd40788453d1078e7a6b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653552"
---
# <a name="msintsuitesmallbusinessrestricted-property"></a><span data-ttu-id="e3d0a-103">Propiedad MsiNTSuiteSmallBusinessRestricted</span><span class="sxs-lookup"><span data-stu-id="e3d0a-103">MsiNTSuiteSmallBusinessRestricted property</span></span>

<span data-ttu-id="e3d0a-104">En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad **MsiNTSuiteSmallBusinessRestricted** en 1 si Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor.</span><span class="sxs-lookup"><span data-stu-id="e3d0a-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteSmallBusinessRestricted** property to 1 if Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="e3d0a-105">El instalador establece esta propiedad en 1 solo si la \_ marca ver \_ conjunto \_ de SMALLBUSINESS restringido está establecida en la estructura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="e3d0a-105">The installer sets this property to 1 only if the VER\_SUITE\_SMALLBUSINESS\_RESTRICTED flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="e3d0a-106">En caso contrario, el instalador no establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e3d0a-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3d0a-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3d0a-107">Requirements</span></span>



| <span data-ttu-id="e3d0a-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3d0a-108">Requirement</span></span> | <span data-ttu-id="e3d0a-109">Value</span><span class="sxs-lookup"><span data-stu-id="e3d0a-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d0a-110">Versión</span><span class="sxs-lookup"><span data-stu-id="e3d0a-110">Version</span></span><br/> | <span data-ttu-id="e3d0a-111">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e3d0a-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e3d0a-112">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e3d0a-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e3d0a-113">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e3d0a-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e3d0a-114">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e3d0a-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3d0a-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e3d0a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3d0a-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3d0a-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
