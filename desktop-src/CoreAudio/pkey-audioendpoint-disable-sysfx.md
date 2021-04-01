---
description: La \_ propiedad PKEY AudioEndpoint \_ Disable \_ SysFx especifica si los efectos del sistema están habilitados en la secuencia de modo compartido que fluye hacia o desde el dispositivo de punto de conexión de audio.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153342"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a><span data-ttu-id="39d03-103">PKEY \_ AudioEndpoint \_ deshabilitar \_ SysFx</span><span class="sxs-lookup"><span data-stu-id="39d03-103">PKEY\_AudioEndpoint\_Disable\_SysFx</span></span>

<span data-ttu-id="39d03-104">La propiedad **PKEY \_ AudioEndpoint \_ Disable \_ SysFx** especifica si los efectos del sistema están habilitados en la secuencia de modo compartido que fluye hacia o desde el dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="39d03-104">The **PKEY\_AudioEndpoint\_Disable\_SysFx** property specifies whether system effects are enabled in the shared-mode stream that flows to or from the audio endpoint device.</span></span>

<span data-ttu-id="39d03-105">Los efectos del sistema se implementan como objetos de procesamiento de audio (APOs) que se pueden insertar en una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="39d03-105">System effects are implemented as audio processing objects (APOs) that can be inserted into an audio stream.</span></span> <span data-ttu-id="39d03-106">APOs son módulos de software que realizan funciones de procesamiento de audio como el control de volumen y la conversión de formato.</span><span class="sxs-lookup"><span data-stu-id="39d03-106">APOs are software modules that perform audio processing functions such as volume control and format conversion.</span></span> <span data-ttu-id="39d03-107">Deshabilitar los efectos del sistema para un dispositivo de extremo permite que el flujo asociado pase a través de APOs sin modificar.</span><span class="sxs-lookup"><span data-stu-id="39d03-107">Disabling the system effects for an endpoint device enables the associated stream to pass through the APOs unmodified.</span></span>

<span data-ttu-id="39d03-108">Para obtener más información acerca de los efectos del sistema en Windows Vista, consulte las notas del producto titulada "efectos de audio personalizados en Windows Vista" y "reutilización de los efectos del sistema de audio de Windows Vista" en el sitio Web [de tecnologías de dispositivos de audio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="39d03-108">For more information about system effects in Windows Vista, see the white papers titled "Custom Audio Effects in Windows Vista" and "Reusing Windows Vista Audio System Effects" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="39d03-109">Esta propiedad sólo se aplica a los efectos locales y a los efectos globales APOs que instalaron el archivo. inf que instaló el adaptador de audio al que está conectado el dispositivo de extremo.</span><span class="sxs-lookup"><span data-stu-id="39d03-109">This property applies only to the local-effects and global-effects APOs that were installed by the .inf file that installed the audio adapter to which the endpoint device is connected.</span></span> <span data-ttu-id="39d03-110">Además, esta propiedad solo afecta al dispositivo de extremo de destino: no tiene ningún efecto en los efectos del sistema para otros dispositivos de extremo, aunque se conecten al mismo adaptador.</span><span class="sxs-lookup"><span data-stu-id="39d03-110">In addition, this property affects only the target endpoint device—it has no effect on the system effects for any other endpoint devices, even if they connect to the same adapter.</span></span>

<span data-ttu-id="39d03-111">El miembro **VT** de la estructura **PROPVARIANT** se establece en **VT \_ UI4**.</span><span class="sxs-lookup"><span data-stu-id="39d03-111">The **vt** member of the **PROPVARIANT** structure is set to **VT\_UI4**.</span></span>

<span data-ttu-id="39d03-112">El miembro **ulVal** de la estructura **PROPVARIANT** se establece en el **extremo \_ SYSFX \_ habilitado** si se habilitan los efectos del sistema o en el **extremo \_ SYSFX \_ deshabilitado** si están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="39d03-112">The **ulVal** member of the **PROPVARIANT** structure is set to **ENDPOINT\_SYSFX\_ENABLED** if system effects are enabled or to **ENDPOINT\_SYSFX\_DISABLED** if they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="39d03-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39d03-113">Requirements</span></span>



| <span data-ttu-id="39d03-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="39d03-114">Requirement</span></span> | <span data-ttu-id="39d03-115">Value</span><span class="sxs-lookup"><span data-stu-id="39d03-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="39d03-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39d03-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39d03-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="39d03-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="39d03-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39d03-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39d03-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="39d03-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="39d03-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39d03-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39d03-121"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39d03-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39d03-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="39d03-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d03-123">**Propiedades de punto de conexión de audio**</span><span class="sxs-lookup"><span data-stu-id="39d03-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="39d03-124">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="39d03-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




