---
description: Obtiene un objeto de tipo IMFCollection que contiene objetos IMFSample que contienen unidades de capa de abstracción de red (NALUs) e información de mejora adicional (SEI) reenviadas por un descodificador.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: MFSampleExtension_ForwardedDecodeUnits atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720496"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a><span data-ttu-id="e230a-103">\_Atributo ForwardedDecodeUnits de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="e230a-103">MFSampleExtension\_ForwardedDecodeUnits attribute</span></span>

<span data-ttu-id="e230a-104">Obtiene un objeto de tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que contiene objetos [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que contienen unidades de capa de abstracción de red (NALUs) e información de mejora adicional (SEI) reenviadas por un descodificador.</span><span class="sxs-lookup"><span data-stu-id="e230a-104">Gets an object of type [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) containing [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) objects which contain network abstraction layer units (NALUs) and Supplemental Enhancement Information (SEI) units forwarded by a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="e230a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e230a-105">Data type</span></span>

<span data-ttu-id="e230a-106">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="e230a-106">**IUnknown**</span></span>

## <a name="remarks"></a><span data-ttu-id="e230a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e230a-107">Remarks</span></span>

<span data-ttu-id="e230a-108">La colección contiene todas las unidades NALU/SEI personalizadas desde el fotograma anterior con bytes de prevención de emulación quitados.</span><span class="sxs-lookup"><span data-stu-id="e230a-108">The collection contains all custom NALU/SEI units since previous frame with emulation prevention bytes removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e230a-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e230a-109">Requirements</span></span>



| <span data-ttu-id="e230a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e230a-110">Requirement</span></span> | <span data-ttu-id="e230a-111">Value</span><span class="sxs-lookup"><span data-stu-id="e230a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e230a-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e230a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e230a-113">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="e230a-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e230a-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e230a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e230a-115">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="e230a-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e230a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e230a-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e230a-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e230a-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




