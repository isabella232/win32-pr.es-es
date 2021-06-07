---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifica la propiedad \_ Ui PKEY \_ FontProperties \_ ForegroundColorType.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f261256a36ee7a387c6c3a695d8c1182898690c2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444356"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a><span data-ttu-id="08399-103">UI \_ PKEY \_ FontProperties \_ ForegroundColorType</span><span class="sxs-lookup"><span data-stu-id="08399-103">UI\_PKEY\_FontProperties\_ForegroundColorType</span></span>

<span data-ttu-id="08399-104">Identifica la propiedad \_ Ui PKEY \_ FontProperties \_ ForegroundColorType.</span><span class="sxs-lookup"><span data-stu-id="08399-104">Identifies the UI\_PKEY\_FontProperties\_ForegroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="08399-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08399-105">Remarks</span></span>

<span data-ttu-id="08399-106">Una \_ aplicación usa ui PKEY FontProperties ForegroundColorType, junto con la interfaz de usuario \_ \_ [ \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md),  para consultar la configuración de la galería de colores de texto.</span><span class="sxs-lookup"><span data-stu-id="08399-106">UI\_PKEY\_FontProperties\_ForegroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), to query **Text color** gallery settings.</span></span>

<span data-ttu-id="08399-107">El valor de propiedad es de la [**\_ enumeración SWATCHCOLORTYPE de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="08399-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="08399-108">El valor predeterminado es `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="08399-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="08399-109">En la tabla siguiente se describen los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="08399-109">The following table describes the property values.</span></span>



|     <span data-ttu-id="08399-110">Valor</span><span class="sxs-lookup"><span data-stu-id="08399-110">Value</span></span>                           |     <span data-ttu-id="08399-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="08399-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="08399-112">No es compatible con [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="08399-112">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="08399-113">La aplicación debe consultar la métrica del sistema adecuada para el valor de color normalmente el color actual del **texto** del tema de Windows que se recupera con GetSysColor(COLOR \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="08399-113">Application should query the appropriate system metric for the color value typically the current Windows theme **text color** that is retrieved with GetSysColor(COLOR\_WINDOWTEXT).</span></span>                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="08399-114">La aplicación debe consultar [la interfaz de usuario \_ \_ PKEY FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) para el valor de color.</span><span class="sxs-lookup"><span data-stu-id="08399-114">Application should query [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) for the color value.</span></span> <span data-ttu-id="08399-115">El valor de color de [ui \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) se muestra en el botón **Color** de texto y se selecciona en la **galería de colores** de texto.</span><span class="sxs-lookup"><span data-stu-id="08399-115">The color value of [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) is displayed on the **Text color** button and selected in the **Text color** gallery.</span></span><br/> |



 

<span data-ttu-id="08399-116">Ui PKEY FontProperties ForegroundColorType se pasa al método de devolución de llamada \_ \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)  cuando se selecciona una muestra de color en una galería de colores [**FontControl**](windowsribbon-element-fontcontrol.md) Text.</span><span class="sxs-lookup"><span data-stu-id="08399-116">UI\_PKEY\_FontProperties\_ForegroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="08399-117">Se recomienda encarecidamente que la aplicación solo establezca un valor de **color text inicial** y no vuelva a establecer este valor cuando el cursor se cambia de posición dentro de un documento.</span><span class="sxs-lookup"><span data-stu-id="08399-117">It is highly recommended that the application only set an initial **Text color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="08399-118">Se debe mantener la última selección para evitar la necesidad de volver a seleccionar el color deseado.</span><span class="sxs-lookup"><span data-stu-id="08399-118">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="08399-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08399-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08399-120">Propiedades del control de fuentes</span><span class="sxs-lookup"><span data-stu-id="08399-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="08399-121">**UI \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="08399-121">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="08399-122">Control de fuentes</span><span class="sxs-lookup"><span data-stu-id="08399-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

