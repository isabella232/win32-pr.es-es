---
description: Obtiene estadísticas del receptor de medios de la Alianza de redes digitales (DLNA).
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: MF_MP2DLNA_STATISTICS atributo (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544366"
---
# <a name="mf_mp2dlna_statistics-attribute"></a><span data-ttu-id="e71ef-103">\_Atributo MF MP2DLNA \_ Statistics</span><span class="sxs-lookup"><span data-stu-id="e71ef-103">MF\_MP2DLNA\_STATISTICS attribute</span></span>

<span data-ttu-id="e71ef-104">Obtiene estadísticas del receptor de medios de la Alianza de redes digitales (DLNA).</span><span class="sxs-lookup"><span data-stu-id="e71ef-104">Gets statistics from the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="e71ef-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e71ef-105">Data type</span></span>

<span data-ttu-id="e71ef-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** almacenado como **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e71ef-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="e71ef-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="e71ef-107">Get/set</span></span>

<span data-ttu-id="e71ef-108">Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="e71ef-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="e71ef-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e71ef-109">Remarks</span></span>

<span data-ttu-id="e71ef-110">Durante el streaming, el receptor de medios DLNA actualiza este atributo con estadísticas sobre la codificación y multiplexación de las secuencias MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="e71ef-110">During streaming, the DLNA media sink updates this attribute with statistics about the encoding and multiplexing of the MPEG-2 streams.</span></span> <span data-ttu-id="e71ef-111">La aplicación puede consultar este atributo en cualquier momento para obtener los valores más recientes.</span><span class="sxs-lookup"><span data-stu-id="e71ef-111">The application can query this attribute at any time to get the latest values.</span></span>

<span data-ttu-id="e71ef-112">Establecer este atributo en el receptor de medios DLNA no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="e71ef-112">Setting this attribute on the DLNA media sink has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="e71ef-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e71ef-113">Requirements</span></span>



| <span data-ttu-id="e71ef-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e71ef-114">Requirement</span></span> | <span data-ttu-id="e71ef-115">Value</span><span class="sxs-lookup"><span data-stu-id="e71ef-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e71ef-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e71ef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e71ef-117">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e71ef-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e71ef-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e71ef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e71ef-119">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e71ef-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e71ef-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e71ef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e71ef-121"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="e71ef-121"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e71ef-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e71ef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e71ef-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e71ef-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




