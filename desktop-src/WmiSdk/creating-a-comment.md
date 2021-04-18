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
# <a name="creating-a-comment"></a><span data-ttu-id="63f64-103">Crear un comentario</span><span class="sxs-lookup"><span data-stu-id="63f64-103">Creating a Comment</span></span>

<span data-ttu-id="63f64-104">El compilador de Managed Object Format (MOF) admite dos estilos de comentario usando dos estilos diferentes de delimitadores de comentario.</span><span class="sxs-lookup"><span data-stu-id="63f64-104">The Managed Object Format (MOF) compiler supports two styles of comment using two different styles of comment delimiters.</span></span>

<span data-ttu-id="63f64-105">En la tabla siguiente se enumeran los delimitadores que se utilizan para los comentarios y el efecto que tienen los delimitadores en el código.</span><span class="sxs-lookup"><span data-stu-id="63f64-105">The following table lists the delimiters that are used for comments and the effect that the delimiters have in the code.</span></span>



| <span data-ttu-id="63f64-106">Delimitador</span><span class="sxs-lookup"><span data-stu-id="63f64-106">Delimiter</span></span>   | <span data-ttu-id="63f64-107">Marcas</span><span class="sxs-lookup"><span data-stu-id="63f64-107">Marks</span></span>                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | <span data-ttu-id="63f64-108">Inicio de un comentario que finaliza al final de la línea.</span><span class="sxs-lookup"><span data-stu-id="63f64-108">Start of a comment that terminates at the end of the line.</span></span>                                    |
| <span data-ttu-id="63f64-109">/\* etc \*/</span><span class="sxs-lookup"><span data-stu-id="63f64-109">/\* and \*/</span></span> | <span data-ttu-id="63f64-110">Principio y final de un comentario que puede abarcar varias líneas o abarcar solo una parte de una línea.</span><span class="sxs-lookup"><span data-stu-id="63f64-110">Beginning and end of a comment that may span multiple lines or only span a portion of a line.</span></span> |



 

<span data-ttu-id="63f64-111">Como en los lenguajes de programación C y C++, debe utilizar el delimitador//solo con comentarios de una sola línea, pero use \* los \* delimitadores/y/con comentarios de una línea o de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="63f64-111">As in the C and C++ programming languages, you must use the // delimiter with single-line comments only, but use the /\* and \*/ delimiters with either single-line or multiple-line comments.</span></span>

<span data-ttu-id="63f64-112">En el ejemplo de código siguiente se describen los dos estilos de delimitador.</span><span class="sxs-lookup"><span data-stu-id="63f64-112">The following code example describes the two delimiter styles.</span></span>

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a><span data-ttu-id="63f64-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63f64-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63f64-114">Diseñar clases de Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="63f64-114">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



