---
description: Especifica cómo la sesión multimedia apaga un objeto en la topología.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: MF_TOPONODE_NOSHUTDOWN_ON_REMOVE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705795"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a><span data-ttu-id="608c6-103">MF \_ TOPONODE \_ noshutdown \_ en el \_ atributo Remove</span><span class="sxs-lookup"><span data-stu-id="608c6-103">MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE attribute</span></span>

<span data-ttu-id="608c6-104">Especifica cómo la sesión multimedia apaga un objeto en la topología.</span><span class="sxs-lookup"><span data-stu-id="608c6-104">Specifies how the Media Session shuts down an object in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="608c6-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="608c6-105">Data type</span></span>

<span data-ttu-id="608c6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="608c6-106">**UINT32**</span></span>

<span data-ttu-id="608c6-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="608c6-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="608c6-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="608c6-108">Remarks</span></span>

<span data-ttu-id="608c6-109">Este atributo se aplica a los siguientes tipos de nodo topología:</span><span class="sxs-lookup"><span data-stu-id="608c6-109">This attribute applies to the following types of toplogy node:</span></span>

-   <span data-ttu-id="608c6-110">Nodos de salida</span><span class="sxs-lookup"><span data-stu-id="608c6-110">Output nodes</span></span>
-   <span data-ttu-id="608c6-111">Cualquier nodo de transformación que contenga una transformación de Media Foundation *asincrónica* (MFT).</span><span class="sxs-lookup"><span data-stu-id="608c6-111">Any transform node that contains an *asynchronous* Media Foundation transform (MFT).</span></span>

<span data-ttu-id="608c6-112">El atributo puede tener los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="608c6-112">The attribute can have the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="608c6-113">Value</span><span class="sxs-lookup"><span data-stu-id="608c6-113">Value</span></span></th>
<th><span data-ttu-id="608c6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="608c6-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="608c6-115"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="608c6-115"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="608c6-116">Cuando la sesión multimedia cambia a una nueva topología o borra la topología actual, no cierra el objeto que pertenece a este nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="608c6-116">When the Media Session switches to a new topology or clears the current topology, it does not shut down the object that belongs to this topology node.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="608c6-117"><strong>FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="608c6-117"><strong>FALSE</strong></span></span></td>
<td><span data-ttu-id="608c6-118">Cuando la sesión multimedia cambia a una nueva topología o borra la topología actual, cierra el objeto de nodo, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="608c6-118">When the Media Session switches to a new topology or clears the current topology, it shuts down the node object, as follows:</span></span>
<ul>
<li><span data-ttu-id="608c6-119">Nodos de salida: la sesión llama a <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink:: Shutdown</strong></a> en el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="608c6-119">Output nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink::Shutdown</strong></a> on the media sink.</span></span></li>
<li><span data-ttu-id="608c6-120">Transformar nodos: la sesión llama a <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown:: Shutdown</strong></a> en la MFT.</span><span class="sxs-lookup"><span data-stu-id="608c6-120">Transform nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown::Shutdown</strong></a> on the MFT.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="608c6-121">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="608c6-121">The default value is **TRUE**.</span></span>

<span data-ttu-id="608c6-122">Si la aplicación pone en cola varias topologías, es una buena idea establecer este atributo en **false**.</span><span class="sxs-lookup"><span data-stu-id="608c6-122">If your application queues multiple topologies, it is a good idea to set this attribute to **FALSE**.</span></span> <span data-ttu-id="608c6-123">De lo contrario, es posible que los objetos de la topología no se cierren correctamente.</span><span class="sxs-lookup"><span data-stu-id="608c6-123">Otherwise, objects in the topology might not be shut down correctly.</span></span>

<span data-ttu-id="608c6-124">Este atributo no se aplica cuando la aplicación cierra la sesión multimedia mediante una llamada a [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="608c6-124">This attribute does not apply when the application shuts down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="608c6-125">Cuando se cierra la sesión multimedia, siempre cierra los receptores de medios y MFTs asincrónicos en la topología actual.</span><span class="sxs-lookup"><span data-stu-id="608c6-125">When the Media Session shuts down, it always shuts down the media sinks and asynchronous MFTs in the current topology.</span></span>

<span data-ttu-id="608c6-126">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="608c6-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="608c6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="608c6-127">Requirements</span></span>



| <span data-ttu-id="608c6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="608c6-128">Requirement</span></span> | <span data-ttu-id="608c6-129">Value</span><span class="sxs-lookup"><span data-stu-id="608c6-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="608c6-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="608c6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="608c6-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="608c6-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="608c6-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="608c6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="608c6-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="608c6-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="608c6-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="608c6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="608c6-135"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="608c6-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="608c6-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="608c6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="608c6-137">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="608c6-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="608c6-138">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="608c6-138">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="608c6-139">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="608c6-139">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="608c6-140">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="608c6-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="608c6-141">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="608c6-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="608c6-142">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="608c6-142">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




