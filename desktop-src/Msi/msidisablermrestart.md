---
description: La propiedad MSIDISABLERMRESTART determina cómo se deben apagar y reiniciar las aplicaciones o servicios que usan actualmente los archivos afectados por una actualización para habilitar la instalación de la actualización.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: Propiedad MSIDISABLERMRESTART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653741"
---
# <a name="msidisablermrestart-property"></a><span data-ttu-id="7489c-103">Propiedad MSIDISABLERMRESTART</span><span class="sxs-lookup"><span data-stu-id="7489c-103">MSIDISABLERMRESTART property</span></span>

<span data-ttu-id="7489c-104">La propiedad **MSIDISABLERMRESTART** determina cómo se deben apagar y reiniciar las aplicaciones o servicios que usan actualmente los archivos afectados por una actualización para habilitar la instalación de la actualización.</span><span class="sxs-lookup"><span data-stu-id="7489c-104">The **MSIDISABLERMRESTART** property determines how applications or services that are currently using files affected by an update should be shut down and restarted to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="7489c-105">Value</span><span class="sxs-lookup"><span data-stu-id="7489c-105">Value</span></span>



| <span data-ttu-id="7489c-106">Value</span><span class="sxs-lookup"><span data-stu-id="7489c-106">Value</span></span>                                                                        | <span data-ttu-id="7489c-107">Significado</span><span class="sxs-lookup"><span data-stu-id="7489c-107">Meaning</span></span>                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7489c-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7489c-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="7489c-109">Se reinician todos los servicios del sistema que se cerraron para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="7489c-109">All system services that were shut down to install the update are restarted.</span></span> <span data-ttu-id="7489c-110">Se reinician todas las aplicaciones que se registraron con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="7489c-110">All applications that registered themselves with the [Restart Manager](../rstmgr/restart-manager-portal.md) are restarted.</span></span><br/> |
| <dl> <span data-ttu-id="7489c-111"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7489c-111"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7489c-112">Los procesos que se cerraron con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) al instalar la actualización no se reiniciarán una vez aplicada la actualización.</span><span class="sxs-lookup"><span data-stu-id="7489c-112">Processes that were shut down using the [Restart Manager](../rstmgr/restart-manager-portal.md) while installing the update will not be restarted after the update is applied.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="7489c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7489c-113">Remarks</span></span>

<span data-ttu-id="7489c-114">La propiedad **MSIDISABLERMRESTART** se omite si el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) no está disponible o está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7489c-114">The **MSIDISABLERMRESTART** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="7489c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7489c-115">Requirements</span></span>



| <span data-ttu-id="7489c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7489c-116">Requirement</span></span> | <span data-ttu-id="7489c-117">Value</span><span class="sxs-lookup"><span data-stu-id="7489c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7489c-118">Versión</span><span class="sxs-lookup"><span data-stu-id="7489c-118">Version</span></span><br/> | <span data-ttu-id="7489c-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7489c-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7489c-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7489c-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7489c-121">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima requerida por una versión de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7489c-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7489c-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7489c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7489c-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7489c-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="7489c-124">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="7489c-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
