---
title: Propiedades (elementos comunes)
description: Text Services Framework (TSF) proporciona propiedades que asocian metadatos a un intervalo de texto.
ms.assetid: d1d0dd99-f303-4355-9835-917de9491a0b
keywords:
- Text Services Framework (TSF),properties
- TSF (Text Services Framework),properties
- text services,properties
- Aplicaciones habilitadas para TSF, propiedades
- properties
- Text Services Framework (TSF),tipos de propiedad
- TSF (Text Services Framework),tipos de propiedad
- servicios de texto, tipos de propiedad
- Aplicaciones habilitadas para TSF, tipos de propiedad
- tipos de propiedades
- Text Services Framework (TSF), almacenamiento persistente de propiedades
- TSF (Text Services Framework), almacenamiento persistente de propiedades
- servicios de texto, almacenamiento persistente de propiedades
- Aplicaciones habilitadas para TSF, almacenamiento persistente de propiedades
- almacenamiento persistente de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b94a1f6c504fcd3e6491af9e66b399d59a3eeb
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524219"
---
# <a name="properties-common-elements"></a><span data-ttu-id="532fb-118">Propiedades (elementos comunes)</span><span class="sxs-lookup"><span data-stu-id="532fb-118">Properties (Common Elements)</span></span>

<span data-ttu-id="532fb-119">Text Services Framework (TSF) proporciona propiedades que asocian metadatos a un intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="532fb-119">Text Services Framework (TSF) provides properties that associate metadata with a range of text.</span></span> <span data-ttu-id="532fb-120">Estas propiedades incluyen, entre otros, atributos para mostrar, como el texto en negrita, el identificador de idioma del texto y los datos sin procesar proporcionados por un servicio de texto, como los datos de audio asociados al texto del servicio de texto de voz.</span><span class="sxs-lookup"><span data-stu-id="532fb-120">These properties include, but are not limited to, display attributes such as bold text, the language identifier of the text, and raw data provided by a text service such as the audio data associated with text from the speech text service.</span></span>

<span data-ttu-id="532fb-121">En el ejemplo siguiente se muestra cómo se puede ver una propiedad hipotética de color de texto con valores posibles de rojo (R), verde (G) o azul (B).</span><span class="sxs-lookup"><span data-stu-id="532fb-121">The following example demonstrates how a hypothetical text color property with possible values of red (R), green (G), or blue (B) can be viewed.</span></span>


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="532fb-122">Las propiedades de tipos diferentes se pueden superponer.</span><span class="sxs-lookup"><span data-stu-id="532fb-122">Properties of different types can overlap.</span></span> <span data-ttu-id="532fb-123">Por ejemplo, tome el ejemplo anterior y agregue un atributo de texto que pueda ser negrita (B) o cursiva (I).</span><span class="sxs-lookup"><span data-stu-id="532fb-123">For example, take the previous example and add a text attribute that can be either bold (B) or italic (I).</span></span>


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="532fb-124">El texto "this" estaría en negrita, "is" sería negrita y rojo, "some" se mostraría normalmente, "coloreado" sería verde y cursiva y "text" estaría en cursiva.</span><span class="sxs-lookup"><span data-stu-id="532fb-124">The text "this" would be bold, "is" would be both bold and red, "some" would be displayed normally, "colored" would be green and italicized and "text" would be italicized.</span></span>

<span data-ttu-id="532fb-125">Las propiedades del mismo tipo no se pueden superponer.</span><span class="sxs-lookup"><span data-stu-id="532fb-125">Properties of the same type cannot overlap.</span></span> <span data-ttu-id="532fb-126">Por ejemplo, no se permite la siguiente situación porque "is" y "colored" tienen valores superpuestos de los mismos tipos.</span><span class="sxs-lookup"><span data-stu-id="532fb-126">For example, the following situation is not allowed because "is" and "colored" have overlapping values of the same types.</span></span>


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a><span data-ttu-id="532fb-127">Tipos de propiedades</span><span class="sxs-lookup"><span data-stu-id="532fb-127">Property Types</span></span>

