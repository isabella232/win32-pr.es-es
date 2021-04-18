---
description: Almacena en caché internamente la imagen sin filtrar devuelta por el controlador.
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: 'IWiaPreview:: GetNewPreview (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.GetNewPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c3f1251e7ec1b98d43e616c1ff6f2b3b2aacd8b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715189"
---
# <a name="iwiapreviewgetnewpreview-method"></a>IWiaPreview:: GetNewPreview (método)

Almacena en caché internamente la imagen sin filtrar devuelta por el controlador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWiaItem2* \[ de\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Especifica un puntero al elemento [_ *IWiaItem2* *](-wia-iwiaitem2.md) para la imagen.

</dd> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*pWiaTransferCallback* \[ de\]
</dt> <dd>

Tipo: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _

Especifica un puntero a la interfaz [_ *IWiaTransferCallback* *](-wia-iwiatransfercallback.md) de la aplicación que realiza la llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Una aplicación debe llamar a **IWiaPreview:: GetNewPreview** antes de llamar a [**IWiaPreview::D etectregions**](-wia-iwiapreview-detectregions.md).

**IWiaPreview:: GetNewPreview** establece la propiedad de [**\_ \_ vista previa de DPS de WIA**](-wia-wiaitempropscannerdevice.md) (y lo restablece antes de que se devuelva, a menos que se haya establecido antes). Esto permite que el controlador y el hardware, así como el filtro de procesamiento de imágenes, sepan que el elemento es un examen de vista previa.

Internamente, el componente de vista previa de Windows Image Acquisition (WIA) 2,0 crea una instancia del filtro de procesamiento de imágenes del controlador mediante una llamada a [**getExtension**](-wia-iwiaitem2-getextension.md) en *pWiaItem2*. El componente de vista previa de WIA 2,0 lo hace cuando la aplicación llama a **IWiaPreview:: GetNewPreview**. El componente de vista previa de WIA 2,0 también inicializa el filtro en **IWiaPreview:: GetNewPreview**. El componente de vista previa de WIA 2,0 utiliza la misma instancia de filtro durante una llamada a [**IWiaPreview:: UpdatePreview**](-wia-iwiapreview-updatepreview.md).

Antes de llamar al componente de vista previa de WIA 2,0, una aplicación debe llamar a [**checkExtension**](-wia-iwiaitem2-checkextension.md) para asegurarse de que el controlador incluye un filtro de procesamiento de imágenes. Debe llamar a **checkExtension** en el elemento que se pasaría a **IWiaPreview:: GetNewPreview**. No es útil proporcionar vistas previas activas sin un filtro de procesamiento de imágenes. Si una aplicación llama a **IWiaPreview:: GetNewPreview** para un controlador sin un filtro de procesamiento de imágenes, se producirá un error en la llamada.

## <a name="examples"></a>Ejemplos

CheckImgFilter comprueba si el controlador tiene un filtro de procesamiento de imágenes. Antes de llamar al componente de vista previa, una aplicación debe asegurarse de que el controlador tiene un filtro de procesamiento de imágenes.


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



DownloadPreviewImage descarga los datos de imagen del escáner llamando al método **IWiaPreview:: GetNewPreview** del componente de vista previa. A continuación, llama a DetectSubregions si el usuario de la aplicación desea invocar el filtro de segmentación, que crea un elemento secundario en pWiaItem2 para cada región que detecta. Consulte [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) para el método DetectSubregions que se usa en este ejemplo.

En este ejemplo, el usuario de la aplicación establece `m_bUseSegmentationFilter` una casilla. Si la aplicación lo admite, primero debe comprobar que el controlador tiene un filtro de segmentación mediante una llamada a [**checkExtension**](-wia-iwiaitem2-checkextension.md). Vea **IWiaPreview:: GetNewPreview** para obtener el ejemplo del método CheckImgFilter que muestra cómo se puede hacer esto.


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
         // The constructor of AppWiaTransferCallback sets the reference count to 1.
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
         // Do not create an instance of preview component if the driver does
         // not come with an image processing filter.
         // You can use segmentation filter, however, if the driver
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



 

 




