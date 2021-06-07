---
title: UI_PKEY_FontProperties_Bold
description: Identifica la propiedad \_ PKEY FontProperties Bold de la \_ interfaz de \_ usuario.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68800d3cfed72382f3576edfc01272c82b46c825
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444386"
---
# <a name="ui_pkey_fontproperties_bold"></a><span data-ttu-id="f9642-103">UI \_ PKEY \_ FontProperties \_ Bold</span><span class="sxs-lookup"><span data-stu-id="f9642-103">UI\_PKEY\_FontProperties\_Bold</span></span>

<span data-ttu-id="f9642-104">Identifica la propiedad \_ PKEY FontProperties Bold de la \_ interfaz de \_ usuario.</span><span class="sxs-lookup"><span data-stu-id="f9642-104">Identifies the UI\_PKEY\_FontProperties\_Bold property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="f9642-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9642-105">Remarks</span></span>

<span data-ttu-id="f9642-106">La \_ interfaz de usuario \_ PKEY FontProperties \_ Bold se usa en una aplicación para consultar el estado del botón **Negrita.**</span><span class="sxs-lookup"><span data-stu-id="f9642-106">UI\_PKEY\_FontProperties\_Bold is used by an application to query the state of the **Bold** button.</span></span>

<span data-ttu-id="f9642-107">El valor de propiedad es de la [**\_ enumeración FONTPROPERTIES de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f9642-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="f9642-108">El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="f9642-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="f9642-109">En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f9642-109">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="f9642-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f9642-110">Property</span></span>                    |    <span data-ttu-id="f9642-111">Resultado de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="f9642-111">UI Result</span></span>                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="f9642-112">**El** botón negrita está deshabilitado y solo la aplicación puede establecerlo.</span><span class="sxs-lookup"><span data-stu-id="f9642-112">**Bold** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="f9642-113">**El** botón Negrita no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f9642-113">**Bold** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="f9642-114">**El** botón Negrita está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f9642-114">**Bold** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="f9642-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f9642-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9642-116">Propiedades del control de fuentes</span><span class="sxs-lookup"><span data-stu-id="f9642-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="f9642-117">**FONTPROPERTIES \_ de la interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="f9642-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="f9642-118">Control de fuentes</span><span class="sxs-lookup"><span data-stu-id="f9642-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 