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
# <a name="transferring-image-data-in-wia-20"></a><span data-ttu-id="3930c-103">Transferir datos de imagen en WIA 2,0</span><span class="sxs-lookup"><span data-stu-id="3930c-103">Transferring Image Data in WIA 2.0</span></span>

> [!Note]  
> <span data-ttu-id="3930c-104">En este tutorial se muestra cómo transferir datos de imagen en aplicaciones que se ejecutan en Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="3930c-104">This tutorial demonstrates how to transfer image data in applications that run on Windows Vista or later.</span></span> <span data-ttu-id="3930c-105">Consulte [transferencia de datos de imagen en WIA 1,0](-wia-transferring-image-data.md) para obtener información sobre cómo transferir datos de imagen en aplicaciones que se ejecutan en Windows XP o versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3930c-105">See [Transfering Image Data in WIA 1.0](-wia-transferring-image-data.md) for information about transferring image data in applications that run on Windows XP or earlier.</span></span>

 

<span data-ttu-id="3930c-106">Dado que la transferencia de datos de imagen se basa en secuencias en la adquisición de imágenes de Windows (WIA) 2,0, no es necesario especificar un tipo de destino (por ejemplo, memoria o archivo).</span><span class="sxs-lookup"><span data-stu-id="3930c-106">Because image data transfer is stream-based in Windows Image Acquisition (WIA) 2.0, you do not need to specify a destination type (e.g. memory or file).</span></span> <span data-ttu-id="3930c-107">La aplicación simplemente proporciona a WIA 2,0 el flujo que se va a usar y el controlador lee o escribe en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3930c-107">The application simply gives WIA 2.0 the stream to use, and the driver reads or writes to the stream.</span></span> <span data-ttu-id="3930c-108">La secuencia puede ser un flujo de archivo, una secuencia de memoria o cualquier otro tipo de secuencia y es transparente para el controlador.</span><span class="sxs-lookup"><span data-stu-id="3930c-108">The stream can be a file stream, a memory stream, or any other type of stream, and is transparent to the driver.</span></span> <span data-ttu-id="3930c-109">El uso de secuencias también proporciona una fácil integración con el filtro de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="3930c-109">Using streams also provides an easy integration with the Image Processing filter.</span></span>

<span data-ttu-id="3930c-110">Use los métodos de la interfaz [**IWiaTransfer**](-wia-iwiatransfer.md) para transferir datos desde un dispositivo WIA 2,0 a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="3930c-110">Use the methods of the [**IWiaTransfer**](-wia-iwiatransfer.md) interface to transfer data from a WIA 2.0 device to an application.</span></span> <span data-ttu-id="3930c-111">Esta interfaz está disponible a través de la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="3930c-111">This interface is available through the [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span> <span data-ttu-id="3930c-112">La interfaz **IWiaTransfer** tiene métodos para solicitar la carga o descarga de datos hacia y desde un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3930c-112">The **IWiaTransfer** interface has methods for requesting uploading or downloading of data to and from a device.</span></span> <span data-ttu-id="3930c-113">Estos métodos toman una devolución de llamada que la aplicación proporciona y usan una [IStream](/windows/win32/api/objidl/nn-objidl-istream) proporcionada por la aplicación para el destino real de la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="3930c-113">These methods take a callback that the application provides, and use an [IStream](/windows/win32/api/objidl/nn-objidl-istream) provided by the application for the actual destination of the data transfer.</span></span>

<span data-ttu-id="3930c-114">Las aplicaciones deben consultar un elemento de imagen para obtener un puntero a su interfaz [**IWiaTransfer**](-wia-iwiatransfer.md) , tal y como se muestra en el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="3930c-114">Applications must query an image item to obtain a pointer to its [**IWiaTransfer**](-wia-iwiatransfer.md) interface, as shown in the following code sample:</span></span>


```
    // Get the IWiaTransfer interface
    //
    IWiaTransfer *pWiaTransfer = NULL;
    hr = pIWiaItem2->QueryInterface(IID_IWiaTransfer,(void**)&pWiaTransfer);
```



<span data-ttu-id="3930c-115">En el código anterior, suponemos que **pWiaItem2** es un puntero válido a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="3930c-115">In the previous code, we assume that **pWiaItem2** is a valid pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span> <span data-ttu-id="3930c-116">La llamada a [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) rellena **pWiaTransfer** con un puntero a la interfaz [**IWiaTransfer**](-wia-iwiatransfer.md) del elemento al que hace referencia **pWiaItem2**.</span><span class="sxs-lookup"><span data-stu-id="3930c-116">The call to [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) fills **pWiaTransfer** with a pointer to the [**IWiaTransfer**](-wia-iwiatransfer.md) interface of the item referred to by **pWiaItem2**.</span></span>

<span data-ttu-id="3930c-117">A continuación, la aplicación crea una instancia del objeto de devolución de llamada, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="3930c-117">The application then instantiates the callback object, as shown here.</span></span>


```
    //   Instantiate the object which receives the callbacks
    //
    CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
```



<span data-ttu-id="3930c-118">La aplicación siguiente establece las propiedades mediante la interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de [**IWiaItem2**](-wia-iwiaitem2.md) Item y realiza la transferencia.</span><span class="sxs-lookup"><span data-stu-id="3930c-118">The application next sets the properties by using [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface of [**IWiaItem2**](-wia-iwiaitem2.md) item, and performs the transfer.</span></span>

<span data-ttu-id="3930c-119">Descarga:</span><span class="sxs-lookup"><span data-stu-id="3930c-119">Downloading:</span></span>


```
    // Download   
    hr = pWiaTransfer->Download(0,pWiaClassCallback);
```



<span data-ttu-id="3930c-120">Cargar</span><span class="sxs-lookup"><span data-stu-id="3930c-120">Uploading:</span></span>


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



<span data-ttu-id="3930c-121">Este es el ejemplo de transferencia de datos completo:</span><span class="sxs-lookup"><span data-stu-id="3930c-121">Here is the complete data transfer sample:</span></span>


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



 

 
