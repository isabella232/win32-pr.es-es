---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica la propiedad \_ BackgroundColorType de la interfaz de usuario \_ \_ PKEY FontProperties.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bbd2056087d584663c8ca716c4021554098dfa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443826"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a><span data-ttu-id="93077-103">UI \_ PKEY \_ FontProperties \_ BackgroundColorType</span><span class="sxs-lookup"><span data-stu-id="93077-103">UI\_PKEY\_FontProperties\_BackgroundColorType</span></span>

<span data-ttu-id="93077-104">Identifica la propiedad \_ BackgroundColorType de la interfaz de usuario \_ \_ PKEY FontProperties.</span><span class="sxs-lookup"><span data-stu-id="93077-104">Identifies the UI\_PKEY\_FontProperties\_BackgroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="93077-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="93077-105">Remarks</span></span>

<span data-ttu-id="93077-106">Una \_ aplicación usa ui PKEY FontProperties BackgroundColorType, junto con la interfaz de usuario \_ \_ [ \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor),  para consultar la configuración de la galería de colores de resaltado de texto.</span><span class="sxs-lookup"><span data-stu-id="93077-106">UI\_PKEY\_FontProperties\_BackgroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), to query **Text highlight color** gallery settings.</span></span>

<span data-ttu-id="93077-107">El valor de propiedad es de la [**\_ enumeración SWATCHCOLORTYPE de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="93077-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="93077-108">El valor predeterminado es `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="93077-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="93077-109">En la tabla siguiente se describen los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="93077-109">The following table describes the property values.</span></span>



|   <span data-ttu-id="93077-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="93077-110">Property</span></span>                             |   <span data-ttu-id="93077-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="93077-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="93077-112">La aplicación debe consultar la métrica del sistema adecuada para el valor de color normalmente el **color** de fondo actual de la ventana de tema de Windows que se recupera con GetSysColor(COLOR \_ WINDOW).</span><span class="sxs-lookup"><span data-stu-id="93077-112">Application should query the appropriate system metric for the color value typically the current Windows theme **window background color** that is retrieved with GetSysColor(COLOR\_WINDOW).</span></span>                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="93077-113">No es compatible con [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="93077-113">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="93077-114">La aplicación debe consultar [la interfaz de usuario \_ \_ PKEY FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) para el valor de color.</span><span class="sxs-lookup"><span data-stu-id="93077-114">Application should query [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) for the color value.</span></span> <span data-ttu-id="93077-115">El valor de color de [ui \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) se muestra en el botón Color de resaltado de texto y se selecciona en la galería de **colores de resaltado de** texto. </span><span class="sxs-lookup"><span data-stu-id="93077-115">The color value of [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) is displayed on the **Text highlight color** button and selected in the **Text highlight color** gallery.</span></span><br/> |



 

<span data-ttu-id="93077-116">Ui PKEY FontProperties BackgroundColorType se pasa al método de devolución de llamada \_ \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)  cuando se selecciona una muestra de color en una galería de colores de resaltado de texto de [**FontControl.**](windowsribbon-element-fontcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="93077-116">UI\_PKEY\_FontProperties\_BackgroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text highlight color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="93077-117">Se recomienda encarecidamente que la aplicación solo establezca un valor de **color** de resaltado de texto inicial y no vuelva a establecer este valor cuando el cursor se cambia de posición dentro de un documento.</span><span class="sxs-lookup"><span data-stu-id="93077-117">It is highly recommended that the application only set an initial **Text highlight color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="93077-118">Se debe mantener la última selección para evitar la necesidad de volver a seleccionar el color deseado.</span><span class="sxs-lookup"><span data-stu-id="93077-118">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="93077-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93077-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93077-120">Propiedades del control de fuentes</span><span class="sxs-lookup"><span data-stu-id="93077-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="93077-121">**UI \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="93077-121">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="93077-122">Control de fuentes</span><span class="sxs-lookup"><span data-stu-id="93077-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

