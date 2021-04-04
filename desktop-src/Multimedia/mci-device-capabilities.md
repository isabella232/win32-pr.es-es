---
title: Funcionalidades del dispositivo MCI
description: Funcionalidades del dispositivo MCI
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- MCIWndCanConfig (macro)
- MCIWndCanEject (macro)
- MCIWndCanPlay (macro)
- MCIWndCanRecord (macro)
- MCIWndCanSave (macro)
- MCIWndCanWindow (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076273"
---
# <a name="mci-device-capabilities"></a><span data-ttu-id="64657-109">Funcionalidades del dispositivo MCI</span><span class="sxs-lookup"><span data-stu-id="64657-109">MCI Device Capabilities</span></span>

<span data-ttu-id="64657-110">MCIWnd incluye las siguientes macros que permiten consultar los dispositivos MCI en busca de sus capacidades.</span><span class="sxs-lookup"><span data-stu-id="64657-110">MCIWnd includes the following macros to let you query MCI devices for their capabilities.</span></span>



| <span data-ttu-id="64657-111">Macro</span><span class="sxs-lookup"><span data-stu-id="64657-111">Macro</span></span>                                      | <span data-ttu-id="64657-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="64657-112">Description</span></span>                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64657-113">**MCIWndCanConfig**</span><span class="sxs-lookup"><span data-stu-id="64657-113">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | <span data-ttu-id="64657-114">Determina si un dispositivo tiene un cuadro de diálogo de configuración para admitir varias configuraciones, como el dispositivo MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="64657-114">Determines whether a device has a configuration dialog box to support multiple configurations, such as the MCIAVI device.</span></span>                   |
| [<span data-ttu-id="64657-115">**MCIWndCanEject**</span><span class="sxs-lookup"><span data-stu-id="64657-115">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | <span data-ttu-id="64657-116">Determina si un dispositivo tiene una función EJECT controlada por software.</span><span class="sxs-lookup"><span data-stu-id="64657-116">Determines whether a device has a software-controlled eject function.</span></span>                                                                       |
| [<span data-ttu-id="64657-117">**MCIWndCanPlay**</span><span class="sxs-lookup"><span data-stu-id="64657-117">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | <span data-ttu-id="64657-118">Determina si un dispositivo puede reproducir el contenido existente.</span><span class="sxs-lookup"><span data-stu-id="64657-118">Determines whether a device can play the existing content.</span></span>                                                                                  |
| [<span data-ttu-id="64657-119">**MCIWndCanRecord**</span><span class="sxs-lookup"><span data-stu-id="64657-119">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | <span data-ttu-id="64657-120">Determina si un dispositivo puede grabar.</span><span class="sxs-lookup"><span data-stu-id="64657-120">Determines whether a device can record.</span></span>                                                                                                     |
| [<span data-ttu-id="64657-121">**MCIWndCanSave**</span><span class="sxs-lookup"><span data-stu-id="64657-121">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | <span data-ttu-id="64657-122">Determina si un dispositivo puede almacenar datos.</span><span class="sxs-lookup"><span data-stu-id="64657-122">Determines whether a device can store data.</span></span>                                                                                                 |
| [<span data-ttu-id="64657-123">**MCIWndCanWindow**</span><span class="sxs-lookup"><span data-stu-id="64657-123">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | <span data-ttu-id="64657-124">Determina si un dispositivo admite comandos de ventana MCI (como [**Window**](window.md), [**Put**](put.md) y [**Where**](where.md)).</span><span class="sxs-lookup"><span data-stu-id="64657-124">Determines whether a device supports MCI window commands (such as [**window**](window.md), [**put**](put.md) and [**where**](where.md)).</span></span> |



 

<span data-ttu-id="64657-125">Estas macros devuelven **true** si el dispositivo admite la funcionalidad específica o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="64657-125">These macros return **TRUE** if the device supports the specific capability, or **FALSE** otherwise.</span></span>

 

 




