---
description: Al establecer la propiedad ARPNOMODIFY, se deshabilita la funcionalidad agregar o quitar programas del panel de control que modifica el producto.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Propiedad ARPNOMODIFY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653620"
---
# <a name="arpnomodify-property"></a><span data-ttu-id="bf352-103">Propiedad ARPNOMODIFY</span><span class="sxs-lookup"><span data-stu-id="bf352-103">ARPNOMODIFY property</span></span>

<span data-ttu-id="bf352-104">Al establecer la propiedad **ARPNOMODIFY** , se deshabilita la funcionalidad agregar o quitar programas del panel de control que modifica el producto.</span><span class="sxs-lookup"><span data-stu-id="bf352-104">Setting the **ARPNOMODIFY** property disables Add or Remove Programs functionality in Control Panel that modifies the product.</span></span> <span data-ttu-id="bf352-105">En Windows 2000, Esto deshabilita el botón **modificar** del producto en **Agregar o quitar programas** en el **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="bf352-105">For Windows 2000, this disables the **Modify** button for the product in **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="bf352-106">En los sistemas operativos anteriores, al hacer clic en el botón **Agregar o quitar programas** , se desinstala el producto en lugar de entrar en el Asistente para el modo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="bf352-106">On earlier operating systems, clicking the **Add or Remove Programs** button uninstalls the product rather than entering the maintenance mode wizard.</span></span>

<span data-ttu-id="bf352-107">Si se establece la propiedad **ARPNOMODIFY** , la [acción RegisterProduct](registerproduct-action.md) escribe el valor "nomodify" en la clave del registro:</span><span class="sxs-lookup"><span data-stu-id="bf352-107">If the **ARPNOMODIFY** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoModify" under the registry key:</span></span>

<span data-ttu-id="bf352-108">**HKLM** \\ **Software** \\ de **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ **{*clave de producto*}**</span><span class="sxs-lookup"><span data-stu-id="bf352-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="bf352-109">Si se establece la propiedad **ARPNOMODIFY** y no se establece la propiedad [**ARPNOREMOVE**](arpnoremove.md) , la acción RegisterProduct también escribe el valor de UninstallString bajo esta clave.</span><span class="sxs-lookup"><span data-stu-id="bf352-109">If the **ARPNOMODIFY** property is set and the [**ARPNOREMOVE**](arpnoremove.md) property is not set, the RegisterProduct action also writes the UninstallString value under this key.</span></span> <span data-ttu-id="bf352-110">El valor de UnistallString es una línea de comandos para quitar el producto, en lugar de volver a configurar el producto.</span><span class="sxs-lookup"><span data-stu-id="bf352-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf352-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf352-111">Remarks</span></span>

<span data-ttu-id="bf352-112">En Windows 2000, Esto deshabilita el botón **cambiar** del producto en **Agregar o quitar programas** del **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="bf352-112">On Windows 2000, this disables the **Change** button for the product in the **Add or Remove Programs** of the **Control Panel**.</span></span>

<span data-ttu-id="bf352-113">Esta propiedad se puede establecer mediante una transformación de personalización para evitar que los usuarios cambien la personalización de un administrador a través de **Agregar o quitar programas**.</span><span class="sxs-lookup"><span data-stu-id="bf352-113">This property can be set by a customization transform to prevent users from changing an administrator's customization through **Add or Remove Programs**.</span></span> <span data-ttu-id="bf352-114">Esta propiedad solo afecta a **Agregar o quitar programas**.</span><span class="sxs-lookup"><span data-stu-id="bf352-114">This property only affects **Add or Remove Programs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf352-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf352-115">Requirements</span></span>



| <span data-ttu-id="bf352-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf352-116">Requirement</span></span> | <span data-ttu-id="bf352-117">Value</span><span class="sxs-lookup"><span data-stu-id="bf352-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf352-118">Versión</span><span class="sxs-lookup"><span data-stu-id="bf352-118">Version</span></span><br/> | <span data-ttu-id="bf352-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf352-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bf352-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bf352-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bf352-121">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bf352-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bf352-122">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bf352-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf352-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bf352-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf352-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf352-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="bf352-125">Ejemplo de transformación de personalización</span><span class="sxs-lookup"><span data-stu-id="bf352-125">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> </dl>

 

 




