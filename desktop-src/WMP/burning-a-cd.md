---
title: Grabación de un CD
description: Grabación de un CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player, grabación de CD
- Modelo de objetos de Windows Media Player, grabación de CD
- modelo de objetos, grabación de CD
- Control ActiveX de Windows Media Player, grabación de CD
- Control ActiveX, grabación de CD
- Control ActiveX móvil de Windows Media Player, grabación de CD
- Windows Media Player Mobile, grabación de CD
- Grabación de CD, acerca de
- grabar CDs, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149090"
---
# <a name="burning-a-cd"></a>Grabación de un CD

En esta sección se describe cómo usar la interfaz [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) para grabar música en un CD. La interfaz **IWMPCdromBurn** proporciona funcionalidad para grabar listas de reproducción en CDs como datos o pistas de audio, así como para borrar CD-RW.

Uso del código

En los ejemplos de código de esta sección se usan las clases Active Template Library (ATL), como **CComPtr**.

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

Las interfaces para Media Player de Windows se almacenan en las siguientes variables miembro:


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
-   [Borrado de un CD regrabable](erasing-a-rewritable-cd.md)
-   [Recuperación de la unidad y el estado del disco](retrieving-the-drive-and-disc-status.md)
-   [Recuperación del estado de la grabación](retrieving-the-burn-status.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de control del reproductor**](player-control-guide.md)
</dt> </dl>

 

 




