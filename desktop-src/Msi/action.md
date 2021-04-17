---
description: La propiedad ACTION se puede establecer en los valores siguientes.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: ACTION (propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653762"
---
# <a name="action-property"></a><span data-ttu-id="f91fe-103">ACTION (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f91fe-103">ACTION property</span></span>

<span data-ttu-id="f91fe-104">La propiedad **Action** se puede establecer en los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f91fe-104">The **ACTION** property can be set to the following values.</span></span>

## <a name="value"></a><span data-ttu-id="f91fe-105">Value</span><span class="sxs-lookup"><span data-stu-id="f91fe-105">Value</span></span>



| <span data-ttu-id="f91fe-106">Value</span><span class="sxs-lookup"><span data-stu-id="f91fe-106">Value</span></span>                                                                                                                                            | <span data-ttu-id="f91fe-107">Significado</span><span class="sxs-lookup"><span data-stu-id="f91fe-107">Meaning</span></span>                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <span data-ttu-id="f91fe-108"><dt>**INSTALADOS**</dt></span><span class="sxs-lookup"><span data-stu-id="f91fe-108"><dt>**INSTALL**</dt></span></span> </dl>       | [<span data-ttu-id="f91fe-109">Acción de instalación</span><span class="sxs-lookup"><span data-stu-id="f91fe-109">INSTALL Action</span></span>](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <span data-ttu-id="f91fe-110"><dt>**ANUNCIA**</dt></span><span class="sxs-lookup"><span data-stu-id="f91fe-110"><dt>**ADVERTISE**</dt></span></span> </dl> | [<span data-ttu-id="f91fe-111">Acción de anuncio</span><span class="sxs-lookup"><span data-stu-id="f91fe-111">ADVERTISE Action</span></span>](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <span data-ttu-id="f91fe-112"><dt>**ADMINISTRAR**</dt></span><span class="sxs-lookup"><span data-stu-id="f91fe-112"><dt>**ADMIN**</dt></span></span> </dl>             | [<span data-ttu-id="f91fe-113">Acción de administración</span><span class="sxs-lookup"><span data-stu-id="f91fe-113">ADMIN Action</span></span>](admin-action.md)<br/>         |



 

<span data-ttu-id="f91fe-114">La propiedad **Action** determina la acción que se realizará si se proporciona un nombre de acción null a [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o al [**método OnAction**](session-doaction.md).</span><span class="sxs-lookup"><span data-stu-id="f91fe-114">The **ACTION** property determines which action to perform if a Null action name is supplied to [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) or the [**DoAction Method**](session-doaction.md).</span></span> <span data-ttu-id="f91fe-115">Si no se define ningún valor para la propiedad **Action** , el instalador llama a la [acción de instalación](install-action.md).</span><span class="sxs-lookup"><span data-stu-id="f91fe-115">If no value is defined for the **ACTION** property, the installer calls the [INSTALL Action](install-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f91fe-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f91fe-116">Requirements</span></span>



| <span data-ttu-id="f91fe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f91fe-117">Requirement</span></span> | <span data-ttu-id="f91fe-118">Value</span><span class="sxs-lookup"><span data-stu-id="f91fe-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f91fe-119">Versión</span><span class="sxs-lookup"><span data-stu-id="f91fe-119">Version</span></span><br/> | <span data-ttu-id="f91fe-120">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f91fe-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f91fe-121">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f91fe-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f91fe-122">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f91fe-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f91fe-123">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f91fe-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f91fe-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f91fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f91fe-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f91fe-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




