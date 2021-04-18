---
title: UI_PKEY_FontProperties_Bold
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ Bold.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dca8a58b9c5bfa51cfba8d80a477dafb744dfb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705007"
---
# <a name="ui_pkey_fontproperties_bold"></a><span data-ttu-id="e580c-103">UI \_ PKEY \_ FontProperties \_ Bold</span><span class="sxs-lookup"><span data-stu-id="e580c-103">UI\_PKEY\_FontProperties\_Bold</span></span>

<span data-ttu-id="e580c-104">Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ Bold.</span><span class="sxs-lookup"><span data-stu-id="e580c-104">Identifies the UI\_PKEY\_FontProperties\_Bold property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="e580c-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e580c-105">Remarks</span></span>

<span data-ttu-id="e580c-106">\_ \_ \_ Una aplicación usa la interfaz de usuario PKEY FontProperties Bold para consultar el estado del botón **negrita** .</span><span class="sxs-lookup"><span data-stu-id="e580c-106">UI\_PKEY\_FontProperties\_Bold is used by an application to query the state of the **Bold** button.</span></span>

<span data-ttu-id="e580c-107">El valor de la propiedad es de la enumeración [**\_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e580c-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="e580c-108">El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="e580c-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="e580c-109">En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e580c-109">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                     |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="e580c-110">El botón **negrita** está deshabilitado y solo la aplicación puede establecerlo.</span><span class="sxs-lookup"><span data-stu-id="e580c-110">**Bold** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="e580c-111">El botón **negrita** no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e580c-111">**Bold** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="e580c-112">El botón **negrita** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e580c-112">**Bold** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="e580c-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e580c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e580c-114">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="e580c-114">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="e580c-115">**UI \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="e580c-115">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="e580c-116">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="e580c-116">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 