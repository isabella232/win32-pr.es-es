---
title: UI_PKEY_FontProperties_Size
description: Identifica la propiedad de tamaño de la interfaz de usuario \_ PKEY \_ FontProperties \_ .
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685476"
---
# <a name="ui_pkey_fontproperties_size"></a><span data-ttu-id="23ad5-103">Tamaño de FontProperties de UI \_ PKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="23ad5-103">UI\_PKEY\_FontProperties\_Size</span></span>

<span data-ttu-id="23ad5-104">Identifica la propiedad de tamaño de la interfaz de usuario \_ PKEY \_ FontProperties \_ .</span><span class="sxs-lookup"><span data-stu-id="23ad5-104">Identifies the UI\_PKEY\_FontProperties\_Size property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a><span data-ttu-id="23ad5-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23ad5-105">Remarks</span></span>

<span data-ttu-id="23ad5-106">\_ \_ \_ Una aplicación usa el tamaño de FontProperties de PKEY de interfaz de usuario para consultar el valor del control de **tamaño de fuente** .</span><span class="sxs-lookup"><span data-stu-id="23ad5-106">UI\_PKEY\_FontProperties\_Size is used by an application to query the value of the **Font size** control.</span></span>

<span data-ttu-id="23ad5-107">Los valores válidos para esta propiedad oscilan entre 1 y 9999, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="23ad5-107">Valid values for this property range from 1 to 9999, inclusive.</span></span> <span data-ttu-id="23ad5-108">Si un usuario intenta escribir un valor no válido, se rechaza la entrada y el control de **tamaño de fuente** vuelve al último valor válido.</span><span class="sxs-lookup"><span data-stu-id="23ad5-108">If a user tries to enter an invalid value, the entry is rejected and the **Font size** control reverts to the last valid value.</span></span>

<span data-ttu-id="23ad5-109">Si una aplicación intenta establecer un tamaño de fuente mediante programación en un valor fuera del intervalo válido, el marco de la cinta de opciones invalida todas las propiedades de fuente y establece los controles de fuente (**tamaño de fuente** y **fuente**) en blanco o en su estado predeterminado, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="23ad5-109">If an application attempts to set font size programmatically to a value outside the valid range, the Ribbon framework invalidates all font properties and sets the font controls (**Font size** and **Font face**) to blank or to their default state, where appropriate.</span></span>

<span data-ttu-id="23ad5-110">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="23ad5-110">The default value is 0.</span></span>

<span data-ttu-id="23ad5-111">Un valor de 0 especifica que no se selecciona ningún tamaño de punto único (ya sea ningún texto o una ejecución de texto de tamaño heterogéneo).</span><span class="sxs-lookup"><span data-stu-id="23ad5-111">A value of 0 specifies that no single point size is selected (either no text, or a run of heterogeneously sized text, is selected).</span></span>

<span data-ttu-id="23ad5-112">Un usuario no puede establecer el control de **tamaño de fuente** en 0.</span><span class="sxs-lookup"><span data-stu-id="23ad5-112">A user cannot set the **Font size** control to 0.</span></span>

<span data-ttu-id="23ad5-113">Distinto de 0, los valores válidos para el intervalo de tamaño de la interfaz de usuario \_ PKEY \_ FontProperties \_ entre *MinimumFontSize* y *MaximumFontSize* , tal y como se declara en el marcado de [control de fuentes](windowsribbon-controls-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="23ad5-113">Other than 0, valid values for UI\_PKEY\_FontProperties\_Size range between *MinimumFontSize* and *MaximumFontSize* as declared in the [Font Control](windowsribbon-controls-fontcontrol.md) markup.</span></span>

> [!Note]  
> <span data-ttu-id="23ad5-114">El control de **tamaño de fuente** se establece en blanco cuando el tamaño de fuente se establece mediante programación en 0, por ejemplo, cuando se resalta una ejecución de texto de tamaño heterogéneo.</span><span class="sxs-lookup"><span data-stu-id="23ad5-114">The **Font size** control is set to blank when the font size is programmatically set to 0, such as when a run of heterogeneously sized text is highlighted.</span></span>

 

<span data-ttu-id="23ad5-115">Cuando se selecciona una ejecución de texto de tamaño heterogéneo, la aplicación debe consultar la [interfaz de usuario \_ PKEY \_ FontProperties \_ deltas](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) para capturar los comandos **aumentar fuente** y **reducir fuente** .</span><span class="sxs-lookup"><span data-stu-id="23ad5-115">Where a run of heterogeneously sized text is selected, the application should query [UI\_PKEY\_FontProperties\_DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) to capture **Grow font** and **Shrink font** commands.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23ad5-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23ad5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23ad5-117">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="23ad5-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="23ad5-118">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="23ad5-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




