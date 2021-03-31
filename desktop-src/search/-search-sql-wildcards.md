---
description: El predicado CONTAINS admite el uso del asterisco ( \* ) como carácter comodín para representar palabras y frases. Solo puede Agregar el asterisco al final de la palabra o frase. La presencia del asterisco habilita el modo de coincidencia de prefijo.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Usar caracteres comodín en el predicado CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153950"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a><span data-ttu-id="277fd-105">Usar caracteres comodín en el predicado CONTAINS</span><span class="sxs-lookup"><span data-stu-id="277fd-105">Using Wildcard Characters in the CONTAINS Predicate</span></span>

<span data-ttu-id="277fd-106">El predicado CONTAINS admite el uso del asterisco ( \* ) como carácter comodín para representar palabras y frases.</span><span class="sxs-lookup"><span data-stu-id="277fd-106">The CONTAINS predicate supports the use of the asterisk (\*) as a wildcard character to represent words and phrases.</span></span> <span data-ttu-id="277fd-107">Solo puede Agregar el asterisco al final de la palabra o frase.</span><span class="sxs-lookup"><span data-stu-id="277fd-107">You can add the asterisk only at the end of the word or phrase.</span></span> <span data-ttu-id="277fd-108">La presencia del asterisco habilita el modo de coincidencia de prefijo.</span><span class="sxs-lookup"><span data-stu-id="277fd-108">The presence of the asterisk enables the prefix-matching mode.</span></span> <span data-ttu-id="277fd-109">En este modo, se devuelven coincidencias si la columna contiene la palabra de búsqueda especificada seguida de cero o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="277fd-109">In this mode, matches are returned if the column contains the specified search word followed by zero or more other characters.</span></span> <span data-ttu-id="277fd-110">Si se proporciona una frase, se detectan coincidencias si la columna contiene todas las palabras especificadas con cero o más caracteres que siguen a la palabra final.</span><span class="sxs-lookup"><span data-stu-id="277fd-110">If a phrase is provided, matches are detected if the column contains all the specified words with zero or more other characters following the final word.</span></span>

## <a name="examples"></a><span data-ttu-id="277fd-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="277fd-111">Examples</span></span>

<span data-ttu-id="277fd-112">En el primer ejemplo se buscan los documentos que tienen cualquier palabra en la columna FileName que empiece por "serv".</span><span class="sxs-lookup"><span data-stu-id="277fd-112">The first example matches documents that have any word in the FileName column beginning with "serv".</span></span> <span data-ttu-id="277fd-113">Entre las palabras coincidentes de ejemplo se incluyen "servidor", "servidores" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="277fd-113">Example matching words include "server", "servers", and "service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



<span data-ttu-id="277fd-114">En el segundo ejemplo se buscan los documentos con cualquier frase en la columna FileName que empiece por "Comp" y en las que la palabra siguiente comience por "serv".</span><span class="sxs-lookup"><span data-stu-id="277fd-114">The second example matches documents with any phrase in the FileName column that begins with "comp" and in which the next word begins with "serv".</span></span> <span data-ttu-id="277fd-115">Entre las palabras coincidentes de ejemplo se incluyen "servidor de COMP", "servidores de COMP" y "servicio comp".</span><span class="sxs-lookup"><span data-stu-id="277fd-115">Example matching words include "comp server", "comp servers", and "comp service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



<span data-ttu-id="277fd-116">El asterisco solo funciona para la coincidencia de prefijos y solo se puede colocar al final de la palabra o frase; no funciona para la coincidencia de sufijos.</span><span class="sxs-lookup"><span data-stu-id="277fd-116">The asterisk works only for prefix-matching and can be placed only at the end of the word or phrase; it does not work for suffix-matching.</span></span> <span data-ttu-id="277fd-117">La sintaxis siguiente no es válida y no coincide con los documentos que tengan cualquier palabra en la columna FileName que termine en "Serve".</span><span class="sxs-lookup"><span data-stu-id="277fd-117">The following syntax is not valid and does not match documents with any word in the FileName column ending with "serve".</span></span>


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a><span data-ttu-id="277fd-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="277fd-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="277fd-119">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="277fd-119">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="277fd-120">Predicado FREETEXT</span><span class="sxs-lookup"><span data-stu-id="277fd-120">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="277fd-121">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="277fd-121">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



