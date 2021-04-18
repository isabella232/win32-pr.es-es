---
title: Portabilidad de funciones Get de GL de IRIS
description: 'IRIS GL \ 0034; Get \ 0034; las funciones tienen el formato siguiente:'
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- Migración de la contabilidad de IRIS, funciones Get
- portabilidad de IRIS GL, funciones Get
- trasladar a OpenGL desde IRIS GL, obtener funciones
- Exportación de OpenGL desde IRIS GL, obtener funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665696"
---
# <a name="porting-iris-gl-get-functions"></a><span data-ttu-id="b8a7a-107">Portabilidad de funciones Get de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="b8a7a-107">Porting IRIS GL Get Functions</span></span>

<span data-ttu-id="b8a7a-108">Las funciones de "obtener" de la contabilidad de IRIS tienen el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="b8a7a-108">IRIS GL "get" functions take the following form:</span></span>

``` syntax
int getthing();
```

<span data-ttu-id="b8a7a-109">y</span><span class="sxs-lookup"><span data-stu-id="b8a7a-109">and</span></span>

``` syntax
int getthings( int *a, int *b);
```

<span data-ttu-id="b8a7a-110">Probablemente, el código de la contabilidad de IRIS incluye llamadas a funciones Get que tienen un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="b8a7a-110">Your IRIS GL code probably includes get function calls that look something like:</span></span>

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

<span data-ttu-id="b8a7a-111">En OpenGL, se usa uno de los cuatro tipos siguientes de funciones de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) en lugar de funciones equivalentes Get GL de iris:</span><span class="sxs-lookup"><span data-stu-id="b8a7a-111">In OpenGL you use one of the following four types of [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) functions in place of equivalent IRIS GL get functions:</span></span>

-   <span data-ttu-id="b8a7a-112">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="b8a7a-112">**glGetBooleanv**</span></span>
-   <span data-ttu-id="b8a7a-113">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b8a7a-113">**glGetIntegerv**</span></span>
-   <span data-ttu-id="b8a7a-114">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="b8a7a-114">**glGetFloatv**</span></span>
-   <span data-ttu-id="b8a7a-115">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="b8a7a-115">**glGetDoublev**</span></span>

<span data-ttu-id="b8a7a-116">Las funciones tienen la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="b8a7a-116">The functions have the following syntax:</span></span>

``` syntax
glGet<Datatype>v( value, *data );
```

<span data-ttu-id="b8a7a-117">donde *valor* es de tipo **GLenum** y los datos son de tipo **GLdatatype**.</span><span class="sxs-lookup"><span data-stu-id="b8a7a-117">where *value* is of type **GLenum** and data is of type **GLdatatype**.</span></span> <span data-ttu-id="b8a7a-118">Cuando se llama a **glGet** y devuelve un tipo diferente del tipo esperado, el tipo se convierte adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="b8a7a-118">When you call **glGet** and it returns a type different from the type expected, the type is converted appropriately.</span></span> <span data-ttu-id="b8a7a-119">Para obtener una lista completa de los parámetros de **glGet** , consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span><span class="sxs-lookup"><span data-stu-id="b8a7a-119">For a complete list of **glGet** parameters, see [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span></span>

 

 




