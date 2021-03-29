---
title: Copia desde CD mediante la interfaz IWMPCdromRip
description: Copia desde CD mediante la interfaz IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
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
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904412"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Copia desde CD mediante la interfaz IWMPCdromRip

En esta sección se describe cómo usar la interfaz [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) para copiar música desde un CD.

La copia desde CD mediante la interfaz **IWMPCdromRip** tiene el mismo efecto que la copia de música mediante la interfaz de usuario de Windows Media Player. El contenido copiado se agrega automáticamente a la biblioteca según las preferencias del usuario. Para obtener más información acerca de la copia de CD, consulte la sección acerca de la copia de música desde CDs en la ayuda de Windows Media Player.

En los ejemplos de código de esta sección se usan las clases Active Template Library (ATL), como **CComPtr**.

## <a name="included-headers"></a>Encabezados incluidos

Para usar el código de esta sección, incluya los encabezados siguientes:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a>Punteros de interfaz

Las interfaces de Media Player de Windows se almacenan en las siguientes variables de miembro.


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



En las secciones siguientes se describe cómo usar la interfaz IWMPCdromRip

-   [Recuperación de la interfaz de copia desde CD](retrieving-the-ripping-interface.md)
-   [Inicio del proceso RIP](starting-the-rip-process.md)
-   [Recuperación del estado de RIP](retrieving-the-rip-status.md)
-   [Seleccionar elementos para copiar desde CD](selecting-items-for-ripping.md)

 

 




