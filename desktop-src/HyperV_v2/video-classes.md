---
description: Todas las máquinas virtuales reflejan la presencia de un controlador de vídeo S3 emulado y un controlador de vídeo sintético y acelerado.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Clases de vídeo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498023"
---
# <a name="video-classes"></a><span data-ttu-id="23459-103">Clases de vídeo</span><span class="sxs-lookup"><span data-stu-id="23459-103">Video classes</span></span>

<span data-ttu-id="23459-104">Todas las máquinas virtuales reflejan la presencia de un controlador de vídeo S3 emulado y un controlador de vídeo sintético y acelerado.</span><span class="sxs-lookup"><span data-stu-id="23459-104">All virtual machines reflect the presence of an emulated S3 video controller and an accelerated, synthetic video controller.</span></span>

<span data-ttu-id="23459-105">Cada controlador de pantalla tiene un objeto de encabezado de vídeo asociado a él.</span><span class="sxs-lookup"><span data-stu-id="23459-105">Each display controller has a video head object associated with it.</span></span> <span data-ttu-id="23459-106">Solo un controlador de pantalla puede estar activo en una máquina virtual en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="23459-106">Only one display controller can be active in a virtual machine at any time.</span></span>

<span data-ttu-id="23459-107">Existe una conexión de terminal para todas las sesiones remotas activas conectadas a una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="23459-107">A terminal connection is present for every active remote session connected to a virtual machine.</span></span>

<span data-ttu-id="23459-108">A continuación se enumeran las clases WMI de virtualización relacionadas con el vídeo.</span><span class="sxs-lookup"><span data-stu-id="23459-108">The following are virtualization WMI classes related to video.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="23459-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="23459-109">In this section</span></span>



| <span data-ttu-id="23459-110">Tema</span><span class="sxs-lookup"><span data-stu-id="23459-110">Topic</span></span>                                                                                  | <span data-ttu-id="23459-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="23459-111">Description</span></span>                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23459-112">**MSVM \_ S3DisplayController**</span><span class="sxs-lookup"><span data-stu-id="23459-112">**Msvm\_S3DisplayController**</span></span>](msvm-s3displaycontroller.md)<br/>               | <span data-ttu-id="23459-113">Representa el estado del controlador S3 emulado que se encuentra en cada configuración de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="23459-113">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span><br/>       |
| [<span data-ttu-id="23459-114">**MSVM \_ SyntheticDisplayController**</span><span class="sxs-lookup"><span data-stu-id="23459-114">**Msvm\_SyntheticDisplayController**</span></span>](msvm-syntheticdisplaycontroller.md)<br/> | <span data-ttu-id="23459-115">Representa el estado del controlador de pantalla sintético presente en cada configuración de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="23459-115">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span><br/> |
| [<span data-ttu-id="23459-116">**MSVM \_ SystemTerminalConnection**</span><span class="sxs-lookup"><span data-stu-id="23459-116">**Msvm\_SystemTerminalConnection**</span></span>](msvm-systemterminalconnection.md)<br/>     | <span data-ttu-id="23459-117">Asocia una máquina virtual a una conexión de terminal.</span><span class="sxs-lookup"><span data-stu-id="23459-117">Associates a virtual machine with a terminal connection.</span></span><br/>                                                        |
| [<span data-ttu-id="23459-118">**MSVM \_ TerminalConnection**</span><span class="sxs-lookup"><span data-stu-id="23459-118">**Msvm\_TerminalConnection**</span></span>](msvm-terminalconnection.md)<br/>                 | <span data-ttu-id="23459-119">Indica el estado de una sesión remota activa que interactúa con una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="23459-119">Indicates the state of an active remote session interacting with a virtual machine.</span></span><br/>                             |
| [<span data-ttu-id="23459-120">**Videopartida MSVM \_**</span><span class="sxs-lookup"><span data-stu-id="23459-120">**Msvm\_VideoHead**</span></span>](msvm-videohead.md)<br/>                                   | <span data-ttu-id="23459-121">Describe la superficie de dibujo principal en un controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="23459-121">Describes the primary drawing surface on a display controller.</span></span><br/>                                                  |
| [<span data-ttu-id="23459-122">**MSVM \_ VideoHeadOnController**</span><span class="sxs-lookup"><span data-stu-id="23459-122">**Msvm\_VideoHeadOnController**</span></span>](msvm-videoheadoncontroller.md)<br/>           | <span data-ttu-id="23459-123">Asocia un cabezal de vídeo al controlador de vídeo que lo incluye.</span><span class="sxs-lookup"><span data-stu-id="23459-123">Associates a video head with the video controller that includes it.</span></span><br/>                                             |



 

 

 




