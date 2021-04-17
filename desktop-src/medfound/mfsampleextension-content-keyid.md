---
description: Establece el identificador de clave para el ejemplo.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: MFSampleExtension_Content_KeyID atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666873"
---
# <a name="mfsampleextension_content_keyid-attribute"></a><span data-ttu-id="788a9-103">Atributo de ID. de contenido de MFSampleExtension \_ \_</span><span class="sxs-lookup"><span data-stu-id="788a9-103">MFSampleExtension\_Content\_KeyID attribute</span></span>

<span data-ttu-id="788a9-104">Establece el identificador de clave para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="788a9-104">Sets the Key ID for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="788a9-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="788a9-105">Data type</span></span>

<span data-ttu-id="788a9-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="788a9-106">**GUID**</span></span>

## <a name="examples"></a><span data-ttu-id="788a9-107">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="788a9-107">Examples</span></span>

<span data-ttu-id="788a9-108">En el ejemplo siguiente se muestra cómo establecer el identificador de clave para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="788a9-108">The following example shows how to set the Key ID for the sample.</span></span>


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a><span data-ttu-id="788a9-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="788a9-109">Requirements</span></span>



| <span data-ttu-id="788a9-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="788a9-110">Requirement</span></span> | <span data-ttu-id="788a9-111">Value</span><span class="sxs-lookup"><span data-stu-id="788a9-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="788a9-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="788a9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="788a9-113">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="788a9-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="788a9-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="788a9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="788a9-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="788a9-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="788a9-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="788a9-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="788a9-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="788a9-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="788a9-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="788a9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="788a9-119">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="788a9-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="788a9-120">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="788a9-120">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="788a9-121">MFSampleExtension \_ cifrado \_ SubSampleMappingSplit</span><span class="sxs-lookup"><span data-stu-id="788a9-121">MFSampleExtension\_Encryption\_SubSampleMappingSplit</span></span>](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




