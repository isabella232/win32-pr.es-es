---
description: Contiene el identificador de clase (CLSID) de una transformación de Media Foundation (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: MFT_TRANSFORM_CLSID_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001451"
---
# <a name="mft_transform_clsid_attribute-attribute"></a><span data-ttu-id="51e5e-103">\_Atributo de \_ atributo CLSID de transformación de MFT \_</span><span class="sxs-lookup"><span data-stu-id="51e5e-103">MFT\_TRANSFORM\_CLSID\_Attribute attribute</span></span>

<span data-ttu-id="51e5e-104">Contiene el identificador de clase (CLSID) de una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="51e5e-104">Contains the class identifier (CLSID) of a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="51e5e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="51e5e-105">Data type</span></span>

<span data-ttu-id="51e5e-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="51e5e-106">**GUID**</span></span>

## <a name="getset"></a><span data-ttu-id="51e5e-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="51e5e-107">Get/set</span></span>

<span data-ttu-id="51e5e-108">Para obtener este atributo, llame a [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="51e5e-108">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="51e5e-109">Para establecer este atributo, llame a [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="51e5e-109">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="51e5e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51e5e-110">Remarks</span></span>

<span data-ttu-id="51e5e-111">Este atributo se establece en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="51e5e-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="51e5e-112">Este atributo lo usa internamente el objeto de activación cuando crea la MFT.</span><span class="sxs-lookup"><span data-stu-id="51e5e-112">This attribute is used internally by the activation object when it creates the MFT.</span></span> <span data-ttu-id="51e5e-113">Las aplicaciones no deben usar este CLSID directamente para crear la MFT, ya que es posible que el objeto de activación tenga que inicializar la MFT.</span><span class="sxs-lookup"><span data-stu-id="51e5e-113">Applications should not use this CLSID directly to create the MFT, because the activation object might need to initialize the MFT.</span></span> <span data-ttu-id="51e5e-114">Por lo tanto, para crear una instancia de MFT, llame a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) en el objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="51e5e-114">Therefore, to create an instance of the MFT, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the activation object.</span></span>

<span data-ttu-id="51e5e-115">Tenga en cuenta que la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) se comporta de forma diferente a la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) en este sentido.</span><span class="sxs-lookup"><span data-stu-id="51e5e-115">Note that the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function behaves differently than the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function in this respect.</span></span> <span data-ttu-id="51e5e-116">La función **MFTEnum** devuelve CLSIDs, que la aplicación pasa a la función **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="51e5e-116">The **MFTEnum** function returns CLSIDs, which the application passes to the **CoCreateInstance** function.</span></span> <span data-ttu-id="51e5e-117">La función **MFTEnumEx** devuelve objetos de activación en lugar de CLSID.</span><span class="sxs-lookup"><span data-stu-id="51e5e-117">The **MFTEnumEx** function returns activation objects rather than CLSIDs.</span></span>

<span data-ttu-id="51e5e-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="51e5e-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e5e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51e5e-119">Requirements</span></span>



| <span data-ttu-id="51e5e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="51e5e-120">Requirement</span></span> | <span data-ttu-id="51e5e-121">Value</span><span class="sxs-lookup"><span data-stu-id="51e5e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e5e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51e5e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="51e5e-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="51e5e-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="51e5e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51e5e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="51e5e-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="51e5e-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="51e5e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51e5e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="51e5e-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="51e5e-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51e5e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="51e5e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e5e-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="51e5e-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="51e5e-130">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="51e5e-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




