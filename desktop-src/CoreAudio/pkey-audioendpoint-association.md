---
description: La \_ propiedad de asociación PKEY AudioEndpoint \_ asocia una categoría de PIN de streaming de kernel (KS) con un dispositivo de punto de conexión de audio.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659735"
---
# <a name="pkey_audioendpoint_association"></a><span data-ttu-id="e016b-103">Asociación de PKEY \_ AudioEndpoint \_</span><span class="sxs-lookup"><span data-stu-id="e016b-103">PKEY\_AudioEndpoint\_Association</span></span>

<span data-ttu-id="e016b-104">La propiedad de **\_ \_ Asociación PKEY AudioEndpoint** asocia una categoría de PIN de streaming de kernel (KS) con un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="e016b-104">The **PKEY\_AudioEndpoint\_Association** property associates a kernel-streaming (KS) pin category with an audio endpoint device.</span></span> <span data-ttu-id="e016b-105">El archivo. inf que instala un adaptador de audio asigna una categoría de PIN a cada pin de KS en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="e016b-105">The .inf file that installs an audio adapter assigns a pin category to each KS pin in the adapter.</span></span> <span data-ttu-id="e016b-106">Un PIN de KS en un dispositivo adaptador representa el punto en el que una secuencia de audio entra o sale del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e016b-106">A KS pin on an adapter device represents the point at which an audio stream enters or leaves the device.</span></span> <span data-ttu-id="e016b-107">Una categoría de PIN es un GUID que especifica el tipo de función que realiza un PIN de KS.</span><span class="sxs-lookup"><span data-stu-id="e016b-107">A pin category is a GUID that specifies the type of function performed by a KS pin.</span></span> <span data-ttu-id="e016b-108">Por ejemplo, el archivo de encabezado Ksmedia. h define el KSNODETYPE de GUID de categoría de PIN \_ para indicar un PIN de KS que se conecta a un micrófono y KSNODETYPE \_ auriculares para indicar un PIN de KS que se conecta a los auriculares.</span><span class="sxs-lookup"><span data-stu-id="e016b-108">For example, header file Ksmedia.h defines pin-category GUID KSNODETYPE\_MICROPHONE to indicate a KS pin that connects to a microphone, and KSNODETYPE\_HEADPHONES to indicate a KS pin that connects to headphones.</span></span> <span data-ttu-id="e016b-109">Para obtener más información, consulte la descripción de las propiedades de la categoría PIN en la documentación de Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="e016b-109">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="e016b-110">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="e016b-110">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="e016b-111">El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene un GUID de categoría PIN de KS.</span><span class="sxs-lookup"><span data-stu-id="e016b-111">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a KS pin category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="e016b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e016b-112">Requirements</span></span>



| <span data-ttu-id="e016b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e016b-113">Requirement</span></span> | <span data-ttu-id="e016b-114">Value</span><span class="sxs-lookup"><span data-stu-id="e016b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e016b-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e016b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e016b-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e016b-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e016b-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e016b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e016b-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e016b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e016b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e016b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e016b-120"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e016b-120"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e016b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e016b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e016b-122">**Propiedades de punto de conexión de audio**</span><span class="sxs-lookup"><span data-stu-id="e016b-122">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="e016b-123">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="e016b-123">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




