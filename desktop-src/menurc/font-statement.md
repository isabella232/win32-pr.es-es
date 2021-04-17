---
title: FONT (instrucción)
description: Define la fuente con la que el sistema dibujará texto en el cuadro de diálogo. La fuente se debe haber cargado previamente; por ejemplo, mediante una llamada a la función LoadResource.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Menús de la instrucción de fuente y otros recursos
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b31b280a5a973301e8410f1f74340138af07ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487687"
---
# <a name="font-statement"></a><span data-ttu-id="69785-105">FONT (instrucción)</span><span class="sxs-lookup"><span data-stu-id="69785-105">FONT statement</span></span>

<span data-ttu-id="69785-106">Define la fuente con la que el sistema dibujará texto en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="69785-106">Defines the font with which the system will draw text in the dialog box.</span></span> <span data-ttu-id="69785-107">La fuente se debe haber cargado previamente; por ejemplo, mediante una llamada a la función [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .</span><span class="sxs-lookup"><span data-stu-id="69785-107">The font must have been previously loaded; for example, by calling the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span data-ttu-id="69785-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*PointSize*</span><span class="sxs-lookup"><span data-stu-id="69785-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*</span></span>
</dt> <dd>

<span data-ttu-id="69785-109">Tamaño de la fuente, en puntos.</span><span class="sxs-lookup"><span data-stu-id="69785-109">The size of the font, in points.</span></span>

</dd> <dt>

<span data-ttu-id="69785-110"><span id="typeface"></span><span id="TYPEFACE"></span>*tipográfico*</span><span class="sxs-lookup"><span data-stu-id="69785-110"><span id="typeface"></span><span id="TYPEFACE"></span>*typeface*</span></span>
</dt> <dd>

<span data-ttu-id="69785-111">Nombre del tipo de letra.</span><span class="sxs-lookup"><span data-stu-id="69785-111">The name of the typeface.</span></span> <span data-ttu-id="69785-112">Este parámetro debe ir entre comillas (").</span><span class="sxs-lookup"><span data-stu-id="69785-112">This parameter must be enclosed in quotes (").</span></span>

</dd> <dt>

<span data-ttu-id="69785-113"><span id="weight"></span><span id="WEIGHT"></span>*media*</span><span class="sxs-lookup"><span data-stu-id="69785-113"><span id="weight"></span><span id="WEIGHT"></span>*weight*</span></span>
</dt> <dd>

<span data-ttu-id="69785-114">Peso de la fuente en el intervalo comprendido entre 0 y 1000.</span><span class="sxs-lookup"><span data-stu-id="69785-114">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="69785-115">Por ejemplo, 400 es normal y 700 está en negrita.</span><span class="sxs-lookup"><span data-stu-id="69785-115">For example, 400 is normal and 700 is bold.</span></span> <span data-ttu-id="69785-116">Si este valor es 0, se utiliza el peso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="69785-116">If this value is 0, the default weight is used.</span></span> <span data-ttu-id="69785-117">Para obtener una lista de valores predefinidos, vea los valores de **FW \_ \*** definidos en WinGDI. h.</span><span class="sxs-lookup"><span data-stu-id="69785-117">For a list of predefined values, see the **FW\_\*** values defined in WinGDI.h.</span></span>

</dd> <dt>

<span data-ttu-id="69785-118"><span id="italic"></span><span id="ITALIC"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="69785-118"><span id="italic"></span><span id="ITALIC"></span>*italic*</span></span>
</dt> <dd>

<span data-ttu-id="69785-119">Indica una fuente cursiva si está establecida en TRUE.</span><span class="sxs-lookup"><span data-stu-id="69785-119">Indicates an italic font if set to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="69785-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span><span class="sxs-lookup"><span data-stu-id="69785-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span></span>
</dt> <dd>

<span data-ttu-id="69785-121">El conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="69785-121">The character set.</span></span> <span data-ttu-id="69785-122">Para obtener una lista de valores, vea el miembro **lfCharSet** de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="69785-122">For a list of values, see the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="69785-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="69785-123">Examples</span></span>

<span data-ttu-id="69785-124">En el siguiente ejemplo se muestra el uso de la instrucción **Font** :</span><span class="sxs-lookup"><span data-stu-id="69785-124">The following example demonstrates the use of the **FONT** statement:</span></span>

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a><span data-ttu-id="69785-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="69785-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69785-126">**LoadResource**</span><span class="sxs-lookup"><span data-stu-id="69785-126">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 