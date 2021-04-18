---
description: Esta propiedad Windows Installer indica cuándo se ha establecido el nivel interno de la interfaz de usuario para ocultar el botón Cancelar.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: Propiedad MsiUIHideCancel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a25a940921dd4b0d91155765ee6768ec0d6d2bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680794"
---
# <a name="msiuihidecancel-property"></a><span data-ttu-id="45163-103">Propiedad MsiUIHideCancel</span><span class="sxs-lookup"><span data-stu-id="45163-103">MsiUIHideCancel property</span></span>

<span data-ttu-id="45163-104">El instalador establece la propiedad **MsiUIHideCancel** en 1 cuando se ha establecido el nivel de la interfaz de usuario interna para incluir INSTALLUILEVEL \_ HIDECANCEL con la función [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) o la propiedad [elemento uilevel](installer-uilevel.md)del objeto [**Installer**](installer-object.md) o mediante opciones de la [línea de comandos](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="45163-104">The installer sets the **MsiUIHideCancel** property to 1 when the internal user interface level has been set to include INSTALLUILEVEL\_HIDECANCEL with the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function or the [UILevel](installer-uilevel.md)property of the [**Installer**](installer-object.md) object or by using [Command Line Options](command-line-options.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="45163-105">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45163-105">Requirements</span></span>



| <span data-ttu-id="45163-106">Requisito</span><span class="sxs-lookup"><span data-stu-id="45163-106">Requirement</span></span> | <span data-ttu-id="45163-107">Value</span><span class="sxs-lookup"><span data-stu-id="45163-107">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45163-108">Versión</span><span class="sxs-lookup"><span data-stu-id="45163-108">Version</span></span><br/> | <span data-ttu-id="45163-109">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="45163-109">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="45163-110">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="45163-110">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="45163-111">Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="45163-111">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="45163-112">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="45163-112">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45163-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="45163-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45163-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="45163-114">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="45163-115">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="45163-115">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




