---
description: El compilador Managed Object Format (MOF) admite dos estilos de comentario mediante dos estilos diferentes de delimitadores de comentarios.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569372"
---
# <a name="creating-a-comment"></a>Crear un comentario

El compilador Managed Object Format (MOF) admite dos estilos de comentario mediante dos estilos diferentes de delimitadores de comentarios.

En la tabla siguiente se enumeran los delimitadores que se usan para los comentarios y el efecto que tienen los delimitadores en el código.



| Delimitador   | Marcas                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | Inicio de un comentario que finaliza al final de la línea.                                    |
| /\* Y \*/ | Principio y fin de un comentario que puede abarcar varias líneas o solo abarcar una parte de una línea. |



 

Al igual que en los lenguajes de programación C y C++, debe usar el delimitador // solo con comentarios de una sola línea, pero usar los delimitadores / y / con comentarios de una o \* \* varias líneas.

En el ejemplo de código siguiente se describen los dos estilos delimitadores.

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



