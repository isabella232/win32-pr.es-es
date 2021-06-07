---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica la propiedad \_ \_ DeltaSize de PKEY de la interfaz de usuario \_ FontProperties.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67778a710de8f69e0aea1134c12fb9ee3ebe0133
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444396"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="ad448-103">UI \_ PKEY \_ FontProperties \_ DeltaSize</span><span class="sxs-lookup"><span data-stu-id="ad448-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="ad448-104">Identifica la propiedad \_ \_ DeltaSize de PKEY de la interfaz de usuario \_ FontProperties.</span><span class="sxs-lookup"><span data-stu-id="ad448-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="ad448-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad448-105">Remarks</span></span>

<span data-ttu-id="ad448-106">La propiedad FontProperties DeltaSize de ui PKEY la usa una aplicación en casos en los que no es posible que la aplicación especifique un valor para Tamaño de fuente, como cuando se selecciona una ejecución de texto de tamaño \_ \_ \_ heterogéneo. </span><span class="sxs-lookup"><span data-stu-id="ad448-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="ad448-107">El **control Tamaño de** fuente está establecido en en blanco y la interfaz de usuario PKEY FontProperties DeltaSize se usa para capturar la interacción del usuario con los botones Crecimiento de fuente y \_ \_ \_ **Reducción de** fuente. </span><span class="sxs-lookup"><span data-stu-id="ad448-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="ad448-108">Ui \_ PKEY FontProperties DeltaSize se incluye en la interfaz de usuario \_ \_ [ \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span><span class="sxs-lookup"><span data-stu-id="ad448-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="ad448-109">En la siguiente captura de pantalla se muestran los **botones Crecimiento** de fuente y **Reducción de** fuente del [**control FontControl de la cinta**](windowsribbon-element-fontcontrol.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="ad448-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de pantalla de los botones de aumento y reducción de fuentes de fuente en el control de fuente.](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="ad448-111">En la tabla siguiente se describen los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ad448-111">The following table describes the property values.</span></span>



|     <span data-ttu-id="ad448-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ad448-112">Value</span></span>                 |  <span data-ttu-id="ad448-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad448-113">Description</span></span>                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="ad448-114">**Haga clic en el** botón Aumentar fuente.</span><span class="sxs-lookup"><span data-stu-id="ad448-114">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="ad448-115">**Se ha hecho clic en** el botón Reducir fuente.</span><span class="sxs-lookup"><span data-stu-id="ad448-115">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ad448-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad448-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad448-117">Propiedades del control de fuentes</span><span class="sxs-lookup"><span data-stu-id="ad448-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="ad448-118">**\_FONTDELTASIZE de la interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="ad448-118">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="ad448-119">Control de fuentes</span><span class="sxs-lookup"><span data-stu-id="ad448-119">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 