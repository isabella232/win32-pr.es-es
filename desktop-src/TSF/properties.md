---
title: Propiedades (elementos comunes)
description: El marco de trabajo de servicios de texto (TSF) proporciona propiedades que asocian los metadatos a un intervalo de texto.
ms.assetid: d1d0dd99-f303-4355-9835-917de9491a0b
keywords:
- Text Services Framework (TSF), propiedades
- TSF (marco de trabajo de servicios de texto), propiedades
- servicios de texto, propiedades
- Aplicaciones habilitadas para TSF, propiedades
- properties
- Text Services Framework (TSF), tipos de propiedad
- TSF (marco de trabajo de servicios de texto), tipos de propiedad
- servicios de texto, tipos de propiedades
- Aplicaciones habilitadas para TSF, tipos de propiedades
- tipos de propiedades
- Text Services Framework (TSF), almacenamiento persistente de propiedades
- TSF (marco de trabajo de servicios de texto), almacenamiento persistente de propiedades
- servicios de texto, almacenamiento persistente de propiedades
- Aplicaciones habilitadas para TSF, almacenamiento persistente de propiedades
- almacenamiento persistente de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff852bccfb7d9b6c94e57a2fa0cf8eef6fbdf18
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105685832"
---
# <a name="properties-common-elements"></a>Propiedades (elementos comunes)

El marco de trabajo de servicios de texto (TSF) proporciona propiedades que asocian los metadatos a un intervalo de texto. Estas propiedades incluyen, entre otras, atributos que se muestran como texto en negrita, el identificador de idioma del texto y datos sin procesar proporcionados por un servicio de texto como los datos de audio asociados al texto del servicio de texto de voz.

En el ejemplo siguiente se muestra cómo se puede ver una propiedad de color de texto hipotética con valores posibles de rojo (R), verde (G) o azul (B).


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Las propiedades de distintos tipos pueden superponerse. Por ejemplo, tome el ejemplo anterior y agregue un atributo de texto que puede estar en negrita (B) o cursiva (I).


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



El texto "this" debería aparecer en negrita, "is", en negrita y en rojo, "Some" se mostraría normalmente, "color" sería verde y en cursiva y "Text" se cursiva.

Las propiedades del mismo tipo no pueden superponerse. Por ejemplo, la situación siguiente no está permitida porque "es" y "coloreado" tienen valores que se superponen de los mismos tipos.


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a>Tipos de propiedades

TSF define tres tipos diferentes de propiedades.



|                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| estática         | Un objeto de propiedad estática almacena los datos de la propiedad con texto. También almacena el intervalo de información de texto para cada intervalo al que se aplica la propiedad. ITfReadOnlyProperty:: GetType devuelve la \_ \_ categoría estática TFCAT PROPSTYLE GUID \_ .                                                                                                                                                                                                                      |
| Static-Compact | Un objeto de propiedad static-Compact es idéntico a un objeto de propiedad estático, salvo que una propiedad static-Compact no almacena datos de intervalo. Cuando se solicita el intervalo que abarca una propiedad estática-Compact, se crea un intervalo para cada grupo de propiedades adyacentes. Las propiedades estáticas-Compact son la manera más eficaz de almacenar las propiedades por carácter. ITfReadOnlyProperty:: GetType devuelve la \_ categoría GUID TFCAT \_ PROPSTYLE \_ STATICCOMPACT. |
| Personalizados         | Un objeto de propiedad personalizada almacena la información de intervalo para cada intervalo al que se aplica la propiedad. No obstante, no almacena los datos reales para la propiedad. En su lugar, una propiedad personalizada almacena un objeto ITfPropertyStore. El administrador de TSF usa este objeto para tener acceso a los datos de la propiedad y mantenerlos. ITfReadOnlyProperty:: GetType devuelve la \_ \_ categoría personalizada TFCAT PROPSTYLE de GUID \_ .                                                                    |



 

## <a name="working-with-properties"></a>Trabajar con propiedades

Los atributos y el valor de propiedad se obtienen mediante la interfaz [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) y se modifican mediante la interfaz [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) .

