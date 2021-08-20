---
title: Iniciar el proceso de grabación
description: Iniciar el proceso de grabación
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Reproductor de Windows Media, cds
- Reproductor de Windows Media de objetos, cds
- modelo de objetos, grabación de CD
- Reproductor de Windows Media ActiveX control, grabación de CD
- ActiveX control, grabación de CD
- Reproductor de Windows Media Control de ActiveX móvil, grabación de CD
- Reproductor de Windows Media Móvil, grabación de CD
- Grabación de CD, inicio del proceso de grabación
- cds de grabación, inicio del proceso de grabación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f5620ba8fa6ab911cf0fd594fd27f139b5061d1383575f861dadfec45dabbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995085"
---
# <a name="starting-the-burn-process"></a>Iniciar el proceso de grabación

Antes de que pueda comenzar la reproducción, debe asignar una lista de reproducción para que se resalte. Use [IWMPCdromPlay::p ut \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) para especificar una lista de reproducción para la grabación.


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



Para obtener información sobre el uso de listas de reproducción, vea [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).

Para iniciar la operación de grabación, llame [a IWMPCdromRomRom::startRom](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



Puede detener la operación de desenmascarado llamando [a IWMPCdromRomRom::stopRom](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Grabación de un CD**](burning-a-cd.md)
</dt> <dt>

[**Recuperación de la interfaz de grabación de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Borrado de un CD reescrito**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recuperar el estado de la unidad y el disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recuperar el estado de la grabación**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




