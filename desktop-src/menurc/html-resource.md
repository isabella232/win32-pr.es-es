---
title: Recurso HTML
description: Define un archivo HTML.
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- Menús de recursos HTML y otros recursos
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db6477aed5180ae18b99f53f4ebadf9d0ad0c91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904149"
---
# <a name="html-resource"></a><span data-ttu-id="46a2a-104">Recurso HTML</span><span class="sxs-lookup"><span data-stu-id="46a2a-104">HTML resource</span></span>

<span data-ttu-id="46a2a-105">Define un archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="46a2a-105">Defines an HTML file.</span></span>

``` syntax
nameID HTML filename
```

## <a name="parameters"></a><span data-ttu-id="46a2a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46a2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46a2a-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="46a2a-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="46a2a-108">Nombre único o un valor entero sin signo de 16 bits que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="46a2a-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="46a2a-109"><span id="filename"></span><span id="FILENAME"></span>*extensión*</span><span class="sxs-lookup"><span data-stu-id="46a2a-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="46a2a-110">Nombre del archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="46a2a-110">The name of the HTML file.</span></span> <span data-ttu-id="46a2a-111">Debe ser una ruta de acceso completa o relativa si el archivo no está en el directorio de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="46a2a-111">It must be a full or relative path if the file is not in the current working directory.</span></span> <span data-ttu-id="46a2a-112">La ruta de acceso debe ser una cadena entre comillas.</span><span class="sxs-lookup"><span data-stu-id="46a2a-112">The path should be a quoted string.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="46a2a-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="46a2a-113">Examples</span></span>

<span data-ttu-id="46a2a-114">En el ejemplo siguiente se define un recurso HTML:</span><span class="sxs-lookup"><span data-stu-id="46a2a-114">The following example defines an HTML resource:</span></span>

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




