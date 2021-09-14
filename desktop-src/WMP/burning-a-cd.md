---
title: Grabación de un CD
description: Grabación de un CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Reproductor de Windows Media,cds
- Reproductor de Windows Media modelo de objetos, cds
- modelo de objetos, grabación de CD
- Reproductor de Windows Media ActiveX control, grabación de CD
- ActiveX control, grabación de CD
- Reproductor de Windows Media Control de ActiveX móvil, grabación de CD
- Reproductor de Windows Media Móvil, cds
- Grabación de CD, acerca de
- cds, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889537"
---
# <a name="burning-a-cd"></a>Grabación de un CD

En esta sección se describe cómo usar la [interfaz IWMPCdromRomRom Para](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) grabar música en un CD. La **interfaz IWMPCdromGnición proporciona** funcionalidad para grabar listas de reproducción en CD como pistas de datos o audio, así como para borrar CD-RW.

Uso de código

Los ejemplos de código de esta sección usan Active Template Library (ATL), como **CComPtr**.

Encabezados incluidos

Para usar el código de esta sección, incluya los encabezados siguientes:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



Punteros de interfaz

Las interfaces de Reproductor de Windows Media se almacenan en las siguientes variables miembro:


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



En los temas siguientes se describe cómo usar la API de grabación de CD.

-   [Recuperación de la interfaz de grabación de CD](retrieving-the-cd-burning-interface.md)
-   [Iniciar el proceso de grabación](starting-the-burn-process.md)
-   [Borrado de un CD reescrito](erasing-a-rewritable-cd.md)
-   [Recuperar el estado de la unidad y el disco](retrieving-the-drive-and-disc-status.md)
-   [Recuperación del estado de grabación](retrieving-the-burn-status.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de control de reproductor**](player-control-guide.md)
</dt> </dl>

 

 




