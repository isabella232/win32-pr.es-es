---
title: UI_PKEY_FontProperties_Family
description: Identifica la propiedad de la familia de PKEY de interfaz de usuario \_ \_ FontProperties \_ .
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7183e51105a397f14154639512ca11f7c03d44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714387"
---
# <a name="ui_pkey_fontproperties_family"></a><span data-ttu-id="94c7a-103">Familia de FontProperties de UI \_ PKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="94c7a-103">UI\_PKEY\_FontProperties\_Family</span></span>

<span data-ttu-id="94c7a-104">Identifica la propiedad de la familia de PKEY de interfaz de usuario \_ \_ FontProperties \_ .</span><span class="sxs-lookup"><span data-stu-id="94c7a-104">Identifies the UI\_PKEY\_FontProperties\_Family property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="94c7a-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94c7a-105">Remarks</span></span>

<span data-ttu-id="94c7a-106">\_ \_ \_ Una aplicación usa la familia de UI PKEY FontProperties para consultar el valor de la Galería desplegable de la **familia de fuentes** .</span><span class="sxs-lookup"><span data-stu-id="94c7a-106">UI\_PKEY\_FontProperties\_Family is used by an application to query the value of the **Font family** drop-down gallery.</span></span>

<span data-ttu-id="94c7a-107">El valor de la familia de PKEY de interfaz de usuario \_ \_ FontProperties \_ coincide con un nombre de [familias de fuentes de Windows GDI](../gdi/font-families.md) recuperado con la función [EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) o [EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span><span class="sxs-lookup"><span data-stu-id="94c7a-107">The value of UI\_PKEY\_FontProperties\_Family matches a [Windows GDI Font Families](../gdi/font-families.md) name retrieved with the [EnumFontFamilies function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) or [EnumFontFamiliesEx function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span></span>

<span data-ttu-id="94c7a-108">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="94c7a-108">The default value is an empty string.</span></span>

<span data-ttu-id="94c7a-109">Si se proporciona una cadena vacía para el valor de la PKEY de la interfaz de usuario \_ \_ FontProperties \_ Family, se borra la selección de fuente.</span><span class="sxs-lookup"><span data-stu-id="94c7a-109">If an empty string is supplied for the value for UI\_PKEY\_FontProperties\_Family, then the font selection is cleared.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94c7a-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94c7a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94c7a-111">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="94c7a-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="94c7a-112">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="94c7a-112">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 