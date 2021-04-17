---
description: La propiedad de la \_ unidad CCP se establece en la ruta de acceso raíz del volumen extraíble en el que se buscará RMCCPSearch.
ms.assetid: 567b7d11-6d80-4ec5-810d-f32b9ebf5809
title: Propiedad CCP_DRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6215881cd3a998cd63a958bfe258ad3f9872ab1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670745"
---
# <a name="ccp_drive-property"></a><span data-ttu-id="a1dfd-103">Propiedad de la \_ unidad CCP</span><span class="sxs-lookup"><span data-stu-id="a1dfd-103">CCP\_DRIVE property</span></span>

<span data-ttu-id="a1dfd-104">La propiedad de la **\_ unidad CCP** se establece en la ruta de acceso raíz del volumen extraíble en el que se buscará [RMCCPSearch](rmccpsearch-action.md).</span><span class="sxs-lookup"><span data-stu-id="a1dfd-104">The **CCP\_DRIVE** property is set to the root path of the removable volume that is to be searched by [RMCCPSearch](rmccpsearch-action.md).</span></span> <span data-ttu-id="a1dfd-105">La acción RMCCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.</span><span class="sxs-lookup"><span data-stu-id="a1dfd-105">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before performing an upgrade installation.</span></span>

<span data-ttu-id="a1dfd-106">Esta propiedad se establece normalmente a través de la interfaz de usuario o una acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="a1dfd-106">This property is typically set via the user interface or a custom action.</span></span> <span data-ttu-id="a1dfd-107">Esta propiedad debe establecerse antes de que se ejecute la acción [RMCCPSearch](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a1dfd-107">This property should be set before the [RMCCPSearch](rmccpsearch-action.md) action is run.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1dfd-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1dfd-108">Requirements</span></span>



| <span data-ttu-id="a1dfd-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1dfd-109">Requirement</span></span> | <span data-ttu-id="a1dfd-110">Value</span><span class="sxs-lookup"><span data-stu-id="a1dfd-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1dfd-111">Versión</span><span class="sxs-lookup"><span data-stu-id="a1dfd-111">Version</span></span><br/> | <span data-ttu-id="a1dfd-112">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a1dfd-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a1dfd-113">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a1dfd-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a1dfd-114">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a1dfd-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a1dfd-115">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a1dfd-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1dfd-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a1dfd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1dfd-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1dfd-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




