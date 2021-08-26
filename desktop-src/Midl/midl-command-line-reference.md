---
title: Referencia de Command-Line MIDL
description: Esta sección contiene información de referencia para cada modificador de línea de comandos y opción de modificador reconocido por el compilador MIDL de RPC de Microsoft.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, referencia
- referencia de la línea de comandos MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df927ded3f1a46045437fe1f9e72e2c7f80dd17d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887351"
---
# <a name="midl-command-line-reference"></a>Referencia de Command-Line MIDL

Esta sección contiene información de referencia para cada modificador de línea de comandos y opción de modificador reconocido por el compilador MIDL de RPC de Microsoft. Las entradas switch se organizan en orden alfabético. [Sintaxis general de la línea de](general-midl-command-line-syntax.md) comandos midL describe la sintaxis general de la línea de comandos.

<dl>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)  
[El comando archivo de respuesta](the-response-file-command.md)  
[**/acf**](-acf.md)  
[**/align**](-align.md)  
[**/amd64**](-amd64.md)  
[**/app \_ config**](-app-config.md)  
[/backward \_ compat](-backward-compat.md)  
[**/c \_ ext**](-c-ext.md)  
[**/caux**](-caux.md)  
[**/char**](-char.md)  
[**/client**](-client.md)  
[**/confirm**](-confirm.md)  
[**/cpp \_ cmd**](-cpp-cmd.md)  
[**/cpp \_ opt**](-cpp-opt.md)  
[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)  
[**/D**](-d.md)  
[**/dlldata**](-dlldata.md)  
[**/env**](-env.md)  
[**/error**](-error.md)  
[**/error**](-error.md)  
[**/h**](-h.md)  
[**/header**](-header.md)  
[**/help (/?)**](-help-.md)  
[**/ia64**](-ia64.md)  
[**/I**](-i.md)  
[**/iid**](-iid.md)  
[**/import**](-import.md)  
[**/lcid**](-lcid.md)  
[**/mktyplib203**](-mktyplib203.md)  
[**/ms \_ ext**](-ms-ext.md)  
[**/ms \_ union**](-ms-union.md)  
[**/msc \_ ver**](-msc-ver.md)  
[**/new**](-new.md)  
[**/newtlb**](-newtlb.md)  
[**/no \_ cpp, /nocpp**](-no-cpp-nocpp.md)  
[**/no \_ default \_ epv**](-no-default-epv.md)  
[**/no \_ def \_ idir**](-no-def-idir.md)  
[**/no \_ format \_ opt**](-no-format-opt.md)  
[**/no \_ robust**](-no-robust.md)  
[**/no \_ warn**](-no-warn.md)  
[**/nologo**](-nologo.md)  
[**/notlb**](-notlb.md)  
[**/o**](-o.md)  
[**/Oi**](-oi.md)  
[**/old**](-old.md)  
[**/oldtlb**](-oldtlb.md)  
[**/oldnames**](-oldnames.md)  
[**/Os**](-os.md)  
[**/osf**](-osf.md)  
[**/out**](-out.md)  
[**/pack**](-pack.md)  
[**/prefix**](-prefix.md)  
[**/protocol**](-protocol.md)  
[**/proxy**](-proxy.md)  
[**/robust**](-robust.md)  
[**/rpcss**](-rpcss.md)  
[**/sal**](-sal.md)  
[**/sal \_ local**](-sal-local.md)  
[**/s domain**](-saux.md)  
[**/savePP**](-savepp.md)  
[**/sstub**](-sstub.md)  
[**/syntax \_ check**](-syntax-check.md)  
[**/&lt;sistema&gt;**](-system-.md)  
[**/target**](-target.md)  
[**/tlb**](-tlb.md)  
[**/U**](-u.md)  
[**/use \_ epv**](-use-epv.md)  
[**/version \_ stamp**](-version-stamp.md)  
[**/W**](-w.md)  
[**/warn**](-warn.md)  
[**/win32**](-win32.md)  
[**/win64**](-win64.md)  
[**/WX**](-wx.md)  
[**/Zp**](-zp.md)  
[**/Zs**](-zs.md)  
</dl>

El compilador MIDL puede generar código para distintas plataformas y versiones del sistema. Consulte el [**modificador /target**](-target.md) para obtener más información sobre los modificadores sugeridos y cómo generar código optimizado para una versión determinada.

Tenga en cuenta que el signo menos (–) se puede sustituir por la barra diagonal (/) en todos los modificadores de línea de comandos midL que comienzan por una barra diagonal (/). En el ejemplo siguiente se muestra su equivalencia al invocar el compilador MIDL.

## <a name="examples"></a>Ejemplos

**midl /acf my \_ acf.acf** *filename**

**midl -acf my \_ acf.acf** *filename**.idl**

 

 




