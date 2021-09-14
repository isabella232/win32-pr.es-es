---
title: Copia desde CD mediante IWMPPlayerServices setTaskPane
description: Copia desde CD mediante IWMPPlayerServices setTaskPane
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Reproductor de Windows Media,CD
- Reproductor de Windows Media modelo de objetos, cds
- modelo de objetos, cds
- Reproductor de Windows Media ActiveX control de datos, cds
- ActiveX control de datos, cds
- Reproductor de Windows Media Control de ActiveX dispositivos móviles,cds
- Reproductor de Windows Media Móvil, cds
- Interfaz setTaskPane de CD player,IWMPPlayerServices
- Interfaz setTaskPane de CDs e IWMPPlayerServices
- IWMPPlayerServices setTaskPane (interfaz)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb1a09d67f310266ae4818bc0b594fe3b74d128
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070886"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a>Task by Using IWMPPlayerServices::setTaskPane

> [!Note]  
> En esta sección se documenta una característica de Reproductor de Windows Media serie 9 y Reproductor de Windows Media 10 ActiveX controles. Se recomienda usar la interfaz **IWMPCdromRip** con versiones posteriores. Vea [IWMPCdromRip (interfaz).](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)

 

Puede usar el control Reproductor de Windows Media serie 9 o posterior para copiar pistas de CD en el equipo del usuario. Este proceso se denomina *desasoyendo.* Para ello, debe insertar el control Reproductor de Windows Media en modo remoto. Para obtener más información sobre el modo remoto, vea [Comunicación remota Reproductor de Windows Media control](remoting-the-windows-media-player-control.md).

Para iniciar el proceso de task, llame [a IWMPPlayerServices::setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane)y pase copyFromCD. AutoCopy:*valor de* identificador para el parámetro *bstrTaskPane,* donde *id* es el índice de la unidad de CD desde la que se va a copiar. Este índice corresponde al índice de un objeto **Cdrom** en la **interfaz IWMPCdromCollection** o el **evento CdromMediaChange.**

El código de ejemplo siguiente es una función que inicia el proceso de desasoción de un CD desde la unidad de CD identificada por el índice cero. La función usa la siguiente variable miembro:


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



El código siguiente muestra el cuerpo de la función:


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

Al copiar desde un CD, puede recuperar una cadena que contiene información de estado sobre la operación de copia. Para ello, primero debe recuperar una lista de reproducción que contenga elementos multimedia que representen las pistas de CD mediante una llamada a [IWMPCdrom::get \_ ](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist)playlist . Al igual que en el ejemplo anterior, el código de ejemplo siguiente funciona con el índice de unidad de CD cero. Almacena la lista de reproducción recuperada en la siguiente variable miembro:


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



El código siguiente muestra el cuerpo de la función:


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



A continuación, [controle el evento IWMPEvents::MediaChange.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) Este evento tiene lugar cuando se realiza una pista de CD. El **puntero IDispatch** pasado al controlador de eventos apunta a la **interfaz IWMPMedia** para la pista de CD. Llame **a QueryInterface** **a través de IDispatch** para recuperar el puntero a **IWMPMedia**.

Para detectar qué pista de CD se está arrancando, compare el puntero **IWMPMedia** del evento con los elementos multimedia de la lista de reproducción de CD mediante una llamada [a IWMPMedia::get \_ isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).

Llame [a IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)y pase la cadena "Status" como nombre del elemento. **El** estado es un atributo temporal establecido por Reproductor de Windows Media elementos multimedia mientras se migran desde CD. no está disponible en la biblioteca.

En el código de ejemplo siguiente se muestra un **controlador de eventos MediaChange.**


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

[**IWMPCdrom (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**IWMPCdromCollection (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**IWMPEvents (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[**IWMPMedia (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPPlayerServices (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[**IWMPPlaylist (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Guía de control del reproductor**](player-control-guide.md)
</dt> <dt>

[**Resalte mediante la interfaz IWMPCdromRip**](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




