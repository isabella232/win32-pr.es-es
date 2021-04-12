---
description: Representa una solicitud para un ejemplo de un MediaStreamSource.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: Interfaz IMFMediaStreamSourceSampleRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361901"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a><span data-ttu-id="678b6-103">Interfaz IMFMediaStreamSourceSampleRequest</span><span class="sxs-lookup"><span data-stu-id="678b6-103">IMFMediaStreamSourceSampleRequest interface</span></span>

<span data-ttu-id="678b6-104">Representa una solicitud para un ejemplo de un MediaStreamSource.</span><span class="sxs-lookup"><span data-stu-id="678b6-104">Represents a request for a sample from a MediaStreamSource.</span></span>

## <a name="members"></a><span data-ttu-id="678b6-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="678b6-105">Members</span></span>

<span data-ttu-id="678b6-106">La interfaz **IMFMediaStreamSourceSampleRequest** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="678b6-106">The **IMFMediaStreamSourceSampleRequest** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="678b6-107">**IMFMediaStreamSourceSampleRequest** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="678b6-107">**IMFMediaStreamSourceSampleRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="678b6-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="678b6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="678b6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="678b6-109">Methods</span></span>

<span data-ttu-id="678b6-110">La interfaz **IMFMediaStreamSourceSampleRequest** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="678b6-110">The **IMFMediaStreamSourceSampleRequest** interface has these methods.</span></span>



| <span data-ttu-id="678b6-111">Método</span><span class="sxs-lookup"><span data-stu-id="678b6-111">Method</span></span>                                                           | <span data-ttu-id="678b6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="678b6-112">Description</span></span>                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="678b6-113">**SetSample**</span><span class="sxs-lookup"><span data-stu-id="678b6-113">**SetSample**</span></span>](imfmediastreamsourcesamplerequest-setsample.md) | <span data-ttu-id="678b6-114">Establece el ejemplo para el origen de la secuencia de medios.</span><span class="sxs-lookup"><span data-stu-id="678b6-114">Sets the sample for the media stream source.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="678b6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="678b6-115">Remarks</span></span>

<span data-ttu-id="678b6-116">La clase de tiempo de ejecución de [**Windows. Media. Core. MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) implementa **MFMediaStreamSourceSampleRequest** .</span><span class="sxs-lookup"><span data-stu-id="678b6-116">**MFMediaStreamSourceSampleRequest** is implemented by the [**Windows.Media.Core.MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) runtime class.</span></span>

## <a name="requirements"></a><span data-ttu-id="678b6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="678b6-117">Requirements</span></span>



| <span data-ttu-id="678b6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="678b6-118">Requirement</span></span> | <span data-ttu-id="678b6-119">Value</span><span class="sxs-lookup"><span data-stu-id="678b6-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="678b6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="678b6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="678b6-121">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="678b6-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="678b6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="678b6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="678b6-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="678b6-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="678b6-124">IDL</span><span class="sxs-lookup"><span data-stu-id="678b6-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="678b6-125"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="678b6-125"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="678b6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="678b6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="678b6-127">Interfaces de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="678b6-127">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
