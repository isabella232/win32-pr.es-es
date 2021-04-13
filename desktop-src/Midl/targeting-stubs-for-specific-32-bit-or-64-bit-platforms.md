---
title: Destinar códigos auxiliares para plataformas específicas de 32 bits o 64 bits
description: Algunas de las características de Microsoft RPC y los compiladores MIDL 3,0 y versiones posteriores son específicas de la plataforma.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- '32: plataformas de bits MIDL'
- '64: plataformas de bits MIDL'
- código de la auxiliar MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526265a60f8b2ef2f31d19d0356d4ec3a3ae8c8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357448"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a>Destinar códigos auxiliares para plataformas específicas de 32 bits o 64 bits

Algunas de las características de Microsoft RPC y los compiladores MIDL 3,0 y versiones posteriores son específicas de la plataforma.

Como medida de precaución, los compiladores MIDL 3,0 y versiones posteriores generan protecciones que facilitan la comprobación de compatibilidad durante la fase de compilación de C. MIDL genera dos tipos de protecciones: una protección dependiente de la plataforma (32 bits frente a 64 bits) y una protección dependiente de la versión (dependencia del conjunto de características). Por ejemplo, MIDL genera la siguiente protección para evitar la compilación de C de un código auxiliar de 32 bits para otras plataformas:

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

La protección dependiente de la versión se desencadena mediante un conjunto de características que se encuentran en los archivos IDL procesados y el modificador [**/target**](-target.md) . Por ejemplo, si la interfaz utiliza características admitidas solo en Windows 2000 o posterior, MIDL genera una protección con el destino \_ es \_ NT50 \_ o \_ una macro posterior.

Las macros Guard, definidas en Rpcndr. h, dependen de la configuración de WINVER y \_ Win32 \_ WinNT y se evalúan mediante el compilador de C/C++.

Si, en tiempo de compilación de C, recibe un mensaje de error que indica que necesita una plataforma específica para ejecutar un código auxiliar, primero debe comprobar para asegurarse de que no ha usado una característica que no está disponible en esta plataforma. Las características que desencadenan una protección determinada se muestran en el cuerpo de la protección. En el ejemplo anterior, el modificador de compilador-Oicf activó la protección. Entre las características importantes de este tipo se incluyen el modificador [**/Robust**](-robust.md) y el \[ atributo [**async**](async.md) \] disponible en Windows 2000 y versiones posteriores, el constructor de tipo de [**canalización**](pipe.md) , la opción del compilador/OIF y los atributos Marshal y serialización del \[ [**usuario \_**](user-marshal.md) \] \[ [**\_**](wire-marshal.md) \] . Los códigos auxiliares que usan estas características no se ejecutarán en sistemas anteriores.

Si sabe que la plataforma de destino es correcta para las características que está usando y sigue recibiendo un error, puede que tenga que establecer las variables de entorno de forma adecuada.

**Para compilar para Windows 2000 o versiones posteriores**

-   Agregue esta línea al archivo Make:

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**/Target**](-target.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> <dt>

[**async**](async.md)
</dt> <dt>

[**\_UUID asincrónico**](async-uuid.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**codo**](pipe.md)
</dt> <dt>

[**\_serialización de cable**](wire-marshal.md)
</dt> <dt>

[**\_serialización de usuario**](user-marshal.md)
</dt> <dt>

[Serialización de tipos de datos OLE](marshaling-ole-data-types.md)
</dt> </dl>

 

 