<span data-ttu-id="532fb-128">TSF define tres tipos diferentes de propiedades.</span><span class="sxs-lookup"><span data-stu-id="532fb-128">TSF defines three different types of properties.</span></span>



|   <span data-ttu-id="532fb-129">Tipo de propiedad</span><span class="sxs-lookup"><span data-stu-id="532fb-129">Property type</span></span>             |   <span data-ttu-id="532fb-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="532fb-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="532fb-131">estática</span><span class="sxs-lookup"><span data-stu-id="532fb-131">Static</span></span>         | <span data-ttu-id="532fb-132">Un objeto de propiedad estático almacena los datos de propiedad con texto.</span><span class="sxs-lookup"><span data-stu-id="532fb-132">A static property object stores the property data with text.</span></span> <span data-ttu-id="532fb-133">También almacena el intervalo de información de texto para cada intervalo al que se aplica la propiedad .</span><span class="sxs-lookup"><span data-stu-id="532fb-133">It also stores the range of text information for each range that the property applies to.</span></span> <span data-ttu-id="532fb-134">ITfReadOnlyProperty::GetType devuelve la categoría \_ GUID \_ TFCAT PROPSTYLE \_ STATIC.</span><span class="sxs-lookup"><span data-stu-id="532fb-134">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATIC category.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="532fb-135">Static-Compact</span><span class="sxs-lookup"><span data-stu-id="532fb-135">Static-Compact</span></span> | <span data-ttu-id="532fb-136">Un objeto de propiedad estático-compacto es idéntico a un objeto de propiedad estático, salvo que una propiedad estática compacta no almacena datos de intervalo.</span><span class="sxs-lookup"><span data-stu-id="532fb-136">A static-compact property object is identical to a static property object except a static-compact property does not store range data.</span></span> <span data-ttu-id="532fb-137">Cuando se solicita el intervalo cubierto por una propiedad estática-compacta, se crea un intervalo para cada grupo de propiedades adyacentes.</span><span class="sxs-lookup"><span data-stu-id="532fb-137">When the range covered by a static-compact property is requested, a range is created for each group of adjacent properties.</span></span> <span data-ttu-id="532fb-138">Las propiedades estáticas compactas son la manera más eficaz de almacenar propiedades por carácter.</span><span class="sxs-lookup"><span data-stu-id="532fb-138">Static-compact properties are the most efficient way to store properties on a per-character basis.</span></span> <span data-ttu-id="532fb-139">ITfReadOnlyProperty::GetType devuelve la categoría \_ \_ GUID TFCAT PROPSTYLE \_ STATICCOMPACT.</span><span class="sxs-lookup"><span data-stu-id="532fb-139">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATICCOMPACT category.</span></span> |
| <span data-ttu-id="532fb-140">Personalizado</span><span class="sxs-lookup"><span data-stu-id="532fb-140">Custom</span></span>         | <span data-ttu-id="532fb-141">Un objeto de propiedad personalizado almacena la información de intervalo para cada intervalo al que se aplica la propiedad.</span><span class="sxs-lookup"><span data-stu-id="532fb-141">A custom property object stores the range information for each range that the property applies to.</span></span> <span data-ttu-id="532fb-142">Sin embargo, no almacena los datos reales de la propiedad .</span><span class="sxs-lookup"><span data-stu-id="532fb-142">It does not, however, store the actual data for the property.</span></span> <span data-ttu-id="532fb-143">En su lugar, una propiedad personalizada almacena un objeto ITfPropertyStore.</span><span class="sxs-lookup"><span data-stu-id="532fb-143">Instead, a custom property stores an ITfPropertyStore object.</span></span> <span data-ttu-id="532fb-144">El administrador de TSF usa este objeto para tener acceso a los datos de propiedad y mantener estos. ITfReadOnlyProperty::GetType devuelve la categoría \_ GUID TFCAT \_ PROPSTYLE \_ CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="532fb-144">The TSF manager uses this object to access and maintain the property data.ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_CUSTOM category.</span></span>                                                                    |



 

