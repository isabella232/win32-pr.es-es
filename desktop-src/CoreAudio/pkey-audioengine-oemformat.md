---
description: La propiedad PKEY de \_ Audioengine de \_ OEMFormat especifica el formato predeterminado del dispositivo que se usa para representar o capturar un flujo. El OEM rellena los valores en un archivo. inf.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153401"
---
# <a name="pkey_audioengine_oemformat"></a><span data-ttu-id="c42a6-104">PKEY \_ Audioengine \_ OEMFormat</span><span class="sxs-lookup"><span data-stu-id="c42a6-104">PKEY\_AudioEngine\_OEMFormat</span></span>

<span data-ttu-id="c42a6-105">La propiedad PKEY de \_ Audioengine de \_ OEMFormat especifica el formato predeterminado del dispositivo que se usa para representar o capturar un flujo.</span><span class="sxs-lookup"><span data-stu-id="c42a6-105">The PKEY\_AudioEngine\_OEMFormat property specifies the default format of the device that is used for rendering or capturing a stream.</span></span> <span data-ttu-id="c42a6-106">El OEM rellena los valores en un archivo. inf.</span><span class="sxs-lookup"><span data-stu-id="c42a6-106">The values are populated by the OEM in an .inf file.</span></span>

<span data-ttu-id="c42a6-107">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ BLOB.</span><span class="sxs-lookup"><span data-stu-id="c42a6-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="c42a6-108">El miembro **BLOB** de la estructura **PROPVARIANT** es una estructura de tipo **BLOB** que contiene dos miembros.</span><span class="sxs-lookup"><span data-stu-id="c42a6-108">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="c42a6-109">Member **BLOB. cbSize** es un **valor DWORD** que especifica el número de bytes en la descripción de formato.</span><span class="sxs-lookup"><span data-stu-id="c42a6-109">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="c42a6-110">Member **BLOB. pBlobData** apunta a una estructura **WAVEFORMATEX** que contiene la descripción del formato.</span><span class="sxs-lookup"><span data-stu-id="c42a6-110">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="c42a6-111">Para obtener más información sobre BLOB, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c42a6-111">For more information about BLOB, see the Windows SDK documentation.</span></span> <span data-ttu-id="c42a6-112">Para obtener más información acerca de **WAVEFORMATEX**, consulte la documentación de DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="c42a6-112">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c42a6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c42a6-113">Requirements</span></span>



| <span data-ttu-id="c42a6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c42a6-114">Requirement</span></span> | <span data-ttu-id="c42a6-115">Value</span><span class="sxs-lookup"><span data-stu-id="c42a6-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c42a6-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c42a6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c42a6-117">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c42a6-117">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c42a6-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c42a6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c42a6-119">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c42a6-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c42a6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c42a6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c42a6-121"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c42a6-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c42a6-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c42a6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c42a6-123">**Propiedades de punto de conexión de audio**</span><span class="sxs-lookup"><span data-stu-id="c42a6-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="c42a6-124">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="c42a6-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




