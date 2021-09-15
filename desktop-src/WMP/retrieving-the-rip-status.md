---
title: Recuperar el estado de desgarr
description: Recuperar el estado de desgarr
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Reproductor de Windows Media,CD al día
- Reproductor de Windows Media modelo de objetos, algarada de CD
- modelo de objetos, algarada de CD
- Reproductor de Windows Media ActiveX control, cds
- ActiveX control, cds
- Reproductor de Windows Media Control ActiveX dispositivos móviles, algarada de CD
- Reproductor de Windows Media Móvil, cds
- Recuperación del estado de desgarre de CD
- retriev CDs,retrieving rip status (Recuperación del estado de desgarre)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be1fce1a46f9cc2d8477cabcc12a3a1b5bd159d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476187"
---
# <a name="retrieving-the-rip-status"></a>Recuperar el estado de desgarr

Puede supervisar el progreso de la operación de pra llamando periódicamente a [IWMPCdromRip::get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Este método recupera un valor de progreso para toda la operación de async. El valor recuperado es un número que representa el porcentaje de aseadas completadas, de 0 a 100.

El valor de progreso representa el porcentaje completado de todo el proceso de esión. Para determinar el progreso de una pista específica, use [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) con "RipProgress" como nombre del atributo. Para determinar el índice de la pista que se está arrasando actualmente, llame a **IWMPPlaylist::getItemInfo** con "CurrentRipTrackIndex" como nombre del atributo.

Puede supervisar el estado de la operación de integración llamando periódicamente a [IWMPCdromRip::get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Este método recupera un valor de [enumeración WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica si la operación está en curso o detenida. También puede supervisar el estado de la operación de manipulación controlando el evento [IWMPEvents3::CdromRipStateChange.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) (Vea [Control de eventos en C++).](handling-events-in-c.md) Tenga cuidado de comparar el puntero **IWMPCdromRip** (proporcionado por el evento) con el puntero que representa la operación de alerón, para asegurarse de que la operación ha producido el evento.

En el código de ejemplo siguiente se muestra cómo usar estas funciones para recuperar el estado de una operación de arraigo.

Los siguientes controles de cuadro de diálogo se definen para el ejemplo de código.



| Id. de control                   | Descripción                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| PISTA ACTUAL DE IDC \_ \_          | Texto estático que representa el índice de la pista que se está arrasando actualmente.                                         |
| TEXTO DE PROGRESO \_ DE SEGUIMIENTO \_ DE IDC \_   | Texto estático que representa el progreso de la pista que se está arrasando actualmente como porcentaje.                      |
| SEGUIMIENTO DE PROGRESO DE IDC \_ \_         | Barra de progreso con intervalo de 0 a 100 que representa el progreso de la pista que se está arrasando actualmente como porcentaje. |
| TEXTO DE PROGRESO GENERAL DE IDC \_ \_ \_ | Texto estático que representa el progreso del proceso total de esión como porcentaje.                             |
| PROGRESO GENERAL DE IDC \_ \_       | Barra de progreso con un intervalo de 0 a 100 que representa el progreso del proceso total de arrasación como porcentaje.        |
| ESTADO DE \_ RIP DE \_ IDC              | Texto estático que muestra la operación que se está realizando actualmente (" Estando", "Detenido" o "Desconocido")             |



 


```C++
HRESULT CMainDlg::UpdateStatus (void)
{
    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get the current track index.
    HRESULT hr = bstrItemName.Append("CurrentRipTrackIndex");
    if (SUCCEEDED(hr))
    {
        hr = m_spPlaylist->getItemInfo(bstrItemName, &bstrVal);
    }

    // Update the dialog text with the track number.
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_CURRENT_TRACK, bstrVal.m_str);
    }

    // Get an IWMPMedia interface from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    if (SUCCEEDED(hr))
    {
        long lIndex = _wtol(bstrVal.m_str);
        hr = m_spPlaylist->get_item(lIndex, &spMedia);
    }

    // Update the current track progress bar and progress text.
    if (SUCCEEDED(hr))
    {
        bstrItemName.Empty();
        hr = bstrItemName.Append("RipProgress");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(bstrItemName, &bstrVal);
    }

    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemTextW(IDC_TRACK_PROGRESS_TEXT, bstrVal.m_str);

        // Obtain a numerical value from the progress string.
        long lTrackPosition = _wtol(bstrVal.m_str);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_TRACK),
            PBM_SETPOS, lTrackPosition, 0);
    }

    // Update the total progress bar and progress text.
    long lTotalPosition = 0;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripProgress(&lTotalPosition);
    }
    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemInt(IDC_OVERALL_PROGRESS_TEXT, lTotalPosition);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_OVERALL),
            PBM_SETPOS, lTotalPosition, 0);
    }

    // Update the ripping state.
    CComBSTR bstrState;
    WMPRipState wmprs = wmprsUnknown;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripState(&wmprs);
    }
    if (SUCCEEDED(hr))
    {
        switch (wmprs)
        {
            case wmprsUnknown:
            default:
                hr = bstrState.Append("Unknown");
                break;
            case wmprsRipping:
                hr = bstrState.Append("Ripping");
                break;
            case wmprsStopped:
                hr = bstrState.Append("Stopped");
                break;
        }
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_RIP_STATE, bstrState.m_str);
    }

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Arrasar un CD**](ripping-a-cd.md)
</dt> <dt>

[**Recuperación de la interfaz de copia desde CD**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Iniciar el proceso de desgarr**](starting-the-rip-process.md)
</dt> <dt>

[**Selección de elementos para Alcándalo**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




