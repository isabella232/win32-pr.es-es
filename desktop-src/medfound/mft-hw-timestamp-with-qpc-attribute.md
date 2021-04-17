---
description: Especifica si un origen de dispositivo de hardware utiliza la hora del sistema para las marcas de tiempo.
ms.assetid: 54cdfa13-955a-4e92-b337-f645d526a1b8
title: MFT_HW_TIMESTAMP_WITH_QPC_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f6f7d50db89e99e76e7b7ea509f444c3998bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696884"
---
# <a name="mft_hw_timestamp_with_qpc_attribute-attribute"></a><span data-ttu-id="f79f1-103">\_ \_ Marca de tiempo \_ de HW de MFT con \_ \_ atributo de atributo QPC</span><span class="sxs-lookup"><span data-stu-id="f79f1-103">MFT\_HW\_TIMESTAMP\_WITH\_QPC\_Attribute attribute</span></span>

<span data-ttu-id="f79f1-104">Especifica si un origen de dispositivo de hardware utiliza la hora del sistema para las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f79f1-104">Specifies whether a hardware device source uses the system time for time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="f79f1-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f79f1-105">Data type</span></span>

<span data-ttu-id="f79f1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f79f1-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f79f1-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="f79f1-107">Get/set</span></span>

<span data-ttu-id="f79f1-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f79f1-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f79f1-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f79f1-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f79f1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f79f1-110">Remarks</span></span>

<span data-ttu-id="f79f1-111">Si este atributo es **true**, el origen del dispositivo utiliza la hora del sistema, tal como la devuelve **QueryPerformanceCounter**, para las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f79f1-111">If this attribute is **TRUE**, the device source uses the system time, as returned by the **QueryPerformanceCounter**, for time stamps.</span></span> <span data-ttu-id="f79f1-112">De lo contrario, el origen del dispositivo usa el reloj del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f79f1-112">Otherwise, the device source uses the device's clock.</span></span> <span data-ttu-id="f79f1-113">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f79f1-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="f79f1-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f79f1-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f79f1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f79f1-115">Requirements</span></span>



| <span data-ttu-id="f79f1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f79f1-116">Requirement</span></span> | <span data-ttu-id="f79f1-117">Value</span><span class="sxs-lookup"><span data-stu-id="f79f1-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f79f1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f79f1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f79f1-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="f79f1-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f79f1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f79f1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f79f1-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f79f1-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f79f1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f79f1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f79f1-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="f79f1-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f79f1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f79f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79f1-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f79f1-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f79f1-126">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f79f1-126">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




