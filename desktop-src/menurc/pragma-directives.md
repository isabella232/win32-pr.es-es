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
# <a name="pragma-directives"></a>Directivas pragma

RC no es compatible con las directivas pragma admitidas por el compilador de C/C++. Sin embargo, RC admite la Directiva pragma siguiente para cambiar la página de códigos:

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

Esta Pragma no se admite en un archivo de recursos incluido (. RC). Por lo tanto, si tiene un archivo. RC primario e incluye archivos. RC para varios idiomas, use esta directiva pragma antes de incluir otro archivo. RC en lugar de usarlo en el archivo. RC incluido en sí. Esto se muestra en el ejemplo siguiente.

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

Para obtener una lista de los valores de CodePageNum, vea [identificadores de páginas de códigos](../intl/code-page-identifiers.md).

 

 