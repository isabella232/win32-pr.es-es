---
description: El instalador establece la propiedad System64Folder en la ruta de acceso completa a la carpeta System64 predefinida. La propiedad System64Folder existente se establece en la carpeta de 32 bits correspondiente.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Propiedad System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653948"
---
# <a name="system64folder-property"></a><span data-ttu-id="ae644-104">Propiedad System64Folder</span><span class="sxs-lookup"><span data-stu-id="ae644-104">System64Folder property</span></span>

<span data-ttu-id="ae644-105">El instalador establece la propiedad **System64Folder** en la ruta de acceso completa a la carpeta System64 predefinida.</span><span class="sxs-lookup"><span data-stu-id="ae644-105">The installer sets the **System64Folder** property to the full path to the predefined System64 folder.</span></span> <span data-ttu-id="ae644-106">La propiedad **System64Folder** existente se establece en la carpeta de 32 bits correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ae644-106">The existing **System64Folder** property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae644-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae644-107">Remarks</span></span>

<span data-ttu-id="ae644-108">El instalador establece esta propiedad en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ae644-108">The installer sets this property on 64-bit Windows.</span></span> <span data-ttu-id="ae644-109">Por ejemplo, en Windows de 64 bits, el valor puede ser C: \\ Window \\ system32.</span><span class="sxs-lookup"><span data-stu-id="ae644-109">For example, on 64-bit Windows, the value may be C:\\Window\\System32.</span></span> <span data-ttu-id="ae644-110">Esta propiedad no se utiliza en Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ae644-110">This property is not used on 32-bit Windows.</span></span>

<span data-ttu-id="ae644-111">Esta carpeta suele ser un subdirectorio de la carpeta Windows.</span><span class="sxs-lookup"><span data-stu-id="ae644-111">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="ae644-112">Sin embargo, reside en un servidor cuando se configura para las ventanas compartidas.</span><span class="sxs-lookup"><span data-stu-id="ae644-112">However, it resides on a server when configured for Shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae644-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae644-113">Requirements</span></span>



| <span data-ttu-id="ae644-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae644-114">Requirement</span></span> | <span data-ttu-id="ae644-115">Value</span><span class="sxs-lookup"><span data-stu-id="ae644-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae644-116">Versión</span><span class="sxs-lookup"><span data-stu-id="ae644-116">Version</span></span><br/> | <span data-ttu-id="ae644-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ae644-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ae644-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ae644-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ae644-119">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ae644-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ae644-120">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ae644-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae644-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ae644-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae644-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae644-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