## <a name="working-with-properties"></a><span data-ttu-id="532fb-145">Trabajar con propiedades</span><span class="sxs-lookup"><span data-stu-id="532fb-145">Working with Properties</span></span>

<span data-ttu-id="532fb-146">El valor de propiedad y los atributos se obtienen mediante la [interfaz ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) y se modifican mediante la [interfaz ITfProperty.](/windows/desktop/api/Msctf/nn-msctf-itfproperty)</span><span class="sxs-lookup"><span data-stu-id="532fb-146">The property value and attributes are obtained using the [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) interface and modified using the [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) interface.</span></span>

<span data-ttu-id="532fb-147">Si se requiere un tipo de propiedad específico, [se usa ITfContext::GetProperty.](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty)</span><span class="sxs-lookup"><span data-stu-id="532fb-147">If a specific property type is required, then [ITfContext::GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) is used.</span></span> <span data-ttu-id="532fb-148">**ITfContext::GetProperty** requiere un **GUID** que identifique la propiedad que se debe obtener.</span><span class="sxs-lookup"><span data-stu-id="532fb-148">**ITfContext::GetProperty** requires a **GUID** that identifies the property to obtain.</span></span> <span data-ttu-id="532fb-149">TSF define un conjunto de identificadores de propiedad [predefinidos usados](predefined-properties.md) o un servicio de texto puede definir sus propios identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="532fb-149">TSF defines a set of [predefined property identifiers](predefined-properties.md) used or a text service can define its own property identifiers.</span></span> <span data-ttu-id="532fb-150">Si se usa una propiedad personalizada, el proveedor de propiedades debe publicar el **GUID de** propiedad y el formato de los datos obtenidos.</span><span class="sxs-lookup"><span data-stu-id="532fb-150">If a custom property is used, the property provider must publish the property **GUID** and the format of the data obtained.</span></span>

<span data-ttu-id="532fb-151">Por ejemplo, para obtener el **CLSID** para el propietario de un intervalo de texto, llame a **ITfContext::GetProperty** para obtener el objeto de propiedad, llame a [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) para obtener el intervalo que cubre completamente la propiedad y, a continuación, llame a [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) para obtener un [TfGuidAtom](/windows/desktop/TSF/tfguidatom) que representa el **CLSID** del servicio de texto que posee el texto.</span><span class="sxs-lookup"><span data-stu-id="532fb-151">For example, to obtain the **CLSID** for the owner of a range of text, call **ITfContext::GetProperty** to obtain the property object, call [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) to obtain the range that entirely covers the property, then call [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) to get a [TfGuidAtom](/windows/desktop/TSF/tfguidatom) that represents the **CLSID** of the text service that owns the text.</span></span> <span data-ttu-id="532fb-152">En el ejemplo siguiente se muestra una función que, dado un contexto, un intervalo y una cookie de edición, obtendrá el **CLSID** del servicio de texto que posee el texto.</span><span class="sxs-lookup"><span data-stu-id="532fb-152">The following example shows a function that, given a context, range and an edit cookie, will obtain the **CLSID** of the text service that owns the text.</span></span>


