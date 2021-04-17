---
description: A continuación se muestra una lista de los archivos. lib necesarios para compilar varias aplicaciones TAPI 3, desde 1/22/01.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Bibliotecas requeridas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0948599041c466a337d2d6828750a9996dc8d813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677481"
---
# <a name="libraries-required"></a>Bibliotecas requeridas

Una lista de archivos. lib necesarios para compilar varias aplicaciones TAPI 3, desde 1/22/01:

-   Advapi32. lib
-   Amstrmid. lib (GUID de ActiveMovie)
-   Kernel32.lib
-   Mdhcpid. lib (GUID de multidifusión)
-   Ole32. lib (COM)
-   Oleaut32. lib (automatización COM)
-   Rendid. lib (GUID de encuentro)
-   Rpcndr. lib
-   Rpcns4. lib
-   Rpcrt4. lib
-   Sdpblbid. lib (GUID del Protocolo de descriptor de sesión (SDP))
-   Strmiids. lib
-   User32. lib
-   UUID. lib
-   Wldap32. lib
-   Ws2 \_ 32. lib

Si usa Microsoft Visual Studio, es posible que tenga que actualizar la versión. En concreto, Link.exe debe llevar una fecha 3/19/98 o posterior.

La definición del compilador debe incluir \_ Win32 \_ WinNT establecido en al menos 0x500 y \_ Win32 \_ DCOM.

 

 



