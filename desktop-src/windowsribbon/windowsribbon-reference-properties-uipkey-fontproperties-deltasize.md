---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica la \_ propiedad PKEY FontProperties de la interfaz de usuario \_ \_ .
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0046edf41fa61382d45a0662119d8fda237a0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077768"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="4c7b1-103">PKEY de IU \_ \_ FontProperties \_ deltas</span><span class="sxs-lookup"><span data-stu-id="4c7b1-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="4c7b1-104">Identifica la \_ propiedad PKEY FontProperties de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4c7b1-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="4c7b1-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c7b1-105">Remarks</span></span>

<span data-ttu-id="4c7b1-106">La interfaz de usuario \_ PKEY \_ FontProperties \_ deltas se usa en una aplicación en los casos en los que la aplicación no puede especificar un valor para el **tamaño de fuente**, como cuando se selecciona una ejecución de texto de tamaño heterogéneo.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="4c7b1-107">El control de **tamaño de fuente** se establece en Blank y la interfaz de \_ \_ usuario PKEY FontProperties \_ se usa para capturar la interacción del usuario con los botones **aumentar tamaño de fuente** y **reducir fuente** .</span><span class="sxs-lookup"><span data-stu-id="4c7b1-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="4c7b1-108">La \_ interfaz \_ de usuario PKEY FontProperties \_ deltas se incluye en la [interfaz de usuario \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span><span class="sxs-lookup"><span data-stu-id="4c7b1-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="4c7b1-109">En la captura de pantalla siguiente se muestran los botones de **expansión de fuente** y **reducción de fuente** de la cinta de opciones [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="4c7b1-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de pantalla de los botones de expansión de fuente y reducción de fuente en fontcontrol.](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="4c7b1-111">En la tabla siguiente se describen los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-111">The following table describes the property values.</span></span>



|                           |                                 |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="4c7b1-112">Botón **aumentar fuente** , haga clic en él.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-112">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="4c7b1-113">Botón **reducir fuente** en el que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-113">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4c7b1-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c7b1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c7b1-115">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="4c7b1-115">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="4c7b1-116">**UI \_ FONTDELTASIZE**</span><span class="sxs-lookup"><span data-stu-id="4c7b1-116">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="4c7b1-117">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="4c7b1-117">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 