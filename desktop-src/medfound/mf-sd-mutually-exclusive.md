---
description: Especifica si una secuencia es mutuamente excluyente con otras secuencias del mismo tipo.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: MF_SD_MUTUALLY_EXCLUSIVE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716493"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a><span data-ttu-id="50538-103">\_Atributo de \_ uso mutuamente \_ exclusivo de MF SD</span><span class="sxs-lookup"><span data-stu-id="50538-103">MF\_SD\_MUTUALLY\_EXCLUSIVE attribute</span></span>

<span data-ttu-id="50538-104">Especifica si una secuencia es mutuamente excluyente con otras secuencias del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="50538-104">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span>

## <a name="data-type"></a><span data-ttu-id="50538-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="50538-105">Data type</span></span>

<span data-ttu-id="50538-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="50538-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="50538-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="50538-107">Get/set</span></span>

<span data-ttu-id="50538-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="50538-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="50538-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="50538-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="50538-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="50538-110">Applies to</span></span>

[<span data-ttu-id="50538-111">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="50538-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="50538-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50538-112">Remarks</span></span>

<span data-ttu-id="50538-113">Si este atributo es **true** (distinto de cero), la secuencia es mutuamente excluyente con otras secuencias del mismo tipo, como audio o vídeo, dentro de la misma presentación.</span><span class="sxs-lookup"><span data-stu-id="50538-113">If this attribute is **TRUE** (nonzero), the stream is mutually exclusive with other streams of the same type, such as audio or video, within the same presentation.</span></span> <span data-ttu-id="50538-114">Por ejemplo, si un archivo AVI contiene varias secuencias de audio, se marcan como mutuamente excluyentes, porque solo debe reproducirse una secuencia de audio al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="50538-114">For example, if an AVI file contains multiple audio streams, they are marked as mutually exclusive, because only one audio stream should be played at one time.</span></span>

<span data-ttu-id="50538-115">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="50538-115">The default value is **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="50538-116">Este atributo no se utiliza para los archivos de formato de sistema avanzado (ASF), que tienen una forma más sofisticada de representar criterios de exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="50538-116">This attribute is not used for Advanced Systems Format (ASF) files, which have a more sophisticated way to represent mutual exclusion criteria.</span></span> <span data-ttu-id="50538-117">Para obtener más información, vea [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="50538-117">For more information, see [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span></span>

 

<span data-ttu-id="50538-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="50538-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="50538-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50538-119">Requirements</span></span>



| <span data-ttu-id="50538-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="50538-120">Requirement</span></span> | <span data-ttu-id="50538-121">Value</span><span class="sxs-lookup"><span data-stu-id="50538-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50538-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50538-122">Minimum supported client</span></span><br/> | <span data-ttu-id="50538-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="50538-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="50538-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50538-124">Minimum supported server</span></span><br/> | <span data-ttu-id="50538-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="50538-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="50538-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50538-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="50538-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="50538-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50538-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="50538-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50538-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="50538-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="50538-130">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="50538-130">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




