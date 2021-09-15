---
title: Resalte mediante la interfaz IWMPCdromRip
description: Resalte mediante la interfaz IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Reproductor de Windows Media,CD
- Reproductor de Windows Media modelo de objetos, cd-
- modelo de objetos, cds
- Reproductor de Windows Media ActiveX control de datos, cds
- ActiveX control, cds
- Reproductor de Windows Media Control de ActiveX dispositivos móviles,cds
- Reproductor de Windows Media Móvil, cds
- Interfaz CD estamp, IWMPCdromRip
- CDs de ette, interfaz IWMPCdromRip
- IWMPCdromRip (interfaz)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476179"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Resalte mediante la interfaz IWMPCdromRip

En esta sección se describe cómo usar la [interfaz IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) para extraer música de un CD.

El uso de la interfaz **IWMPCdromRip** de un CD tiene el mismo efecto que la música de sonido mediante Reproductor de Windows Media interfaz de usuario. El contenido desasistido se agrega automáticamente a la biblioteca según las preferencias del usuario. Para obtener más información sobre el cds, vea " Resalte música de CDs" en Reproductor de Windows Media Ayuda.

Los ejemplos de código de esta sección usan Active Template Library (ATL), como **CComPtr**.

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

Las interfaces de Reproductor de Windows Media se almacenan en las siguientes variables miembro.


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
-   [Iniciar el proceso de desgarrón](starting-the-rip-process.md)
-   [Recuperación del estado de desgarr](retrieving-the-rip-status.md)
-   [Selección de elementos para Resalte](selecting-items-for-ripping.md)

 

 




