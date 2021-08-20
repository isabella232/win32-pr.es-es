---
description: A continuación se muestra una lista de los archivos .lib necesarios para compilar varias aplicaciones TAPI 3, a partir del 22/1/01.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Bibliotecas necesarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8337042681d84b5f93d5d0218cff18c4bef9259543f60fd13f692ebe5611835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621365"
---
# <a name="libraries-required"></a>Bibliotecas necesarias

Una lista de archivos .lib necesarios para compilar varias aplicaciones TAPI 3, a partir del 22/1/01:

-   Advapi32.lib
-   Amstrmid.lib (GUID de ActiveMovie)
-   Kernel32.lib
-   Mdhcpid.lib (GUID de multidifusión)
-   Ole32.lib (COM)
-   Oleaut32.lib (Automatización COM)
-   Rendid.lib (GUID de Rendezvous)
-   Rpc rpc.lib
-   Rpcns4.lib
-   Rpcrt4.lib
-   Sdpblbid.lib (GUID del Protocolo de descriptor de sesión (SDP)
-   Strmiids.lib
-   User32.lib
-   Uuid.lib
-   Wldap32.lib
-   Ws2 \_ 32.lib

Si usa Microsoft Visual Studio, es posible que tenga que actualizar la versión. En concreto, Link.exe debe llevar una fecha del 19/03/98 o posterior.

Las define el compilador deben incluir WINNT WIN32 establecido en al menos \_ 0x500 y \_ \_ WIN32 \_ DCOM.

 

 



