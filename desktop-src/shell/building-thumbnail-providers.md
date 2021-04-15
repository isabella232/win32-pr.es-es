---
description: A partir de Windows Vista, se usa un mayor uso de imágenes en miniatura específicas del archivo que en versiones anteriores de Windows.
title: Crear controladores de miniaturas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 218264a9-ed26-4049-a721-232943f6ec53
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05e13f24a2f4d70a58bab904150b1e488f74854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984355"
---
# <a name="building-thumbnail-handlers"></a>Crear controladores de miniaturas

A partir de Windows Vista, se usa un mayor uso de imágenes en miniatura específicas del archivo que en versiones anteriores de Windows. Se usan en todas las vistas, en los cuadros de diálogo y para cualquier tipo de archivo que las proporcione. También se ha cambiado la presentación en miniatura. Hay disponible un espectro continuo de tamaños seleccionables por el usuario en lugar de los tamaños discretos, como iconos y miniaturas.

La interfaz [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) facilita una miniatura más sencilla que la anterior [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) o [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2). Sin embargo, tenga en cuenta que el código existente que usa **IExtractImage** o **IExtractImage2** sigue siendo válido y es compatible.

## <a name="the-recipethumbnailprovider-sample"></a>El ejemplo RecipeThumbnailProvider

El ejemplo [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) que se disecciona en esta sección se incluye en el kit de desarrollo de software (SDK) de Windows. La ubicación de instalación predeterminada es C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ Shell \\ AppShellIntegration \\ RecipeThumbnailProvider. Sin embargo, la mayor parte del código también se incluye aquí.

En el ejemplo [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) se muestra la implementación de un controlador de miniaturas para un nuevo tipo de archivo registrado con una extensión. Recipe. En el ejemplo se muestra el uso de las distintas API de controlador de miniaturas para registrar los servidores del modelo de objetos componentes (COM) de extracción en miniatura para tipos de archivo personalizados. Este tema le guía a través del código de ejemplo, resaltando las opciones de codificación y las instrucciones.

Un controlador de miniaturas siempre debe implementar [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) junto con una de estas interfaces:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

Hay casos en los que no es posible la inicialización con secuencias. En escenarios en los que el controlador de miniaturas no implementa [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), debe dejar de ejecutarse en el proceso aislado, donde el indexador del sistema lo coloca de forma predeterminada cuando se produce un cambio en la secuencia. Para no participar en la característica de aislamiento de procesos, establezca el siguiente valor del registro.

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

Si implementa [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) y realiza una inicialización basada en secuencias, el controlador es más seguro y confiable. Normalmente, deshabilitar el aislamiento de procesos solo está pensado para los controladores heredados; Evite deshabilitar esta característica para cualquier código nuevo. **IInitializeWithStream** debe ser la primera opción de la interfaz de inicialización siempre que sea posible.

Dado que el archivo de imagen en el ejemplo no está incrustado en el archivo. receta y no forma parte de su secuencia de archivos, se usa [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) en el ejemplo. La implementación del método [**IInitializeWithItem:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) simplemente pasa sus parámetros a las variables de clase privada.

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) tiene solo un método,[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail), al que se llama con el mayor tamaño deseado de la imagen, en píxeles. Aunque el parámetro se denomina *CX*, su valor se utiliza como el tamaño máximo de las dimensiones x e y de la imagen. Si la miniatura recuperada no es cuadrada, el eje más largo está limitado por *CX* y se conserva la relación de aspecto de la imagen original.

Cuando devuelve, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) proporciona un identificador a la imagen recuperada. También proporciona un valor que indica el formato de color de la imagen y si tiene información alfa válida.

La implementación de GetThumbnail en el ejemplo comienza con una llamada al método privado **\_ GetBase64EncodedImageString** .


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



El tipo de archivo. Recipe es simplemente un archivo XML registrado como una extensión de nombre de archivo única. Incluye un elemento denominado **imagen** que proporciona la ruta de acceso relativa y el nombre de archivo de la imagen que se va a usar como miniatura para este archivo. receta determinado. El elemento de **imagen** está formado por el atributo de **origen** que especifica una imagen codificada en base 64 y un atributo de **tamaño** opcional.

**El tamaño** tiene dos valores: pequeño y grande. Esto le permite proporcionar varios nodos de **imagen** con imágenes independientes. La imagen recuperada depende del valor de tamaño máximo (*CX*) proporcionado en la llamada a [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail). Dado que Windows nunca cambia el tamaño de la imagen a un tamaño mayor que el tamaño máximo, se pueden proporcionar diferentes imágenes para diferentes resoluciones. Sin embargo, para simplificar, el ejemplo omite el atributo de **tamaño** y proporciona una sola imagen para todas las situaciones.

