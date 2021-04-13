---
title: Depurar WOW64
description: Las aplicaciones que se ejecutan bajo WOW64 se pueden depurar con un depurador hospedado en x86 o un depurador nativo.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- WOW64 64 bits programación de Windows, depuración
- depuración de la programación de Windows en WOW64 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421274"
---
# <a name="debugging-wow64"></a>Depurar WOW64

Las aplicaciones que se ejecutan bajo WOW64 se pueden depurar de dos maneras:

-   Use un depurador hospedado en x86 como NTSD, WinDbg o Visual Studio. El NTSD de 32 bits se instala en% systemroot% \\ SysWow64 en las instalaciones comerciales. Tenga en cuenta que los depuradores x86 se pueden usar para depurar código x86, pero no se pueden usar para desensamblar o establecer puntos de interrupción dentro de la capa de código thunk de WOW64 porque es código nativo de 64 bits.
-   Use un depurador nativo como CDB, NTSD o WinDbg y la extensión del depurador de WOW64 Wow64exts.dll. Si el depurador nativo se interrumpe mientras el procesador está en modo x86, el depurador presenta el proceso como un proceso x86. Si el procesador está en modo nativo, el depurador presenta el proceso como nativo.

CDB, NTSD y WinDbg se incluyen en herramientas de depuración para Windows. Para obtener más información, vea la documentación de las [herramientas de depuración para Windows](/windows-hardware/drivers/debugger/) .

La extensión del depurador Wow64exts se instala con WinDbg. Use el comando! LOAD wow64exts para cargar la extensión del depurador. En la tabla siguiente se enumeran los comandos de la extensión del depurador! wow64exts.



| Get-Help                | Descripción                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| ! wow64exts. SW          | Cambia entre el modo x86 y el modo nativo.                                                                                                    |
| ! *recuento* de wow64exts. k   | Vuelca un seguimiento combinado de la pila de 32 o 64 bits. Si se especifica *Count* , el comando vuelca las direcciones del primer *recuento* en cada seguimiento de la pila.  |
| ! wow64exts.info        | Vuelca información básica sobre el PEB del proceso, el TEB del subproceso actual y las ranuras de almacenamiento local para el subproceso (TLS) utilizadas por WOW64. |
| *Dirección* de wow64exts. r | Vuelca el contexto de la dirección especificada. Si no se especifica *Address* , el comando vuelca el contexto del procesador.                     |



 

 

 