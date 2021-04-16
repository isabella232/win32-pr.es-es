---
description: La propiedad MSIRMSHUTDOWN determina cómo se deben cerrar las aplicaciones o servicios que usan actualmente los archivos afectados por una actualización para habilitar la instalación de la actualización.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Propiedad MSIRMSHUTDOWN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671372"
---
# <a name="msirmshutdown-property"></a><span data-ttu-id="78102-103">Propiedad MSIRMSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="78102-103">MSIRMSHUTDOWN property</span></span>

<span data-ttu-id="78102-104">La propiedad **MSIRMSHUTDOWN** determina cómo se deben cerrar las aplicaciones o servicios que usan actualmente los archivos afectados por una actualización para habilitar la instalación de la actualización.</span><span class="sxs-lookup"><span data-stu-id="78102-104">The **MSIRMSHUTDOWN** property determines how applications or services that are currently using files affected by an update should be shut down to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="78102-105">Value</span><span class="sxs-lookup"><span data-stu-id="78102-105">Value</span></span>



| <span data-ttu-id="78102-106">Value</span><span class="sxs-lookup"><span data-stu-id="78102-106">Value</span></span>                                                                        | <span data-ttu-id="78102-107">Significado</span><span class="sxs-lookup"><span data-stu-id="78102-107">Meaning</span></span>                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="78102-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="78102-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="78102-109">Los procesos o servicios que usan actualmente los archivos afectados por la actualización se apagan.</span><span class="sxs-lookup"><span data-stu-id="78102-109">Processes or services that are currently using files affected by the update are shut down.</span></span><br/>                                                                                                                                                                   |
| <dl> <span data-ttu-id="78102-110"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="78102-110"><dt>1</dt></span></span> </dl> | <span data-ttu-id="78102-111">Los procesos o servicios que usan actualmente los archivos afectados por la actualización y que no responden al [Administrador de reinicio](../rstmgr/restart-manager-portal.md), están obligados a cerrarse.</span><span class="sxs-lookup"><span data-stu-id="78102-111">Processes or services that are currently using files affected by the update, and that do not respond to the [Restart Manager](../rstmgr/restart-manager-portal.md), are forced to shut down.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="78102-112"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="78102-112"><dt>2</dt></span></span> </dl> | <span data-ttu-id="78102-113">Los procesos o servicios que usan actualmente archivos afectados por la actualización solo se apagan si se han registrado para un reinicio.</span><span class="sxs-lookup"><span data-stu-id="78102-113">Processes or services that are currently using files affected by the update are shut down only if they have all been registered for a restart.</span></span> <span data-ttu-id="78102-114">Si algún proceso o servicio no se ha registrado para un reinicio, no se cerrarán los procesos ni los servicios.</span><span class="sxs-lookup"><span data-stu-id="78102-114">If any process or service has not been registered for a restart, then no processes or services are shut down.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78102-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78102-115">Remarks</span></span>

<span data-ttu-id="78102-116">La propiedad **MSIRMSHUTDOWN** se omite si el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) no está disponible o está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="78102-116">The **MSIRMSHUTDOWN** property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="78102-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78102-117">Requirements</span></span>



| <span data-ttu-id="78102-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="78102-118">Requirement</span></span> | <span data-ttu-id="78102-119">Value</span><span class="sxs-lookup"><span data-stu-id="78102-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78102-120">Versión</span><span class="sxs-lookup"><span data-stu-id="78102-120">Version</span></span><br/> | <span data-ttu-id="78102-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="78102-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="78102-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="78102-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="78102-123">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima requerida por una versión de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="78102-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78102-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="78102-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78102-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78102-125">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="78102-126">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="78102-126">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
