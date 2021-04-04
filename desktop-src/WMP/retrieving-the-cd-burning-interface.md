---
title: Recuperación de la interfaz de grabación de CD
description: Recuperación de la interfaz de grabación de CD
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player, grabación de CD
- Modelo de objetos de Windows Media Player, grabación de CD
- modelo de objetos, grabación de CD
- Control ActiveX de Windows Media Player, grabación de CD
- Control ActiveX, grabación de CD
- Control ActiveX móvil de Windows Media Player, grabación de CD
- Windows Media Player Mobile, grabación de CD
- Grabación de CD, recuperación de la interfaz IWMPCdromCollection
- grabación de CDs, recuperación de la interfaz IWMPCdromCollection
- Interfaz IWMPCdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077433"
---
# <a name="retrieving-the-cd-burning-interface"></a>Recuperación de la interfaz de grabación de CD

Para enumerar las unidades de CD en el equipo del usuario, use la interfaz **IWMPCdromCollection** . Para recuperar un puntero a esta interfaz, llame a [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

Mediante el uso de los métodos **Get \_ Count** y **Item** , puede recorrer en iteración la colección para recuperar un puntero de la interfaz [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) para cada unidad de CD del equipo del usuario.

La interfaz **IWMPCdrom** representa una unidad de CD individual. Antes de empezar a grabar un CD, primero debe llamar a **QueryInterface** a través de un puntero **IWMPCdrom** para recuperar un puntero a la interfaz [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) .

En el ejemplo de código siguiente se muestra cómo recuperar una interfaz para grabar un CD en una unidad específica:


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Grabación de un CD**](burning-a-cd.md)
</dt> <dt>

[**Iniciar el proceso de grabación**](starting-the-burn-process.md)
</dt> <dt>

[**Borrado de un CD regrabable**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recuperación de la unidad y el estado del disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recuperación del estado de la grabación**](retrieving-the-burn-status.md)
</dt> <dt>

[**Interfaz IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