Si se requiere un tipo de propiedad concreto, se utiliza [ITfContext:: GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) . **ITfContext:: GetProperty** requiere un **GUID** que identifica la propiedad que se va a obtener. TSF define un conjunto de [identificadores de propiedad predefinidos](predefined-properties.md) usados o un servicio de texto puede definir sus propios identificadores de propiedad. Si se utiliza una propiedad personalizada, el proveedor de propiedades debe publicar el **GUID** de la propiedad y el formato de los datos obtenidos.

Por ejemplo, para obtener el **CLSID** para el propietario de un intervalo de texto, llame a **ITfContext:: GetProperty** para obtener el objeto de propiedad, llame a [ITfProperty:: FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) para obtener el intervalo que cubre por completo la propiedad y, después, llame a [ITfReadOnlyProperty:: GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) para obtener un [TfGuidAtom](/windows/desktop/TSF/tfguidatom) que representa el **CLSID** del servicio de texto que posee el texto. En el ejemplo siguiente se muestra una función que, dado un contexto, un intervalo y una cookie de edición, obtendrá el **CLSID** del servicio de texto que posee el texto.


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



Las propiedades también se pueden enumerar obteniendo una interfaz [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) de [ITfContext:: EnumProperties (](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).

## <a name="persistent-storage-of-properties"></a>Almacenamiento persistente de propiedades

A menudo, las propiedades son transparentes para una aplicación y se usan en uno o varios servicios de texto. Para conservar los datos de la propiedad, como cuando se guarda en un archivo, una aplicación debe serializar los datos de la propiedad cuando se almacenan y desaserializan los datos de la propiedad cuando se restauran los datos. En este caso, la aplicación no debe estar interesada en las propiedades individuales, sino que debe enumerar todas las propiedades en el contexto y almacenarlas.

Al almacenar datos de propiedades, una aplicación debe realizar los pasos siguientes.

1.  Obtenga un enumerador de propiedad llamando a **ITfContext:: EnumProperties (**.
2.  Enumere cada propiedad llamando a [IEnumTfProperties:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).
3.  Para cada propiedad, obtenga un enumerador de intervalo mediante una llamada a [ITfReadOnlyProperty:: EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).
4.  Enumere cada intervalo en la propiedad mediante una llamada a [IEnumTfRanges:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).
5.  Para cada intervalo de la propiedad, llame a [ITextStoreACPServices:: Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) con la propiedad, el intervalo, una estructura [ACP de \_ \_ \_ encabezado \_ de propiedad persistente de TF](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) y un objeto de secuencia implementado por la aplicación.
6.  Escriba el contenido de la **estructura \_ \_ ACP del \_ encabezado \_ de propiedad persistente TF** en la memoria persistente.
7.  Escriba el contenido del objeto de secuencia en la memoria persistente.
8.  Continúe con los pasos anteriores para todos los intervalos de todas las propiedades.
9.  La aplicación debe escribir algún tipo de terminiator en la secuencia para que, cuando se restauren los datos, se pueda identificar un punto de detención.


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



**ITextStoreACPServices:: Serialize**[ITfPropertyStore:: Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)

Al restaurar los datos de la propiedad, una aplicación debe realizar los pasos siguientes.

1.  Establezca el puntero de la secuencia al principio de la primera estructura **\_ ACP del \_ \_ encabezado \_ de propiedad persistente de TF** .
2.  Lea la **estructura \_ \_ ACP del \_ encabezado \_ de propiedad persistente TF** .
3.  Llame a **ITfContext:: GetProperty** con el miembro **guidType** de la estructura ACP del **\_ \_ \_ encabezado \_ de propiedad persistente TF** .
4.  En este momento, la aplicación puede realizar una de estas dos acciones.
    1.  Cree una instancia de un objeto [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) que la aplicación debe implementar. Después, llame a [ITextStoreACPServices:: unserializate](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) con **null** para *pStream* y el puntero **ITfPersistentPropertyLoaderACP** .
    2.  Pase el flujo de entrada a **ITextStoreACPServices:: unserializate** y **null** para *pLoader*.

    El primer método es preferible, ya que es el más eficaz. La implementación del segundo método hace que todos los datos de propiedad se lean de la secuencia durante la llamada a **ITextStoreACPServices:: undeserialize** . El primer método hace que los datos de la propiedad se lean a petición en otro momento.
5.  Repita los pasos anteriores hasta que se hayan deserializado todos los bloques de propiedades.


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



 

 
