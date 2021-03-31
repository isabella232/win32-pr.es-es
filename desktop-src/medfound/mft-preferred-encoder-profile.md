---
description: Contiene las propiedades de configuración de un codificador.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: MFT_PREFERRED_ENCODER_PROFILE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfdc85ead0fe813215b3edaea14833400df5445d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001452"
---
# <a name="mft_preferred_encoder_profile-attribute"></a><span data-ttu-id="81797-103">\_Atributo de \_ Perfil de codificador preferido de MFT \_</span><span class="sxs-lookup"><span data-stu-id="81797-103">MFT\_PREFERRED\_ENCODER\_PROFILE attribute</span></span>

<span data-ttu-id="81797-104">Contiene las propiedades de configuración de un codificador.</span><span class="sxs-lookup"><span data-stu-id="81797-104">Contains configuration properties for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="81797-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="81797-105">Data type</span></span>

<span data-ttu-id="81797-106">**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ almacenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="81797-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="81797-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="81797-107">Get/set</span></span>

<span data-ttu-id="81797-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="81797-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="81797-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="81797-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="81797-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="81797-110">Applies to</span></span>

[<span data-ttu-id="81797-111">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="81797-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="81797-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81797-112">Remarks</span></span>

<span data-ttu-id="81797-113">Este atributo se puede establecer en el objeto de activación devuelto por la función [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) .</span><span class="sxs-lookup"><span data-stu-id="81797-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="81797-114">El atributo solo se aplica cuando el objeto de activación está configurado para crear un codificador.</span><span class="sxs-lookup"><span data-stu-id="81797-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="81797-115">El valor del atributo es un puntero a un almacén de atributos, que a su vez contiene las propiedades que se van a establecer en el codificador.</span><span class="sxs-lookup"><span data-stu-id="81797-115">The value of the attribute is a pointer to an attribute store, which itself contains properties to set on the encoder.</span></span>

<span data-ttu-id="81797-116">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="81797-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="81797-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81797-117">Requirements</span></span>



| <span data-ttu-id="81797-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="81797-118">Requirement</span></span> | <span data-ttu-id="81797-119">Value</span><span class="sxs-lookup"><span data-stu-id="81797-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="81797-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81797-120">Minimum supported client</span></span><br/> | <span data-ttu-id="81797-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="81797-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="81797-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81797-122">Minimum supported server</span></span><br/> | <span data-ttu-id="81797-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="81797-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="81797-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81797-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="81797-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="81797-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81797-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="81797-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81797-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="81797-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="81797-128">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="81797-128">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="81797-129">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="81797-129">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




