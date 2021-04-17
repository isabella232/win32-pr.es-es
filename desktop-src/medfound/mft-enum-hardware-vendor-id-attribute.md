---
description: Especifica el identificador de proveedor para un Microsoft Media Foundation basado en hardware.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: MFT_ENUM_HARDWARE_VENDOR_ID_Attribute atributo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4d92585936e52cbb0b9b65201a5de0d3a02b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659831"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a><span data-ttu-id="011e9-103">\_Atributo de \_ \_ atributo de identificador de proveedor de hardware de \_ enumeración MFT \_</span><span class="sxs-lookup"><span data-stu-id="011e9-103">MFT\_ENUM\_HARDWARE\_VENDOR\_ID\_Attribute attribute</span></span>

<span data-ttu-id="011e9-104">Especifica el identificador de proveedor para una transformación de Microsoft Media Foundation basado en hardware (MFT).</span><span class="sxs-lookup"><span data-stu-id="011e9-104">Specifies the vendor ID for a hardware-based Microsoft Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="011e9-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="011e9-105">Data type</span></span>

<span data-ttu-id="011e9-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="011e9-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="011e9-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="011e9-107">Get/set</span></span>

<span data-ttu-id="011e9-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="011e9-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="011e9-109">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="011e9-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="011e9-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="011e9-110">Remarks</span></span>

<span data-ttu-id="011e9-111">Este atributo es informativo y opcional.</span><span class="sxs-lookup"><span data-stu-id="011e9-111">This attribute is informational and optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="011e9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="011e9-112">Requirements</span></span>



| <span data-ttu-id="011e9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="011e9-113">Requirement</span></span> | <span data-ttu-id="011e9-114">Value</span><span class="sxs-lookup"><span data-stu-id="011e9-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="011e9-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="011e9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="011e9-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="011e9-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="011e9-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="011e9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="011e9-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="011e9-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="011e9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="011e9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="011e9-120"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="011e9-120"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="011e9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="011e9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="011e9-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="011e9-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="011e9-123">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="011e9-123">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="011e9-124">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="011e9-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




