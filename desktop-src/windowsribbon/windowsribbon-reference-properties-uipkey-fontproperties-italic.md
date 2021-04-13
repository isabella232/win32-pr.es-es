---
title: UI_PKEY_FontProperties_Italic
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ cursiva.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420855"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="dbf5f-103">UI \_ PKEY \_ FontProperties \_ cursiva</span><span class="sxs-lookup"><span data-stu-id="dbf5f-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="dbf5f-104">Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ cursiva.</span><span class="sxs-lookup"><span data-stu-id="dbf5f-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="dbf5f-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbf5f-105">Remarks</span></span>

<span data-ttu-id="dbf5f-106">\_ \_ \_ Una aplicación usa la interfaz de usuario PKEY FontProperties cursiva para consultar el estado del botón **cursiva** .</span><span class="sxs-lookup"><span data-stu-id="dbf5f-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="dbf5f-107">El valor de la propiedad es de la enumeración [**\_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dbf5f-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="dbf5f-108">El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="dbf5f-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="dbf5f-109">En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dbf5f-109">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="dbf5f-110">El botón **cursiva** está deshabilitado y solo la aplicación puede establecerlo.</span><span class="sxs-lookup"><span data-stu-id="dbf5f-110">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="dbf5f-111">El botón **cursiva** no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="dbf5f-111">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="dbf5f-112">El botón **cursiva** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="dbf5f-112">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="dbf5f-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dbf5f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbf5f-114">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="dbf5f-114">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="dbf5f-115">**UI \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="dbf5f-115">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="dbf5f-116">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="dbf5f-116">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 