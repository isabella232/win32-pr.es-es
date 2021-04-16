---
title: Inicio del proceso RIP
description: Inicio del proceso RIP
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- Copiar CD, iniciar el proceso RIP
- copiar CDs, iniciar el proceso RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695538"
---
# <a name="starting-the-rip-process"></a>Inicio del proceso RIP

Una vez que haya recuperado la interfaz de copia desde CD como se explicó en la sección anterior, inicie el proceso de copia desde CD llamando a [IWMPCdromRip:: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



Puede detener la operación de copia desde CD llamando a [IWMPCdromRip:: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Copia desde CD**](ripping-a-cd.md)
</dt> <dt>

[**Recuperación de la interfaz de copia desde CD**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Recuperación del estado de RIP**](retrieving-the-rip-status.md)
</dt> <dt>

[**Seleccionar elementos para copiar desde CD**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




