---
description: Implementación de conversión de un objeto de entrada manuscrita de texto (tInk) en la entrada de lápiz.
ms.assetid: 9365da4c-3667-49f0-838f-f099d28dab44
title: Convertir un objeto de entrada de lápiz de texto en tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8c7fe4a7847834fffda2df9c4ab94293756cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275106"
---
# <a name="converting-a-text-ink-object-to-ink"></a>Convertir un objeto de entrada de lápiz de texto en tinta

Implementación de conversión de un objeto de entrada manuscrita de texto (tInk) en la entrada de lápiz.

## <a name="to-convert-from-a-text-ink-object-to-ink"></a>Para convertir un objeto de entrada de lápiz de texto en entrada de lápiz

1.  Use la interfaz [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) para escribir el contenido del objeto de entrada de lápiz de texto en una secuencia. El objeto de entrada manuscrita de texto usa el formato serializado de tinta para escribir en la secuencia.
2.  Lea el contenido de la secuencia en una matriz de BYTEs.
3.  Use el método [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) del objeto [**InkDisp**](inkdisp-class.md) para cargar el contenido de la secuencia en el objeto **InkDisp** .

## <a name="text-ink-object-to-ink-object-example"></a>Ejemplo de objeto de entrada de lápiz de texto en objeto de entrada manuscrita

En el siguiente fragmento de código se convierte un objeto de entrada manuscrita en tinta.

En primer lugar, el código obtiene un objeto de entrada manuscrita de texto.


```C++
/* Create a variable to hold the text ink object */
CComPtr<IInkObject *> spITextInk;

/* Obtain the text ink object */
```



A continuación, el código crea un puntero para la secuencia que contiene el contenido del objeto de entrada manuscrita.


```C++
// Create a Stream pointer to hold the saved object
CComPtr<IStream *> spStream = NULL; 
```



A continuación, el código obtiene la interfaz [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) del objeto de entrada de texto.


```C++
// Declare the IPersistStream to be used for retrieving the saved data from the text ink
CComPtr<IPersistStream *> spIPersistStream = NULL;
// Get the actual IPersistStream interface off of the TextInk
HRESULT hr = pITextInk->QueryInterface(IID_IPersistStream, (void **)&spIPersistStream);
ASSERT(SUCCEEDED(hr) && spIPersistStream);
```



A continuación, el código usa la interfaz [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) para guardar el contenido del objeto de entrada de lápiz en la secuencia.


```C++
if( SUCCEEDED(hr) && pIPersistStream )
{
    // Create the stream 
    if( SUCCEEDED(hr=CreateStreamOnHGlobal(NULL, TRUE, &spStream)) && spStream )
    {
        // Save the TextInk through IPersistStream Interface to the IStream
        hr = spIPersistStream->Save(spStream, FALSE);
    }
}
```



A continuación, el código crea un objeto [**InkCollector**](inkcollector-class.md) , crea un objeto [**InkDisp**](inkdisp-class.md) para **InkCollector**, adjunta **InkCollector** a la ventana de la aplicación y habilita la colección de entradas de lápiz en **InkCollector**.


```C++
// Now create an InkCollector object along with InkDisp Object
if( SUCCEEDED(hr) && spStream)
{
    CComPtr<IInkCollector *> spIInkCollector;
    CComPtr<IInkDisp *> spIInkDisp = NULL;

    // Create the InkCollector object.
    hr = CoCreateInstance(CLSID_InkCollector, 
        NULL, CLSCTX_INPROC_SERVER, 
        IID_IInkCollector, 
        (void **) &spIInkCollector);
    if (FAILED(hr)) 
        return -1;

    // Get a pointer to the Ink object
    hr = spIInkCollector->get_Ink(&spIInkDisp);
    if (FAILED(hr)) 
        return -1;

    // Tell InkCollector the window to collect ink in
    hr = spIInkCollector->put_hWnd((long)hwnd);
    if (FAILED(hr)) 
        return -1;

    // Enable ink input in the window
    hr = spIInkCollector->put_Enabled(VARIANT_TRUE);
    if (FAILED(hr)) 
        return -1;
```



Después, el código recupera el tamaño de la secuencia y crea una matriz segura para almacenar el contenido de la secuencia.


```C++
    // Now create a variant data type based on the IStream data
    const LARGE_INTEGER li0 = {0, 0};
    ULARGE_INTEGER uli = {0,0};

    // Find the size of the stream
    hr = spStream->Seek(li0, STREAM_SEEK_END, &uli);
    ASSERT(0 == uli.HighPart);
    DWORD dwSize = uli.LowPart;

    // Set uli to point to the beginning of the stream.
    hr=spStream->Seek(li0, STREAM_SEEK_SET, &uli);
    ASSERT(SUCCEEDED(hr));

    // Create a safe array to hold the stream contents
    if( SUCCEEDED(hr) )
    {
        VARIANT vtData;
        VariantInit(&vtData);
        vtData.vt = VT_ARRAY | VT_UI1;

        vtData.parray = ::SafeArrayCreateVector(VT_UI1, 0, dwSize);
        if (vtData.parray)
        {
```



Por último, el código tiene acceso a la matriz segura y usa el método [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) del objeto [**InkDisp**](inkdisp-class.md) para cargar la tinta de la matriz.


```C++
            DWORD dwRead = 0;
            LPBYTE pbData = NULL; 

            if (SUCCEEDED(::SafeArrayAccessData(vtData.parray, (void**)&pbData)))
            {
                // Read the data from the stream to the varian data and load that into an InkDisp object
                if (TRUE == spStream->Read(pbData, uli.LowPart, &dwRead)
                    && SUCCEEDED(spIInkDisp->Load(vtData)))
                {
                    hr = S_OK;
                }
                ::SafeArrayUnaccessData(vtData.parray);
            }
            ::SafeArrayDestroy(vtData.parray);
        }
    }
}
```



 

 
