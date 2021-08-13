---
title: / conmutador de sistema
description: El modificador /system indica al compilador MIDL que genere una biblioteca de tipos para el sistema especificado. El valor predeterminado es el sistema operativo actual.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /system switch MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31def6297a1a91f6ed28943290a66b544dc368d5a00a91932035a338af50bac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643783"
---
# <a name="system-switch"></a>/<system> Interruptor

El **/<system>** modificador indica al compilador MIDL que genere una biblioteca de tipos para el sistema especificado. El valor predeterminado es el sistema operativo actual.

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>win32**


</dt> <dd>

Windows 2000, Windows XP, Windows Vista, Windows 7

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64**


</dt> <dd>

Un entorno de Windows de 64 bits basado en Intel, como Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64**


</dt> <dd>

Un entorno de Windows de 64 bits basado en American Micro Devices, como Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

El modificador es funcionalmente el mismo que la opción MIDL /env y lo reconoce el compilador midl únicamente por compatibilidad con versiones anteriores con **/<system>** MkTypLib. [](-env.md) Si va a generar un nuevo archivo Make, use el **modificador /env.**

## <a name="examples"></a>Ejemplos

**midl /win32 filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> </dl>

 

 




