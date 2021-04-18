---
description: Un valor que indica si un fotograma se capturó con la iluminación de infrarrojos (IR) activa.
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: MF_CAPTURE_METADATA_FRAME_ILLUMINATION atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696603"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a><span data-ttu-id="d227b-103">\_Atributo de \_ \_ iluminación de fotogramas de metadatos de captura MF \_</span><span class="sxs-lookup"><span data-stu-id="d227b-103">MF\_CAPTURE\_METADATA\_FRAME\_ILLUMINATION attribute</span></span>

<span data-ttu-id="d227b-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="d227b-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d227b-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="d227b-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d227b-106">Un valor que indica si un fotograma se capturó con la iluminación de infrarrojos (IR) activa.</span><span class="sxs-lookup"><span data-stu-id="d227b-106">A value indicating whether a frame was captured using active infrared (IR) illumination.</span></span>

## <a name="data-type"></a><span data-ttu-id="d227b-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d227b-107">Data type</span></span>

<span data-ttu-id="d227b-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="d227b-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="d227b-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d227b-109">Remarks</span></span>

<span data-ttu-id="d227b-110">Este atributo es una máscara de máscara.</span><span class="sxs-lookup"><span data-stu-id="d227b-110">This attribute is a bitmask.</span></span> <span data-ttu-id="d227b-111">Es un valor de 64 bits para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="d227b-111">It is a 64 bit value for backward compatibility.</span></span>

<span data-ttu-id="d227b-112">La iluminación activa es cuando un dispositivo tiene un emisor de luz cerca de la cámara de INFRARROJOs que emite un rayo de luz para iluminar la escena, lo que normalmente emite luz de INFRARROJOs, por lo que no afectará a los ojos humanos.</span><span class="sxs-lookup"><span data-stu-id="d227b-112">Active illumination is when a device has a light emitter close to the IR camera emitting a beam of light to illuminate the scene, typically emitting IR light so it won’t disturb human eyes.</span></span> <span data-ttu-id="d227b-113">Establezca valor en (valor & 0x1)! = 0 si el fotograma se capturó cuando la iluminación activa estaba activada y establecida (valor & 0x1) = = 0 si la iluminación activa estaba desactivada.</span><span class="sxs-lookup"><span data-stu-id="d227b-113">Set value to (value & 0x1) != 0 if frame was captured when active illumination was on and set (value & 0x1) == 0 if active illumination was off.</span></span>

## <a name="requirements"></a><span data-ttu-id="d227b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d227b-114">Requirements</span></span>



| <span data-ttu-id="d227b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d227b-115">Requirement</span></span> | <span data-ttu-id="d227b-116">Value</span><span class="sxs-lookup"><span data-stu-id="d227b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d227b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d227b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d227b-118">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="d227b-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d227b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d227b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d227b-120">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="d227b-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="d227b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d227b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d227b-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d227b-122"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




