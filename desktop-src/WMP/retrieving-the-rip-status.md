---
title: Recuperación del estado de RIP
description: Recuperación del estado de RIP
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- Copiar CD, recuperar el estado de RIP
- copiar CDs, recuperar el estado de RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be1fce1a46f9cc2d8477cabcc12a3a1b5bd159d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077356"
---
# <a name="retrieving-the-rip-status"></a>Recuperación del estado de RIP

Puede supervisar el progreso de la operación de copia desde CD llamando periódicamente a [IWMPCdromRip:: get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Este método recupera un valor de progreso para toda la operación de copia. El valor recuperado es un número que representa el porcentaje de copia completada, de 0 a 100.

El valor de progreso representa el porcentaje completado de todo el proceso de copia. Para determinar el progreso de una pista concreta, use [IWMPMedia:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) con "RipProgress" como nombre de atributo. Para determinar el índice de la pista que se está copiando actualmente, llame a **IWMPPlaylist:: getItemInfo** con "CurrentRipTrackIndex" como nombre de atributo.

Puede supervisar el estado de la operación de copia desde CD llamando periódicamente a [IWMPCdromRip:: get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Este método recupera un valor de enumeración [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica si la operación está en curso o detenido. También puede supervisar el estado de la operación de copia desde CD mediante el control del evento [IWMPEvents3:: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) . (Vea [controlar eventos en C++](handling-events-in-c.md)). Tenga cuidado de comparar el puntero **IWMPCdromRip** (proporcionado por el evento) con el puntero que representa la operación de copia desde CD, para asegurarse de que la operación ha generado el evento.

En el ejemplo de código siguiente se muestra cómo usar estas funciones para recuperar el estado de una operación de copia desde CD.

En el ejemplo de código se definen los siguientes controles de cuadro de diálogo.



| Id. de control                   | Descripción                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| \_seguimiento actual de IDC \_          | Texto estático que representa el índice de la pista que se está copiando en ese momento.                                         |
| \_texto de \_ progreso de seguimiento de IDC \_   | Texto estático que representa el progreso de la pista que se está copiando actualmente como porcentaje.                      |
| \_seguimiento de progreso de IDC \_         | Barra de progreso con el intervalo de 0 a 100 que representa el progreso de la pista que se está copiando actualmente como porcentaje. |
| \_texto de \_ progreso \_ General de IDC | Texto estático que representa el progreso del proceso de copia de copia total como un porcentaje.                             |
| \_progreso \_ General de IDC       | Barra de progreso con el intervalo de 0 a 100 que representa el progreso del proceso de copia de copia total como un porcentaje.        |
| \_Estado RIP de IDC \_              | Texto estático que muestra la operación que se está realizando actualmente ("copia desde CD", "detenida" o "desconocida")             |



 


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

[**Copia desde CD**](ripping-a-cd.md)
</dt> <dt>

[**Recuperación de la interfaz de copia desde CD**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Inicio del proceso RIP**](starting-the-rip-process.md)
</dt> <dt>

[**Seleccionar elementos para copiar desde CD**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




