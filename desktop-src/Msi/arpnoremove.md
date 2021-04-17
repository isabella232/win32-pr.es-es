---
description: Al establecer la propiedad ARPNOREMOVE, se deshabilita la funcionalidad agregar o quitar programas del panel de control que quita el producto.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: Propiedad ARPNOREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670833"
---
# <a name="arpnoremove-property"></a><span data-ttu-id="f0caf-103">Propiedad ARPNOREMOVE</span><span class="sxs-lookup"><span data-stu-id="f0caf-103">ARPNOREMOVE property</span></span>

<span data-ttu-id="f0caf-104">Al establecer la propiedad **ARPNOREMOVE** , se deshabilita la funcionalidad **Agregar o quitar programas** del **Panel de control** que quita el producto.</span><span class="sxs-lookup"><span data-stu-id="f0caf-104">Setting the **ARPNOREMOVE** property disables the **Add or Remove Programs** functionality in **Control Panel** that removes the product.</span></span> <span data-ttu-id="f0caf-105">En Windows 2000, Esto deshabilita el botón **quitar** del producto en **Agregar o quitar programas** en el **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="f0caf-105">For Windows 2000, this disables the **Remove** button for the product from the **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="f0caf-106">En el caso de los sistemas operativos anteriores, esto tiene el efecto de quitar el producto de la lista de productos instalados en **Agregar o quitar programas** en el **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="f0caf-106">For earlier operating systems, this has the effect of removing the product from the list of installed products on the **Add or Remove Programs** in **Control Panel**.</span></span>

<span data-ttu-id="f0caf-107">Si se establece la propiedad **ARPNOREMOVE** , la [acción RegisterProduct](registerproduct-action.md) escribe el valor "noremove" en la clave del registro:</span><span class="sxs-lookup"><span data-stu-id="f0caf-107">If the **ARPNOREMOVE** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoRemove" under the registry key:</span></span>

<span data-ttu-id="f0caf-108">**HKLM** \\ **Software** \\ de **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ **{*clave de producto*}**</span><span class="sxs-lookup"><span data-stu-id="f0caf-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="f0caf-109">El establecimiento de la propiedad **ARPNOREMOVE** evita que el valor de UninstallString se escriba en esta clave.</span><span class="sxs-lookup"><span data-stu-id="f0caf-109">Setting the **ARPNOREMOVE** property prevents the UninstallString value from being written under this key.</span></span> <span data-ttu-id="f0caf-110">El valor de UnistallString es una línea de comandos para quitar el producto, en lugar de volver a configurar el producto.</span><span class="sxs-lookup"><span data-stu-id="f0caf-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0caf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0caf-111">Remarks</span></span>

<span data-ttu-id="f0caf-112">Por ejemplo, esta propiedad se puede establecer durante una transformación de personalización para impedir que los usuarios quiten una personalización de administrador.</span><span class="sxs-lookup"><span data-stu-id="f0caf-112">For example, this property can be set during a customization transform to prevent users from removing an administrator customization.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0caf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0caf-113">Requirements</span></span>



| <span data-ttu-id="f0caf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0caf-114">Requirement</span></span> | <span data-ttu-id="f0caf-115">Value</span><span class="sxs-lookup"><span data-stu-id="f0caf-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0caf-116">Versión</span><span class="sxs-lookup"><span data-stu-id="f0caf-116">Version</span></span><br/> | <span data-ttu-id="f0caf-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f0caf-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f0caf-118">Windows Installer 4,0 o Windows Installer 4,5 o posterior en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f0caf-118">Windows Installer 4.0 or Windows Installer 4.5 or later on Windows Vista.</span></span> <span data-ttu-id="f0caf-119">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f0caf-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f0caf-120">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f0caf-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f0caf-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f0caf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0caf-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0caf-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




