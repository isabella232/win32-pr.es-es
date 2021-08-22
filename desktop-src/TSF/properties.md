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
ms.openlocfilehash: 97bb8ef470600dcb0c782ffcfde1f24071111aadd7c40ef641e4486877e2065d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118875650"
---
# <a name="properties-common-elements"></a>Propiedades (elementos comunes)

Text Services Framework (TSF) proporciona propiedades que asocian metadatos a un intervalo de texto. Estas propiedades incluyen, entre otros, atributos para mostrar, como el texto en negrita, el identificador de idioma del texto y los datos sin procesar proporcionados por un servicio de texto, como los datos de audio asociados al texto del servicio de texto de voz.

En el ejemplo siguiente se muestra cómo se puede ver una propiedad hipotética de color de texto con valores posibles de rojo (R), verde (G) o azul (B).


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Las propiedades de tipos diferentes se pueden superponer. Por ejemplo, tome el ejemplo anterior y agregue un atributo de texto que pueda ser negrita (B) o cursiva (I).


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



El texto "this" estaría en negrita, "is" sería negrita y rojo, "some" se mostraría normalmente, "coloreado" sería verde y cursiva y "text" estaría en cursiva.

Las propiedades del mismo tipo no se pueden superponer. Por ejemplo, no se permite la siguiente situación porque "is" y "colored" tienen valores superpuestos de los mismos tipos.


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a>Tipos de propiedades

TSF define tres tipos diferentes de propiedades.



|   Tipo de propiedad             |   Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| estática         | Un objeto de propiedad estático almacena los datos de propiedad con texto. También almacena el intervalo de información de texto para cada intervalo al que se aplica la propiedad . ITfReadOnlyProperty::GetType devuelve la categoría \_ GUID \_ TFCAT PROPSTYLE \_ STATIC.                                                                                                                                                                                                                      |
| Static-Compact | Un objeto de propiedad estático-compacto es idéntico a un objeto de propiedad estático, salvo que una propiedad estática compacta no almacena datos de intervalo. Cuando se solicita el intervalo cubierto por una propiedad estática-compacta, se crea un intervalo para cada grupo de propiedades adyacentes. Las propiedades estáticas compactas son la manera más eficaz de almacenar propiedades por carácter. ITfReadOnlyProperty::GetType devuelve la categoría \_ \_ GUID TFCAT PROPSTYLE \_ STATICCOMPACT. |
| Personalizado         | Un objeto de propiedad personalizado almacena la información de intervalo para cada intervalo al que se aplica la propiedad. Sin embargo, no almacena los datos reales de la propiedad . En su lugar, una propiedad personalizada almacena un objeto ITfPropertyStore. El administrador de TSF usa este objeto para tener acceso a los datos de propiedad y mantener estos. ITfReadOnlyProperty::GetType devuelve la categoría \_ GUID TFCAT \_ PROPSTYLE \_ CUSTOM.                                                                    |



 

## <a name="working-with-properties"></a>Trabajar con propiedades

El valor de propiedad y los atributos se obtienen mediante la [interfaz ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) y se modifican mediante la [interfaz ITfProperty.](/windows/desktop/api/Msctf/nn-msctf-itfproperty)

Si se requiere un tipo de propiedad específico, [se usa ITfContext::GetProperty.](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) **ITfContext::GetProperty** requiere un **GUID** que identifique la propiedad que se debe obtener. TSF define un conjunto de identificadores de propiedad [predefinidos usados](predefined-properties.md) o un servicio de texto puede definir sus propios identificadores de propiedad. Si se usa una propiedad personalizada, el proveedor de propiedades debe publicar el **GUID de** propiedad y el formato de los datos obtenidos.

Por ejemplo, para obtener el **CLSID** del propietario de un intervalo de texto, llame a **ITfContext::GetProperty** para obtener el objeto de propiedad, llame a [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) para obtener el intervalo que cubre completamente la propiedad y, a continuación, llame a [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) para obtener un [TfGuidAtom](/windows/desktop/TSF/tfguidatom) que representa el **CLSID** del servicio de texto que posee el texto. En el ejemplo siguiente se muestra una función que, dado un contexto, un intervalo y una cookie de edición, obtendrá el **CLSID** del servicio de texto que posee el texto.


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



Las propiedades también se pueden enumerar mediante la obtención de una [interfaz IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) de [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).

## <a name="persistent-storage-of-properties"></a>Propiedades Storage persistentes

A menudo, las propiedades son transparentes para una aplicación y los usan uno o varios servicios de texto. Para conservar los datos de propiedad, como cuando se guardan en un archivo, una aplicación debe serializar los datos de propiedad cuando se almacenan y deserializar los datos de propiedad cuando se restauran los datos. En este caso, la aplicación no debe estar interesada en propiedades individuales, pero debe enumerar todas las propiedades del contexto y almacenarlas.

Al almacenar datos de propiedad, una aplicación debe realizar los pasos siguientes.

1.  Obtenga un enumerador de propiedades mediante una **llamada a ITfContext::EnumProperties**.
2.  Para enumerar cada propiedad, llame a [IEnumTfProperties::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).
3.  Para cada propiedad, obtenga un enumerador de intervalo llamando a [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).
4.  Enumere cada intervalo de la propiedad llamando a [IEnumTfRanges::Next.](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next)
5.  Para cada intervalo de la propiedad , llame a [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) con la propiedad , el intervalo, una estructura [TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) y un objeto de secuencia implementado por la aplicación.
6.  Escriba el contenido de la estructura **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP** en memoria persistente.
7.  Escriba el contenido del objeto de secuencia en memoria persistente.
8.  Continúe con los pasos anteriores para todos los intervalos de todas las propiedades.
9.  La aplicación debe escribir algún tipo deator en la secuencia para que, cuando se restauran los datos, se pueda identificar un punto de detención.


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



**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)

Al restaurar los datos de propiedad, una aplicación debe realizar los pasos siguientes.

1.  Establezca el puntero de secuencia en el inicio de la primera **estructura TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP.**
2.  Lea la **estructura TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP.**
3.  Llame **a ITfContext::GetProperty con** el miembro **guidType** de la estructura **TF PERSISTENT PROPERTY HEADER \_ \_ \_ \_ ACP.**
4.  La aplicación puede hacer una de estas dos cosas en este momento.
    1.  Cree una instancia de un [objeto ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) que la aplicación debe implementar. A [continuación, llame a ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) con **NULL** para *pStream* y el **puntero ITfPersistentPropertyLoaderACP.**
    2.  Pase el flujo de entrada **a ITextStoreACPServices::Unserialize** y **NULL** para *pLoader.*

    Se prefiere el primer método, ya que es el más eficaz. La implementación del segundo método hace que todos los datos de propiedad se lean de la secuencia durante la **llamada a ITextStoreACPServices::Unserialize.** El primer método hace que los datos de propiedad se lean a petición más adelante.
5.  Repita los pasos anteriores hasta que se deserialicen todos los bloques de propiedades.


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



 

 
