---
description: La \_ propiedad PKEY \_ AudioEndpoint \_ admite \_ el modo EventDriven indica si el punto de conexión admite el modo basado en eventos.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000750"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a><span data-ttu-id="39877-103">PKEY \_ AudioEndpoint \_ admite \_ el \_ modo EventDriven</span><span class="sxs-lookup"><span data-stu-id="39877-103">PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode</span></span>

<span data-ttu-id="39877-104">La propiedad **PKEY \_ AudioEndpoint admite el \_ \_ \_ modo EventDriven** indica si el punto de conexión admite el modo basado en eventos.</span><span class="sxs-lookup"><span data-stu-id="39877-104">The **PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode** property indicates whether the endpoint supports the event-driven mode.</span></span>

<span data-ttu-id="39877-105">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="39877-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="39877-106">El miembro **uintVal** de la estructura **PROPVARIANT** es un **valor DWORD** que indica si el punto de conexión admite el modo basado en eventos.</span><span class="sxs-lookup"><span data-stu-id="39877-106">The **uintVal** member of the **PROPVARIANT** structure is a **DWORD** that indicates if the endpoint supports the event-driven mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="39877-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39877-107">Remarks</span></span>

<span data-ttu-id="39877-108">El valor de esta propiedad se rellena con un OEM de audio en un archivo. inf para indicar que el hardware HDAudio admite el modo basado en eventos según el requisito de WHQL.</span><span class="sxs-lookup"><span data-stu-id="39877-108">This property value is populated by an audio OEM in an .inf file to indicate that the HDAudio hardware supports event driven mode as per the WHQL requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="39877-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39877-109">Requirements</span></span>



| <span data-ttu-id="39877-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="39877-110">Requirement</span></span> | <span data-ttu-id="39877-111">Value</span><span class="sxs-lookup"><span data-stu-id="39877-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="39877-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39877-112">Minimum supported client</span></span><br/> | <span data-ttu-id="39877-113">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="39877-113">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="39877-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39877-114">Minimum supported server</span></span><br/> | <span data-ttu-id="39877-115">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="39877-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39877-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39877-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="39877-117"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39877-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39877-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="39877-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39877-119">**Propiedades de punto de conexión de audio**</span><span class="sxs-lookup"><span data-stu-id="39877-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="39877-120">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="39877-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




