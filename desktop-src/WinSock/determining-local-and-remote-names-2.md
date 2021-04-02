---
description: WSPGetSockName se utiliza para recuperar la dirección local para Sockets enlazados.
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: Determinar los nombres locales y remotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082122"
---
# <a name="determining-local-and-remote-names"></a>Determinar los nombres locales y remotos

[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) se utiliza para recuperar la dirección local para Sockets enlazados. Esto es especialmente útil cuando se ha realizado una llamada a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) sin hacer un [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) primero; **WSPGetSockName** proporciona el único medio para determinar la asociación local que el proveedor ha establecido implícitamente.

Una vez configurada una conexión, se puede usar [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) para determinar la dirección del elemento del mismo nivel al que está conectado un socket.

 

 
