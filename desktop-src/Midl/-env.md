---
title: Modificador /env
description: El modificador /env selecciona el entorno en el que se ejecuta la aplicación.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- /env switch MIDL
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159756"
---
# <a name="env-switch"></a>Modificador /env

El **modificador /env** selecciona el entorno en el que se ejecuta la aplicación.

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>win32**


</dt> <dd>

Dirige al compilador MIDL para generar archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de 32 bits.

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64**


</dt> <dd>

Dirige al compilador MIDL para que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de arquitectura Intel de 64 bits (IA64).

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64**


</dt> <dd>

Dirige al compilador MIDL para que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno advanced micro devices de 64 bits (AMD64).

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span id="win64"></span><span id="WIN64"></span>win64**


</dt> <dd>

El mismo comportamiento que *ia64.*

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

El **modificador /env** afecta principalmente al nivel de empaquetado utilizado para las estructuras de ese entorno. Asegúrese de especificar la misma configuración de nivel de empaquetado para el compilador MIDL y el compilador de C.

El **modificador /env** determina el nivel de empaquetado y otras opciones de configuración como se muestra a continuación:

-   Al especificar **win32, los** códigos auxiliares generados usan el nivel 8 de empaquetado del compilador de C para todos los tipos implicados en operaciones remotas. Los [**tipos de**](int.md) datos int son de 32 bits. Los punteros son de 32 bits.
-   Al especificar **ia64** o **amd64,** el compilador MIDL se ejecuta en modo entre compiladores para la plataforma de 64 bits indicada (Intel o AMD). Los códigos auxiliares generados usan el nivel 8 de empaquetado del compilador de C para todos los tipos implicados en las operaciones remotas. Los [**tipos de**](long.md) datos long e [**int**](int.md) son de 32 bits. Los punteros son de 64 bits.

Los [**modificadores /align**](-align.md), [**/pack**](-pack.md)y [**/Zp**](-zp.md) tienen prioridad sobre **la configuración de /env.**

Para obtener más información sobre la compatibilidad de 64 bits con MIDL y RPC, vea Diseño de interfaces compatibles con [64 bits.](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)

## <a name="examples"></a>Ejemplos

**midl /env win32 filename.idl**

**midl /env ia64 filename.idl**

**midl /env amd64 filename.idl**

**midl /env win64 filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/pack**](-pack.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 