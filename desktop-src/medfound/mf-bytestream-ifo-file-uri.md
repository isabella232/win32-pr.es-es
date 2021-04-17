---
description: 'Contiene la dirección URL del archivo IFO (información de DVD) especificado por el servidor HTTP en el encabezado HTTP, &\# 0034; Pragma: ifoFileURI.dlna.org&\# 0034;.'
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: MF_BYTESTREAM_IFO_FILE_URI atributo (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687217"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a><span data-ttu-id="ae98e-103">MF \_ BYTESTREAM \_ IFO \_ \_ atributo URI de archivo</span><span class="sxs-lookup"><span data-stu-id="ae98e-103">MF\_BYTESTREAM\_IFO\_FILE\_URI attribute</span></span>

<span data-ttu-id="ae98e-104">Contiene la dirección URL del archivo IFO (información de DVD) especificado por el servidor HTTP en el encabezado HTTP "pragma: ifoFileURI.dlna.org".</span><span class="sxs-lookup"><span data-stu-id="ae98e-104">Contains the URL of the IFO (DVD Information) file specified by the HTTP server in the HTTP header, "Pragma: ifoFileURI.dlna.org".</span></span>

## <a name="data-type"></a><span data-ttu-id="ae98e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ae98e-105">Data type</span></span>

<span data-ttu-id="ae98e-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ae98e-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="ae98e-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="ae98e-107">Get/set</span></span>

<span data-ttu-id="ae98e-108">Para obtener este atributo, llame a [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="ae98e-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="ae98e-109">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="ae98e-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ae98e-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="ae98e-110">Applies to</span></span>

[<span data-ttu-id="ae98e-111">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="ae98e-111">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="ae98e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae98e-112">Remarks</span></span>

<span data-ttu-id="ae98e-113">El flujo de bytes HTTP busca la cadena "ifoFileURI.dlna.org" en el encabezado HTTP.</span><span class="sxs-lookup"><span data-stu-id="ae98e-113">The HTTP byte stream searches the HTTP header for the "ifoFileURI.dlna.org" string.</span></span> <span data-ttu-id="ae98e-114">Si se encuentra la cadena, se copia en este atributo en el flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="ae98e-114">If the string is found, it is copied to this attribute on the byte stream.</span></span>

<span data-ttu-id="ae98e-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ae98e-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae98e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae98e-116">Requirements</span></span>



| <span data-ttu-id="ae98e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae98e-117">Requirement</span></span> | <span data-ttu-id="ae98e-118">Value</span><span class="sxs-lookup"><span data-stu-id="ae98e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae98e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae98e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae98e-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="ae98e-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                                        |
| <span data-ttu-id="ae98e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae98e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae98e-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="ae98e-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="ae98e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae98e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae98e-124"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae98e-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae98e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae98e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae98e-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae98e-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae98e-127">Atributos de secuencia de bytes</span><span class="sxs-lookup"><span data-stu-id="ae98e-127">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae98e-128">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="ae98e-128">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




