---
description: La propiedad PKEY de \_ Audioengine \_ DeviceFormat especifica el formato del dispositivo, que es el formato que el usuario ha seleccionado para la secuencia que fluye entre el motor de audio y el dispositivo de punto de conexión de audio cuando el dispositivo funciona en modo compartido.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807826"
---
# <a name="pkey_audioengine_deviceformat"></a><span data-ttu-id="d6407-103">PKEY \_ Audioengine \_ DeviceFormat</span><span class="sxs-lookup"><span data-stu-id="d6407-103">PKEY\_AudioEngine\_DeviceFormat</span></span>

<span data-ttu-id="d6407-104">La propiedad **PKEY de \_ Audioengine \_ DeviceFormat** especifica el formato del dispositivo, que es el formato que el usuario ha seleccionado para la secuencia que fluye entre el motor de audio y el dispositivo de punto de conexión de audio cuando el dispositivo funciona en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="d6407-104">The **PKEY\_AudioEngine\_DeviceFormat** property specifies the device format, which is the format that the user has selected for the stream that flows between the audio engine and the audio endpoint device when the device operates in shared mode.</span></span> <span data-ttu-id="d6407-105">Es posible que este formato no sea el mejor formato predeterminado para que lo use una aplicación en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d6407-105">This format might not be the best default format for an exclusive-mode application to use.</span></span> <span data-ttu-id="d6407-106">Normalmente, una aplicación de modo exclusivo busca un formato de dispositivo adecuado realizando un número de llamadas al método [**IAudioClient:: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="d6407-106">Typically, an exclusive-mode application finds a suitable device format by making some number of calls to the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method.</span></span> <span data-ttu-id="d6407-107">Para obtener más información, vea [formatos de dispositivo](device-formats.md).</span><span class="sxs-lookup"><span data-stu-id="d6407-107">For more information, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="d6407-108">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ BLOB.</span><span class="sxs-lookup"><span data-stu-id="d6407-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="d6407-109">El miembro **BLOB** de la estructura **PROPVARIANT** es una estructura de tipo **BLOB** que contiene dos miembros.</span><span class="sxs-lookup"><span data-stu-id="d6407-109">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="d6407-110">Member **BLOB. cbSize** es un **valor DWORD** que especifica el número de bytes en la descripción de formato.</span><span class="sxs-lookup"><span data-stu-id="d6407-110">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="d6407-111">Member **BLOB. pBlobData** apunta a una estructura **WAVEFORMATEX** que contiene la descripción del formato.</span><span class="sxs-lookup"><span data-stu-id="d6407-111">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="d6407-112">Para obtener más información sobre **BLOB**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d6407-112">For more information about **BLOB**, see the Windows SDK documentation.</span></span> <span data-ttu-id="d6407-113">Para obtener más información acerca de **WAVEFORMATEX**, consulte la documentación de DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="d6407-113">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6407-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6407-114">Requirements</span></span>



| <span data-ttu-id="d6407-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6407-115">Requirement</span></span> | <span data-ttu-id="d6407-116">Value</span><span class="sxs-lookup"><span data-stu-id="d6407-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6407-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6407-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d6407-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d6407-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d6407-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6407-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d6407-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6407-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d6407-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6407-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6407-122"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6407-122"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6407-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6407-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6407-124">**Propiedades de punto de conexión de audio**</span><span class="sxs-lookup"><span data-stu-id="d6407-124">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="d6407-125">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="d6407-125">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




