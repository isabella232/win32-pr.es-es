---
title: UI_PKEY_FontProperties_Italic
description: Identifica la propiedad Ui \_ PKEY \_ FontProperties \_ Italic.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d0dfa07b5112e91d8c25a4ff8c4f31175adf9b7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443816"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="95746-103">UI \_ PKEY \_ FontProperties \_ Italic</span><span class="sxs-lookup"><span data-stu-id="95746-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="95746-104">Identifica la propiedad Ui \_ PKEY \_ FontProperties \_ Italic.</span><span class="sxs-lookup"><span data-stu-id="95746-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="95746-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95746-105">Remarks</span></span>

<span data-ttu-id="95746-106">Una aplicación usa ui PKEY FontProperties Italic para consultar \_ el estado del botón \_ \_ **Cursiva.**</span><span class="sxs-lookup"><span data-stu-id="95746-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="95746-107">El valor de propiedad es de la [**\_ enumeración FONTPROPERTIES de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="95746-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="95746-108">El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="95746-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="95746-109">En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="95746-109">The following table describes the properties and the UI result.</span></span>



|    <span data-ttu-id="95746-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="95746-110">Property</span></span>                      |       <span data-ttu-id="95746-111">Resultado de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="95746-111">UI Result</span></span>                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="95746-112">**El** botón Cursiva está deshabilitado y solo la aplicación puede establecerlo.</span><span class="sxs-lookup"><span data-stu-id="95746-112">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="95746-113">**El** botón Cursiva no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="95746-113">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="95746-114">**El** botón Cursiva está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="95746-114">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="95746-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95746-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95746-116">Propiedades del control de fuentes</span><span class="sxs-lookup"><span data-stu-id="95746-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="95746-117">**FONTPROPERTIES \_ de la interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="95746-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="95746-118">Control de fuentes</span><span class="sxs-lookup"><span data-stu-id="95746-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 