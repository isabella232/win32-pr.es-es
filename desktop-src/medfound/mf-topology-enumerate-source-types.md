---
description: Especifica si el cargador de topología enumera los tipos de medios proporcionados por el origen de medios.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360261"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a><span data-ttu-id="b2d1d-103">\_Enumeración de topología MF \_ atributo de \_ tipos de origen \_</span><span class="sxs-lookup"><span data-stu-id="b2d1d-103">MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute</span></span>

<span data-ttu-id="b2d1d-104">Especifica si el cargador de topología enumera los tipos de medios proporcionados por el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-104">Specifies whether the topology loader enumerates the media types provided by the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="b2d1d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b2d1d-105">Data type</span></span>

<span data-ttu-id="b2d1d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b2d1d-106">**UINT32**</span></span>

<span data-ttu-id="b2d1d-107">Use uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-107">Use one of the following values.</span></span>



| <span data-ttu-id="b2d1d-108">Value</span><span class="sxs-lookup"><span data-stu-id="b2d1d-108">Value</span></span>                                                                                                                                    | <span data-ttu-id="b2d1d-109">Significado</span><span class="sxs-lookup"><span data-stu-id="b2d1d-109">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="b2d1d-110"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b2d1d-110"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="b2d1d-111">No enumere los tipos de medios de origen.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-111">Do not enumerate the source media types.</span></span><br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="b2d1d-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b2d1d-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="b2d1d-113">Enumera los tipos de medios de origen.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-113">Enumerate the source media types.</span></span><br/>        |



 

## <a name="getset"></a><span data-ttu-id="b2d1d-114">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="b2d1d-114">Get/set</span></span>

<span data-ttu-id="b2d1d-115">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b2d1d-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b2d1d-116">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b2d1d-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b2d1d-117">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="b2d1d-117">Applies to</span></span>

