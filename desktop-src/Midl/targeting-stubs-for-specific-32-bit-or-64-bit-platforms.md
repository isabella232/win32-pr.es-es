---
title: Código auxiliar de destino para plataformas específicas de 32 o 64 bits
description: Algunas de las características de Microsoft RPC y los compiladores MIDL 3.0 y versiones posteriores son específicas de la plataforma.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- MIDL de plataformas de 32 bits
- MIDL de plataformas de 64 bits
- stubs MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04e0f78e47ed078bf7cd1fd78fa8730b597554a6c8ba1ed4fc5a67bc562e7d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641175"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a>Código auxiliar de destino para plataformas específicas de 32 o 64 bits

Algunas de las características de Microsoft RPC y los compiladores MIDL 3.0 y versiones posteriores son específicas de la plataforma.

Como precaución, los compiladores midl 3.0 y posteriores generan medidas de protección que facilitan la comprobación de compatibilidad durante la fase de compilación de C. MIDL genera dos tipos de protección: una protección dependiente de la plataforma (32 bits frente a 64 bits) y una protección dependiente de la versión (dependencia del conjunto de características). Por ejemplo, MIDL genera la siguiente protección para evitar la compilación en C de un código auxiliar de 32 bits para otras plataformas:

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

La protección dependiente de la versión se desencadena mediante un conjunto de características que se encuentran en los archivos IDL procesados y por el [**modificador /target.**](-target.md) Por ejemplo, si la interfaz usa características admitidas solo en Windows 2000 o posterior, MIDL genera una protección con la \_ macro TARGET IS \_ NT50 \_ O \_ POSTERIOR.

Las macros de protección, definidas en Rpc rpc, dependen de la configuración de WINVER y WIN32 WINNT y las evalúa el \_ \_ compilador de C/C++.

Si, en tiempo de compilación en C, recibe un mensaje de error que indica que necesita una plataforma específica para ejecutar un código auxiliar, primero compruebe que no ha usado una característica que no está disponible en esta plataforma. Las características que desencadenan una protección determinada se enumeran en el cuerpo de la protección. En el ejemplo anterior, el modificador del compilador -Oicf desencadenó la protección. Entre las características importantes de este tipo se incluyen el modificador [**/robust**](-robust.md) y el atributo async disponibles en \[ [](async.md) \] Windows 2000 [](pipe.md) y versiones posteriores, el constructor de tipo de canalización, la opción del compilador /Oif y los atributos de serialización de usuario y de referencias de \[ [**\_**](user-marshal.md) \] \[ [**\_**](wire-marshal.md) \] conexión. Los códigos auxiliares que usan estas características no se ejecutarán en sistemas anteriores.

Si sabe que la plataforma de destino es correcta para las características que usa y sigue recibiendo un error, es posible que tenga que establecer las variables de entorno correctamente.

**Para compilar para Windows 2000 o versiones posteriores**

-   Agregue esta línea al archivo Make:

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**/target**](-target.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**Async**](async.md)
</dt> <dt>

[**uuid \_ asincrónico**](async-uuid.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**Pipa**](pipe.md)
</dt> <dt>

[**wire \_ marshal**](wire-marshal.md)
</dt> <dt>

[**serialización \_ de usuario**](user-marshal.md)
</dt> <dt>

[Serialización de tipos de datos OLE](marshaling-ole-data-types.md)
</dt> </dl>

 

 




