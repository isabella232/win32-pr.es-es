---
description: La \_ \_ propiedad JackSubType de AUDIOENDPOINT de PKEY contiene un GUID de categoría de salida para un dispositivo de punto de conexión de audio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153406"
---
# <a name="pkey_audioendpoint_jacksubtype"></a><span data-ttu-id="20ab0-103">PKEY \_ AudioEndpoint \_ JackSubType</span><span class="sxs-lookup"><span data-stu-id="20ab0-103">PKEY\_AudioEndpoint\_JackSubType</span></span>

<span data-ttu-id="20ab0-104">La **propiedad \_ \_ JackSubType de AudioEndpoint de PKEY** contiene un GUID de categoría de salida para un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="20ab0-104">The **PKEY\_AudioEndpoint\_JackSubType** property contains an output category GUID for an audio endpoint device.</span></span> <span data-ttu-id="20ab0-105">El archivo de encabezado Ksmedia. h define los GUID; cada GUID especifica el tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="20ab0-105">The header file Ksmedia.h defines the GUIDs; each GUID specifies the type of connection.</span></span> <span data-ttu-id="20ab0-106">Estos GUID también tienen categorías de PIN asociadas.</span><span class="sxs-lookup"><span data-stu-id="20ab0-106">These GUIDs also have associated pin categories.</span></span> <span data-ttu-id="20ab0-107">Por ejemplo, el archivo de encabezado Ksmedia. h define **la \_ \_ interfaz GUID KSNODETYPE DisplayPort** para un puerto de pantalla que se conecta con el PIN de KS definido por el GUID **PINNAME \_ DisplayPort \_ out**.</span><span class="sxs-lookup"><span data-stu-id="20ab0-107">For example, header file Ksmedia.h defines the GUID **KSNODETYPE\_DISPLAYPORT\_INTERFACE** for a display port that connects with the KS pin defined by the GUID **PINNAME\_DISPLAYPORT\_OUT**.</span></span>

<span data-ttu-id="20ab0-108">Para obtener más información, consulte la descripción de las propiedades de la categoría PIN en la documentación de Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="20ab0-108">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="20ab0-109">El miembro **VT** de la estructura **PROPVARIANT** se establece en **VT \_ LPWStr**.</span><span class="sxs-lookup"><span data-stu-id="20ab0-109">The **vt** member of the **PROPVARIANT** structure is set to **VT\_LPWSTR**.</span></span>

<span data-ttu-id="20ab0-110">El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene un GUID de categoría.</span><span class="sxs-lookup"><span data-stu-id="20ab0-110">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="20ab0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20ab0-111">Requirements</span></span>



| <span data-ttu-id="20ab0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="20ab0-112">Requirement</span></span> | <span data-ttu-id="20ab0-113">Value</span><span class="sxs-lookup"><span data-stu-id="20ab0-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ab0-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20ab0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="20ab0-115">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="20ab0-115">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="20ab0-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20ab0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="20ab0-117">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="20ab0-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20ab0-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20ab0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="20ab0-119"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="20ab0-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20ab0-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="20ab0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ab0-121">**Propiedades de punto de conexión de audio**</span><span class="sxs-lookup"><span data-stu-id="20ab0-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="20ab0-122">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="20ab0-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




