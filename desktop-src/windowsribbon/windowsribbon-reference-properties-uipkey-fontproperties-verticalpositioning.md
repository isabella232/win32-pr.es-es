---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ VerticalPositioning.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b67e2a099b7ce02b3c94f7c9d799fcdda5e881
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078220"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a><span data-ttu-id="683c2-103">UI \_ PKEY \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="683c2-103">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>

<span data-ttu-id="683c2-104">Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ VerticalPositioning.</span><span class="sxs-lookup"><span data-stu-id="683c2-104">Identifies the UI\_PKEY\_FontProperties\_VerticalPositioning property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a><span data-ttu-id="683c2-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="683c2-105">Remarks</span></span>

<span data-ttu-id="683c2-106">\_ \_ \_ Una aplicación usa la interfaz de usuario PKEY FontProperties VerticalPositioning para consultar el valor de  los controles de superíndice y **subíndice** .</span><span class="sxs-lookup"><span data-stu-id="683c2-106">UI\_PKEY\_FontProperties\_VerticalPositioning is used by an application to query the value of the **Superscript** and **Subscript** controls.</span></span>

<span data-ttu-id="683c2-107">El valor de la propiedad es de la enumeración [**\_ FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="683c2-107">The property value is from the [**UI\_FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) enumeration.</span></span>

<span data-ttu-id="683c2-108">El valor predeterminado es `UI_FONTVERTICALPOSITION_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="683c2-108">The default value is `UI_FONTVERTICALPOSITION_NOTSET`.</span></span>

<span data-ttu-id="683c2-109">En la captura de pantalla siguiente se muestran los botones de superíndice y **subíndice** **de la cinta** de opciones [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="683c2-109">The following screen shot shows the **Superscript** and **Subscript** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-subsuper.png)

<span data-ttu-id="683c2-111">En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="683c2-111">The following table describes the properties and the UI result.</span></span>



|                                        |                                                                                                |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | <span data-ttu-id="683c2-112">Los **botones de superíndice y** **subíndice** están deshabilitados y solo se pueden establecer en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="683c2-112">**Superscript** and **Subscript** buttons are disabled and can only be set by the application.</span></span> |
| `UI_FONTVERTICALPOSITION_NOTSET`       | <span data-ttu-id="683c2-113">Los **botones de superíndice** y **subíndice** no están seleccionados.</span><span class="sxs-lookup"><span data-stu-id="683c2-113">**Superscript** and **Subscript** buttons are not selected.</span></span>                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | <span data-ttu-id="683c2-114">El botón **Superscript** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="683c2-114">**Superscript** button is selected.</span></span>                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | <span data-ttu-id="683c2-115">El botón **subíndice** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="683c2-115">**Subscript** button is selected.</span></span>                                                              |



 

> [!Note]  
> <span data-ttu-id="683c2-116">Los **botones de superíndice y** **subíndice** no se pueden seleccionar a la vez.</span><span class="sxs-lookup"><span data-stu-id="683c2-116">The **Superscript** and **Subscript** buttons cannot both be selected.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="683c2-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="683c2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="683c2-118">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="683c2-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="683c2-119">**UI \_ FONTVERTICALPOSITION**</span><span class="sxs-lookup"><span data-stu-id="683c2-119">**UI\_FONTVERTICALPOSITION**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[<span data-ttu-id="683c2-120">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="683c2-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 