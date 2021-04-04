---
description: La \_ propiedad ControlPanelPageProvider de AudioEndpoint de PKEY \_ especifica el CLSID del proveedor registrado de la extensión de propiedades de dispositivo para el dispositivo de punto de conexión de audio.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907242"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a><span data-ttu-id="4ef8c-103">PKEY \_ AudioEndpoint \_ ControlPanelPageProvider</span><span class="sxs-lookup"><span data-stu-id="4ef8c-103">PKEY\_AudioEndpoint\_ControlPanelPageProvider</span></span>

<span data-ttu-id="4ef8c-104">La **propiedad \_ \_ ControlPanelPageProvider de AudioEndpoint de PKEY** especifica el CLSID del proveedor registrado de la extensión de propiedades de dispositivo para el dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="4ef8c-104">The **PKEY\_AudioEndpoint\_ControlPanelPageProvider** property specifies the CLSID of the registered provider of the device-properties extension for the audio endpoint device.</span></span> <span data-ttu-id="4ef8c-105">La extensión proporciona las propiedades del punto de conexión de audio que se muestran en la página Propiedades del dispositivo del panel de control multimedia de Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="4ef8c-105">The extension supplies the audio endpoint properties that are displayed in the device-properties page of the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="4ef8c-106">Para obtener más información acerca de Mmsys.cpl, consulte la documentación de DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="4ef8c-106">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="4ef8c-107">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="4ef8c-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="4ef8c-108">El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene un GUID que identifica el proveedor de la extensión del panel de control.</span><span class="sxs-lookup"><span data-stu-id="4ef8c-108">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the provider of the control-panel extension.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ef8c-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ef8c-109">Requirements</span></span>



| <span data-ttu-id="4ef8c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ef8c-110">Requirement</span></span> | <span data-ttu-id="4ef8c-111">Value</span><span class="sxs-lookup"><span data-stu-id="4ef8c-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef8c-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ef8c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4ef8c-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4ef8c-113">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4ef8c-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ef8c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4ef8c-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4ef8c-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4ef8c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ef8c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ef8c-117"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ef8c-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ef8c-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ef8c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ef8c-119">**Propiedades de punto de conexión de audio**</span><span class="sxs-lookup"><span data-stu-id="4ef8c-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="4ef8c-120">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="4ef8c-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




