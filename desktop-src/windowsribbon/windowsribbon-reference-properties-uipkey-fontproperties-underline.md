---
title: UI_PKEY_FontProperties_Underline
description: Identifica la \_ propiedad de \_ subrayado PKEY FontProperties de la interfaz de usuario \_ .
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 380c3fdadb636775f80b789a585c42ff2369234a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487955"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="98a33-103">Subrayado de UI \_ PKEY \_ FontProperties \_</span><span class="sxs-lookup"><span data-stu-id="98a33-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="98a33-104">Identifica la \_ propiedad de \_ subrayado PKEY FontProperties de la interfaz de usuario \_ .</span><span class="sxs-lookup"><span data-stu-id="98a33-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="98a33-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98a33-105">Remarks</span></span>

<span data-ttu-id="98a33-106">\_ \_ \_ Una aplicación usa el subrayado FontProperties PKEY de interfaz de usuario para consultar el estado del botón de **subrayado** .</span><span class="sxs-lookup"><span data-stu-id="98a33-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="98a33-107">El valor de la propiedad es de la enumeración [**\_ FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="98a33-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="98a33-108">El valor predeterminado es `UI_FONTUNDERLINE_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="98a33-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="98a33-109">En la captura de pantalla siguiente se muestra el botón **subrayado** de la cinta de opciones [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="98a33-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-underline.png)

<span data-ttu-id="98a33-111">En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="98a33-111">The following table describes the properties and the UI result.</span></span>



|                                 |                                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="98a33-112">El botón **subrayado** está deshabilitado y solo la aplicación puede establecerlo.</span><span class="sxs-lookup"><span data-stu-id="98a33-112">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="98a33-113">El botón **subrayado** no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="98a33-113">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="98a33-114">El botón **subrayado** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="98a33-114">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="98a33-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98a33-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98a33-116">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="98a33-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="98a33-117">**UI \_ FONTUNDERLINE**</span><span class="sxs-lookup"><span data-stu-id="98a33-117">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="98a33-118">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="98a33-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 