[<span data-ttu-id="b2d1d-118">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="b2d1d-118">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="b2d1d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2d1d-119">Remarks</span></span>

<span data-ttu-id="b2d1d-120">Cada secuencia de un origen multimedia puede ofrecer más de un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-120">Each stream on a media source can offer more than one media type.</span></span> <span data-ttu-id="b2d1d-121">La lista de tipos se enumera a través de la interfaz [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) en el descriptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-121">The list of types is enumerated through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream descriptor.</span></span>

<span data-ttu-id="b2d1d-122">El orden en el que el cargador de topología intenta los tipos de medios de un origen multimedia se controla mediante dos atributos:</span><span class="sxs-lookup"><span data-stu-id="b2d1d-122">The order in which the topology loader tries a media source's media types is controlled by two attributes:</span></span>

-   <span data-ttu-id="b2d1d-123">El \_ atributo MF Topology \_ enumerar \_ \_ tipos de origen en la topología.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-123">The MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute on the topology.</span></span>
-   <span data-ttu-id="b2d1d-124">El atributo de [**\_ método de \_ conexión \_ MF TOPONODE**](mf-toponode-connect-method-attribute.md) en el nodo de origen.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-124">The [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node.</span></span>

<span data-ttu-id="b2d1d-125">Si el \_ atributo MF Topology \_ enumerar \_ tipos de origen \_ es **false** o no está establecido, el cargador de topología usa el tipo de medio actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-125">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **FALSE** or not set, the topology loader uses the stream's current media type.</span></span> <span data-ttu-id="b2d1d-126">No enumera la lista de tipos posibles.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-126">It does not enumerate the list of possible types.</span></span> <span data-ttu-id="b2d1d-127">Si el tipo de medio actual es incompatible con el nodo de la topología de bajada y no se puede encontrar una combinación de descodificadores/convertidores, se produce un error en la resolución de topología.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-127">If the current media type is incompatible with the downstream topology node, and no combination of decoders/converters can be found, topology resolution fails.</span></span>

<span data-ttu-id="b2d1d-128">Si el \_ atributo MF Topology \_ enumerar \_ tipos de origen \_ es **true**, el cargador de topología enumera los tipos de medios del origen hasta que encuentra un tipo compatible.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-128">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **TRUE**, the topology loader enumerates the source's media types until it finds a compatible type.</span></span> <span data-ttu-id="b2d1d-129">En ese caso, el orden exacto de las operaciones depende de si el atributo de [**\_ método de \_ conexión \_ MF TOPONODE**](mf-toponode-connect-method-attribute.md) en el nodo de origen incluye la marca **MF \_ Connect \_ Resolve \_ independiente de \_ OUTPUTTYPES** .</span><span class="sxs-lookup"><span data-stu-id="b2d1d-129">In that case, the exact order of operations depends on the whether the [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node includes the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span>

<span data-ttu-id="b2d1d-130">Si \_ \_ los tipos de origen de la enumeración MF \_ \_ son **true** y se establece la marca **MF \_ Connect de \_ \_ \_ OUTPUTTYPES independiente** , el cargador de topología agotará cada tipo de medio antes de pasar al siguiente, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="b2d1d-130">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** and the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set, the topology loader exhausts each media type before moving to the next, as follows:</span></span>

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

<span data-ttu-id="b2d1d-131">Si \_ la enumeración de la topología MF \_ \_ \_ es **true** , pero no se establece **MF \_ Connect \_ Resolve \_ Independent \_ OUTPUTTYPES** , el cargador de topología probará una conexión directa con cada tipo de medio y, a continuación, probará cada tipo de medio con convertidores y, por último, probará cada tipo de medio con descodificadores:</span><span class="sxs-lookup"><span data-stu-id="b2d1d-131">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** but **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** is not set, the topology loader tries a direct connection with each media type, then tries each media type with converters, and finally tries each media type with decoders:</span></span>

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

<span data-ttu-id="b2d1d-132">Si \_ \_ se enumeran \_ \_ los tipos de origen de la topología MF es **false**, se omite la marca **MF \_ Connect \_ Resolve \_ Independent \_ OUTPUTTYPES** .</span><span class="sxs-lookup"><span data-stu-id="b2d1d-132">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is ignored.</span></span>

<span data-ttu-id="b2d1d-133">El valor predeterminado de MF \_ Topology \_ Enumerate \_ \_ Types de origen es **false**, por compatibilidad con las aplicaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-133">The default value of MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, for compatibility with existing applications.</span></span>

<span data-ttu-id="b2d1d-134">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-134">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="example"></a><span data-ttu-id="b2d1d-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2d1d-135">Example</span></span>

<span data-ttu-id="b2d1d-136">Este es un ejemplo en el que se muestra la marca **MF \_ Connect \_ Resolve \_ Independent \_ OUTPUTTYPES** .</span><span class="sxs-lookup"><span data-stu-id="b2d1d-136">Here is an example that illustrates the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span> <span data-ttu-id="b2d1d-137">Supongamos que la topología tiene el \_ atributo MF Topology \_ enumerar \_ \_ tipos de origen establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-137">Assume the topology has the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute set to **TRUE**.</span></span>

<span data-ttu-id="b2d1d-138">El origen de medios ofrece los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="b2d1d-138">The media source offers the following types:</span></span>

-   <span data-ttu-id="b2d1d-139">T1, T2, T3</span><span class="sxs-lookup"><span data-stu-id="b2d1d-139">T1, T2, T3</span></span>

<span data-ttu-id="b2d1d-140">El receptor de medios acepta los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="b2d1d-140">The media sink accepts the following types:</span></span>

-   <span data-ttu-id="b2d1d-141">T3, T4</span><span class="sxs-lookup"><span data-stu-id="b2d1d-141">T3, T4</span></span>

<span data-ttu-id="b2d1d-142">Caso 1: se establece la marca **MF \_ Connect \_ \_ \_ OUTPUTTYPES independiente** .</span><span class="sxs-lookup"><span data-stu-id="b2d1d-142">Case 1: The **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set.</span></span>

1.  <span data-ttu-id="b2d1d-143">El cargador de topología intenta una conexión directa con T1.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-143">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="b2d1d-144">El receptor rechaza T1.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-144">The sink rejects T1.</span></span>
2.  <span data-ttu-id="b2d1d-145">El cargador de topología inserta un descodificador que acepta T1 y salidas T4.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-145">The topology loader inserts a decoder that accepts T1 and outputs T4.</span></span> <span data-ttu-id="b2d1d-146">El receptor acepta T4.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-146">The sink accepts T4.</span></span>
3.  <span data-ttu-id="b2d1d-147">La topología final contiene: origen de medios → descodificador → receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-147">The final topology contains: media source → decoder → media sink.</span></span>

<span data-ttu-id="b2d1d-148">Caso 2: no se ha establecido la marca.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-148">Case 2: The flag is not set.</span></span>

1.  <span data-ttu-id="b2d1d-149">El cargador de topología intenta una conexión directa con T1.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-149">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="b2d1d-150">El receptor rechaza T1.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-150">The sink rejects T1.</span></span>
2.  <span data-ttu-id="b2d1d-151">El cargador de topología intenta una conexión directa con T2.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-151">The topology loader tries a direct connection with T2.</span></span> <span data-ttu-id="b2d1d-152">El receptor rechaza T2.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-152">The sink rejects T2.</span></span>
3.  <span data-ttu-id="b2d1d-153">El cargador de topología intenta una conexión directa con T3.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-153">The topology loader tries a direct connection with T3.</span></span> <span data-ttu-id="b2d1d-154">El receptor acepta T3.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-154">The sink accepts T3.</span></span>
4.  <span data-ttu-id="b2d1d-155">La topología final contiene: origen de medios → receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="b2d1d-155">The final topology contains: media source → media sink.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2d1d-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2d1d-156">Requirements</span></span>



| <span data-ttu-id="b2d1d-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2d1d-157">Requirement</span></span> | <span data-ttu-id="b2d1d-158">Value</span><span class="sxs-lookup"><span data-stu-id="b2d1d-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d1d-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2d1d-159">Minimum supported client</span></span><br/> | <span data-ttu-id="b2d1d-160">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2d1d-160">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b2d1d-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2d1d-161">Minimum supported server</span></span><br/> | <span data-ttu-id="b2d1d-162">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2d1d-162">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b2d1d-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2d1d-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2d1d-164"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2d1d-164"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2d1d-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2d1d-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d1d-166">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b2d1d-166">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2d1d-167">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="b2d1d-167">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




