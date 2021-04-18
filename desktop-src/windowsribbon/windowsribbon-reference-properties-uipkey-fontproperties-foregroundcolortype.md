---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ ForegroundColorType.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5589e9b21fc7ab0884a3cac51eba114ee77036b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420971"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a><span data-ttu-id="6e2e7-103">UI \_ PKEY \_ FontProperties \_ ForegroundColorType</span><span class="sxs-lookup"><span data-stu-id="6e2e7-103">UI\_PKEY\_FontProperties\_ForegroundColorType</span></span>

<span data-ttu-id="6e2e7-104">Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ ForegroundColorType.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-104">Identifies the UI\_PKEY\_FontProperties\_ForegroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="6e2e7-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e2e7-105">Remarks</span></span>

<span data-ttu-id="6e2e7-106">La \_ interfaz \_ de usuario PKEY FontProperties \_ ForegroundColorType se usa en una aplicación, junto con la [interfaz de usuario \_ PKEY \_ FontProperties \_ foregroundcolor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), para consultar la configuración de la galería de **colores de texto** .</span><span class="sxs-lookup"><span data-stu-id="6e2e7-106">UI\_PKEY\_FontProperties\_ForegroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), to query **Text color** gallery settings.</span></span>

<span data-ttu-id="6e2e7-107">El valor de la propiedad es de la enumeración [**\_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="6e2e7-108">El valor predeterminado es `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="6e2e7-109">En la tabla siguiente se describen los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-109">The following table describes the property values.</span></span>



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="6e2e7-110">No es compatible con [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="6e2e7-110">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="6e2e7-111">La aplicación debe consultar la métrica del sistema adecuada para el valor de color normalmente el **color de texto** del tema de Windows actual que se recupera con GETSYSCOLOR (color \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="6e2e7-111">Application should query the appropriate system metric for the color value typically the current Windows theme **text color** that is retrieved with GetSysColor(COLOR\_WINDOWTEXT).</span></span>                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="6e2e7-112">La aplicación debe consultar la [interfaz de usuario \_ PKEY \_ FontProperties \_ foregroundcolor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) para obtener el valor de color.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-112">Application should query [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) for the color value.</span></span> <span data-ttu-id="6e2e7-113">El valor de color de la [interfaz de usuario \_ PKEY \_ FontProperties \_ foregroundcolor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) se muestra en el botón **color del texto** y se selecciona en la Galería color de **texto** .</span><span class="sxs-lookup"><span data-stu-id="6e2e7-113">The color value of [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) is displayed on the **Text color** button and selected in the **Text color** gallery.</span></span><br/> |



 

<span data-ttu-id="6e2e7-114">La interfaz de usuario \_ PKEY \_ FontProperties \_ ForegroundColorType se pasa al método de devolución de llamada [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) cuando se selecciona una muestra de color en una galería de **colores de texto** [**FontControl**](windowsribbon-element-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="6e2e7-114">UI\_PKEY\_FontProperties\_ForegroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="6e2e7-115">Se recomienda encarecidamente que la aplicación solo establezca un valor de **color de texto** inicial y no vuelva a establecer este valor cuando el cursor se cambie de posición dentro de un documento.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-115">It is highly recommended that the application only set an initial **Text color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="6e2e7-116">La última selección debe mantenerse para evitar la necesidad de volver a seleccionar el color deseado.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-116">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6e2e7-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e2e7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e2e7-118">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="6e2e7-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="6e2e7-119">**UI \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="6e2e7-119">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="6e2e7-120">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="6e2e7-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

