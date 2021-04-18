---
description: En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad MsiNTSuiteEnterprise en 1 si Windows 2000 Advanced Server está instalado.
ms.assetid: f5384467-3791-4b0b-a70e-b5343c70db46
title: Propiedad MsiNTSuiteEnterprise
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137b4ece4dbaecdd83b78fd2ce7cfd57820e029d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653379"
---
# <a name="msintsuiteenterprise-property"></a><span data-ttu-id="a9147-103">Propiedad MsiNTSuiteEnterprise</span><span class="sxs-lookup"><span data-stu-id="a9147-103">MsiNTSuiteEnterprise property</span></span>

<span data-ttu-id="a9147-104">En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad **MsiNTSuiteEnterprise** en 1 si Windows 2000 Advanced Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="a9147-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteEnterprise** property to 1 if Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="a9147-105">El instalador establece esta propiedad en 1 solo si \_ \_ se establece la marca de la versión Enterprise de ver conjunto en la estructura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="a9147-105">The installer sets this property to 1 only if the VER\_SUITE\_ENTERPRISE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="a9147-106">De lo contrario, el instalador no establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a9147-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9147-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9147-107">Requirements</span></span>



| <span data-ttu-id="a9147-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9147-108">Requirement</span></span> | <span data-ttu-id="a9147-109">Value</span><span class="sxs-lookup"><span data-stu-id="a9147-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9147-110">Versión</span><span class="sxs-lookup"><span data-stu-id="a9147-110">Version</span></span><br/> | <span data-ttu-id="a9147-111">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a9147-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a9147-112">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a9147-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a9147-113">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a9147-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a9147-114">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a9147-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9147-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a9147-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9147-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9147-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
