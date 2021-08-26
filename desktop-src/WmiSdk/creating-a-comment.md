---
description: El compilador Managed Object Format (MOF) admite dos estilos de comentario mediante dos estilos diferentes de delimitadores de comentario.
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
ms.openlocfilehash: 870833f1dbb86f53c7114c4e376af2b4882906ffe1b8cc10f5876bd2c80492e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097345"
---
# <a name="creating-a-comment"></a>Crear un comentario

El compilador Managed Object Format (MOF) admite dos estilos de comentario mediante dos estilos diferentes de delimitadores de comentario.

En la tabla siguiente se enumeran los delimitadores que se usan para los comentarios y el efecto que tienen los delimitadores en el código.



| Delimitador   | Marcas                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | Inicio de un comentario que finaliza al final de la línea.                                    |
| /\* Y \*/ | Principio y final de un comentario que puede abarcar varias líneas o abarcar solo una parte de una línea. |



 

Al igual que en los lenguajes de programación C y C++, debe usar el delimitador // solo con comentarios de una sola línea, pero usar los delimitadores / y / con comentarios de una o varias \* \* líneas.

En el ejemplo de código siguiente se describen los dos estilos delimitadores.

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



