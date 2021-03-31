---
description: Contiene un puntero IMFFieldOfUseMFTUnlock, que se puede usar para desbloquear una transformación de Media Foundation (MFT). La interfaz IMFFieldOfUseMFTUnlock se usa para desbloquear una MFT que tiene restricciones de campo de uso.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: MFT_FIELDOFUSE_UNLOCK_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812602"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="eb845-104">\_Atributo de \_ atributo Unlock FIELDOFUSE de MFT \_</span><span class="sxs-lookup"><span data-stu-id="eb845-104">MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="eb845-105">Contiene un puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que se puede usar para desbloquear una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="eb845-105">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which can be used to unlock a Media Foundation transform (MFT).</span></span> <span data-ttu-id="eb845-106">La interfaz **IMFFieldOfUseMFTUnlock** se usa para desbloquear una MFT que tiene restricciones de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="eb845-106">The **IMFFieldOfUseMFTUnlock** interface is used to unlock an MFT that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="eb845-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="eb845-107">Data type</span></span>

<span data-ttu-id="eb845-108">**[](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) IMFFieldOfUseMFTUnlock \** _ almacenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="eb845-108">**[**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="eb845-109">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="eb845-109">Get/set</span></span>

<span data-ttu-id="eb845-110">Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="eb845-110">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="eb845-111">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="eb845-111">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb845-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb845-112">Remarks</span></span>

<span data-ttu-id="eb845-113">Para obtener más información sobre este atributo, vea el [campo de restricciones de uso](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="eb845-113">For more information about this attribute, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

<span data-ttu-id="eb845-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="eb845-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb845-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb845-115">Requirements</span></span>



| <span data-ttu-id="eb845-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb845-116">Requirement</span></span> | <span data-ttu-id="eb845-117">Value</span><span class="sxs-lookup"><span data-stu-id="eb845-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb845-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb845-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eb845-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="eb845-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="eb845-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb845-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eb845-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="eb845-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="eb845-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb845-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb845-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb845-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb845-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb845-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb845-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eb845-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="eb845-126">Campo de restricciones de uso</span><span class="sxs-lookup"><span data-stu-id="eb845-126">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="eb845-127">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="eb845-127">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




