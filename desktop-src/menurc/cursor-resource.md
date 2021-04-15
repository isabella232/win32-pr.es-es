---
title: Recurso de CURSOR
description: Define un mapa de bits que define la forma del cursor en la pantalla de presentación o un cursor animado.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Menús de recursos de CURSOR y otros recursos
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676361"
---
# <a name="cursor-resource"></a><span data-ttu-id="c150e-104">Recurso de CURSOR</span><span class="sxs-lookup"><span data-stu-id="c150e-104">CURSOR resource</span></span>

<span data-ttu-id="c150e-105">Define un mapa de bits que define la forma del cursor en la pantalla de presentación o un cursor animado.</span><span class="sxs-lookup"><span data-stu-id="c150e-105">Defines a bitmap that defines the shape of the cursor on the display screen or an animated cursor.</span></span>

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a><span data-ttu-id="c150e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c150e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c150e-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="c150e-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="c150e-108">Nombre único o entero de 16 bits sin signo que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="c150e-108">Unique name or a 16-bit unsigned integer identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="c150e-109"><span id="filename"></span><span id="FILENAME"></span>*extensión*</span><span class="sxs-lookup"><span data-stu-id="c150e-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="c150e-110">Nombre del archivo que contiene el recurso.</span><span class="sxs-lookup"><span data-stu-id="c150e-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="c150e-111">El nombre debe ser un nombre de archivo válido. debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="c150e-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="c150e-112">La ruta de acceso debe ser una cadena entre comillas.</span><span class="sxs-lookup"><span data-stu-id="c150e-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="c150e-113">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="c150e-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="c150e-114">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="c150e-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c150e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c150e-115">Remarks</span></span>

<span data-ttu-id="c150e-116">Los recursos de icono y cursor pueden contener más de una imagen.</span><span class="sxs-lookup"><span data-stu-id="c150e-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="c150e-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c150e-117">Examples</span></span>

<span data-ttu-id="c150e-118">En el ejemplo siguiente se definen dos recursos de cursor: uno por nombre (cursor1) y el otro por el número (2):</span><span class="sxs-lookup"><span data-stu-id="c150e-118">The following example defines two cursor resources; one by name (cursor1) and the other by number (2):</span></span>

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a><span data-ttu-id="c150e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c150e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c150e-120">Uso de cursores</span><span class="sxs-lookup"><span data-stu-id="c150e-120">Using Cursors</span></span>](./using-cursors.md)
</dt> </dl>

 

 