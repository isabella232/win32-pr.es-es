---
title: Modificador /c_ext
description: Este modificador está obsoleto a partir de la versión 3.0 del compilador MIDL. Sin embargo, el uso del modificador c ext no generará un error del compilador, por lo que no es necesario quitar las referencias a /ms ext o /c ext de un \_ \_ archivo Make \_ existente.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext switch MIDL
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159774"
---
# <a name="c_ext-switch"></a>Modificador /c \_ ext

Este modificador está obsoleto a partir de la versión 3.0 del compilador MIDL. Sin embargo, el uso del modificador **\_ c ext** no generará un error del compilador, por lo que no es necesario quitar las referencias a [**/ms \_ ext**](-ms-ext.md) o **/c \_ ext** de un archivo Make existente.

``` syntax
midl /c_ext
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Las siguientes características ahora están disponibles de forma predeterminada:

-   Muchos archivos de encabezado existentes definen tipos con calificadores, como **far** y **stdcall**, que no forman parte del IDL de DCE. Esos compiladores (y el compilador MIDL en modo de compatibilidad con DCE) generan errores al intentar procesar estos calificadores. El compilador MIDL permite compilar archivos IDL que contienen estos calificadores. Los calificadores de tipo no afectan a la forma en que se transmiten los datos en la red.
-   Puede omitir atributos direccionales, como [**\[ dentro \]**](in.md) o [**\[ fuera \]**](out-idl.md)de .

Las siguientes extensiones de lenguaje C se admiten en el modo predeterminado:

-   Campos de bits en estructuras y uniones
-   Comentarios que comienzan con dos caracteres de barra diagonal (//)
-   Declaraciones externas
-   Procedimientos con puntos suspensivos en la lista de parámetros (...)
-   En plataformas de 32 bits, [**int**](int.md) es un tipo base nativo de 32 bits; en plataformas de 16 bits, **int** se reconoce, pero no es un tipo remotable.
-   Tipo [**\* void**](void.md) que no se usa en operaciones remotas
-   Los calificadores de tipo, incluido el formulario con el prefijo compatible con ANSI, contienen dos caracteres de subrayado: **cdecl**, **\_ \_ cdecl**, [**const**](const.md), **\_ \_ const**, **export**, **\_ \_ export**, **far**, **\_ \_ far**, **loadds , loadds**, **\_ \_ loadds**, **near** **, \_ \_** near , **pascal**, **\_ \_ pascal**, **\_ \_ stdcall**, **stdcall**, **volatile** y **\_ \_ volatile.**

Para obtener más información sobre los calificadores de declaración, vea la documentación de Microsoft C/C++.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**/app \_ config**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




