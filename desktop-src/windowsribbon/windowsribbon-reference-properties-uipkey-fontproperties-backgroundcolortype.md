---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ BackgroundColorType.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568898cb2706eb932ea708f929aa4791f0643c74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487795"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a><span data-ttu-id="ef946-103">UI \_ PKEY \_ FontProperties \_ BackgroundColorType</span><span class="sxs-lookup"><span data-stu-id="ef946-103">UI\_PKEY\_FontProperties\_BackgroundColorType</span></span>

<span data-ttu-id="ef946-104">Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ BackgroundColorType.</span><span class="sxs-lookup"><span data-stu-id="ef946-104">Identifies the UI\_PKEY\_FontProperties\_BackgroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="ef946-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef946-105">Remarks</span></span>

<span data-ttu-id="ef946-106">La \_ interfaz \_ de usuario PKEY FontProperties \_ BackgroundColorType se usa en una aplicación, junto con la [interfaz de usuario \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), para consultar la configuración de la galería de **colores de resaltado de texto** .</span><span class="sxs-lookup"><span data-stu-id="ef946-106">UI\_PKEY\_FontProperties\_BackgroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), to query **Text highlight color** gallery settings.</span></span>

<span data-ttu-id="ef946-107">El valor de la propiedad es de la enumeración [**\_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ef946-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="ef946-108">El valor predeterminado es `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="ef946-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="ef946-109">En la tabla siguiente se describen los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ef946-109">The following table describes the property values.</span></span>



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="ef946-110">La aplicación debe consultar la métrica del sistema correspondiente para el valor de color normalmente el **color de fondo** de la ventana de tema de Windows actual que se recupera con GetSysColor (ventana de color \_ ).</span><span class="sxs-lookup"><span data-stu-id="ef946-110">Application should query the appropriate system metric for the color value typically the current Windows theme **window background color** that is retrieved with GetSysColor(COLOR\_WINDOW).</span></span>                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="ef946-111">No es compatible con [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="ef946-111">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="ef946-112">La aplicación debe consultar la [interfaz de usuario \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) para el valor de color.</span><span class="sxs-lookup"><span data-stu-id="ef946-112">Application should query [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) for the color value.</span></span> <span data-ttu-id="ef946-113">El valor de color de [UI \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) se muestra en el botón color de **resaltado de texto** y se selecciona en la galería de colores de **resaltado de texto** .</span><span class="sxs-lookup"><span data-stu-id="ef946-113">The color value of [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) is displayed on the **Text highlight color** button and selected in the **Text highlight color** gallery.</span></span><br/> |



 

<span data-ttu-id="ef946-114">La interfaz de usuario \_ PKEY \_ FontProperties \_ BackgroundColorType se pasa al método de devolución de llamada [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) cuando se selecciona una muestra de color en una galería de **colores de resaltado de texto** [**FontControl**](windowsribbon-element-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="ef946-114">UI\_PKEY\_FontProperties\_BackgroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text highlight color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="ef946-115">Se recomienda encarecidamente que la aplicación solo establezca un valor de **color de resaltado de texto** inicial y no vuelva a establecer este valor cuando el cursor se cambie de posición dentro de un documento.</span><span class="sxs-lookup"><span data-stu-id="ef946-115">It is highly recommended that the application only set an initial **Text highlight color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="ef946-116">La última selección debe mantenerse para evitar la necesidad de volver a seleccionar el color deseado.</span><span class="sxs-lookup"><span data-stu-id="ef946-116">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ef946-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef946-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef946-118">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="ef946-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="ef946-119">**UI \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="ef946-119">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="ef946-120">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="ef946-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

