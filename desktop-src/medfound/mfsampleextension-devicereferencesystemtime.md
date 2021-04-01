---
description: Especifica la marca de tiempo del dispositivo original en el ejemplo.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: MFSampleExtension_DeviceReferenceSystemTime atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908379"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a><span data-ttu-id="1e0f4-103">\_Atributo DeviceReferenceSystemTime de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="1e0f4-103">MFSampleExtension\_DeviceReferenceSystemTime attribute</span></span>

<span data-ttu-id="1e0f4-104">Especifica la marca de tiempo del dispositivo original en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-104">Specifies the original device timestamp on the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="1e0f4-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1e0f4-105">Data type</span></span>

<span data-ttu-id="1e0f4-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1e0f4-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="1e0f4-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e0f4-107">Remarks</span></span>

<span data-ttu-id="1e0f4-108">Se trata de una marca de tiempo de referencia de dispositivo de ejemplos de medios en la resolución de 100 NS.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-108">This is the a device reference time stamp of media samples in 100ns resolution.</span></span> <span data-ttu-id="1e0f4-109">Esta marca de tiempo puede o no contener el valor real del contador de rendimiento de la consulta (QPC), dependiendo del origen que produzca los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-109">This time stamp may or may not carry the actual value of the query performance counter (QPC), depending on the source producing the samples.</span></span> <span data-ttu-id="1e0f4-110">Otros componentes de la canalización multimedia pueden modificar este valor.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-110">This value may be modified by other components in the media pipeline.</span></span> <span data-ttu-id="1e0f4-111">Este valor no está disponible para MFTs insertado en la canalización de captura.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-111">This value is not available to MFTs inserted into the capture pipeline.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e0f4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e0f4-112">Requirements</span></span>



| <span data-ttu-id="1e0f4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e0f4-113">Requirement</span></span> | <span data-ttu-id="1e0f4-114">Value</span><span class="sxs-lookup"><span data-stu-id="1e0f4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0f4-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e0f4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1e0f4-116">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0f4-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1e0f4-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e0f4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1e0f4-118">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e0f4-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e0f4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e0f4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e0f4-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e0f4-120"><dt>Mfcaptureengine.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e0f4-121">IDL</span><span class="sxs-lookup"><span data-stu-id="1e0f4-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e0f4-122"><dt>Mfcaptureengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e0f4-122"><dt>Mfcaptureengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e0f4-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e0f4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0f4-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e0f4-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




