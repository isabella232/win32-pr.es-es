---
title: Referencia de Command-Line de MIDL
description: Esta sección contiene información de referencia para cada modificador de línea de comandos y opción de modificador que reconoce el compilador de MIDL de Microsoft RPC.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, referencia
- referencia de la línea de comandos MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1569e29daf8a2976379576a5f1671f5117e7990c
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105666095"
---
# <a name="midl-command-line-reference"></a>Referencia de Command-Line de MIDL

Esta sección contiene información de referencia para cada modificador de línea de comandos y opción de modificador que reconoce el compilador de MIDL de Microsoft RPC. Las entradas de conmutador están organizadas en orden alfabético. La [Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md) describe la sintaxis de línea de comandos general.

<dl>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)  
[Comando de archivo de respuesta](the-response-file-command.md)  
[**/acf**](-acf.md)  
[**especific**](-align.md)  
[**/amd64**](-amd64.md)  
[**configuración de/APP \_**](-app-config.md)  
[compatibilidad con/backward \_](-backward-compat.md)  
[**/c \_ ext**](-c-ext.md)  
[**/caux**](-caux.md)  
[**/Char**](-char.md)  
[**/Client**](-client.md)  
[**/confirm**](-confirm.md)  
[**/CPP \_ cmd**](-cpp-cmd.md)  
[**/CPP \_ OPC**](-cpp-opt.md)  
[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)  
[**/D.**](-d.md)  
[**/dlldata**](-dlldata.md)  
[**/ENV**](-env.md)  
[**/error**](-error.md)  
[**/error**](-error.md)  
[**/h**](-h.md)  
[**/header**](-header.md)  
[**/Help (/?)**](-help-.md)  
[**/ia64**](-ia64.md)  
[**/I**](-i.md)  
[**/IID**](-iid.md)  
[**/Import**](-import.md)  
[**/LCID**](-lcid.md)  
[**/mktyplib203**](-mktyplib203.md)  
[**\_ext/MS**](-ms-ext.md)  
[**\_Unión/MS**](-ms-union.md)  
[**/MSC \_ ver**](-msc-ver.md)  
[**/pedidos nuevos**](-new.md)  
[**/newtlb**](-newtlb.md)  
[**/no \_ CPP,/nocpp**](-no-cpp-nocpp.md)  
[**/no \_ default \_ EPV**](-no-default-epv.md)  
[**/no \_ Def \_ Idir**](-no-def-idir.md)  
[**/no \_ format \_ OPC**](-no-format-opt.md)  
[**/no \_ robusto**](-no-robust.md)  
[**/no \_ WARN**](-no-warn.md)  
[**/nologo**](-nologo.md)  
[**/notlb**](-notlb.md)  
[**/o**](-o.md)  
[**/OI**](-oi.md)  
[**/Old**](-old.md)  
[**/oldtlb**](-oldtlb.md)  
[**/oldnames**](-oldnames.md)  
[**/Os**](-os.md)  
[**/osf**](-osf.md)  
[**/out**](-out.md)  
[**/Pack**](-pack.md)  
[**/prefix**](-prefix.md)  
[**/Protocolo**](-protocol.md)  
[**/proxy**](-proxy.md)  
[**/Robust**](-robust.md)  
[**/rpcss**](-rpcss.md)  
[**/sal**](-sal.md)  
[**/sal \_ local**](-sal-local.md)  
[**/saux**](-saux.md)  
[**/savePP**](-savepp.md)  
[**/sstub**](-sstub.md)  
[**comprobación de/Syntax \_**](-syntax-check.md)  
[**/<system>**](-system-.md)  
[**/Target**](-target.md)  
[**/TLB**](-tlb.md)  
[**/U**](-u.md)  
[**/Use \_ EPV**](-use-epv.md)  
[**\_marca/version**](-version-stamp.md)  
[**/W**](-w.md)  
[**/WARN**](-warn.md)  
[**/win32**](-win32.md)  
[**/win64**](-win64.md)  
[**/WX**](-wx.md)  
[**/ZP**](-zp.md)  
[**/ZS**](-zs.md)  
</dl>

El compilador MIDL puede generar código para distintas plataformas y versiones del sistema. Consulte el modificador [**/target**](-target.md) para obtener más información acerca de los modificadores sugeridos y cómo generar código optimizado para una versión determinada.

Tenga en cuenta que el signo menos (–) se puede sustituir por la barra diagonal (/) en todos los modificadores de la línea de comandos de MIDL que comienzan por una barra diagonal (/). En el ejemplo siguiente se muestra su equivalencia al invocar el compilador de MIDL.

## <a name="examples"></a>Ejemplos

**MIDL/ACF My \_ ACF. ACF** *filename * * *. idl**

**MIDL-ACF My \_ ACF. ACF** *filename * * *. idl**

 

 




