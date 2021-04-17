---
description: Especifica si el receptor de captura de muestra usa el reloj de presentación para programar ejemplos.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: MF_SAMPLEGRABBERSINK_IGNORE_CLOCK atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716346"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a><span data-ttu-id="5a53d-103">MF \_ SAMPLEGRABBERSINK \_ omitir \_ atributo de reloj</span><span class="sxs-lookup"><span data-stu-id="5a53d-103">MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute</span></span>

<span data-ttu-id="5a53d-104">Especifica si el receptor de captura de muestra usa el reloj de presentación para programar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="5a53d-104">Specifies whether the sample-grabber sink uses the presentation clock to schedule samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="5a53d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5a53d-105">Data type</span></span>

<span data-ttu-id="5a53d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5a53d-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5a53d-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="5a53d-107">Get/set</span></span>

<span data-ttu-id="5a53d-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5a53d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5a53d-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="5a53d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a53d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a53d-110">Remarks</span></span>

<span data-ttu-id="5a53d-111">Puede establecer este atributo en el objeto de activación creado por la función [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="5a53d-111">You can set this attribute on the activation object created by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="5a53d-112">Establezca el atributo antes de llamar al método [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) en el objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="5a53d-112">Set the attribute before calling the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method on the activation object.</span></span>

<span data-ttu-id="5a53d-113">De forma predeterminada, cuando el receptor del captador de muestra recibe un ejemplo, espera hasta que el tiempo de presentación del ejemplo invoque la devolución de llamada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5a53d-113">By default, when the sample-grabber sink receives a sample, it waits until the presentation time of the sample to invoke the application's callback.</span></span> <span data-ttu-id="5a53d-114">Si el \_ \_ atributo de reloj MF SAMPLEGRABBERSINK omitir \_ es distinto de cero, el receptor de captura de muestras omite el reloj de la presentación e invoca la devolución de llamada en cuanto recibe cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5a53d-114">If the MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute is nonzero, the sample-grabber sink ignores the presentation clock and invokes the callback as soon as it receives each sample.</span></span>

<span data-ttu-id="5a53d-115">Uso recomendado:</span><span class="sxs-lookup"><span data-stu-id="5a53d-115">Recommended usage:</span></span>

-   <span data-ttu-id="5a53d-116">Si desea procesar los ejemplos lo más rápido posible, establezca este atributo en **true**.</span><span class="sxs-lookup"><span data-stu-id="5a53d-116">If you want to process samples as quickly as possible, set this attribute to **TRUE**.</span></span>
-   <span data-ttu-id="5a53d-117">Si desea que las llamadas al método de devolución de llamada se sincronicen con el reloj, no establezca este atributo o establézcalo en **false**.</span><span class="sxs-lookup"><span data-stu-id="5a53d-117">If you want the calls to the callback method to be synchronized with the clock, either do not set this attribute or set it to **FALSE**.</span></span> <span data-ttu-id="5a53d-118">Puede obtener ejemplos ligeramente por encima del reloj, mientras sigue sincronizando, estableciendo el atributo de [**desplazamiento de \_ \_ \_ tiempo \_ de ejemplo MF SAMPLEGRABBERSINK**](mf-samplegrabbersink-sample-time-offset-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="5a53d-118">You can get samples slightly ahead of the clock, while still remaining synchronized, by setting the [**MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET**](mf-samplegrabbersink-sample-time-offset-attribute.md) attribute.</span></span>

<span data-ttu-id="5a53d-119">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5a53d-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a53d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a53d-120">Requirements</span></span>



| <span data-ttu-id="5a53d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a53d-121">Requirement</span></span> | <span data-ttu-id="5a53d-122">Value</span><span class="sxs-lookup"><span data-stu-id="5a53d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5a53d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a53d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5a53d-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a53d-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5a53d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a53d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5a53d-126">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a53d-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5a53d-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a53d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a53d-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a53d-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a53d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a53d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a53d-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a53d-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5a53d-131">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a53d-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




