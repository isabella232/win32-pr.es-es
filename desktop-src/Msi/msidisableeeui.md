---
description: Para deshabilitar la interfaz de usuario insertada para la instalación definida en la tabla MsiEmbeddedUI, establezca la propiedad MSIDISABLEEEUI en 1 en la línea de comandos.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Propiedad MSIDISABLEEEUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d89ce43f649d406e4ae086db236375c02c43e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671059"
---
# <a name="msidisableeeui-property"></a><span data-ttu-id="38827-103">Propiedad MSIDISABLEEEUI</span><span class="sxs-lookup"><span data-stu-id="38827-103">MSIDISABLEEEUI property</span></span>

<span data-ttu-id="38827-104">Para deshabilitar la interfaz de usuario insertada para la instalación definida en la [tabla MsiEmbeddedUI](msiembeddedui-table.md), establezca la propiedad MSIDISABLEEEUI en 1 en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="38827-104">To disable the embedded user interface for the installation defined in the [MsiEmbeddedUI table](msiembeddedui-table.md), set the MSIDISABLEEEUI property to 1 on the command line.</span></span>

<span data-ttu-id="38827-105">**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="38827-105">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="38827-106">Las versiones anteriores a Windows Installer 4,5 omiten la propiedad MSIDISABLEEEUI.</span><span class="sxs-lookup"><span data-stu-id="38827-106">Versions earlier than Windows Installer 4.5 ignore the MSIDISABLEEEUI Property.</span></span>

## <a name="remarks"></a><span data-ttu-id="38827-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38827-107">Remarks</span></span>

<span data-ttu-id="38827-108">En una instalación de varios paquetes, un paquete secundario debe usar normalmente la interfaz de usuario del paquete primario y no inicializar su propia interfaz de usuario incrustada.</span><span class="sxs-lookup"><span data-stu-id="38827-108">In a multiple-package installation, a child package should typically use the user interface of the parent package and not initialize its own embedded UI.</span></span> <span data-ttu-id="38827-109">Si la propiedad MSIDISABLEEEUI no se establece en el paquete primario, el paquete secundario utiliza de forma predeterminada la interfaz de usuario incrustada del paquete primario y omite la propiedad MSIDISABLEEEUI en el paquete secundario.</span><span class="sxs-lookup"><span data-stu-id="38827-109">If the MSIDISABLEEEUI property is not set inside the parent package, the child package uses the embedded UI of the parent package by default and ignores the MSIDISABLEEEUI property within the child package.</span></span>

<span data-ttu-id="38827-110">La propiedad MSIDISABLEEEUI deshabilita la interfaz de usuario incrustada para un único paquete.</span><span class="sxs-lookup"><span data-stu-id="38827-110">The MSIDISABLEEEUI property disables the embedded user interface for a single package.</span></span> <span data-ttu-id="38827-111">Puede usar la directiva [MsiDisableEmbeddedUI](msidisableembeddedui.md) para deshabilitar las interfaces de usuario incrustadas para todos los paquetes del equipo.</span><span class="sxs-lookup"><span data-stu-id="38827-111">You can use the [MsiDisableEmbeddedUI](msidisableembeddedui.md) policy to disable embedded user interfaces for all packages on the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="38827-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38827-112">Requirements</span></span>



| <span data-ttu-id="38827-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="38827-113">Requirement</span></span> | <span data-ttu-id="38827-114">Value</span><span class="sxs-lookup"><span data-stu-id="38827-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38827-115">Versión</span><span class="sxs-lookup"><span data-stu-id="38827-115">Version</span></span><br/> | <span data-ttu-id="38827-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="38827-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="38827-117">Windows Installer 4,5 en Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="38827-117">Windows Installer 4.5 on Windows Server 2008, Windows Vista, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="38827-118">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="38827-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38827-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38827-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38827-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38827-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




