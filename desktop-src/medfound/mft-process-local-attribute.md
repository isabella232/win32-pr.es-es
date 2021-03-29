---
description: Especifica si una transformación de Media Foundation (MFT) solo se registra en el proceso de aplicaciones.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: MFT_PROCESS_LOCAL_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811606"
---
# <a name="mft_process_local_attribute-attribute"></a><span data-ttu-id="202fe-103">\_Atributo de \_ atributo local de proceso de MFT \_</span><span class="sxs-lookup"><span data-stu-id="202fe-103">MFT\_PROCESS\_LOCAL\_Attribute attribute</span></span>

<span data-ttu-id="202fe-104">Especifica si una transformación de Media Foundation (MFT) solo se registra en el proceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="202fe-104">Specifies whether a Media Foundation transform (MFT) is registered only in the application's process.</span></span>

## <a name="data-type"></a><span data-ttu-id="202fe-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="202fe-105">Data type</span></span>

<span data-ttu-id="202fe-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="202fe-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="202fe-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="202fe-107">Get/set</span></span>

<span data-ttu-id="202fe-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="202fe-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="202fe-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="202fe-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="202fe-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="202fe-110">Remarks</span></span>

<span data-ttu-id="202fe-111">Este atributo se usa como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="202fe-111">This attribute is used as follows:</span></span>

1.  <span data-ttu-id="202fe-112">La aplicación registra un MFT local llamando a la función [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) .</span><span class="sxs-lookup"><span data-stu-id="202fe-112">The application registers a local MFT by calling either the [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) function.</span></span> <span data-ttu-id="202fe-113">Estas funciones registran la MFT en el proceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="202fe-113">These functions register the MFT in the application's process.</span></span>
2.  <span data-ttu-id="202fe-114">Se llama a la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para enumerar MFTs que coinciden con un determinado conjunto de criterios.</span><span class="sxs-lookup"><span data-stu-id="202fe-114">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function is called to enumerate MFTs that match a particular set of criteria.</span></span> <span data-ttu-id="202fe-115">La aplicación podría llamar directamente a la función **MFTEnumEx** , pero el cargador de topología llama a esta función con mayor frecuencia.</span><span class="sxs-lookup"><span data-stu-id="202fe-115">The application might call the **MFTEnumEx** function directly, but more often this function is called by the topology loader.</span></span>
3.  <span data-ttu-id="202fe-116">La función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) recupera una matriz de punteros de [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , cada uno de los cuales representa un objeto de activación para una MFT.</span><span class="sxs-lookup"><span data-stu-id="202fe-116">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function retrieves an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each representing an activation object for an MFT.</span></span> <span data-ttu-id="202fe-117">Si una MFT se registra localmente, el \_ atributo de \_ atributo local del proceso MFT \_ se establece en **true** en el objeto de activación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="202fe-117">If an MFT is registered locally, the MFT\_PROCESS\_LOCAL\_Attribute attribute is set to **TRUE** on the corresponding activation object.</span></span>

<span data-ttu-id="202fe-118">El valor predeterminado de este atributo es **false**.</span><span class="sxs-lookup"><span data-stu-id="202fe-118">The default value for this attribute is **FALSE**.</span></span>

<span data-ttu-id="202fe-119">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="202fe-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="202fe-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="202fe-120">Requirements</span></span>



| <span data-ttu-id="202fe-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="202fe-121">Requirement</span></span> | <span data-ttu-id="202fe-122">Value</span><span class="sxs-lookup"><span data-stu-id="202fe-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="202fe-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="202fe-123">Minimum supported client</span></span><br/> | <span data-ttu-id="202fe-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="202fe-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="202fe-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="202fe-125">Minimum supported server</span></span><br/> | <span data-ttu-id="202fe-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="202fe-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="202fe-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="202fe-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="202fe-128"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="202fe-128"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="202fe-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="202fe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="202fe-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="202fe-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="202fe-131">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="202fe-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




