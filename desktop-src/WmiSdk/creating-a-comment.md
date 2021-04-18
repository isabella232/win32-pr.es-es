---
description: El compilador de Managed Object Format (MOF) admite dos estilos de comentario usando dos estilos diferentes de delimitadores de comentario.
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: Crear un comentario
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d0e7cf2484fef018c62c8c47d9c55d245191681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715844"
---
# <a name="creating-a-comment"></a>Crear un comentario

El compilador de Managed Object Format (MOF) admite dos estilos de comentario usando dos estilos diferentes de delimitadores de comentario.

En la tabla siguiente se enumeran los delimitadores que se utilizan para los comentarios y el efecto que tienen los delimitadores en el código.



| Delimitador   | Marcas                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | Inicio de un comentario que finaliza al final de la línea.                                    |
| /\* etc \*/ | Principio y final de un comentario que puede abarcar varias líneas o abarcar solo una parte de una línea. |



 

Como en los lenguajes de programación C y C++, debe utilizar el delimitador//solo con comentarios de una sola línea, pero use \* los \* delimitadores/y/con comentarios de una línea o de varias líneas.

En el ejemplo de código siguiente se describen los dos estilos de delimitador.

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases de Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



