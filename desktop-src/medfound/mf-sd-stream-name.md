---
description: Contiene el nombre de una secuencia.
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: MF_SD_STREAM_NAME atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734c2d20390ba1a450a40c03054b4c67c5c0409a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361423"
---
# <a name="mf_sd_stream_name-attribute"></a><span data-ttu-id="18ac5-103">\_Atributo de \_ nombre de flujo SD MF \_</span><span class="sxs-lookup"><span data-stu-id="18ac5-103">MF\_SD\_STREAM\_NAME attribute</span></span>

<span data-ttu-id="18ac5-104">Contiene el nombre de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="18ac5-104">Contains the name of a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="18ac5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="18ac5-105">Data type</span></span>

<span data-ttu-id="18ac5-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="18ac5-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="18ac5-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="18ac5-107">Get/set</span></span>

<span data-ttu-id="18ac5-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="18ac5-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="18ac5-109">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="18ac5-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="18ac5-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="18ac5-110">Applies to</span></span>

[<span data-ttu-id="18ac5-111">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="18ac5-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="18ac5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18ac5-112">Remarks</span></span>

<span data-ttu-id="18ac5-113">El origen de medios AVI establece este atributo si el archivo AVI contiene un fragmento "STRN".</span><span class="sxs-lookup"><span data-stu-id="18ac5-113">The AVI media source sets this attribute if the AVI file contains a 'strn' chunk.</span></span>

<span data-ttu-id="18ac5-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="18ac5-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ac5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18ac5-115">Requirements</span></span>



| <span data-ttu-id="18ac5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="18ac5-116">Requirement</span></span> | <span data-ttu-id="18ac5-117">Value</span><span class="sxs-lookup"><span data-stu-id="18ac5-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18ac5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18ac5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="18ac5-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="18ac5-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="18ac5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18ac5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="18ac5-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="18ac5-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="18ac5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18ac5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="18ac5-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="18ac5-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ac5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="18ac5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ac5-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18ac5-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="18ac5-126">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="18ac5-126">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




