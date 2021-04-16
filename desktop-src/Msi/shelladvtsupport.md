---
description: El instalador establece la propiedad ShellAdvtSupport si la interfaz IShellLink del sistema admite la resolución de descriptores de instalador.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Propiedad ShellAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678941"
---
# <a name="shelladvtsupport-property"></a><span data-ttu-id="fd5b0-103">Propiedad ShellAdvtSupport</span><span class="sxs-lookup"><span data-stu-id="fd5b0-103">ShellAdvtSupport property</span></span>

<span data-ttu-id="fd5b0-104">El instalador establece la propiedad **ShellAdvtSupport** si la interfaz [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema admite la resolución de descriptores de instalador.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-104">The **ShellAdvtSupport** property is set by the installer if the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd5b0-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd5b0-105">Remarks</span></span>

<span data-ttu-id="fd5b0-106">Si se establece esta propiedad, la interfaz [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema admite la resolución de descriptores de instalador.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-106">If this property is set, the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span> <span data-ttu-id="fd5b0-107">Es compatible con Windows 2000 y los sistemas que ejecutan Internet Explorer 4,01.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-107">This is supported by Windows 2000 and systems running Internet Explorer 4.01.</span></span> <span data-ttu-id="fd5b0-108">Si no se establece esta propiedad, el instalador tiene el comportamiento predeterminado de la creación de características no anunciadas durante la instalación, ya sea de forma local o se ejecuta desde el origen.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-108">If this property is not set, the installer has the default behavior of creating non-advertised features during installation, either locally or run from source.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd5b0-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd5b0-109">Requirements</span></span>



| <span data-ttu-id="fd5b0-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd5b0-110">Requirement</span></span> | <span data-ttu-id="fd5b0-111">Value</span><span class="sxs-lookup"><span data-stu-id="fd5b0-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5b0-112">Versión</span><span class="sxs-lookup"><span data-stu-id="fd5b0-112">Version</span></span><br/> | <span data-ttu-id="fd5b0-113">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fd5b0-114">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fd5b0-115">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fd5b0-116">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd5b0-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fd5b0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd5b0-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd5b0-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="fd5b0-119">Compatibilidad de la plataforma con el anuncio</span><span class="sxs-lookup"><span data-stu-id="fd5b0-119">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)
</dt> </dl>

 

 
