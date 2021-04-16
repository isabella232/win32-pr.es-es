---
description: La propiedad Intel se establece mediante el Windows Installer en el nivel de procesador numérico cuando se ejecuta en un procesador Intel.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Propiedad Intel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690572"
---
# <a name="intel-property"></a><span data-ttu-id="d8fb5-103">Propiedad Intel</span><span class="sxs-lookup"><span data-stu-id="d8fb5-103">Intel property</span></span>

<span data-ttu-id="d8fb5-104">La propiedad **Intel** se establece mediante el Windows Installer en el nivel de procesador numérico cuando se ejecuta en un procesador Intel.</span><span class="sxs-lookup"><span data-stu-id="d8fb5-104">The **Intel** property is set by the Windows Installer to the numeric processor level when running on an Intel processor.</span></span> <span data-ttu-id="d8fb5-105">Los valores son los mismos que el campo *wProcessorLevel* de la estructura de [**\_ información del sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="d8fb5-105">The values are the same as the *wProcessorLevel* field of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span> <span data-ttu-id="d8fb5-106">Cuando se ejecuta en un procesador x64, el Windows Installer establece la propiedad **Intel** para que refleje el procesador x86 emulado por el equipo x64, tal y como lo indica el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d8fb5-106">When running on a x64 processor, the Windows Installer sets the **Intel** property to reflect the x86 processor emulated by the x64 computer as reported by the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8fb5-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8fb5-107">Requirements</span></span>



| <span data-ttu-id="d8fb5-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8fb5-108">Requirement</span></span> | <span data-ttu-id="d8fb5-109">Value</span><span class="sxs-lookup"><span data-stu-id="d8fb5-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8fb5-110">Versión</span><span class="sxs-lookup"><span data-stu-id="d8fb5-110">Version</span></span><br/> | <span data-ttu-id="d8fb5-111">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d8fb5-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d8fb5-112">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d8fb5-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d8fb5-113">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d8fb5-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d8fb5-114">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d8fb5-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8fb5-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d8fb5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8fb5-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d8fb5-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
