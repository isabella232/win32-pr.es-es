---
title: Depuración de WOW64
description: Las aplicaciones que se ejecutan en WOW64 se pueden depurar con un depurador hospedado en x86 o un depurador nativo.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- WOW64 64 bits Windows programación , depuración
- depuración de WOW64 de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa0f101f382239d146cf668e46efc245753f86ec3c876087f9a4a94bbd356f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121815"
---
# <a name="debugging-wow64"></a>Depuración de WOW64

Las aplicaciones que se ejecutan en WOW64 se pueden depurar de dos maneras:

-   Use un depurador hospedado en x86, como NTSD, WinDbg o Visual Studio. NtSD de 32 bits se instala en %systemroot% \\ syswow64 en instalaciones comerciales. Tenga en cuenta que los depuradores x86 se pueden usar para depurar código x86, pero no se pueden usar para desensamblar o establecer puntos de interrupción dentro de la capa wow64 thunk porque es código nativo de 64 bits.
-   Use un depurador nativo como CDB, NTSD o WinDbg y la extensión del depurador WOW64, Wow64exts.dll. Si el depurador nativo se interrumpe mientras el procesador está en modo x86, el depurador presenta el proceso como un proceso x86. Si el procesador está en modo nativo, el depurador presenta el proceso como nativo.

CDB, NTSD y WinDbg se incluyen en Herramientas de depuración para Windows. Para obtener más información, vea [la documentación sobre las herramientas de Windows](/windows-hardware/drivers/debugger/) depuración.

La extensión del depurador Wow64exts se instala con WinDbg. Use el comando !load wow64exts para cargar la extensión del depurador. En la tabla siguiente se enumeran los comandos de extensión del depurador !wow64exts.



| Get-Help                | Descripción                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| !wow64exts.sw          | Cambia entre x86 y el modo nativo.                                                                                                    |
| !wow64exts.k *count*   | Vuelca un seguimiento combinado de pila de 32 bits/64 bits. Si se especifica *count,* el comando vuelca las primeras direcciones *de recuento* en cada seguimiento de la pila.  |
| !wow64exts.info        | Vuelca información básica sobre el PEB del proceso, el TEB del subproceso actual y las ranuras de almacenamiento local de subprocesos (TLS) usadas por WOW64. |
| !wow64exts.r *address* | Vuelca el contexto de la dirección especificada. Si *no* se especifica address, el comando vuelca el contexto para el procesador.                     |



 

 

 