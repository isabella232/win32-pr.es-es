---
title: Recuperación de la interfaz de copia desde CD
description: Recuperación de la interfaz de copia desde CD
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Reproductor de Windows Media,CD
- Reproductor de Windows Media modelo de objetos, cds
- modelo de objetos, cds
- Reproductor de Windows Media ActiveX control de datos, cds
- ActiveX control de datos, cds
- Reproductor de Windows Media Control de ActiveX dispositivos móviles,cds
- Reproductor de Windows Media Móvil, cds
- Interfaz CD estamp, IWMPCdromRip
- CDs de ette, interfaz IWMPCdromRip
- IWMPCdromRip (interfaz)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903fa285404700e35363a94239c79706e7af0e34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070890"
---
# <a name="retrieving-the-ripping-interface"></a>Recuperación de la interfaz de copia desde CD

Para enumerar las unidades de CD en el equipo del usuario, use la **interfaz IWMPCdromCollection.** Recupere un puntero a esta interfaz llamando a [IWMPCore::get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

Mediante los métodos [get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) y [item,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) puede iterar la colección para recuperar una interfaz [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) para cada unidad de CD del equipo del usuario.

La **interfaz IWMPCdrom** representa una unidad de CD individual. Antes de empezar a trabajar con un CD, primero debe llamar a **QueryInterface** a través de un puntero **IWMPCdrom** para recuperar la [interfaz IWMPCdromRip.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)

En el ejemplo de código siguiente se muestra cómo recuperar una interfaz para extraer un CD de una unidad específica:


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Resalte un CD**](ripping-a-cd.md)
</dt> <dt>

[**Iniciar el proceso de desgarrón**](starting-the-rip-process.md)
</dt> <dt>

[**Recuperación del estado de desgarr**](retrieving-the-rip-status.md)
</dt> <dt>

[**Selección de elementos para Resalte**](selecting-items-for-ripping.md)
</dt> <dt>

[**IWMPCdromCollection (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




