---
title: Selección de elementos para Resalte
description: Selección de elementos para Resalte
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Reproductor de Windows Media,CD
- Reproductor de Windows Media modelo de objetos, cds
- modelo de objetos, cds
- Reproductor de Windows Media ActiveX control de datos, cds
- ActiveX control de datos, cds
- Reproductor de Windows Media Control de ActiveX dispositivos móviles,cds
- Reproductor de Windows Media Móvil, cds
- CD agarrón, selección de elementos
- CDs de resalte, selección de elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc18ded43b609be6c7ac1f16833b0c8a33505ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070861"
---
# <a name="selecting-items-for-ripping"></a>Selección de elementos para Resalte

A veces, un usuario no quiere extraer todas las pistas de un CD. Reproductor de Windows Media proporciona una interfaz para especificar las pistas que se seleccionan para la eliminación. Normalmente, en una aplicación de cd- a-cd hay una interfaz de usuario que permite al usuario activar las casillas de una lista de pistas en el CD.

Es posible que algunas pistas no se seleccionen para la instalación de forma predeterminada. Si una pista ya está en la Reproductor de Windows Media, no se seleccionará automáticamente para la eliminación. En el segundo ejemplo de código de esta sección se muestra cómo omitir el valor predeterminado y seleccionar manualmente una pista para su omisión si ya se ha convertido en un error.

En el ejemplo de código siguiente se muestra cómo determinar si se ha seleccionado una pista para la prueba:


```C++
HRESULT CMainDlg::IsTrackSelected(long lIndex, bool &bSelected)
{
    // The track is selected unless the
    // "SelectedForRip" attribute is true.
    bSelected = true;

    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Check whether it is selected for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(
            bstrItemName,
            &bstrVal);
    }
    if (SUCCEEDED(hr))
    {
        // If getItemInfo("SelectedForRip") is not "True"
        // then the track is not selected.
        if (wcscmp(bstrVal.m_str, L"True"))
            bSelected = false;
    }

    return hr;
}

```



En el ejemplo de código siguiente se muestra cómo especificar si se selecciona una pista para la especificaciones.


```C++
HRESULT CMainDlg::SelectTrack (long lIndex, bool bSelected)
{
    // bstrItemName and bstrVal are used for setItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Select the track for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        if (bSelected)
        {
            hr = bstrVal.Append("True");
        }
        else
        {
            hr = bstrVal.Append("False");
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->setItemInfo(
            bstrItemName,
            bstrVal);
    }

    return hr;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Resalte un CD**](ripping-a-cd.md)
</dt> <dt>

[**Recuperación de la interfaz de copia desde CD**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Iniciar el proceso de desgarrón**](starting-the-rip-process.md)
</dt> <dt>

[**Recuperación del estado de desgarr**](retrieving-the-rip-status.md)
</dt> </dl>

 

 




