---
description: Almacena la cadena enviada en el encabezado Accept-Language.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: Propiedad MFNETSOURCE_STREAM_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200c49d4a14146277c66fbb3389cf1ba6ab13fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423523"
---
# <a name="mfnetsource_stream_language-property"></a><span data-ttu-id="b431f-103">Propiedad de lenguaje de \_ secuencia de MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="b431f-103">MFNETSOURCE\_STREAM\_LANGUAGE property</span></span>

<span data-ttu-id="b431f-104">Almacena la cadena enviada en el encabezado Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="b431f-104">Stores the string sent in the Accept-Language header.</span></span>



<span data-ttu-id="b431f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b431f-105">Data type</span></span>

<span data-ttu-id="b431f-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="b431f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="b431f-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="b431f-107">PROPVARIANT member</span></span>

<span data-ttu-id="b431f-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="b431f-108">\**WCHAR\** _</span></span>

<span data-ttu-id="b431f-109">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="b431f-109">VT\_LPWSTR</span></span>

<span data-ttu-id="b431f-110">_ *pwszVal*\*</span><span class="sxs-lookup"><span data-stu-id="b431f-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="b431f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b431f-111">Remarks</span></span>

<span data-ttu-id="b431f-112">La \_ \_ constante de lenguaje de secuencia MFNETSOURCE define el GUID de la clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b431f-112">The MFNETSOURCE\_STREAM\_LANGUAGE constant defines the GUID for the property key.</span></span> <span data-ttu-id="b431f-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="b431f-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="b431f-114">Para establecer esta propiedad en el origen de red, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="b431f-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="b431f-115">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="b431f-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b431f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b431f-116">Requirements</span></span>



| <span data-ttu-id="b431f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b431f-117">Requirement</span></span> | <span data-ttu-id="b431f-118">Value</span><span class="sxs-lookup"><span data-stu-id="b431f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b431f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b431f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b431f-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b431f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b431f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b431f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b431f-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b431f-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b431f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b431f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b431f-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b431f-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b431f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b431f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b431f-126">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b431f-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b431f-127">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b431f-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




