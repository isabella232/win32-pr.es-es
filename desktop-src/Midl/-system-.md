---
title: /conmutador del sistema
description: El modificador/System indica al compilador de MIDL que genere una biblioteca de tipos para el sistema especificado. El valor predeterminado es el sistema operativo actual.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /modificador del sistema MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e09f2cf97f8edb86ad831cff35420fad9a07d76
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358145"
---
# <a name="system-switch"></a>/<system> conmutador

El **/<system>** modificador indica al compilador de MIDL que genere una biblioteca de tipos para el sistema especificado. El valor predeterminado es el sistema operativo actual.

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Windows 2000, Windows XP, Windows Vista, Windows 7

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * *


</dt> <dd>

Un entorno Windows de 64 de 64 bits basado en Intel, como Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>AMD64 * * * *


</dt> <dd>

Un entorno de Windows de 64 bits basado en dispositivos de American micro, como Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

El **/<system>** modificador es funcionalmente igual que la opción de MIDL [**/env**](-env.md) y el COMpilador MIDL lo reconoce únicamente para mantener la compatibilidad con MkTypLib. Si va a generar un nuevo archivo make, use el modificador **/env** .

## <a name="examples"></a>Ejemplos

**MIDL/Win32 nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ENV**](-env.md)
</dt> </dl>

 

 




