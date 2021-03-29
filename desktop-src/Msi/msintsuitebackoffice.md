---
description: En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad MsiNTSuiteBackOffice en 1 si los componentes de Microsoft BackOffice están instalados.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: Propiedad MsiNTSuiteBackOffice
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2d9f2f1d95446c32b4f2addf520f3d5b4dadc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653916"
---
# <a name="msintsuitebackoffice-property"></a><span data-ttu-id="6226a-103">Propiedad MsiNTSuiteBackOffice</span><span class="sxs-lookup"><span data-stu-id="6226a-103">MsiNTSuiteBackOffice property</span></span>

<span data-ttu-id="6226a-104">En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad **MsiNTSuiteBackOffice** en 1 si los componentes de Microsoft BackOffice están instalados.</span><span class="sxs-lookup"><span data-stu-id="6226a-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteBackOffice** property to 1 if Microsoft BackOffice components are installed.</span></span> <span data-ttu-id="6226a-105">El instalador establece esta propiedad en 1 solo si la \_ marca de BackOffice del conjunto de versión \_ se establece en la estructura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="6226a-105">The installer sets this property to 1 only if the VER\_SUITE\_BACKOFFICE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="6226a-106">De lo contrario, el instalador no establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="6226a-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6226a-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6226a-107">Requirements</span></span>



| <span data-ttu-id="6226a-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="6226a-108">Requirement</span></span> | <span data-ttu-id="6226a-109">Value</span><span class="sxs-lookup"><span data-stu-id="6226a-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6226a-110">Versión</span><span class="sxs-lookup"><span data-stu-id="6226a-110">Version</span></span><br/> | <span data-ttu-id="6226a-111">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6226a-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6226a-112">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6226a-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6226a-113">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6226a-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6226a-114">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6226a-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6226a-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6226a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6226a-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6226a-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
