---
title: Recuperación de la interfaz de copia desde CD
description: Recuperación de la interfaz de copia desde CD
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- Copia desde CD, interfaz de IWMPCdromRip
- copia desde CD, interfaz de IWMPCdromRip
- Interfaz IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903fa285404700e35363a94239c79706e7af0e34
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103904439"
---
# <a name="retrieving-the-ripping-interface"></a>Recuperación de la interfaz de copia desde CD

Para enumerar las unidades de CD en el equipo del usuario, use la interfaz **IWMPCdromCollection** . Recupere un puntero a esta interfaz llamando a [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

Mediante el uso de los métodos [Get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) y [Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) , puede recorrer en iteración la colección para recuperar una interfaz [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) para cada unidad de CD en el equipo del usuario.

La interfaz **IWMPCdrom** representa una unidad de CD individual. Antes de empezar a copiar un CD, primero debe llamar a **QueryInterface** a través de un puntero **IWMPCdrom** para recuperar la interfaz [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) .

En el ejemplo de código siguiente se muestra cómo recuperar una interfaz para copiar desde CD desde una unidad específica:


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

[**Copia desde CD**](ripping-a-cd.md)
</dt> <dt>

[**Inicio del proceso RIP**](starting-the-rip-process.md)
</dt> <dt>

[**Recuperación del estado de RIP**](retrieving-the-rip-status.md)
</dt> <dt>

[**Seleccionar elementos para copiar desde CD**](selecting-items-for-ripping.md)
</dt> <dt>

[**Interfaz IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




