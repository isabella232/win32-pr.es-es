---
title: UI_PKEY_ColorType
description: Identifica la propiedad de la interfaz de usuario \_ PKEY \_ ColorType.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313d2a657d889a7c582d86d8f8c9e4ebd2cfd01e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359162"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="63a1f-103">Interfaz de usuario \_ PKEY \_ ColorType</span><span class="sxs-lookup"><span data-stu-id="63a1f-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="63a1f-104">Identifica la propiedad de la interfaz de usuario \_ PKEY \_ ColorType.</span><span class="sxs-lookup"><span data-stu-id="63a1f-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="63a1f-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63a1f-105">Remarks</span></span>

<span data-ttu-id="63a1f-106">\_ \_ Una aplicación usa la interfaz de usuario PKEY ColorType para consultar la configuración de color del control [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="63a1f-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="63a1f-107">El valor de la propiedad es de la enumeración [**\_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="63a1f-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|                                |                                                                                                                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63a1f-108">SWATCHCOLORTYPE de IU \_ \_ nocolor</span><span class="sxs-lookup"><span data-stu-id="63a1f-108">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="63a1f-109">La aplicación debe tratar la configuración de color como transparente.</span><span class="sxs-lookup"><span data-stu-id="63a1f-109">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="63a1f-110">Normalmente, se usa junto con la configuración de color **sin** color.</span><span class="sxs-lookup"><span data-stu-id="63a1f-110">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="63a1f-111">UI \_ SWATCHCOLORTYPE \_ automática</span><span class="sxs-lookup"><span data-stu-id="63a1f-111">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="63a1f-112">La aplicación debe consultar [GetSysColor (color \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span><span class="sxs-lookup"><span data-stu-id="63a1f-112">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="63a1f-113">Normalmente, se usa junto con la configuración de color **automática** .</span><span class="sxs-lookup"><span data-stu-id="63a1f-113">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="63a1f-114">UI \_ SWATCHCOLORTYPE \_ RGB</span><span class="sxs-lookup"><span data-stu-id="63a1f-114">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="63a1f-115">La aplicación debe consultar el [ \_ \_ color PKEY](windowsribbon-reference-properties-uipkey-color.md) de la interfaz de usuario para la configuración de color.</span><span class="sxs-lookup"><span data-stu-id="63a1f-115">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="63a1f-116">La interfaz de usuario \_ PKEY \_ ColorType se pasa al método de devolución de llamada [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) cuando se selecciona una muestra de color en una [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="63a1f-116">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="63a1f-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63a1f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63a1f-118">Propiedades del selector de colores</span><span class="sxs-lookup"><span data-stu-id="63a1f-118">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 