```C++
HRESULT GetTextOwner(   ITfContext *pContext, 
                        ITfRange *pRange, 
                        TfEditCookie ec, 
                        CLSID *pclsidOwner)
{
    HRESULT     hr;
    ITfProperty *pProp;

    *pclsidOwner = GUID_NULL;

    hr = pContext->GetProperty(GUID_PROP_TEXTOWNER, &pProp);
    if(S_OK == hr)
    {
        ITfRange    *pPropRange;

        hr = pProp->FindRange(ec, pRange, &pPropRange, TF_ANCHOR_START);
        if(S_OK == hr)
        {
            VARIANT var;

            VariantInit(&var);
            hr = pProp->GetValue(ec, pPropRange, &var);
            if(S_OK == hr)
            {
                if(VT_I4 == var.vt)
                {
                    /*
                    var.lVal is a TfGuidAtom that represents the CLSID of the 
                    text owner. Use ITfCategoryMgr to obtain the CLSID from 
                    the TfGuidAtom.
                    */
                    ITfCategoryMgr  *pCatMgr;

                    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                                            NULL, 
                                            CLSCTX_INPROC_SERVER, 
                                            IID_ITfCategoryMgr, 
                                            (LPVOID*)&pCatMgr);
                    if(SUCCEEDED(hr))
                    {
                        hr = pCatMgr->GetGUID((TfGuidAtom)var.lVal, pclsidOwner);
                        if(SUCCEEDED(hr))
                        {
                            /*
                            *pclsidOwner now contains the CLSID of the text 
                            service that owns the text at the selection.
                            */
                        }

                        pCatMgr->Release();
                    }
                }
                else
                {
                    //Unrecognized VARIANT type 
                    hr = E_FAIL;
                }
                
                VariantClear(&var);
            }
            
            pPropRange->Release();
        }
        
        pProp->Release();
    }

    return hr;
}

```



