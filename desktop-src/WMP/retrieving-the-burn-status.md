---
title: Recuperación del estado de la grabación
description: Recuperación del estado de la grabación
ms.assetid: 63b6525d-00be-4c68-8473-3bc1a58fde15
keywords:
- Windows Media Player, grabación de CD
- Modelo de objetos de Windows Media Player, grabación de CD
- modelo de objetos, grabación de CD
- Control ActiveX de Windows Media Player, grabación de CD
- Control ActiveX, grabación de CD
- Control ActiveX móvil de Windows Media Player, grabación de CD
- Windows Media Player Mobile, grabación de CD
- Grabación de CD, recuperación del estado de la grabación
- grabar CDs, recuperar el estado de la grabación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9b9ab1d865b728c3a23b9b77f45ab022226605
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994963"
---
# <a name="retrieving-the-burn-status"></a>Recuperación del estado de la grabación

En el ejemplo de código siguiente, se definen los siguientes controles de cuadro de diálogo:



| Id. de control           | Descripción                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| \_Estado de grabación de IDC \_     | Texto estático que representa el estado de la operación de grabación de CD.             |
| progreso de IDC \_        | Barra de progreso con un intervalo de 0 a 100 que representa el progreso total de la grabación. |
| \_texto de progreso de IDC \_  | Texto estático que representa el progreso de la grabación total como un número comprendido entre 0 y 100. |
| \_hora disponible de IDC \_ | Texto estático para mostrar la hora disponible en el CD, en segundos.               |
| \_espacio libre de IDC \_     | Texto estático para mostrar el espacio disponible en el CD, en bytes.                     |
| \_espacio total de IDC \_    | Texto estático que muestra la capacidad total del CD, en bytes.                 |



 

Puede supervisar el progreso de la operación de grabación llamando periódicamente a [IWMPCdromBurn:: get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) mientras se graba el CD. Este método recupera un valor de progreso para toda la operación de grabación. El valor recuperado es un número que representa el porcentaje de grabación completada, de 0 a 100.


```C++
// Update the progress bar IDC_PROGRESS
// and the corresponding text string IDC_PROGRESS_TEXT.
long lProgress = 0;
hr = m_spCdromBurn->get_burnProgress(&lProgress);
if (SUCCEEDED(hr))
{
    SendMessage(GetDlgItem(IDC_PROGRESS),
        PBM_SETPOS, lProgress, 0);
    SetDlgItemInt(IDC_PROGRESS_TEXT, lProgress);
}

```



Puede obtener el estado actual de la operación de grabación llamando a [IWMPCdromBurn:: get \_ burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate). Este método recupera una enumeración que especifica la operación actual que se está llevando a cabo.


```C++
// Retrieve the burn state.
WMPBurnState wmpbs = wmpbsUnknown;
HRESULT hr = m_spCdromBurn->get_burnState(&wmpbs);

if (SUCCEEDED(hr))
{
    // Set the burn state string.
    CComBSTR bstrState;
    switch (wmpbs)
    {
        case wmpbsUnknown:
        default:
            hr = bstrState.Append("Unknown state.");
            break;
        case wmpbsBusy:
            hr = bstrState.Append("Windows Media Player is Busy.");
            break;
        case wmpbsReady:
            hr = bstrState.Append("Ready to begin burning.");
            break;
        case wmpbsWaitingForDisc:
            hr = bstrState.Append("Waiting for disc.");
            break;
        case wmpbsRefreshStatusPending:
            hr = bstrState.Append("The burn playlist has changed.");
            m_spCdromBurn->refreshStatus();
            break;
        case wmpbsPreparingToBurn:
            hr = bstrState.Append("Preparing to burn the CD.");
            break;
        case wmpbsBurning:
            hr = bstrState.Append("The CD is being burned.");
            break;
        case wmpbsStopped:
            hr = bstrState.Append("The burning operation is stopped.");
            break;
        case wmpbsErasing:
            hr = bstrState.Append("Erasing the CD.");
            break;
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_BURN_STATE, bstrState.m_str);
    }
}

```



Para recuperar el número de segundos de audio que puede contener el CD, llame a [IWMPCdromBurn:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) con "AvailableTime" como primer parámetro. El valor recuperado por esta función se representa mediante una cadena.


```C++
// Set "AvailableTime" string
CComBSTR bstrTime;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("AvailableTime");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTime);
}
if (SUCCEEDED(hr))
{
    hr = bstrTime.Append(" seconds");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_AVAILABLE_TIME, bstrTime.m_str);
}

```



Para recuperar la cantidad de espacio libre en un disco, llame a **IWMPCdromBurn:: getItemInfo** con "FreeSpace" como primer parámetro. El valor recuperado por esta función es una cadena que representa el número de bytes libres disponibles en el disco.


```C++
// Set "FreeSpace" string
CComBSTR bstrFreeSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("FreeSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrFreeSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrFreeSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_FREE_SPACE, bstrFreeSpace.m_str);
}

```



Para recuperar la capacidad total de un disco, llame a **IWMPCdromBurn:: getItemInfo** con "TotalSpace" como primer parámetro. El valor recuperado por esta función es una cadena que corresponde al número total de bytes del disco.


```C++
// Set "TotalSpace" string.
CComBSTR bstrTotalSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("TotalSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTotalSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrTotalSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_TOTAL_SPACE, bstrTotalSpace.m_str);
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Grabación de un CD**](burning-a-cd.md)
</dt> <dt>

[**Recuperación de la interfaz de grabación de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Iniciar el proceso de grabación**](starting-the-burn-process.md)
</dt> <dt>

[**Borrado de un CD regrabable**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recuperación de la unidad y el estado del disco**](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




