---
description: Especifica si un codificador debe estar incluido en la topología de transcodificación.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: MF_TRANSCODE_DONOT_INSERT_ENCODER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696634"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a><span data-ttu-id="0d013-103">MF \_ Transcode \_ donot \_ Insertar \_ atributo Encoder</span><span class="sxs-lookup"><span data-stu-id="0d013-103">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER attribute</span></span>

<span data-ttu-id="0d013-104">Especifica si un codificador debe estar incluido en la topología de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="0d013-104">Specifies whether an encoder must be included in the transcode topology.</span></span>

<span data-ttu-id="0d013-105">La función [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) comprueba este atributo durante la creación de la topología.</span><span class="sxs-lookup"><span data-stu-id="0d013-105">The [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function checks this attribute during topology building.</span></span> <span data-ttu-id="0d013-106">Si no se establece este atributo, se inserta un codificador en la topología de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="0d013-106">If this attribute is not set, an encoder is inserted in the transcode topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="0d013-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0d013-107">Data type</span></span>

<span data-ttu-id="0d013-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0d013-108">**UINT32**</span></span>



| <span data-ttu-id="0d013-109">Value</span><span class="sxs-lookup"><span data-stu-id="0d013-109">Value</span></span>                                                                        | <span data-ttu-id="0d013-110">Significado</span><span class="sxs-lookup"><span data-stu-id="0d013-110">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d013-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0d013-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="0d013-112">Se inserta un codificador en la topología de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="0d013-112">An encoder is inserted in the transcode topology.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="0d013-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0d013-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="0d013-114">Un codificador no se incluye en la topología de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="0d013-114">An encoder is not included in the transcode topology.</span></span> <span data-ttu-id="0d013-115">El nodo de origen se conecta al nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="0d013-115">The source node is connected to the output node.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d013-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d013-116">Remarks</span></span>

<span data-ttu-id="0d013-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0d013-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d013-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d013-118">Requirements</span></span>



| <span data-ttu-id="0d013-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d013-119">Requirement</span></span> | <span data-ttu-id="0d013-120">Value</span><span class="sxs-lookup"><span data-stu-id="0d013-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d013-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d013-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d013-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d013-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0d013-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d013-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d013-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d013-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0d013-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d013-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d013-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d013-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d013-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d013-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d013-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0d013-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d013-129">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0d013-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