El método **\_ GetBase64EncodedImageString** , cuya implementación se muestra aquí, usa las API de Document Object Model XML (dom) para recuperar el nodo de **imagen** . Desde ese nodo, extrae la imagen de los datos del atributo de **origen** .


```C++
HRESULT CRecipeThumbProvider::_GetBase64EncodedImageString(UINT /* cx */, 
                                                           PWSTR *ppszResult)
{
    *ppszResult = NULL;

    IXMLDOMDocument *pXMLDoc;
    HRESULT hr = _LoadXMLDocument(&pXMLDoc);
    if (SUCCEEDED(hr))
    {
        BSTR bstrQuery = SysAllocString(L"Recipe/Attachments/Picture");
        hr = bstrQuery ? S_OK : E_OUTOFMEMORY;
        if (SUCCEEDED(hr))
        {
            IXMLDOMNode *pXMLNode;
            hr = pXMLDoc->selectSingleNode(bstrQuery, &pXMLNode);
            if (SUCCEEDED(hr))
            {
                IXMLDOMElement *pXMLElement;
                hr = pXMLNode->QueryInterface(&pXMLElement);
                if (SUCCEEDED(hr))
                {
                    BSTR bstrAttribute = SysAllocString(L"Source");
                    hr = bstrAttribute ? S_OK : E_OUTOFMEMORY;
                    if (SUCCEEDED(hr))
                    {
                        VARIANT varValue;
                        hr = pXMLElement->getAttribute(bstrAttribute, &varValue);
                        if (SUCCEEDED(hr))
                        {
                            if ((varValue.vt == VT_BSTR) && varValue.bstrVal && varValue.bstrVal[0])
                            {
                                hr = SHStrDupW(varValue.bstrVal, ppszResult);
                            }
                            else
                            {
                                hr = E_FAIL;
                            }
                            VariantClear(&varValue);
                        }
                        SysFreeString(bstrAttribute);
                    }
                    pXMLElement->Release();
                }
                pXMLNode->Release();
            }
            SysFreeString(bstrQuery);
        }
        pXMLDoc->Release();
    }
    return hr;
}
```



A continuación, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) pasa la cadena recuperada a **\_ GetStreamFromString**.


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
```



El método **\_ GetStreamFromString** , cuya implementación se muestra aquí, que convierte la imagen codificada en una secuencia.


```C++
HRESULT CRecipeThumbProvider::_GetStreamFromString(PCWSTR pszImageName, 
                                                   IStream **ppImageStream)
{
    HRESULT hr = E_FAIL;

    DWORD dwDecodedImageSize = 0;
    DWORD dwSkipChars        = 0;
    DWORD dwActualFormat     = 0;

    // Base64-decode the string
    BOOL fSuccess = CryptStringToBinaryW(pszImageName, 
                                         NULL, 
                                         CRYPT_STRING_BASE64,
                                         NULL, 
                                         &dwDecodedImageSize, 
                                         &dwSkipChars, 
                                         &dwActualFormat);
    if (fSuccess)
    {
        BYTE *pbDecodedImage = (BYTE*)LocalAlloc(LPTR, dwDecodedImageSize);
        if (pbDecodedImage)
        {
            fSuccess = CryptStringToBinaryW(pszImageName, 
                                            lstrlenW(pszImageName), 
                                            CRYPT_STRING_BASE64,
                                            pbDecodedImage, 
                                            &dwDecodedImageSize, 
                                            &dwSkipChars, 
                                            &dwActualFormat);
            if (fSuccess)
            {
                *ppImageStream = SHCreateMemStream(pbDecodedImage, 
                                                   dwDecodedImageSize);
                if (*ppImageStream != NULL)
                {
                    hr = S_OK;
                }
            }
            LocalFree(pbDecodedImage);
        }
    }
    return hr;
}
```



A continuación, **GetThumbnail** usa las API de Windows Imaging Component (WIC) para extraer un mapa de bits de la secuencia y obtener un identificador para dicho mapa de bits. La información alfa está establecida, WIC está correctamente cerrado y el método finaliza correctamente.


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
        if (SUCCEEDED(hr))
        {
            hr = WICCreate32BitsPerPixelHBITMAP(pImageStream, 
                                                cx, 
                                                phbmp, 
                                                pdwAlpha);;

            pImageStream->Release();
        }
        CoTaskMemFree(pszBase64EncodedImageString);
    }
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores en miniatura](thumbnail-providers.md)
</dt> <dt>

[Instrucciones de controlador de miniaturas](thumbnail-provider-guidelines.md)
</dt> <dt>

[**IID \_ PPV \_ args**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
