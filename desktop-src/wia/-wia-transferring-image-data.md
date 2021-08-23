---
description: Use los métodos de la interfaz IWiaDataTransfer para transferir datos de un dispositivo Windows Image Acquisition (WIA) 1.0 a una aplicación.
ms.assetid: 67fbf3d9-6965-4464-b04c-10989b2fd55d
title: Transferencia de datos de imagen en WIA 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e2c1dfce551f105b0df1627f11e9b4ccb7ee8a420e395f3fd0cc1ba932f136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813675"
---
# <a name="transferring-image-data-in-wia-10"></a>Transferencia de datos de imagen en WIA 1.0

> [!Note]  
> Este tutorial trata sobre la transferencia de datos de imagen en aplicaciones que se ejecutarán Windows XP o versiones anteriores. Consulte Transferencia de datos de imagen en [WIA 2.0](-wia-transferring-image-data-in-wia2.md) para obtener información sobre cómo transferir datos de imagen en aplicaciones que se ejecutarán en Windows Vista o versiones posteriores.

 

Use los métodos de la [**interfaz IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) para transferir datos de un dispositivo Windows Image Acquisition (WIA) 1.0 a una aplicación. Esta interfaz admite una ventana de memoria compartida para transferir datos desde el objeto de dispositivo a la aplicación y eliminar copias de datos innecesarias durante la marshalling.

Las aplicaciones deben consultar un elemento de imagen para obtener un puntero a su [**interfaz IWiaDataTransfer,**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) como en el ejemplo de código siguiente:


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



En el código anterior, se supone que **pWiaItem** es un puntero válido a la [**interfaz IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) La llamada a [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) rellena **pWiaDataTransfer** con un puntero a la interfaz [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) del elemento al que hace referencia **pWiaItem**.

A continuación, la aplicación establece [los miembros de la estructura STGMEDIUM.](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) Para obtener información, vea STGMEDIUM y [TYMED.](/windows/win32/api/objidl/ne-objidl-tymed)


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



Si proporciona un nombre de archivo, debe incluir la extensión de archivo adecuada; WIA 1.0 no proporciona extensiones de archivo. Si el **miembro lpszFileName** de **StgMedium** es **NULL,** WIA 1.0 genera un nombre de archivo y una ruta de acceso aleatorios para los datos transferidos. Mueva o copie este archivo antes de llamar a ReleaseStgMedium, ya que esta función eliminará el archivo.

A continuación, la aplicación llama al [**método IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) para ejecutar la transferencia de datos:


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



En la llamada a [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata), el segundo parámetro especifica un puntero a la [**interfaz IWiaDataCallback.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) Las aplicaciones deben implementar esta interfaz para recibir devoluciones de llamada durante las transferencias de datos. Para obtener información sobre cómo implementar esta interfaz, vea [**IWiaDataCallback::BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

A continuación, la aplicación libera los punteros a la interfaz [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) y libera los datos asignados en la [estructura STGMEDIUM.](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)

La aplicación también puede transferir la imagen mediante transferencias de datos en memoria en lugar de transferencias de archivos. En este caso, la aplicación usa el método idtGetBandedData en lugar del método idtGetData.

Este es el ejemplo de transferencia de datos completo:


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



 

 
