---
title: Directivas pragma
description: RC no es compatible con las directivas pragma admitidas por el compilador de C/C++.
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0c92136ba5e00d5b821d35ea05a337e7d6abe7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077729"
---
# <a name="pragma-directives"></a><span data-ttu-id="f9c16-103">Directivas pragma</span><span class="sxs-lookup"><span data-stu-id="f9c16-103">Pragma Directives</span></span>

<span data-ttu-id="f9c16-104">RC no es compatible con las directivas pragma admitidas por el compilador de C/C++.</span><span class="sxs-lookup"><span data-stu-id="f9c16-104">RC does not support the pragma directives supported by the C/C++ compiler.</span></span> <span data-ttu-id="f9c16-105">Sin embargo, RC admite la Directiva pragma siguiente para cambiar la página de códigos:</span><span class="sxs-lookup"><span data-stu-id="f9c16-105">However, RC does support the following pragma directive for changing the code page:</span></span>

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

<span data-ttu-id="f9c16-106">Esta Pragma no se admite en un archivo de recursos incluido (. RC).</span><span class="sxs-lookup"><span data-stu-id="f9c16-106">This pragma is not supported in an included resource file (.rc).</span></span> <span data-ttu-id="f9c16-107">Por lo tanto, si tiene un archivo. RC primario e incluye archivos. RC para varios idiomas, use esta directiva pragma antes de incluir otro archivo. RC en lugar de usarlo en el archivo. RC incluido en sí.</span><span class="sxs-lookup"><span data-stu-id="f9c16-107">Therefore, if you have a parent .rc file and it includes .rc files for multiple languages, use this pragma before including another .rc file rather than using it in the included .rc file itself.</span></span> <span data-ttu-id="f9c16-108">Esto se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="f9c16-108">This is demonstrated in the following example.</span></span>

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

<span data-ttu-id="f9c16-109">Para obtener una lista de los valores de CodePageNum, vea [identificadores de páginas de códigos](../intl/code-page-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="f9c16-109">For a list of values for CodePageNum, see [Code Page Identifiers](../intl/code-page-identifiers.md).</span></span>

 

 