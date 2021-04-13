---
description: Dado que la transferencia de datos de imagen se basa en secuencias en la adquisición de imágenes de Windows (WIA) 2,0, no es necesario especificar un tipo de destino (por ejemplo,
ms.assetid: ebb9fce5-9450-4ffe-b480-b21670b60f90
title: Transferir datos de imagen en WIA 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ded5c6cd8fb94b1beccd86c3cd8aef3018aed0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360330"
---
# <a name="transferring-image-data-in-wia-20"></a>Transferir datos de imagen en WIA 2,0

> [!Note]  
> En este tutorial se muestra cómo transferir datos de imagen en aplicaciones que se ejecutan en Windows Vista o posterior. Consulte [transferencia de datos de imagen en WIA 1,0](-wia-transferring-image-data.md) para obtener información sobre cómo transferir datos de imagen en aplicaciones que se ejecutan en Windows XP o versiones anteriores.

 

Dado que la transferencia de datos de imagen se basa en secuencias en la adquisición de imágenes de Windows (WIA) 2,0, no es necesario especificar un tipo de destino (por ejemplo, memoria o archivo). La aplicación simplemente proporciona a WIA 2,0 el flujo que se va a usar y el controlador lee o escribe en la secuencia. La secuencia puede ser un flujo de archivo, una secuencia de memoria o cualquier otro tipo de secuencia y es transparente para el controlador. El uso de secuencias también proporciona una fácil integración con el filtro de procesamiento de imágenes.

Use los métodos de la interfaz [**IWiaTransfer**](-wia-iwiatransfer.md) para transferir datos desde un dispositivo WIA 2,0 a una aplicación. Esta interfaz está disponible a través de la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) . La interfaz **IWiaTransfer** tiene métodos para solicitar la carga o descarga de datos hacia y desde un dispositivo. Estos métodos toman una devolución de llamada que la aplicación proporciona y usan una [IStream](/windows/win32/api/objidl/nn-objidl-istream) proporcionada por la aplicación para el destino real de la transferencia de datos.

Las aplicaciones deben consultar un elemento de imagen para obtener un puntero a su interfaz [**IWiaTransfer**](-wia-iwiatransfer.md) , tal y como se muestra en el ejemplo de código siguiente:


```
    // Get the IWiaTransfer interface
    //
    IWiaTransfer *pWiaTransfer = NULL;
    hr = pIWiaItem2->QueryInterface(IID_IWiaTransfer,(void**)&pWiaTransfer);
```



En el código anterior, suponemos que **pWiaItem2** es un puntero válido a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) . La llamada a [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) rellena **pWiaTransfer** con un puntero a la interfaz [**IWiaTransfer**](-wia-iwiatransfer.md) del elemento al que hace referencia **pWiaItem2**.

A continuación, la aplicación crea una instancia del objeto de devolución de llamada, como se muestra aquí.


```
    //   Instantiate the object which receives the callbacks
    //
    CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
```



La aplicación siguiente establece las propiedades mediante la interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de [**IWiaItem2**](-wia-iwiaitem2.md) Item y realiza la transferencia.

Descarga:


```
    // Download   
    hr = pWiaTransfer->Download(0,pWiaClassCallback);
```



Cargar


```
    //Create child item which eventually will be the uploaded image 
    IWiaItem2* pWiaItemChild = NULL;
    HRESULT hr = pIWiaItem2->CreateChildItem(WiaItemTypeImage|WiaItemTypeFile,0,bzUploadFileName,&pWiaItemChild);
    
    if(SUCCEEDED(hr))
    {
                
        //Set the format for the child item as BMP 
        IWiaPropertyStorage* pWiaChildPropertyStorage = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaChildPropertyStorage );
        if(SUCCEEDED(hr))
        {
            WritePropertyGuid(pWiaChildPropertyStorage,WIA_IPA_FORMAT,WiaImgFmt_BMP );

            //release pWiaChildPropertyStorage
            pWiaChildPropertyStorage->Release();
            pWiaChildPropertyStorage = NULL;
        }
        

        //Get the IWiaTransfer interface of the child
        IWiaTransfer* pWiaTransferChild = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransferChild );
        if(SUCCEEDED(hr)){
            IStream* pUploadStream = NULL;
                                        
            //Create stream on test.BMP file
            hr = SHCreateStreamOnFile(L"test.BMP",STGM_READ, &pUploadStream);
            if(SUCCEEDED(hr)){
                pWiaTransferChild->Upload(0,pUploadStream,pWiaClassCallback);
                
            }
         }
   
      }
```



