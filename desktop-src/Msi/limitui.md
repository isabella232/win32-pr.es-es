---
description: Si se establece la propiedad LIMITUI, el nivel de la interfaz de usuario (UI) que se usa al instalar el paquete está restringido a básico.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Propiedad LIMITUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690042"
---
# <a name="limitui-property"></a><span data-ttu-id="028ce-103">Propiedad LIMITUI</span><span class="sxs-lookup"><span data-stu-id="028ce-103">LIMITUI property</span></span>

<span data-ttu-id="028ce-104">Si se establece la propiedad **LIMITUI** , el nivel de la interfaz de usuario (UI) que se usa al instalar el paquete está restringido a básico.</span><span class="sxs-lookup"><span data-stu-id="028ce-104">If the **LIMITUI** property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span> <span data-ttu-id="028ce-105">Esta propiedad es necesaria en los paquetes que no tienen ninguna interfaz de usuario creada pero que todavía contienen tablas de interfaz de usuario como la [tabla de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="028ce-105">This property is required in packages that have no authored UI but still contain UI tables such as the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="028ce-106">Para obtener una descripción de los niveles de interfaz de usuario, consulte [ **MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span><span class="sxs-lookup"><span data-stu-id="028ce-106">For a description of UI levels, see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span></span>

## <a name="remarks"></a><span data-ttu-id="028ce-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="028ce-107">Remarks</span></span>

<span data-ttu-id="028ce-108">Los paquetes de instalación que contienen la propiedad **LIMITUI** también deben contener la propiedad [**ARPNOMODIFY**](arpnomodify.md) .</span><span class="sxs-lookup"><span data-stu-id="028ce-108">Installation packages containing the **LIMITUI** property must also contain the [**ARPNOMODIFY**](arpnomodify.md) property.</span></span> <span data-ttu-id="028ce-109">Esto es necesario para que un usuario obtenga el comportamiento correcto de **Agregar o quitar programas** en la utilidad del **Panel de control** al intentar configurar un producto.</span><span class="sxs-lookup"><span data-stu-id="028ce-109">This is required for a user to obtain the correct behavior from the **Add or Remove Programs** in the **Control Panel** utility when attempting to configure a product.</span></span>

## <a name="requirements"></a><span data-ttu-id="028ce-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="028ce-110">Requirements</span></span>



| <span data-ttu-id="028ce-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="028ce-111">Requirement</span></span> | <span data-ttu-id="028ce-112">Value</span><span class="sxs-lookup"><span data-stu-id="028ce-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="028ce-113">Versión</span><span class="sxs-lookup"><span data-stu-id="028ce-113">Version</span></span><br/> | <span data-ttu-id="028ce-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="028ce-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="028ce-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="028ce-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="028ce-116">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="028ce-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="028ce-117">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="028ce-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="028ce-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="028ce-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="028ce-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="028ce-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="028ce-120">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="028ce-120">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[<span data-ttu-id="028ce-121">**ARPNOMODIFY**</span><span class="sxs-lookup"><span data-stu-id="028ce-121">**ARPNOMODIFY**</span></span>](arpnomodify.md)
</dt> </dl>

 

 




