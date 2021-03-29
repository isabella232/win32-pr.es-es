---
title: Control de icono
description: Define un control de icono. Este control es un icono que se muestra en un cuadro de diálogo.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Menús de control de icono y otros recursos
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400136395a17f039d552373fa35cba0f3545a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487122"
---
# <a name="icon-control"></a><span data-ttu-id="72ba9-105">Control de icono</span><span class="sxs-lookup"><span data-stu-id="72ba9-105">ICON control</span></span>

<span data-ttu-id="72ba9-106">Define un control de icono.</span><span class="sxs-lookup"><span data-stu-id="72ba9-106">Defines an icon control.</span></span> <span data-ttu-id="72ba9-107">Este control es un icono que se muestra en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="72ba9-107">This control is an icon displayed in a dialog box.</span></span>

<span data-ttu-id="72ba9-108">La instrucción de control de **icono** , que solo se puede usar en una instrucción [**DIALOGEX**](dialogex-resource.md) , define el identificador de recurso de icono, el identificador de control de icono, la posición y los atributos de un control.</span><span class="sxs-lookup"><span data-stu-id="72ba9-108">The **ICON** control statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the icon-resource identifier, icon-control identifier, position, and attributes of a control.</span></span>

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="72ba9-109"><span id="text"></span><span id="TEXT"></span>*negrita*</span><span class="sxs-lookup"><span data-stu-id="72ba9-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="72ba9-110">Nombre de un icono (no un nombre de archivo) definido en otra parte del archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="72ba9-110">Name of an icon (not a file name) defined elsewhere in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="72ba9-111"><span id="width"></span><span id="WIDTH"></span>*Ancho*</span><span class="sxs-lookup"><span data-stu-id="72ba9-111"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="72ba9-112">Este valor se omite y debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="72ba9-112">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="72ba9-113"><span id="height"></span><span id="HEIGHT"></span>*alto*</span><span class="sxs-lookup"><span data-stu-id="72ba9-113"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="72ba9-114">Este valor se omite y debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="72ba9-114">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="72ba9-115"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="72ba9-115"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="72ba9-116">Estilo de control.</span><span class="sxs-lookup"><span data-stu-id="72ba9-116">Control style.</span></span> <span data-ttu-id="72ba9-117">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="72ba9-117">This parameter is optional.</span></span> <span data-ttu-id="72ba9-118">El único valor que se puede especificar es el estilo de **\_ icono de SS** .</span><span class="sxs-lookup"><span data-stu-id="72ba9-118">The only value that can be specified is the **SS\_ICON** style.</span></span> <span data-ttu-id="72ba9-119">Este es el estilo predeterminado si este parámetro se especifica o no.</span><span class="sxs-lookup"><span data-stu-id="72ba9-119">This is the default style whether this parameter is specified or not.</span></span>

</dd> </dl>

<span data-ttu-id="72ba9-120">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="72ba9-120">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="72ba9-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="72ba9-121">Examples</span></span>

<span data-ttu-id="72ba9-122">En este ejemplo se define un control de icono cuyo identificador de icono es 901 y cuyo nombre es mi Icon:</span><span class="sxs-lookup"><span data-stu-id="72ba9-122">This example defines an icon control whose icon identifier is 901 and whose name is myicon:</span></span>

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a><span data-ttu-id="72ba9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="72ba9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ba9-124">**ICONO**</span><span class="sxs-lookup"><span data-stu-id="72ba9-124">**ICON**</span></span>](icon-resource.md)
</dt> </dl>

 

 




