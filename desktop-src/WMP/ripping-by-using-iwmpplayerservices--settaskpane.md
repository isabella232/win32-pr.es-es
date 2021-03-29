---
title: Copia desde CD mediante IWMPPlayerServices setTaskPane
description: Copia desde CD mediante IWMPPlayerServices setTaskPane
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- Copia de CD, interfaz de IWMPPlayerServices setTaskPane
- copia desde CD, IWMPPlayerServices setTaskPane interface
- Interfaz IWMPPlayerServices setTaskPane
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb1a09d67f310266ae4818bc0b594fe3b74d128
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104487354"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a>Copiar mediante IWMPPlayerServices:: setTaskPane

> [!Note]  
> En esta sección se documenta una característica de los controles ActiveX de Windows Media Player 9 y Windows Media Player 10. Se recomienda utilizar la interfaz **IWMPCdromRip** con versiones posteriores. Consulte la [interfaz IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).

 

Puede usar la serie Windows Media Player 9 o el control posterior para copiar las pistas de CD en el equipo del usuario. Este proceso se denomina *copia desde CD*. Para ello, debe incrustar el control Media Player de Windows en modo remoto. Para obtener más información sobre el modo remoto, vea [comunicación remota del control de Media Player de Windows](remoting-the-windows-media-player-control.md).

Para iniciar el proceso de copia desde CD, llame a [IWMPPlayerServices:: setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), pasando CopyFromCD? Autocopy: valor del *identificador* para el parámetro *bstrTaskPane* , donde *ID* es el índice de la unidad de CD desde la que se va a copiar. Este índice corresponde al índice de un objeto **CDROM** en la interfaz **IWMPCdromCollection** o el evento **CdromMediaChange** .

El código de ejemplo siguiente es una función que inicia el proceso de copia desde CD desde la unidad de CD identificada por el índice cero. La función utiliza la siguiente variable miembro:


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



En el código siguiente se muestra el cuerpo de la función:


```C++
HRESULT CMyApp::StartRip()
{
    CComPtr<IWMPPlayerApplication>  spPlayerApp;
    CComPtr<IWMPPlayerServices>     spPlayerServices;
    CComBSTR bstrParam;  // Contains the parameter string.

    ATLASSERT(m_spPlayer.p);

    HRESULT hr = m_spPlayer->QueryInterface(&spPlayerServices);

    if(SUCCEEDED(hr))
    {
        // Create the parameter string.
        hr = bstrParam.Append(_T("CopyFromCD?AutoCopy:0"));
    }

    if(SUCCEEDED(hr))
    {
        // Rip the CD in drive 0.
        hr = spPlayerServices->setTaskPane(bstrParam);
    }

    return hr;
}

```



Mostrar el estado al usuario

Al copiar desde un CD, puede recuperar una cadena que contiene información de estado sobre la operación de copia. Para ello, primero debe recuperar una lista de reproducción que contenga elementos multimedia que representen las pistas del CD mediante una llamada a [IWMPCdrom:: get \_ playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist). Al igual que en el ejemplo anterior, el código de ejemplo siguiente funciona con el índice de unidad de CD cero. Almacena la lista de reproducción recuperada en la siguiente variable miembro:


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



En el código siguiente se muestra el cuerpo de la función:


```C++
HRESULT CMyApp::GetCDPlaylist()
{
    HRESULT hr = S_OK;

    // Release any existing playlist instance.
    m_spCDPlaylist.Release();

    CComPtr<IWMPCdromCollection> spCDDrives;
    CComPtr<IWMPCdrom>  spDrive;
    long lCount = 0;  // Count of CD drives.

    ATLASSERT(m_spPlayer);

    hr = m_spPlayer->get_cdromCollection(&spCDDrives);

    // Test to make sure there is at least one drive.
    if(SUCCEEDED(hr))
    {
        hr = spCDDrives->get_count(&lCount);
    }

    if(SUCCEEDED(hr) && lCount < 1)
    {
        MessageBox(_T("No CD drive detected"), 
                   _T("CD Rip Error"), MB_OK);
        hr = NS_E_CD_READ_ERROR;
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the first drive.
        hr = spCDDrives->item(0, &spDrive);
    }
    
    if(SUCCEEDED(hr))
    {
        // Get the playlist.
        hr = spDrive->get_playlist(&m_spCDPlaylist);
    }
   
    return hr;
}

```



A continuación, controle el evento [IWMPEvents:: MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) . Este evento se produce cuando se copia una pista de CD. El puntero **IDispatch** que se pasa al controlador de eventos apunta a la interfaz **IWMPMedia** para la pista del CD. Llame a **QueryInterface** a **IDispatch** para recuperar el puntero a **IWMPMedia**.

Para detectar la pista del CD que se va a copiar, compare el puntero **IWMPMedia** del evento con los elementos multimedia de la lista de reproducción del CD llamando a [IWMPMedia:: get \_ isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).

Llame a [IWMPMedia:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), pasando la cadena "status" como nombre del elemento. **Status** es un atributo temporal establecido por Windows Media Player en los elementos multimedia mientras se copian desde CD; no está disponible en la biblioteca.

En el ejemplo de código siguiente se muestra un controlador de eventos **MediaChange** .


```C++
void CMyApp::MediaChange(IDispatch * Item)
{
    // Test whether the CD playlist exists.
    if(!m_spCDPlaylist)
    {
        return;
    }

    // Declare and initialize variables.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = S_OK;
    VARIANT_BOOL vbIdentical = VARIANT_FALSE;
    CComBSTR bstrVal;
    CComBSTR bstrName;
    long lCount = 0;  

    // Create the attribute value string.
    hr = bstrName.Append(_T("Status"));

    if(SUCCEEDED(hr))
    { 
        // Retrieve the IWMPMedia pointer from IDispatch.
        hr = Item->QueryInterface(__uuidof(IWMPMedia),(void**)&spMedia);
    }

    if(SUCCEEDED(hr))
    {
        // Get the value of the Status attribute.
        hr = spMedia->getItemInfo(bstrName, &bstrVal);
    }

    if(SUCCEEDED(hr))
    {
        // If the attribute is empty, set a failure code
        // to simply exit the function.
        if(bstrVal.Length() == 0)
        {
            hr = E_PENDING;
        }
    }
      
    if(SUCCEEDED(hr))
    {
        // Retrieve the count of items in the CD playlist.
        hr = m_spCDPlaylist->get_count(&lCount);
    }

    if(lCount < 1)
    {
        // Exit if the playlist is empty.
        hr = E_PENDING;
    }    

    if(SUCCEEDED(hr) && spMedia)
    {
        // Iterate through the playlist.
        // Compare the media item that raised the event
        // to each CD track. This detects which track
        // has a new status.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spTrack;

            // Retrieve the CD track as a media object.
            hr = m_spCDPlaylist->get_item(i, &spTrack);

            if(SUCCEEDED(hr))
            {
                // Do the comparison.
                hr = spMedia->get_isIdentical(spTrack, &vbIdentical);
            }

            if(SUCCEEDED(hr) && VARIANT_TRUE == vbIdentical)
            {
                 // spTrack represents a track with changed status.
                 // bstrVal contains a status string. For example:
                 // "Ripping (10%)"
                 //
                 // TODO: Retrieve metadata about the track, and then
                 // display the status to the user.
            }
        }
    }

    return;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMPCdrom**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Interfaz IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**Interfaz IWMPEvents**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[**Interfaz IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Interfaz IWMPPlayerServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[**Interfaz IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Guía de control del reproductor**](player-control-guide.md)
</dt> <dt>

[**Copia desde CD mediante la interfaz IWMPCdromRip**](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




