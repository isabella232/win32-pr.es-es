---
title: Iniciar el proceso de desgarr
description: Iniciar el proceso de desgarr
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Reproductor de Windows Media,CD al día
- Reproductor de Windows Media modelo de objetos, algarada de CD
- modelo de objetos, resalte de CD
- Reproductor de Windows Media ActiveX control, cds
- ActiveX control, cds
- Reproductor de Windows Media Control ActiveX dispositivos móviles, cds
- Reproductor de Windows Media Móvil, cds
- Cd a, iniciar el proceso de desgarre
- CDs de arras, iniciar el proceso de desgarre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d6d4e7bac4de9fc82f26d7231020e002570553ecdd6447c55f981601e5830a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002165"
---
# <a name="starting-the-rip-process"></a>Iniciar el proceso de desgarr

Una vez que haya recuperado la interfaz de desenlazador, como se explicó en la sección anterior, inicie el proceso de desasociación mediante una llamada a [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



Puede detener la operación de zilla llamando a [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Arrasar un CD**](ripping-a-cd.md)
</dt> <dt>

[**Recuperación de la interfaz de copia desde CD**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Recuperar el estado de desgarr**](retrieving-the-rip-status.md)
</dt> <dt>

[**Selección de elementos para Alcándalo**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




