---
title: parámetro/env
description: El modificador/env selecciona el entorno en el que se ejecuta la aplicación.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- /ENV (modificador) MIDL
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420582"
---
# <a name="env-switch"></a>parámetro/env

El modificador **/env** selecciona el entorno en el que se ejecuta la aplicación.

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Indica al compilador de MIDL que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de 32 bits.

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * *


</dt> <dd>

Indica al compilador de MIDL que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de arquitectura Intel 64 bits (IA64).

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>AMD64 * * * *


</dt> <dd>

Indica al compilador de MIDL que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de micro de64 Vices (AMD64) avanzado.

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span id="win64"></span><span id="WIN64"></span>Win64 * * * *


</dt> <dd>

Mismo comportamiento que *ia64*.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

El modificador **/env** afecta principalmente al nivel de empaquetado utilizado para las estructuras de ese entorno. Asegúrese de especificar la misma configuración de nivel de empaquetado para el compilador de MIDL y el compilador de C.

El modificador **/env** determina el nivel de empaquetado y otras opciones de configuración como se indica a continuación:

-   Cuando se especifica **Win32**, el código auxiliar generado usa el nivel de empaquetado del compilador de C para todos los tipos implicados en las operaciones remotas. Los tipos de datos [**int**](int.md) son de 32 bits. Los punteros son de 32 bits.
-   Cuando se especifica **ia64** o **AMD64**, el compilador MIDL se ejecuta en modo de compilador cruzado para la plataforma indicada (Intel o AMD) 64 bits. El código auxiliar generado usa el nivel de empaquetado del compilador C 8 para todos los tipos implicados en las operaciones remotas. Los tipos de datos [**Long**](long.md) e [**int**](int.md) son de 32 bits. Los punteros son de 64 bits.

Los modificadores [**/align**](-align.md), [**/Pack**](-pack.md)y [**/ZP**](-zp.md) tienen prioridad sobre la configuración de **/env** .

Para obtener más información sobre la compatibilidad con 64 bits para MIDL y RPC, vea [diseñar interfaces compatibles con 64 bits](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).

## <a name="examples"></a>Ejemplos

**MIDL/env Win32 FILENAME. idl**

**MIDL/env ia64 nombreDeArchivo. idl**

**MIDL/env AMD64 nombreDeArchivo. idl**

**MIDL/env Win64 nombreDeArchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Pack**](-pack.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 