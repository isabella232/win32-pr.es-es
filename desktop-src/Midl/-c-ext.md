---
title: modificador/c_ext
description: Este modificador está obsoleto a partir de la versión 3,0 del compilador de MIDL. Sin embargo, el uso del \_ modificador ext de c no generará un error del compilador, por lo que no tendrá que quitar las referencias a/MS \_ ext o/c \_ ext de un archivo make existente.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext modificador MIDL
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685654"
---
# <a name="c_ext-switch"></a>/c ( \_ modificador ext)

Este modificador está obsoleto a partir de la versión 3,0 del compilador de MIDL. Sin embargo, el uso del modificador **\_ ext de c** no generará un error del compilador, por lo que no tendrá que quitar las referencias a [**/MS \_ ext**](-ms-ext.md) o **/c \_ ext** de un archivo make existente.

``` syntax
midl /c_ext
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Las siguientes características están ahora disponibles de forma predeterminada:

-   Muchos archivos de encabezado existentes definen tipos con calificadores, como **Far** y **Stdcall**, que no forman parte del IDL de DCE. Esos compiladores (y el compilador de MIDL en modo de compatibilidad de DCE) generan errores al intentar procesar estos calificadores. El compilador MIDL le permite compilar archivos IDL que contienen estos calificadores. Los calificadores de tipo no afectan a la manera en que se transmiten los datos en la red.
-   Puede omitir atributos direccionales como [**\[ in \]**](in.md) o [**\[ out \]**](out-idl.md).

Las siguientes extensiones del lenguaje C se admiten en el modo predeterminado:

-   Campos de bits en estructuras y uniones
-   Comentarios que comienzan con dos caracteres de barra diagonal (//)
-   Declaraciones externas
-   Procedimientos con puntos suspensivos en la lista de parámetros (...)
-   En las plataformas de 32 bits, [**int**](int.md) es un tipo base de 32 bits nativo; en las plataformas de 16 bits, se reconoce **int** pero no es un tipo utilizable de forma remota.
-   Tipo [**void \***](void.md) que no se usa en operaciones remotas
-   Los calificadores de tipo, incluido el formulario con el prefijo compatible con ANSI, contienen dos caracteres de subrayado: **Cdecl**, **\_ \_ Cdecl**, [**const**](const.md), **\_ \_ const**, **Export**, **\_ \_ Export**, **Far**, **\_ \_ Far**, **loadds**, **\_ \_ loadds**, **Near**, **\_ \_ Near**, **Pascal**, **\_ \_ Pascal**, **Stdcall**, **\_ \_ Stdcall**, **volatile** y **\_ \_ volatile**.

Para obtener más información acerca de los calificadores de declaración, vea la documentación de Microsoft C/C++.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**configuración de/APP \_**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




