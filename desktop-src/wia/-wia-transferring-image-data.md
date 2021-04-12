---
description: Use los métodos de la interfaz IWiaDataTransfer para transferir datos de un dispositivo de adquisición de imágenes de Windows (WIA) 1,0 a una aplicación.
ms.assetid: 67fbf3d9-6965-4464-b04c-10989b2fd55d
title: Transferir datos de imagen en WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00fc7ff76576b6c140358f9af3a0f9d17d4b180e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154385"
---
# <a name="transferring-image-data-in-wia-10"></a><span data-ttu-id="32699-103">Transferir datos de imagen en WIA 1,0</span><span class="sxs-lookup"><span data-stu-id="32699-103">Transferring Image Data in WIA 1.0</span></span>

> [!Note]  
> <span data-ttu-id="32699-104">Este tutorial trata sobre la transferencia de datos de imagen en aplicaciones que ejecutan Windows XP o una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="32699-104">This tutorial is about transferring image data in applications that will run Windows XP or earlier.</span></span> <span data-ttu-id="32699-105">Consulte [transferencia de datos de imagen en WIA 2,0](-wia-transferring-image-data-in-wia2.md) para obtener información acerca de la transferencia de datos de imagen en aplicaciones que se ejecutarán en Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="32699-105">See [Transferring Image Data in WIA 2.0](-wia-transferring-image-data-in-wia2.md) for information about transferring image data in applications that will run on Windows Vista or later.</span></span>

 

<span data-ttu-id="32699-106">Use los métodos de la interfaz [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) para transferir datos de un dispositivo de adquisición de imágenes de Windows (WIA) 1,0 a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="32699-106">Use the methods of the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface to transfer data from a Windows Image Acquisition (WIA) 1.0 device to an application.</span></span> <span data-ttu-id="32699-107">Esta interfaz admite una ventana de memoria compartida para transferir datos del objeto de dispositivo a la aplicación y eliminar copias de datos innecesarias durante el cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="32699-107">This interface supports a shared memory window to transfer data from the device object to the application and eliminate unnecessary data copies during marshalling.</span></span>

