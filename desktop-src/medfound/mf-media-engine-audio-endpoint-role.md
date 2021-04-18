---
description: Especifica el rol de dispositivo para la secuencia de audio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE atributo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b1b00115a28592140e41463cf296acf54ad7cde
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707544"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a><span data-ttu-id="c9414-103">\_Atributo de \_ rol de \_ punto de conexión de audio del motor \_ multimedia \_ MF</span><span class="sxs-lookup"><span data-stu-id="c9414-103">MF\_MEDIA\_ENGINE\_AUDIO\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="c9414-104">Especifica el rol de dispositivo para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="c9414-104">Specifies the device role for the audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="c9414-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c9414-105">Data type</span></span>

<span data-ttu-id="c9414-106">**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c9414-106">**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c9414-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9414-107">Remarks</span></span>

<span data-ttu-id="c9414-108">El valor de este atributo es un miembro de la enumeración [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .</span><span class="sxs-lookup"><span data-stu-id="c9414-108">The value of this attribute is a member of the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>

<span data-ttu-id="c9414-109">Este atributo se usa con el método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="c9414-109">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="c9414-110">El atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="c9414-110">The attribute is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9414-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9414-111">Requirements</span></span>



| <span data-ttu-id="c9414-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9414-112">Requirement</span></span> | <span data-ttu-id="c9414-113">Value</span><span class="sxs-lookup"><span data-stu-id="c9414-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9414-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9414-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c9414-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="c9414-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="c9414-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9414-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c9414-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c9414-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c9414-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9414-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9414-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9414-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9414-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9414-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9414-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9414-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
