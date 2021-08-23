---
title: Selección de elementos para Alcándalo
description: Selección de elementos para Alcándalo
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Reproductor de Windows Media,CD al día
- Reproductor de Windows Media modelo de objetos, algarada de CD
- modelo de objetos, resalte de CD
- Reproductor de Windows Media ActiveX control, cds
- ActiveX control, cds
- Reproductor de Windows Media Control ActiveX dispositivos móviles,cd- estad
- Reproductor de Windows Media Móvil, cds
- Cd al, seleccionar elementos
- CDs de arras, selección de elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea677028fab6b3c39466e916bd8bb59ea8cee4d370730c096cbb98978f4abc49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646655"
---
# <a name="selecting-items-for-ripping"></a>Selección de elementos para Alcándalo

A veces, un usuario no quiere extraer todas las pistas de un CD. Reproductor de Windows Media proporciona una interfaz para especificar qué pistas se seleccionan para la eliminación. Normalmente, en una aplicación de registro de CD hay una interfaz de usuario que permite al usuario activar las casillas de una lista de pistas en el CD.

Es posible que algunas pistas no se seleccionen para la omisión de forma predeterminada. Si una pista ya está en la biblioteca Reproductor de Windows Media, no se seleccionará automáticamente para la eliminación. En el segundo ejemplo de código de esta sección se muestra cómo omitir el valor predeterminado y seleccionar manualmente una pista para la extracción si ya se ha roto.

En el ejemplo de código siguiente se muestra cómo determinar si se selecciona una pista para el arraigo:


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



En el ejemplo de código siguiente se muestra cómo especificar si se selecciona una pista para el arraigo.


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

[**Arrasar un CD**](ripping-a-cd.md)
</dt> <dt>

[**Recuperación de la interfaz de copia desde CD**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Iniciar el proceso de desgarr**](starting-the-rip-process.md)
</dt> <dt>

[**Recuperar el estado de desgarr**](retrieving-the-rip-status.md)
</dt> </dl>

 

 




