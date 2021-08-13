---
description: Determina las subrecciones de una imagen colocadas en la placa plana para que cada una de las subrecciones se pueda adquirir en un elemento de imagen independiente.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: Método IWiaSegmentationFilter::D etectRegions (Wia.h)
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
ms.openlocfilehash: 46496360d7b54bed837ba287d604233a9fac98ee13807744b4adbfb52e9934d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450265"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a>Método IWiaSegmentationFilter::D etectRegions

Determina las subrecciones de una imagen colocadas en la placa plana para que cada una de las subrecciones se pueda adquirir en un elemento de imagen independiente.

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

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*pInputStream* \[ En\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Especifica un puntero a la imagen de [vista previa de IStream.](/windows/win32/api/objidl/nn-objidl-istream)

</dd> <dt>

*pWiaItem2* \[ En\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Especifica un puntero al elemento [**IWiaItem2**](-wia-iwiaitem2.md) para el que *se adquirió pInputStream.* El filtro de segmentación crea elementos secundarios para este elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Este método determina las subrecciones de la imagen representada por pInputStream. Para cada subrecciones que detecta, crea un elemento secundario para el elemento [**IWiaItem2**](-wia-iwiaitem2.md) especificado en el *parámetro pWiaItem2.* Para cada elemento secundario, el filtro de segmentación debe establecer valores para el rectángulo delimitador del área que se va a examinar, utilizando las siguientes constantes de propiedad de elemento [**WIA del analizador**](-wia-wiaitempropscanneritem.md).

-   [**WIA \_ IPS \_ XPOS**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ YPOS**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ XEXTENT**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ YEXTENT**](-wia-wiaitempropscanneritem.md)

Un filtro más avanzado también puede requerir otras constantes de propiedad de elemento WIA del analizador, como **WIA \_ IPS \_ DESKEW \_ X** y **WIA \_ IPS \_ DESKEW \_ Y,** si el controlador admite la desessgajo. [](-wia-wiaitempropscanneritem.md)

Si la aplicación llama a **IWiaSegmentationFilter::D etectRegions** más de una vez, la aplicación debe eliminar primero los elementos secundarios creados por la última llamada a **IWiaSegmentationFilter::D etectRegions**.

Si una aplicación cambia las propiedades a *pWiaItem2,* entre adquirir la imagen en *pInputStream* y su llamada a **IWiaSegmentationFilter::D etectRegions**, se deben restaurar las propiedades originales (es decir, las propiedades que tenía el elemento cuando se adquirió la secuencia). Esto se puede hacer [**mediante GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) y [**SetPropertyStream.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream)

La aplicación debe restablecer [IStream](/windows/win32/api/objidl/nn-objidl-istream) si su llamada pasa la misma secuencia al filtro de segmentación más de una vez. La aplicación también debe restablecer la secuencia después de la descarga inicial y antes de llamar a **IWiaSegmentationFilter::D etectRegions**.

## <a name="examples"></a>Ejemplos

La segmentación realiza la detección de regiones en el flujo ( `pImageStream` ) pasado a DetectSubregions. Vea el [**método GetExtension**](-wia-iwiaitem2-getextension.md) para CreateSegmentationFilter que se usa en este ejemplo.


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



DownloadPreviewImage descarga los datos de imagen del analizador mediante una llamada al [**método GetNewPreview del**](-wia-iwiapreview-getnewpreview.md) componente de vista previa. A continuación, llama a DetectSubregions si el usuario de la aplicación desea invocar el filtro de segmentación, que crea un elemento secundario en pWiaItem2 para cada región que detecta. Vea **IWiaSegmentationFilter::D etectRegions para** el método DetectSubregions usado en este ejemplo.

En este ejemplo, el usuario de la aplicación `m_bUseSegmentationFilter` establece haciendo clic en una casilla. Si la aplicación lo admite, primero debe comprobar que el controlador tiene un filtro de segmentación llamando a [**CheckExtension**](-wia-iwiaitem2-checkextension.md). Consulte [**GetNewPreview para obtener el**](-wia-iwiapreview-getnewpreview.md) ejemplo del método CheckImgFilter que muestra cómo se puede hacer esto.


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
