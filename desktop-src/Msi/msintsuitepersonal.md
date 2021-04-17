---
description: En Windows XP y sistemas operativos posteriores, el instalador establece la propiedad MsiNTSuitePersonal en 1 si el sistema operativo es Windows XP Home Edition.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: Propiedad MsiNTSuitePersonal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8932cf2d2c9c5079d6955571512cbc9836e41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653554"
---
# <a name="msintsuitepersonal-property"></a><span data-ttu-id="503a7-103">Propiedad MsiNTSuitePersonal</span><span class="sxs-lookup"><span data-stu-id="503a7-103">MsiNTSuitePersonal property</span></span>

<span data-ttu-id="503a7-104">En Windows XP y sistemas operativos posteriores, el instalador establece la propiedad **MsiNTSuitePersonal** en 1 si el sistema operativo es Windows XP Home Edition.</span><span class="sxs-lookup"><span data-stu-id="503a7-104">On Windows XP and later operating systems, the installer sets the **MsiNTSuitePersonal** property to 1 if the operating system is Windows XP Home Edition.</span></span> <span data-ttu-id="503a7-105">El instalador establece esta propiedad en 1 solo si \_ \_ se establece la marca personal de ver conjunto en la estructura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="503a7-105">The installer sets this property to 1 only if the VER\_SUITE\_PERSONAL flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="503a7-106">En caso contrario, el instalador no establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="503a7-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="503a7-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="503a7-107">Requirements</span></span>



| <span data-ttu-id="503a7-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="503a7-108">Requirement</span></span> | <span data-ttu-id="503a7-109">Value</span><span class="sxs-lookup"><span data-stu-id="503a7-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="503a7-110">Versión</span><span class="sxs-lookup"><span data-stu-id="503a7-110">Version</span></span><br/> | <span data-ttu-id="503a7-111">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="503a7-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="503a7-112">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="503a7-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="503a7-113">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="503a7-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="503a7-114">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="503a7-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="503a7-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="503a7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="503a7-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="503a7-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