<span data-ttu-id="532fb-153">Las propiedades también se pueden enumerar mediante la obtención de una [interfaz IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) de [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span><span class="sxs-lookup"><span data-stu-id="532fb-153">Properties can also be enumerated by obtaining an [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) interface from [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span></span>

## <a name="persistent-storage-of-properties"></a><span data-ttu-id="532fb-154">Almacenamiento persistente de propiedades</span><span class="sxs-lookup"><span data-stu-id="532fb-154">Persistent Storage of Properties</span></span>

<span data-ttu-id="532fb-155">A menudo, las propiedades son transparentes para una aplicación y los usan uno o varios servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="532fb-155">Often, properties are transparent to an application and are used by one or more text services.</span></span> <span data-ttu-id="532fb-156">Para conservar los datos de propiedad, como cuando se guardan en un archivo, una aplicación debe serializar los datos de propiedad cuando se almacenan y deserializar los datos de propiedad cuando se restauran.</span><span class="sxs-lookup"><span data-stu-id="532fb-156">In order to preserve the property data, such as when saving to a file, an application must serialize the property data when it is stored and unserialize the property data when the data is restored.</span></span> <span data-ttu-id="532fb-157">En este caso, la aplicación no debe estar interesada en propiedades individuales, pero debe enumerar todas las propiedades del contexto y almacenarlas.</span><span class="sxs-lookup"><span data-stu-id="532fb-157">In this case, the application should not be interested in individual properties, but should enumerate all properties in the context and store them.</span></span>

<span data-ttu-id="532fb-158">Al almacenar datos de propiedad, una aplicación debe realizar los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="532fb-158">When storing property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="532fb-159">Obtenga un enumerador de propiedades mediante una **llamada a ITfContext::EnumProperties**.</span><span class="sxs-lookup"><span data-stu-id="532fb-159">Obtain a property enumerator by calling **ITfContext::EnumProperties**.</span></span>
2.  <span data-ttu-id="532fb-160">Para enumerar cada propiedad, llame a [IEnumTfProperties::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span><span class="sxs-lookup"><span data-stu-id="532fb-160">Enumerate each property by calling [IEnumTfProperties::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span></span>
3.  <span data-ttu-id="532fb-161">Para cada propiedad, obtenga un enumerador de intervalo llamando a [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span><span class="sxs-lookup"><span data-stu-id="532fb-161">For each property, obtain a range enumerator by calling [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span></span>
4.  <span data-ttu-id="532fb-162">Para enumerar cada intervalo de la propiedad , llame a [IEnumTfRanges::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span><span class="sxs-lookup"><span data-stu-id="532fb-162">Enumerate each range in the property by calling [IEnumTfRanges::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span></span>
5.  <span data-ttu-id="532fb-163">Para cada intervalo de la propiedad , llame a [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) con la propiedad , el intervalo, una estructura [TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) y un objeto de secuencia implementado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="532fb-163">For each range in the property, call [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) with the property, range, a [TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) structure, and a stream object implemented by the application.</span></span>
6.  <span data-ttu-id="532fb-164">Escriba el contenido de la estructura **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP** en memoria persistente.</span><span class="sxs-lookup"><span data-stu-id="532fb-164">Write the contents of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure into persistent memory.</span></span>
7.  <span data-ttu-id="532fb-165">Escriba el contenido del objeto de secuencia en memoria persistente.</span><span class="sxs-lookup"><span data-stu-id="532fb-165">Write the contents of the stream object into persistent memory.</span></span>
8.  <span data-ttu-id="532fb-166">Continúe con los pasos anteriores para todos los intervalos de todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="532fb-166">Continue the previous steps for all of the ranges in all of the properties.</span></span>
9.  <span data-ttu-id="532fb-167">La aplicación debe escribir algún tipo deator en la secuencia para que, cuando se restauran los datos, se pueda identificar un punto de detención.</span><span class="sxs-lookup"><span data-stu-id="532fb-167">The application should write some type of terminiator into the stream so that, when the data is restored, a stopping point can be identified.</span></span>


```C++
HRESULT SaveProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        TfEditCookie ec, 
                        IStream *pStream)
{
    HRESULT             hr;
    IEnumTfProperties   *pEnumProps;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;
    ULONG uWritten;
    
    //Enumerate the properties in the context. 
    hr = pContext->EnumProperties(&pEnumProps);
    if(SUCCEEDED(hr))
    {
        ITfProperty *pProp;
        ULONG       uFetched;

        while(SUCCEEDED(pEnumProps->Next(1, &pProp, &uFetched)) && uFetched)
        {
            //Enumerate all the ranges that contain the property. 
            IEnumTfRanges   *pEnumRanges;
            hr = pProp->EnumRanges(ec, &pEnumRanges, NULL);
            if(SUCCEEDED(hr))
            {
                IStream *pTempStream;

                //Create a temporary stream to write the property data to. 
                hr = CreateStreamOnHGlobal(NULL, TRUE, &pTempStream);
                if(SUCCEEDED(hr))
                {
                    ITfRange    *pRange;

                    while(SUCCEEDED(pEnumRanges->Next(1, &pRange, &uFetched)) && uFetched)
                    {
                        LARGE_INTEGER li;

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);
                        
                        //Get the property header and data for the range. 
                        hr = pServices->Serialize(pProp, pRange, &PropHeader, pTempStream);

                        /*
                        Write the property header into the primary stream. 
                        The header also contains the size of the property 
                        data.
                        */
                        hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);

                        //Copy the property data from the temporary stream into the primary stream. 
                        ULARGE_INTEGER  uli;
                        uli.QuadPart = PropHeader.cb;

                        hr = pTempStream->CopyTo(pStream, uli, NULL, NULL);

                        pRange->Release();
                    }
                    
                    pTempStream->Release();
                }
                
                pEnumRanges->Release();
            }
            
            pProp->Release();
        }
        
        pEnumProps->Release();
    }

    //Write a property header with zero size and guid into the stream as a terminator 
    ZeroMemory(&PropHeader, sizeof(PropHeader));
    hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

    return hr;
}

```



<span data-ttu-id="532fb-168">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span><span class="sxs-lookup"><span data-stu-id="532fb-168">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span></span>

<span data-ttu-id="532fb-169">Al restaurar los datos de propiedad, una aplicación debe realizar los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="532fb-169">When restoring property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="532fb-170">Establezca el puntero de secuencia en el inicio de la primera **estructura TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP.**</span><span class="sxs-lookup"><span data-stu-id="532fb-170">Set the stream pointer to the start of the first **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
2.  <span data-ttu-id="532fb-171">Lea la **estructura TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP.**</span><span class="sxs-lookup"><span data-stu-id="532fb-171">Read the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
3.  <span data-ttu-id="532fb-172">Llame **a ITfContext::GetProperty con** el miembro **guidType** de la estructura **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP.**</span><span class="sxs-lookup"><span data-stu-id="532fb-172">Call **ITfContext::GetProperty** with the **guidType** member of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
4.  <span data-ttu-id="532fb-173">La aplicación puede hacer una de estas dos cosas en este momento.</span><span class="sxs-lookup"><span data-stu-id="532fb-173">The application can do one of two things at this point.</span></span>
    1.  <span data-ttu-id="532fb-174">Cree una instancia de un [objeto ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) que la aplicación debe implementar.</span><span class="sxs-lookup"><span data-stu-id="532fb-174">Create an instance of an [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) object that the application must implement.</span></span> <span data-ttu-id="532fb-175">A [continuación, llame a ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) con **NULL** para *pStream* y el **puntero ITfPersistentPropertyLoaderACP.**</span><span class="sxs-lookup"><span data-stu-id="532fb-175">Then call [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) with **NULL** for *pStream* and the **ITfPersistentPropertyLoaderACP** pointer.</span></span>
    2.  <span data-ttu-id="532fb-176">Pase el flujo de entrada **a ITextStoreACPServices::Unserialize** y **NULL** para *pLoader.*</span><span class="sxs-lookup"><span data-stu-id="532fb-176">Pass the input stream to **ITextStoreACPServices::Unserialize** and **NULL** for *pLoader*.</span></span>

    <span data-ttu-id="532fb-177">Se prefiere el primer método, ya que es el más eficaz.</span><span class="sxs-lookup"><span data-stu-id="532fb-177">The first method is preferred as it is the most efficient.</span></span> <span data-ttu-id="532fb-178">La implementación del segundo método hace que todos los datos de propiedad se lean de la secuencia durante la **llamada a ITextStoreACPServices::Unserialize.**</span><span class="sxs-lookup"><span data-stu-id="532fb-178">Implementing the second method causes all of the property data to be read from the stream during the **ITextStoreACPServices::Unserialize** call.</span></span> <span data-ttu-id="532fb-179">El primer método hace que los datos de propiedad se lean a petición más adelante.</span><span class="sxs-lookup"><span data-stu-id="532fb-179">The first method causes the property data to be read on demand at a later time.</span></span>
5.  <span data-ttu-id="532fb-180">Repita los pasos anteriores hasta que se deserialicen todos los bloques de propiedades.</span><span class="sxs-lookup"><span data-stu-id="532fb-180">Repeat the previous steps until all property blocks are unserialized.</span></span>


```C++
HRESULT LoadProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        IStream *pStream)
{
    HRESULT hr;
    ULONG   uRead;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;

    /*
    Read each property header and property data from the stream. The 
    list of properties is terminated by a TF_PERSISTENT_PROPERTY_HEADER_ACP 
    structure with a cb member of zero.
    */
    hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    while(  SUCCEEDED(hr) && 
            (sizeof(PropHeader) == uRead) && 
            (0 != PropHeader.cb))
    {
        ITfProperty *pProp;

        hr = pContext->GetProperty(PropHeader.guidType, &pProp);
        if(SUCCEEDED(hr))
        {
            /*
            Have TSF read the property data from the stream. This call 
            requests a read-only lock, so be sure it can be granted 
            or else this method will fail.
            */
            CTSFPersistentPropertyLoader *pLoader = new CTSFPersistentPropertyLoader(&PropHeader, pStream);
            hr = pServices->Unserialize(pProp, &PropHeader, NULL, pLoader);

            pProp->Release();
        }

        //Read the next header. 
        hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    }

    return hr;
}

```



 

 
