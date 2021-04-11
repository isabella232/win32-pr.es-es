---
description: Especifica el identificador de clave para un archivo de formato de sistema avanzado (ASF) cifrado. Este atributo corresponde al campo de identificador de clave del encabezado de cifrado de contenido, definido en la especificación ASF.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: MF_PD_ASF_CONTENTENCRYPTION_KEYID atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd49c7a006345cceba01edde7caf76e499323b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154189"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a><span data-ttu-id="2ed65-104">MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ atributo de ID. de la ID.</span><span class="sxs-lookup"><span data-stu-id="2ed65-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_KEYID attribute</span></span>

<span data-ttu-id="2ed65-105">Especifica el identificador de clave para un archivo de formato de sistema avanzado (ASF) cifrado.</span><span class="sxs-lookup"><span data-stu-id="2ed65-105">Specifies the key identifier for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="2ed65-106">Este atributo corresponde al campo de identificador de clave del encabezado de cifrado de contenido, definido en la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="2ed65-106">This attribute corresponds to the Key ID field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="2ed65-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2ed65-107">Data type</span></span>

<span data-ttu-id="2ed65-108">Cadena de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="2ed65-108">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="2ed65-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ed65-109">Remarks</span></span>

<span data-ttu-id="2ed65-110">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="2ed65-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="2ed65-111">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) recupera el campo de ID. de clave, lo convierte en una cadena de caracteres anchos y, a continuación, rellena una matriz terminada en NULL de **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="2ed65-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Key ID field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="2ed65-112">El tamaño de la matriz es igual al campo de longitud de identificador de clave del encabezado de cifrado de contenido.</span><span class="sxs-lookup"><span data-stu-id="2ed65-112">The size of the array equals the Key ID Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ed65-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ed65-113">Requirements</span></span>



| <span data-ttu-id="2ed65-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ed65-114">Requirement</span></span> | <span data-ttu-id="2ed65-115">Value</span><span class="sxs-lookup"><span data-stu-id="2ed65-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed65-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ed65-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2ed65-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2ed65-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2ed65-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ed65-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2ed65-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ed65-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2ed65-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ed65-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ed65-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ed65-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ed65-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ed65-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ed65-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2ed65-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2ed65-124">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="2ed65-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="2ed65-125">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="2ed65-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="2ed65-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2ed65-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="2ed65-127">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="2ed65-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2ed65-128">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="2ed65-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="2ed65-129">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="2ed65-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




