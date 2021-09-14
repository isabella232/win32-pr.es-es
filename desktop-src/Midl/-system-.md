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
ms.openlocfilehash: 01b6455807aedb99d7bd525c69fffc524dbe25d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159706"
---
# <a name="ltsystemgt-switch"></a>/&lt;conmutador &gt; del sistema

El **/ &lt; modificador &gt;** del sistema indica al compilador MIDL que genere una biblioteca de tipos para el sistema especificado. El valor predeterminado es el sistema operativo actual.

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>Cambiar opciones

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

Un entorno de Windows de 64 bits basado en Micro Devices estadounidense, como Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

El **/ &lt; modificador &gt;** del sistema es funcionalmente el mismo que la opción MIDL [**/env**](-env.md) y el compilador de MIDL lo reconoce únicamente por compatibilidad con versiones anteriores con MkTypLib. Si va a generar un nuevo archivo Make, use el **modificador /env.**

## <a name="examples"></a>Ejemplos

**midl /win32 filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> </dl>

 

 




