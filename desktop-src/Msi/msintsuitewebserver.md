---
description: En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad MsiNTSuiteWebServer en 1 si el instalador se ejecuta en una edición web de Windows Server 2003.
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: Propiedad MsiNTSuiteWebServer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082e3ae7f107bf3499f5a48473d53ebb530138a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670721"
---
# <a name="msintsuitewebserver-property"></a><span data-ttu-id="bec35-103">Propiedad MsiNTSuiteWebServer</span><span class="sxs-lookup"><span data-stu-id="bec35-103">MsiNTSuiteWebServer property</span></span>

<span data-ttu-id="bec35-104">En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad **MsiNTSuiteWebServer** en 1 si el instalador se ejecuta en una edición web de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bec35-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteWebServer** property to 1 if the installer is running on a web edition of the Windows Server 2003.</span></span> <span data-ttu-id="bec35-105">El instalador establece esta propiedad en 1 solo si la \_ marca de la hoja de ver conjunto \_ está establecida en la estructura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="bec35-105">The installer sets this property to 1 only if the VER\_SUITE\_BLADE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="bec35-106">En caso contrario, el instalador no establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="bec35-106">Otherwise the installer does not set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="bec35-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bec35-107">Remarks</span></span>

<span data-ttu-id="bec35-108">Esta propiedad solo está disponible en la versión 2003 del instalador de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="bec35-108">This property is available only with the Windows Server 2003 release of the installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="bec35-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bec35-109">Requirements</span></span>



| <span data-ttu-id="bec35-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="bec35-110">Requirement</span></span> | <span data-ttu-id="bec35-111">Value</span><span class="sxs-lookup"><span data-stu-id="bec35-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec35-112">Versión</span><span class="sxs-lookup"><span data-stu-id="bec35-112">Version</span></span><br/> | <span data-ttu-id="bec35-113">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bec35-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bec35-114">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bec35-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bec35-115">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bec35-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bec35-116">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bec35-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bec35-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bec35-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec35-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bec35-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="bec35-119">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="bec35-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 
