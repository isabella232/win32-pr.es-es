---
description: Permite al motor multimedia reproducir contenido protegido.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb99d1df36c9b9adbf1c099d619df60e1144b87
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707542"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a><span data-ttu-id="c57e8-103">MF \_ \_ atributo del \_ Administrador de protección de contenido de media Engine \_ \_</span><span class="sxs-lookup"><span data-stu-id="c57e8-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="c57e8-104">Permite al motor multimedia reproducir contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="c57e8-104">Enables the Media Engine to play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="c57e8-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c57e8-105">Data type</span></span>

<span data-ttu-id="c57e8-106">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="c57e8-106">**IUnknown\***</span></span>

## <a name="remarks"></a><span data-ttu-id="c57e8-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c57e8-107">Remarks</span></span>

<span data-ttu-id="c57e8-108">El valor de este atributo es un puntero a la interfaz [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .</span><span class="sxs-lookup"><span data-stu-id="c57e8-108">The value of this attribute is a pointer to the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span> <span data-ttu-id="c57e8-109">El autor de la llamada debe implementar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="c57e8-109">The caller must implement the interface.</span></span>

<span data-ttu-id="c57e8-110">Este atributo puede ser uno de los atributos que se pasan a [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="c57e8-110">This attribute can be one of the attributes passed to [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="c57e8-111">Es necesario si se va a reproducir contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="c57e8-111">It is required if protected content is to be played.</span></span>

## <a name="requirements"></a><span data-ttu-id="c57e8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c57e8-112">Requirements</span></span>



| <span data-ttu-id="c57e8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c57e8-113">Requirement</span></span> | <span data-ttu-id="c57e8-114">Value</span><span class="sxs-lookup"><span data-stu-id="c57e8-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c57e8-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c57e8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c57e8-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="c57e8-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="c57e8-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c57e8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c57e8-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c57e8-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="c57e8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c57e8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c57e8-120"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="c57e8-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c57e8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c57e8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57e8-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c57e8-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c57e8-123">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="c57e8-123">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




