---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica la propiedad \_ Tachado PKEY FontProperties de la interfaz \_ de \_ usuario.
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b684704fdd90a8dd1b88b14db2b52540b15fccb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443796"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a><span data-ttu-id="1c5dc-103">UI \_ PKEY \_ FontProperties \_ Strikethrough</span><span class="sxs-lookup"><span data-stu-id="1c5dc-103">UI\_PKEY\_FontProperties\_Strikethrough</span></span>

<span data-ttu-id="1c5dc-104">Identifica la propiedad \_ Tachado PKEY FontProperties de la interfaz \_ de \_ usuario.</span><span class="sxs-lookup"><span data-stu-id="1c5dc-104">Identifies the UI\_PKEY\_FontProperties\_Strikethrough property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="1c5dc-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c5dc-105">Remarks</span></span>

<span data-ttu-id="1c5dc-106">Una aplicación usa la interfaz de usuario PKEY FontProperties Strikethrough para consultar \_ el estado del botón \_ \_ **Tachado.**</span><span class="sxs-lookup"><span data-stu-id="1c5dc-106">UI\_PKEY\_FontProperties\_Strikethrough is used by an application to query the state of the **Strikethrough** button.</span></span>

<span data-ttu-id="1c5dc-107">El valor de propiedad es de la [**\_ enumeración FONTPROPERTIES de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1c5dc-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="1c5dc-108">El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="1c5dc-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="1c5dc-109">En la siguiente captura de pantalla se muestra **el botón Tachado** del control [**FontControl de la cinta**](windowsribbon-element-fontcontrol.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="1c5dc-109">The following screen shot shows the **Strikethrough** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-strikethrough.png)

<span data-ttu-id="1c5dc-111">En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1c5dc-111">The following table describes the properties and the UI result.</span></span>



|   <span data-ttu-id="1c5dc-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1c5dc-112">Property</span></span>                       |    <span data-ttu-id="1c5dc-113">Resultado de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="1c5dc-113">UI Result</span></span>                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="1c5dc-114">**El botón Tachado** está deshabilitado y solo la aplicación puede establecerlo.</span><span class="sxs-lookup"><span data-stu-id="1c5dc-114">**Strikethrough** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="1c5dc-115">**El botón Tachado** no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="1c5dc-115">**Strikethrough** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="1c5dc-116">**El botón Tachado** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="1c5dc-116">**Strikethrough** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="1c5dc-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c5dc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c5dc-118">Propiedades del control de fuentes</span><span class="sxs-lookup"><span data-stu-id="1c5dc-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="1c5dc-119">**FONTPROPERTIES \_ de la interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="1c5dc-119">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="1c5dc-120">Control de fuentes</span><span class="sxs-lookup"><span data-stu-id="1c5dc-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 