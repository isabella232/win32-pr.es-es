---
description: Especifica si el IMFTransform desea recibir notificaciones de finalización de MEPolicySet.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720486"
---
# <a name="mft_policy_set_aware-attribute"></a><span data-ttu-id="78089-103">\_ \_ Atributo consciente de conjunto de directivas de MFT \_</span><span class="sxs-lookup"><span data-stu-id="78089-103">MFT\_POLICY\_SET\_AWARE attribute</span></span>

<span data-ttu-id="78089-104">Si es distinto de cero, indica que **IMFTransform** desea recibir notificaciones de finalización de [MEPolicySet](./mepolicyset.md) .</span><span class="sxs-lookup"><span data-stu-id="78089-104">If non-zero, indicates that the **IMFTransform** wants to receive [MEPolicySet](./mepolicyset.md) completion notifications.</span></span>

## <a name="data-type"></a><span data-ttu-id="78089-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="78089-105">Data type</span></span>

<span data-ttu-id="78089-106">**UINT32** (se trata como **bool**)</span><span class="sxs-lookup"><span data-stu-id="78089-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="78089-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="78089-107">Get/set</span></span>

<span data-ttu-id="78089-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="78089-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="78089-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="78089-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="78089-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="78089-110">Applies to</span></span>

[<span data-ttu-id="78089-111">**IMFInputTrustAuthority**</span><span class="sxs-lookup"><span data-stu-id="78089-111">**IMFInputTrustAuthority**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a><span data-ttu-id="78089-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78089-112">Remarks</span></span>

<span data-ttu-id="78089-113">Este atributo puede ser utilizado por un Decrypter **IMFInputTrustAuthority** .</span><span class="sxs-lookup"><span data-stu-id="78089-113">This attributet can be used by an **IMFInputTrustAuthority** decrypter.</span></span> <span data-ttu-id="78089-114">Una implementación de un módulo de descifrado de contenido (CDM) puede incluir una implementación de **IMFInputTrustAuthority**.</span><span class="sxs-lookup"><span data-stu-id="78089-114">An implementation of a Content Decryption Module (CDM) may include an implementation of **IMFInputTrustAuthority**.</span></span> <span data-ttu-id="78089-115">Se tiene acceso al objeto **IMFInputTrustAuthority** a través de [IMFContentDecryptionModule:: CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span><span class="sxs-lookup"><span data-stu-id="78089-115">The **IMFInputTrustAuthority** object is accessed through [IMFContentDecryptionModule::CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span></span>


<span data-ttu-id="78089-116">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="78089-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="78089-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78089-117">Requirements</span></span>



| <span data-ttu-id="78089-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="78089-118">Requirement</span></span> | <span data-ttu-id="78089-119">Value</span><span class="sxs-lookup"><span data-stu-id="78089-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="78089-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78089-120">Minimum supported client</span></span><br/> | <span data-ttu-id="78089-121">Actualización 2020 de abril de Windows 10</span><span class="sxs-lookup"><span data-stu-id="78089-121">Windows 10 April 2020 Update</span></span>   <br/>                                        |
| <span data-ttu-id="78089-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78089-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="78089-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="78089-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78089-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="78089-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78089-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="78089-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="78089-126">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="78089-126">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