<span data-ttu-id="32699-108">Las aplicaciones deben consultar un elemento de imagen para obtener un puntero a su interfaz [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , como en el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="32699-108">Applications must query an image item to obtain a pointer to its [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface, as in the following code sample:</span></span>


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



<span data-ttu-id="32699-109">En el código anterior, se supone que **pWiaItem** es un puntero válido a la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="32699-109">In the previous code, it is assumed that **pWiaItem** is a valid pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface.</span></span> <span data-ttu-id="32699-110">La llamada a [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) rellena **pWiaDataTransfer** con un puntero a la interfaz [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) del elemento al que hace referencia **pWiaItem**.</span><span class="sxs-lookup"><span data-stu-id="32699-110">The call to [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) fills **pWiaDataTransfer** with a pointer to the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface of the item referred to by **pWiaItem**.</span></span>

<span data-ttu-id="32699-111">A continuación, la aplicación establece los miembros de la estructura [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .</span><span class="sxs-lookup"><span data-stu-id="32699-111">The application then sets the [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure members.</span></span> <span data-ttu-id="32699-112">Para obtener información, consulte STGMEDIUM y [TYMED](/windows/win32/api/objidl/ne-objidl-tymed).</span><span class="sxs-lookup"><span data-stu-id="32699-112">For information, see STGMEDIUM and [TYMED](/windows/win32/api/objidl/ne-objidl-tymed).</span></span>


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



<span data-ttu-id="32699-113">Si proporciona un nombre de archivo, debe incluir la extensión de archivo adecuada. WIA 1,0 no proporciona extensiones de archivo.</span><span class="sxs-lookup"><span data-stu-id="32699-113">If you supply a filename, it should include the proper file extension; WIA 1.0 does not provide file extensions.</span></span> <span data-ttu-id="32699-114">Si el miembro **lpszFileName** de **StgMedium** es **null**, WIA 1,0 genera un nombre de archivo aleatorio y una ruta de acceso para los datos transferidos.</span><span class="sxs-lookup"><span data-stu-id="32699-114">If the **lpszFileName** member of **StgMedium** is **NULL**, WIA 1.0 generates a random file name and path for the transferred data.</span></span> <span data-ttu-id="32699-115">Mueva o copie este archivo antes de llamar a ReleaseStgMedium, porque esta función eliminará el archivo.</span><span class="sxs-lookup"><span data-stu-id="32699-115">Move or copy this file before calling ReleaseStgMedium, because this function will delete the file.</span></span>

<span data-ttu-id="32699-116">A continuación, la aplicación llama al método [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) para ejecutar la transferencia de datos:</span><span class="sxs-lookup"><span data-stu-id="32699-116">The application then calls the [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) method to run the data transfer:</span></span>


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



<span data-ttu-id="32699-117">En la llamada a [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata), el segundo parámetro especifica un puntero a la interfaz [**IWiaDataCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) .</span><span class="sxs-lookup"><span data-stu-id="32699-117">In the call to [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata), the second parameter specifies a pointer to the [**IWiaDataCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) interface.</span></span> <span data-ttu-id="32699-118">Las aplicaciones deben implementar esta interfaz para recibir devoluciones de llamada durante las transferencias de datos.</span><span class="sxs-lookup"><span data-stu-id="32699-118">Applications must implement this interface to receive callbacks during data transfers.</span></span> <span data-ttu-id="32699-119">Para obtener información sobre la implementación de esta interfaz, vea [**IWiaDataCallback:: BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="32699-119">For information about implementing this interface, see [**IWiaDataCallback::BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

<span data-ttu-id="32699-120">A continuación, la aplicación libera los punteros a la interfaz [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) y libera los datos asignados en la estructura [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .</span><span class="sxs-lookup"><span data-stu-id="32699-120">The application then releases the pointers to the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface and frees any data allocated in the [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure.</span></span>

<span data-ttu-id="32699-121">La aplicación también puede transferir la imagen mediante transferencias de datos en memoria en lugar de transferencias de archivos.</span><span class="sxs-lookup"><span data-stu-id="32699-121">The application can also transfer the image using in-memory data transfers instead of file transfers.</span></span> <span data-ttu-id="32699-122">En este caso, la aplicación usa el método idtGetBandedData en lugar del método idtGetData.</span><span class="sxs-lookup"><span data-stu-id="32699-122">In this case, the application uses the idtGetBandedData method in place of the idtGetData method.</span></span>

<span data-ttu-id="32699-123">Este es el ejemplo de transferencia de datos completo:</span><span class="sxs-lookup"><span data-stu-id="32699-123">Here is the complete data transfer sample:</span></span>


```
HRESULT TransferWiaItem( IWiaItem *pWiaItem )
{
    //
    // Validate arguments
    //
    if (NULL == pWiaItem)
    {
        return E_INVALIDARG;
    }

    //
    // Get the IWiaPropertyStorage interface so you can set required properties.
    //
    IWiaPropertyStorage *pWiaPropertyStorage = NULL;
    HRESULT hr = pWiaItem->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaPropertyStorage );
    if (SUCCEEDED(hr))
    {
        //
        // Prepare PROPSPECs and PROPVARIANTs for setting the
        // media type and format
        //
        PROPSPEC PropSpec[2] = {0};
        PROPVARIANT PropVariant[2] = {0};
        const ULONG c_nPropCount = sizeof(PropVariant)/sizeof(PropVariant[0]);

        //
        // Use BMP as the output format
        //
        GUID guidOutputFormat = WiaImgFmt_BMP;

        //
        // Initialize the PROPSPECs
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_IPA_FORMAT;
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_IPA_TYMED;

        //
        // Initialize the PROPVARIANTs
        //
        PropVariant[0].vt = VT_CLSID;
        PropVariant[0].puuid = &guidOutputFormat;
        PropVariant[1].vt = VT_I4;
        PropVariant[1].lVal = TYMED_FILE;

        //
        // Set the properties
        //
        hr = pWiaPropertyStorage->WriteMultiple( c_nPropCount, PropSpec, PropVariant, WIA_IPA_FIRST );
        if (SUCCEEDED(hr))
        {
            //
            // Get the IWiaDataTransfer interface
            //
            IWiaDataTransfer *pWiaDataTransfer = NULL;
            hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
            if (SUCCEEDED(hr))
            {
                //
                // Create our callback class
                //
                CWiaDataCallback *pCallback = new CWiaDataCallback;
                if (pCallback)
                {
                    //
                    // Get the IWiaDataCallback interface from our callback class.
                    //
                    IWiaDataCallback *pWiaDataCallback = NULL;
                    hr = pCallback->QueryInterface( IID_IWiaDataCallback, (void**)&pWiaDataCallback );
                    if (SUCCEEDED(hr))
                    {
                        //
                        // Perform the transfer using default settings
                        //
                        STGMEDIUM stgMedium = {0};
                        StgMedium.tymed = TYMED_FILE;
                        hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
                        if (S_OK == hr)
                        {
                            //
                            // Print the filename (note that this filename is always
                            // a WCHAR string, not TCHAR).
                            //
                            _tprintf( TEXT("Transferred filename: %ws\n"), stgMedium.lpszFileName );

                            //
                            // Release any memory associated with the stgmedium
                            // This will delete the file stgMedium.lpszFileName.
                            //
                            ReleaseStgMedium( &stgMedium );
                        }

                        //
                        // Release the callback interface
                        //
                        pWiaDataCallback->Release();
                        pWiaDataCallback = NULL;
                    }

                    //
                    // Release our callback.  It should now delete itself.
                    //
                    pCallback->Release();
                    pCallback = NULL;
                }

                //
                // Release the IWiaDataTransfer
                //
                pWiaDataTransfer->Release();
                pWiaDataTransfer = NULL;
            }
        }

        //
        // Release the IWiaPropertyStorage
        //
        pWiaPropertyStorage->Release();
        pWiaPropertyStorage = NULL;
    }

    return hr;
}
```



 

 
