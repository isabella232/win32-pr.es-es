---
title: Asegar mediante la interfaz IWMPCdromRip
description: Asegar mediante la interfaz IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Reproductor de Windows Media,CD al día
- Reproductor de Windows Media modelo de objetos, desasocución de CD
- modelo de objetos, resalte de CD
- Reproductor de Windows Media ActiveX control de datos, desasocución de CD
- ActiveX control, cds
- Reproductor de Windows Media Control ActiveX dispositivos móviles, cds
- Reproductor de Windows Media Móvil, cds
- Interfaz CD estamp, IWMPCdromRip
- Interfaz IWMPCdromRip y CDs de arras
- Interfaz IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50651629f5a11f13bb27a11927c1f08c33de7162130fd7f10f33fe4c74386692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569801"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Asegar mediante la interfaz IWMPCdromRip

En esta sección se describe cómo usar la [interfaz IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) para extraer música de un CD.

El uso de un CD mediante la interfaz **IWMPCdromRip** tiene el mismo efecto que la música de ala mediante la interfaz Reproductor de Windows Media usuario. El contenido desmesado se agrega automáticamente a la biblioteca según las preferencias del usuario. Para obtener más información sobre la instalación de CD, vea " Resalte la música de CDs" en Reproductor de Windows Media Ayuda.

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
-   [Iniciar el proceso de desgarr](starting-the-rip-process.md)
-   [Recuperar el estado de desgarr](retrieving-the-rip-status.md)
-   [Selección de elementos para Alcándalo](selecting-items-for-ripping.md)

 

 




