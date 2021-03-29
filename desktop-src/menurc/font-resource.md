---
title: Recurso de fuente
description: Define un archivo que contiene una fuente.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Menús de recursos de fuentes y otros recursos
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784276"
---
# <a name="font-resource"></a><span data-ttu-id="3d7ed-104">Recurso de fuente</span><span class="sxs-lookup"><span data-stu-id="3d7ed-104">FONT resource</span></span>

<span data-ttu-id="3d7ed-105">Define un archivo que contiene una fuente.</span><span class="sxs-lookup"><span data-stu-id="3d7ed-105">Defines a file that contains a font.</span></span>

``` syntax
nameID FONT filename
```

## <a name="parameters"></a><span data-ttu-id="3d7ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d7ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d7ed-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="3d7ed-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="3d7ed-108">Valor entero de 16 bits sin signo único que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="3d7ed-108">Unique 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="3d7ed-109"><span id="filename"></span><span id="FILENAME"></span>*extensión*</span><span class="sxs-lookup"><span data-stu-id="3d7ed-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="3d7ed-110">Nombre del archivo que contiene el recurso.</span><span class="sxs-lookup"><span data-stu-id="3d7ed-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="3d7ed-111">El nombre debe ser un nombre de archivo válido. debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="3d7ed-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="3d7ed-112">La ruta de acceso debe ser una cadena entre comillas.</span><span class="sxs-lookup"><span data-stu-id="3d7ed-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="3d7ed-113">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3d7ed-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="3d7ed-114">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="3d7ed-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3d7ed-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3d7ed-115">Examples</span></span>

<span data-ttu-id="3d7ed-116">En el ejemplo siguiente se define un recurso de fuente único:</span><span class="sxs-lookup"><span data-stu-id="3d7ed-116">The following example defines a single font resource:</span></span>

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




