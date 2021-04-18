---
description: Indica que la información de longitud de NALU se enviará como un BLOB con cada ejemplo H. 264 comprimido.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: MF_NALU_LENGTH_SET atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697760"
---
# <a name="mf_nalu_length_set-attribute"></a><span data-ttu-id="b5041-103">\_Atributo de \_ conjunto de longitud MF Nalu \_</span><span class="sxs-lookup"><span data-stu-id="b5041-103">MF\_NALU\_LENGTH\_SET attribute</span></span>

<span data-ttu-id="b5041-104">Indica que la información de longitud de NALU se enviará como un **BLOB** con cada ejemplo H. 264 comprimido.</span><span class="sxs-lookup"><span data-stu-id="b5041-104">Indicates that NALU length information will be sent as a **BLOB** with each compressed H.264 sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="b5041-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b5041-105">Data type</span></span>

<span data-ttu-id="b5041-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b5041-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b5041-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5041-107">Remarks</span></span>

<span data-ttu-id="b5041-108">Establezca este atributo en el tipo de medio de entrada de MEDIASUBTYPE \_ H264.</span><span class="sxs-lookup"><span data-stu-id="b5041-108">Set this attribute on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="b5041-109">Establezca MF \_ Nalu \_ longitud \_ establecida en el tipo de medio de entrada del descodificador H. 264, que indica que cada ejemplo de entrada tendrá una longitud Nalu disponible y que cada ejemplo de entrada contenga una imagen principal completa.</span><span class="sxs-lookup"><span data-stu-id="b5041-109">Set MF\_NALU\_LENGTH\_SET on input media type of H.264 decoder, indicating each input sample will have a NALU length available and each input sample contains one complete primary picture.</span></span>

<span data-ttu-id="b5041-110">El **BLOB** que contiene la información de longitud de Nalu se puede recuperar del atributo de [ \_ información de \_ longitud \_ MF Nalu](mf-nalu-length-information.md) en el ejemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="b5041-110">The **BLOB** containing the NALU length information can be retrieved from [MF\_NALU\_LENGTH\_INFORMATION](mf-nalu-length-information.md) attribute on the input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5041-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5041-111">Requirements</span></span>



| <span data-ttu-id="b5041-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5041-112">Requirement</span></span> | <span data-ttu-id="b5041-113">Value</span><span class="sxs-lookup"><span data-stu-id="b5041-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5041-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5041-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b5041-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="b5041-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b5041-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5041-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b5041-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="b5041-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b5041-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5041-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5041-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5041-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5041-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5041-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5041-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b5041-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b5041-122">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="b5041-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




