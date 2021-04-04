---
description: Determina las subregiones de una imagen que se distribuyen en la placa de plano, de modo que cada una de las subregiones pueda adquirirse en un elemento de imagen independiente.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: IWiaSegmentationFilter::D método etectRegions (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 94fe2f5076e9ff7cc0de0f7c916f6edacf2d03fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154395"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a>IWiaSegmentationFilter::D método etectRegions

Determina las subregiones de una imagen que se distribuyen en la placa de plano, de modo que cada una de las subregiones pueda adquirirse en un elemento de imagen independiente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*pInputStream* \[ de\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

Especifica un puntero a la imagen de vista previa de [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> <dt>

_pWiaItem2 * \[ en\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Especifica un puntero al elemento [_ *IWiaItem2* *](-wia-iwiaitem2.md) para el que se adquirió *pInputStream* . El filtro segmentación crea elementos secundarios para este elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método determina las subregiones de la imagen representada por pInputStream. Para cada subregión detectada, se crea un elemento secundario para el elemento [**IWiaItem2**](-wia-iwiaitem2.md) especificado en el parámetro *pWiaItem2* . Para cada elemento secundario, el filtro de segmentación debe establecer valores para el rectángulo delimitador del área que se va a examinar, mediante las siguientes [**constantes de propiedades de elemento WIA de escáner**](-wia-wiaitempropscanneritem.md).

-   [**IP de WIA ( \_ \_ XPOS)**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IP \_ YPOS**](-wia-wiaitempropscanneritem.md)
-   [**\_XEXTENT de IP WIA \_**](-wia-wiaitempropscanneritem.md)
-   [**\_YEXTENT de IP WIA \_**](-wia-wiaitempropscanneritem.md)

Un filtro más avanzado también puede requerir otras [**constantes de propiedad del elemento WIA del escáner**](-wia-wiaitempropscanneritem.md) , como la desfragmentación de las direcciones **IP de WIA \_ \_ \_ X** y **WIA, \_ \_ dessesgado \_ y**, si el controlador admite la anulación del sesgo.

Si la aplicación llama a **IWiaSegmentationFilter::D etectregions** más de una vez, la aplicación debe eliminar primero los elementos secundarios creados por la última llamada a **IWiaSegmentationFilter::D etectregions**.

Si una aplicación cambia cualquier propiedad en *pWiaItem2*, entre la adquisición de la imagen en *pInputStream* y su llamada a **IWiaSegmentationFilter::D etectregions**, se deben restaurar las propiedades originales (es decir, las propiedades que tenía el elemento cuando se adquirió la secuencia). Esto puede realizarse mediante [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) y [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).

La aplicación debe restablecer la [IStream](/windows/win32/api/objidl/nn-objidl-istream) si su llamada pasa el mismo flujo al filtro de segmentación más de una vez. La aplicación también debe restablecer la secuencia después de la descarga inicial y antes de llamar a **IWiaSegmentationFilter::D etectregions**.

## <a name="examples"></a>Ejemplos

La segmentación realiza la detección de regiones en la secuencia ( `pImageStream` ) que se pasa a DetectSubregions. Vea el método [**getExtension**](-wia-iwiaitem2-getextension.md) para CreateSegmentationFilter que se usa en este ejemplo.


```C++
HRESULT
DetectSubregions(
   IN IStream   *pImageStream,
   IN IWiaItem2 *pWiaItem2)
{
   HRESULT                 hr                  = S_OK;
   IWiaSegmentationFilter* pSegmentationFilter = NULL;

   if (!pWiaItem2 || !pImageStream)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      hr = CreateSegmentationFilter(pWiaItem2, &pSegmentationFilter);
   }

   if (SUCCEEDED(hr))
   {
      hr = pSegmentationFilter->DetectRegions(0,pImageStream, pWiaItem2); 
   }

   if (pSegmentationFilter)
   {
      pSegmentationFilter->Release();
      pSegmentationFilter = NULL;
   }

   return hr;
}
```



DownloadPreviewImage descarga los datos de imagen del escáner llamando al método [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) del componente de vista previa. A continuación, llama a DetectSubregions si el usuario de la aplicación desea invocar el filtro de segmentación, que crea un elemento secundario en pWiaItem2 para cada región que detecta. Vea **IWiaSegmentationFilter::D etectregions** para el método DetectSubregions que se usa en este ejemplo.

En este ejemplo, el usuario de la aplicación establece `m_bUseSegmentationFilter` una casilla. Si la aplicación lo admite, primero debe comprobar que el controlador tiene un filtro de segmentación mediante una llamada a [**checkExtension**](-wia-iwiaitem2-checkextension.md). Consulte [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para ver el ejemplo de método CheckImgFilter que muestra cómo se puede hacer esto.


```C++
HRESULT
DownloadPreviewImage(
   IN IWiaItem2 *pWiaFlatbedItem2)
{
   HRESULT hr              = S_OK;
   BOOL    bHasImgFilter   = FALSE;

   IWiaTransferCallback *pAppWiaTransferCallback = NULL;

   hr = CheckImgFilter(pWiaFlatbedItem2, &bHasImgFilter)

   if (SUCCEEDED(hr))
   {
      if (bHasImgFilter)
      {
         IWiaPreview *pWiaPreview = NULL;

         // In this example, the AppWiaTransferCallback class implements 
         // the IWiaTransferCallback interface.  
         // The constructor of AppWiaTransferCallback sets the reference count 
         // to 1.
         pAppWiaTransferCallback = new AppWiaTransferCallback();

         hr = pAppWiaTransferCallback ? S_OK : E_OUTOFMEMORY;

         if (SUCCEEDED(hr))
         {
            // Acquire image from scanner
            hr = m_pWiaPreview->GetNewPreview(pWiaFlatbedItem2,
                                              0,
                                              pAppWiaTransferCallback);    
         }

         //
         // Check the application UI for whether the user wants
         // to use the segmentation filter indicated by the value 
         // of m_bUseSegmentationFilter.
         //
         // m_FlatbedPreviewStream is the stream that
         // AppWiaTransferCallback::GetNextStream returned for the
         // flatbed item.
         // This stream is where the image data is stored after
         // the successful return of GetNewPreview.
         // The stream is passed into the segmentation filter
         // for region detection.
         if (SUCCEEDED(hr) && m_bUseSegmentationFilter)
         {
            DetectSubregions(m_FlatbedPreviewStream, pWiaFlatbedItem2);
         }

         if (pAppWiaTransferCallback)
         {
            // If the call to GetNewPreview was successful, the
            // preview component calls AddRef on the callback so
            // this call doesn't delete the object.

            pAppWiaTransferCallback->Release();
         }

      }
      else
      {
         // Do not create an instance of preview component if the driver 
         // does not come with an image-processing filter.
         // You can use a segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
