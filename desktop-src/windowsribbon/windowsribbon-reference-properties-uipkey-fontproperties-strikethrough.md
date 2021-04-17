---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica la \_ propiedad PKEY \_ FontProperties StrikeThrough de la interfaz de usuario \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07804a74671bb219b34b1c67580af083fd5c34c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421250"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a><span data-ttu-id="92c9b-103">PKEY de IU \_ \_ FontProperties \_ tachado</span><span class="sxs-lookup"><span data-stu-id="92c9b-103">UI\_PKEY\_FontProperties\_Strikethrough</span></span>

<span data-ttu-id="92c9b-104">Identifica la \_ propiedad PKEY \_ FontProperties StrikeThrough de la interfaz de usuario \_ .</span><span class="sxs-lookup"><span data-stu-id="92c9b-104">Identifies the UI\_PKEY\_FontProperties\_Strikethrough property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="92c9b-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92c9b-105">Remarks</span></span>

<span data-ttu-id="92c9b-106">\_La interfaz de usuario PKEY \_ FontProperties \_ StrikeThrough se usa en una aplicación para consultar el estado del botón de **tachado** .</span><span class="sxs-lookup"><span data-stu-id="92c9b-106">UI\_PKEY\_FontProperties\_Strikethrough is used by an application to query the state of the **Strikethrough** button.</span></span>

<span data-ttu-id="92c9b-107">El valor de la propiedad es de la enumeración [**\_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="92c9b-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="92c9b-108">El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="92c9b-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="92c9b-109">En la captura de pantalla siguiente se muestra el botón **tachado** de la cinta de opciones [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="92c9b-109">The following screen shot shows the **Strikethrough** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-strikethrough.png)

<span data-ttu-id="92c9b-111">En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="92c9b-111">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                              |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="92c9b-112">El botón **tachado** está deshabilitado y solo la aplicación puede establecerlo.</span><span class="sxs-lookup"><span data-stu-id="92c9b-112">**Strikethrough** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="92c9b-113">El botón **tachado** no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="92c9b-113">**Strikethrough** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="92c9b-114">El botón **tachado** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="92c9b-114">**Strikethrough** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="92c9b-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92c9b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92c9b-116">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="92c9b-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="92c9b-117">**UI \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="92c9b-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="92c9b-118">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="92c9b-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 