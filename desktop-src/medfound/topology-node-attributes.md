---
description: Atributos de nodo de topología
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Atributos de nodo de topología
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001583"
---
# <a name="topology-node-attributes"></a><span data-ttu-id="7700d-103">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="7700d-103">Topology Node Attributes</span></span>

<span data-ttu-id="7700d-104">Los siguientes atributos se aplican a los nodos de la topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-104">The following attributes apply to topology nodes.</span></span>

## <a name="general-topology-node-attributes"></a><span data-ttu-id="7700d-105">Atributos de nodo de topología general</span><span class="sxs-lookup"><span data-stu-id="7700d-105">General Topology Node Attributes</span></span>



| <span data-ttu-id="7700d-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="7700d-106">Attribute</span></span>                                                                       | <span data-ttu-id="7700d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7700d-107">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7700d-108">**\_método de \_ conexión MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="7700d-108">**MF\_TOPONODE\_CONNECT\_METHOD**</span></span>](mf-toponode-connect-method-attribute.md)   | <span data-ttu-id="7700d-109">Especifica cómo el cargador de topología conecta este nodo de topología y si este nodo es opcional.</span><span class="sxs-lookup"><span data-stu-id="7700d-109">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>                                                        |
| [<span data-ttu-id="7700d-110">**descodificador de MF \_ TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="7700d-110">**MF\_TOPONODE\_DECODER**</span></span>](mf-toponode-decoder-attribute.md)                  | <span data-ttu-id="7700d-111">Especifica si el objeto de un nodo topología es un descodificador.</span><span class="sxs-lookup"><span data-stu-id="7700d-111">Specifies whether a toplogy node's object is a decoder.</span></span>                                                                                                  |
| [<span data-ttu-id="7700d-112">**\_DEScifrador MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="7700d-112">**MF\_TOPONODE\_DECRYPTOR**</span></span>](mf-toponode-decryptor-attribute.md)              | <span data-ttu-id="7700d-113">Especifica si el objeto subyacente de un nodo topología es un descifrador.</span><span class="sxs-lookup"><span data-stu-id="7700d-113">Specifies whether a toplogy node's underlying object is a decryptor.</span></span>                                                                                     |
| [<span data-ttu-id="7700d-114">**MF \_ TOPONODE \_ descartable**</span><span class="sxs-lookup"><span data-stu-id="7700d-114">**MF\_TOPONODE\_DISCARDABLE**</span></span>](mf-toponode-discardable-attribute.md)          | <span data-ttu-id="7700d-115">Especifica si la canalización puede quitar ejemplos de un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-115">Specifies whether the pipeline can drop samples from a topology node.</span></span>                                                                                    |
| [<span data-ttu-id="7700d-116">**\_MAJORTYPE TOPONODE \_ error de MF \_**</span><span class="sxs-lookup"><span data-stu-id="7700d-116">**MF\_TOPONODE\_ERROR\_MAJORTYPE**</span></span>](mf-toponode-error-majortype-attribute.md) | <span data-ttu-id="7700d-117">Contiene el tipo de medio principal para un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-117">Contains the major media type for a topology node.</span></span> <span data-ttu-id="7700d-118">Este atributo se establece cuando no se puede cargar la topología porque no se pudo encontrar el descodificador correcto.</span><span class="sxs-lookup"><span data-stu-id="7700d-118">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span> |
| [<span data-ttu-id="7700d-119">**subtipo de \_ error MF TOPONODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7700d-119">**MF\_TOPONODE\_ERROR\_SUBTYPE**</span></span>](mf-toponode-error-subtype-attribute.md)     | <span data-ttu-id="7700d-120">Contiene el subtipo de medio para un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-120">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="7700d-121">Este atributo se establece cuando no se puede cargar la topología porque no se pudo encontrar el descodificador correcto.</span><span class="sxs-lookup"><span data-stu-id="7700d-121">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>    |
| [<span data-ttu-id="7700d-122">**\_código de \_ ERRORCODE TOPONODE MF**</span><span class="sxs-lookup"><span data-stu-id="7700d-122">**MF\_TOPONODE\_ERRORCODE**</span></span>](mf-toponode-errorcode-attribute.md)              | <span data-ttu-id="7700d-123">Contiene el código de error del error de conexión más reciente para este nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-123">Contains the error code from the most recent connection failure for this topology node.</span></span>                                                                  |
| [<span data-ttu-id="7700d-124">**MF \_ TOPONODE \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="7700d-124">**MF\_TOPONODE\_LOCKED**</span></span>](mf-toponode-locked-attribute.md)                    | <span data-ttu-id="7700d-125">Especifica si los tipos de medios se pueden cambiar en este nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-125">Specifies whether the media types can be changed on this topology node.</span></span>                                                                                  |
| [<span data-ttu-id="7700d-126">**\_TOPONODE MF \_ \_ aquí**</span><span class="sxs-lookup"><span data-stu-id="7700d-126">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)         | <span data-ttu-id="7700d-127">Especifica si la canalización aplica el marcado en este nodo.</span><span class="sxs-lookup"><span data-stu-id="7700d-127">Specifies whether the pipeline applies mark-in at this node.</span></span>                                                                                             |
| [<span data-ttu-id="7700d-128">**MF \_ TOPONODE \_ MARKOUT \_ aquí**</span><span class="sxs-lookup"><span data-stu-id="7700d-128">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)       | <span data-ttu-id="7700d-129">Especifica si la canalización aplica el marcado en este nodo.</span><span class="sxs-lookup"><span data-stu-id="7700d-129">Specifies whether the pipeline applies mark-out at this node.</span></span>                                                                                            |



 

## <a name="source-node-attributes"></a><span data-ttu-id="7700d-130">Atributos del nodo de origen</span><span class="sxs-lookup"><span data-stu-id="7700d-130">Source Node Attributes</span></span>



| <span data-ttu-id="7700d-131">Atributo</span><span class="sxs-lookup"><span data-stu-id="7700d-131">Attribute</span></span>                                                                                       | <span data-ttu-id="7700d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7700d-132">Description</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7700d-133">**MF \_ TOPONODE \_ MEDIASTART**</span><span class="sxs-lookup"><span data-stu-id="7700d-133">**MF\_TOPONODE\_MEDIASTART**</span></span>](mf-toponode-mediastart-attribute.md)                            | <span data-ttu-id="7700d-134">Especifica la hora de inicio de una presentación, relativa al inicio del archivo de origen multimedia, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="7700d-134">Specifies the start time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="7700d-135">**MF \_ TOPONODE \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="7700d-135">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)                              | <span data-ttu-id="7700d-136">Especifica la hora de detención de una presentación, relativa al inicio del archivo de origen multimedia, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="7700d-136">Specifies the stop time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span>  |
| [<span data-ttu-id="7700d-137">**descriptor de presentación de MF \_ TOPONODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7700d-137">**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**</span></span>](mf-toponode-presentation-descriptor-attribute.md) | <span data-ttu-id="7700d-138">Contiene un puntero al descriptor de presentación para el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="7700d-138">Contains a pointer to the presentation descriptor for the media source.</span></span>                                           |
| [<span data-ttu-id="7700d-139">**MF \_ TOPONODE \_ Sequence \_ ELEMENTID**</span><span class="sxs-lookup"><span data-stu-id="7700d-139">**MF\_TOPONODE\_SEQUENCE\_ELEMENTID**</span></span>](mf-toponode-sequence-elementid-attribute.md)           | <span data-ttu-id="7700d-140">Especifica el elemento que contiene un nodo de origen.</span><span class="sxs-lookup"><span data-stu-id="7700d-140">Specifies the element that contains a source node.</span></span>                                                                |
| [<span data-ttu-id="7700d-141">**origen de MF \_ TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="7700d-141">**MF\_TOPONODE\_SOURCE**</span></span>](mf-toponode-source-attribute.md)                                    | <span data-ttu-id="7700d-142">Contiene un puntero al origen multimedia asociado a un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-142">Contains a pointer to the media source associated with a topology node.</span></span>                                           |
| [<span data-ttu-id="7700d-143">**descriptor de secuencia MF \_ TOPONODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7700d-143">**MF\_TOPONODE\_STREAM\_DESCRIPTOR**</span></span>](mf-toponode-stream-descriptor-attribute.md)             | <span data-ttu-id="7700d-144">Contiene un puntero al descriptor de flujo para el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="7700d-144">Contains a pointer to the stream descriptor for the media source.</span></span>                                                 |
| [<span data-ttu-id="7700d-145">**identificador de WORKQUEUE de MF \_ TOPONODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7700d-145">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)                       | <span data-ttu-id="7700d-146">Especifica una cola de trabajo para un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-146">Specifies a work queue for a topology node.</span></span>                                                                       |
| [<span data-ttu-id="7700d-147">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS ( \_ clase)**</span><span class="sxs-lookup"><span data-stu-id="7700d-147">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)    | <span data-ttu-id="7700d-148">Especifica una tarea del servicio de programador de clases multimedia (MMCSS) para un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-148">Specifies a Multimedia Class Scheduler Service (MMCSS) task for a topology node.</span></span>                                  |
| [<span data-ttu-id="7700d-149">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="7700d-149">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | <span data-ttu-id="7700d-150">Especifica un identificador de la tarea MMCSS para un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-150">Specifies a MMCSS task identifier for a topology node.</span></span>                                                            |



 

## <a name="transform-node-attributes"></a><span data-ttu-id="7700d-151">Transformación de atributos de nodo</span><span class="sxs-lookup"><span data-stu-id="7700d-151">Transform Node Attributes</span></span>



| <span data-ttu-id="7700d-152">Atributo</span><span class="sxs-lookup"><span data-stu-id="7700d-152">Attribute</span></span>                                                                             | <span data-ttu-id="7700d-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="7700d-153">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7700d-154">**MF \_ TOPONODE \_ D3DAWARE**</span><span class="sxs-lookup"><span data-stu-id="7700d-154">**MF\_TOPONODE\_D3DAWARE**</span></span>](mf-toponode-d3daware-attribute.md)                      | <span data-ttu-id="7700d-155">Especifica si la transformación asociada a un nodo de topología es compatible con la aceleración de vídeo de DirectX (DXVA)</span><span class="sxs-lookup"><span data-stu-id="7700d-155">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA)</span></span> |
| [<span data-ttu-id="7700d-156">**\_desagüe TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="7700d-156">**MF\_TOPONODE\_DRAIN**</span></span>](mf-toponode-drain-attribute.md)                            | <span data-ttu-id="7700d-157">Especifica cuándo se purga una transformación.</span><span class="sxs-lookup"><span data-stu-id="7700d-157">Specifies when a transform is drained.</span></span>                                                                     |
| [<span data-ttu-id="7700d-158">**\_vaciado de TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="7700d-158">**MF\_TOPONODE\_FLUSH**</span></span>](mf-toponode-flush-attribute.md)                            | <span data-ttu-id="7700d-159">Especifica cuándo se vacía una transformación.</span><span class="sxs-lookup"><span data-stu-id="7700d-159">Specifies when a transform is flushed.</span></span>                                                                     |
| [<span data-ttu-id="7700d-160">**MF \_ TOPONODE \_ Transform \_ objectId**</span><span class="sxs-lookup"><span data-stu-id="7700d-160">**MF\_TOPONODE\_TRANSFORM\_OBJECTID**</span></span>](mf-toponode-transform-objectid-attribute.md) | <span data-ttu-id="7700d-161">Identificador de clase (CLSID) de la transformación asociada a este nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-161">The class identifier (CLSID) of the transform associated with this topology node.</span></span>                          |



 

## <a name="output-node-attributes"></a><span data-ttu-id="7700d-162">Atributos del nodo de salida</span><span class="sxs-lookup"><span data-stu-id="7700d-162">Output Node Attributes</span></span>



| <span data-ttu-id="7700d-163">Atributo</span><span class="sxs-lookup"><span data-stu-id="7700d-163">Attribute</span></span>                                                                                  | <span data-ttu-id="7700d-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="7700d-164">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7700d-165">**MF \_ TOPONODE \_ deshabilitar \_ preroll**</span><span class="sxs-lookup"><span data-stu-id="7700d-165">**MF\_TOPONODE\_DISABLE\_PREROLL**</span></span>](mf-toponode-disable-preroll-attribute.md)            | <span data-ttu-id="7700d-166">Especifica si la sesión multimedia utiliza el preparado en el receptor de medios representado por este nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-166">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>            |
| [<span data-ttu-id="7700d-167">**MF \_ TOPONODE \_ noshutdown \_ al \_ quitar**</span><span class="sxs-lookup"><span data-stu-id="7700d-167">**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**</span></span>](mf-toponode-noshutdown-on-remove-attribute.md) | <span data-ttu-id="7700d-168">Especifica si la sesión multimedia apaga el receptor de medios cuando el nodo de salida se quita de la topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-168">Specifies whether the Media Session shuts down the media sink when the output node is removed from the topology.</span></span> |
| [<span data-ttu-id="7700d-169">**MF \_ TOPONODE sin \_ velocidad**</span><span class="sxs-lookup"><span data-stu-id="7700d-169">**MF\_TOPONODE\_RATELESS**</span></span>](mf-toponode-rateless-attribute.md)                           | <span data-ttu-id="7700d-170">Especifica si el receptor de medios asociado a este nodo de topología tiene un número inestable.</span><span class="sxs-lookup"><span data-stu-id="7700d-170">Specifies whether the media sink associated with this topology node is rateless.</span></span>                                 |
| [<span data-ttu-id="7700d-171">**MF \_ TOPONODE \_ STREAMID**</span><span class="sxs-lookup"><span data-stu-id="7700d-171">**MF\_TOPONODE\_STREAMID**</span></span>](mf-toponode-streamid-attribute.md)                           | <span data-ttu-id="7700d-172">El identificador de flujo del receptor de flujo asociado a este nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="7700d-172">The stream identifier of the stream sink associated with this topology node.</span></span>                                     |



 

## <a name="tee-node-attributes"></a><span data-ttu-id="7700d-173">Tee (atributos de nodo)</span><span class="sxs-lookup"><span data-stu-id="7700d-173">Tee Node Attributes</span></span>



| <span data-ttu-id="7700d-174">Atributo</span><span class="sxs-lookup"><span data-stu-id="7700d-174">Attribute</span></span>                                                                  | <span data-ttu-id="7700d-175">Descripción</span><span class="sxs-lookup"><span data-stu-id="7700d-175">Description</span></span>                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="7700d-176">**MF \_ TOPONODE \_ PRIMARYOUTPUT**</span><span class="sxs-lookup"><span data-stu-id="7700d-176">**MF\_TOPONODE\_PRIMARYOUTPUT**</span></span>](mf-toponode-primaryoutput-attribute.md) | <span data-ttu-id="7700d-177">Indica qué salida es la salida principal en un nodo tee.</span><span class="sxs-lookup"><span data-stu-id="7700d-177">Indicates which output is the primary output on a tee node.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7700d-178">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7700d-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7700d-179">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="7700d-179">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="7700d-180">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7700d-180">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7700d-181">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="7700d-181">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 