Este es el ejemplo de transferencia de datos completo:


```
HRESULT TransferWiaItem( IWiaItem2 *pIWiaItem2)
{
    // Validate arguments
    if (NULL == pIWiaItem2)
    {
        _tprintf(TEXT("\nInvalid parameters passed"));
        return E_INVALIDARG;
    }
    
    // Get the IWiaTransfer interface
    IWiaTransfer *pWiaTransfer = NULL;
    HRESULT hr = pIWiaItem2->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransfer );
    if (SUCCEEDED(hr))
    {
        // Create our callback class
        CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
        if (pWiaClassCallback)
        {
            
              LONG lItemType = 0;
              hr = pIWiaItem2->GetItemType( &lItemType );

              //download all items which have WiaItemTypeTransfer flag set
              if(lItemType & WiaItemTypeTransfer)
              {

                  // If it is a folder, do folder download . Hence with one API call, all the leaf nodes of this folder 
                  // will be transferred
                  if ((lItemType & WiaItemTypeFolder))
                  {
                        _tprintf ( L"\nI am a folder item");
                        hr = pWiaTransfer->Download(WIA_TRANSFER_ACQUIRE_CHILDREN, pWiaClassCallback);
                        if(S_OK == hr)
                        {
                            _tprintf(TEXT("\npWiaTransfer->Download() on folder item SUCCEEDED"));
                        }
                        else if(S_FALSE == hr)
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item returned S_FALSE. Folder may not be having child items"),hr);
                        }
                        else if(FAILED(hr))
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item failed"),hr);
                        }
                   }

                  
                  // If this is an file type, do file download
                  else if (lItemType & WiaItemTypeFile )
                  {
                      hr = pWiaTransfer->Download(0,pWiaClassCallback);
                      if(S_OK == hr)
                      {
                          _tprintf(TEXT("\npWiaTransfer->Download() on file item SUCCEEDED"));
                      }
                      else if(S_FALSE == hr)
                      {
                          ReportError(TEXT("\npWiaTransfer->Download() on file item returned S_FALSE. File may be empty"),hr);
                      }
                      else if(FAILED(hr))
                      {
                         ReportError(TEXT("\npWiaTransfer->Download() on file item failed"),hr);
                      }
                  }                     
                }
                
                // Release our callback.  It should now delete itself.
                pWiaClassCallback->Release();
                pWiaClassCallback = NULL;
        }
        else
        {
            ReportError( TEXT("\nUnable to create CWiaTransferCallback class instance") );
        }
            
        // Release the IWiaTransfer
        pWiaTransfer->Release();
        pWiaTransfer = NULL;
    }
    else
    {
        ReportError( TEXT("\npIWiaItem2->QueryInterface failed on IID_IWiaTransfer"), hr );
    }
    return hr;
}

// Callback Class should be something like this:

class CWiaTransferCallback : public IWiaTransferCallback
{
public: // Constructors, destructor
    CWiaTransferCallback () : m_cRef(1) {};
    ~ CWiaTransferCallback () {};

public: // IWiaTransferCallback
    HRESULT __stdcall TransferCallback(
        LONG                lFlags,
        WiaTransferParams   *pWiaTransferParams)
    {
        HRESULT hr = S_OK;

        switch (pWiaTransferParams->lMessage)
        {
            case WIA_TRANSFER_MSG_STATUS:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_STREAM:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_TRANSFER:
                ...
                break;
            default:
                break;
        }

        return hr;
    }

    HRESULT __stdcall GetNextStream(
        LONG    lFlags,
        BSTR    bstrItemName,
        BSTR    bstrFullItemName,
        IStream **ppDestination)
    {

        HRESULT hr = S_OK;

        //  Return a new stream for this item's data.
        //
        hr = CreateDestinationStream(bstrItemName, ppDestination);
        return hr;
    }

public: // IUnknown
        .
        .
        . // Etc.

private:
    /// For ref counting implementation
    LONG                m_cRef;
};

```



 

 
