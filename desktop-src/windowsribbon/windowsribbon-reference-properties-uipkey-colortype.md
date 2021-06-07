---
title: UI_PKEY_ColorType
description: Identifica la propiedad \_ PKEY ColorType de la \_ interfaz de usuario.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443896"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="05356-103">UI \_ PKEY \_ ColorType</span><span class="sxs-lookup"><span data-stu-id="05356-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="05356-104">Identifica la propiedad \_ PKEY ColorType de la \_ interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="05356-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="05356-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05356-105">Remarks</span></span>

<span data-ttu-id="05356-106">La interfaz de usuario PKEY ColorType la usa una aplicación para consultar la configuración \_ de color del control \_ [**DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)</span><span class="sxs-lookup"><span data-stu-id="05356-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="05356-107">El valor de propiedad es de la [**\_ enumeración SWATCHCOLORTYPE de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="05356-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|    <span data-ttu-id="05356-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="05356-108">Property</span></span>                            |    <span data-ttu-id="05356-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="05356-109">Description</span></span>                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05356-110">UI \_ SWATCHCOLORTYPE \_ NOCOLOR</span><span class="sxs-lookup"><span data-stu-id="05356-110">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="05356-111">La aplicación debe tratar la configuración de color como transparente.</span><span class="sxs-lookup"><span data-stu-id="05356-111">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="05356-112">Normalmente se usa junto con la **configuración Sin** color.</span><span class="sxs-lookup"><span data-stu-id="05356-112">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="05356-113">UI \_ SWATCHCOLORTYPE \_ AUTOMATIC</span><span class="sxs-lookup"><span data-stu-id="05356-113">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="05356-114">La aplicación debe [consultar GetSysColor(COLOR \_ WINDOWTEXT).](/windows/win32/api/winuser/nf-winuser-getsyscolor)</span><span class="sxs-lookup"><span data-stu-id="05356-114">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="05356-115">Normalmente se usa junto con la **configuración de** color Automático.</span><span class="sxs-lookup"><span data-stu-id="05356-115">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="05356-116">UI \_ SWATCHCOLORTYPE \_ RGB</span><span class="sxs-lookup"><span data-stu-id="05356-116">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="05356-117">La aplicación debe consultar [el \_ color PKEY de la \_ interfaz](windowsribbon-reference-properties-uipkey-color.md) de usuario para la configuración de color.</span><span class="sxs-lookup"><span data-stu-id="05356-117">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="05356-118">Ui PKEY ColorType se pasa al método de devolución de llamada \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) cuando se selecciona una muestra de color en [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="05356-118">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="05356-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05356-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05356-120">Selector de colores propiedades</span><span class="sxs-lookup"><span data-stu-id="05356-120">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 