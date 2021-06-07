---
title: UI_PKEY_FontProperties_Underline
description: Identifica la propiedad \_ FontProperties Underline de PKEY \_ de la interfaz de \_ usuario.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066027e5f62416667619937eea7dbe493a3ff279
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443786"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="9438a-103">Subrayado \_ fontproperties PKEY de la interfaz \_ de \_ usuario</span><span class="sxs-lookup"><span data-stu-id="9438a-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="9438a-104">Identifica la propiedad \_ FontProperties Underline de PKEY \_ de la interfaz de \_ usuario.</span><span class="sxs-lookup"><span data-stu-id="9438a-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="9438a-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9438a-105">Remarks</span></span>

<span data-ttu-id="9438a-106">La \_ interfaz de usuario \_ PKEY FontProperties \_ Underline se usa en una aplicación para consultar el estado del botón **Subrayado.**</span><span class="sxs-lookup"><span data-stu-id="9438a-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="9438a-107">El valor de propiedad es de la [**\_ enumeración FONTUNDERLINE de la interfaz de**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) usuario.</span><span class="sxs-lookup"><span data-stu-id="9438a-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="9438a-108">El valor predeterminado es `UI_FONTUNDERLINE_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="9438a-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="9438a-109">En la captura de pantalla siguiente se muestra **el botón Subrayado** de [**FontControl de**](windowsribbon-element-fontcontrol.md)la cinta de opciones .</span><span class="sxs-lookup"><span data-stu-id="9438a-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-underline.png)

<span data-ttu-id="9438a-111">En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9438a-111">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="9438a-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9438a-112">Property</span></span>                   |       <span data-ttu-id="9438a-113">Resultado de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="9438a-113">UI Result</span></span>                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="9438a-114">**El** botón Subrayado está deshabilitado y solo la aplicación puede establecerlo.</span><span class="sxs-lookup"><span data-stu-id="9438a-114">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="9438a-115">**El botón** Subrayado no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9438a-115">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="9438a-116">**El botón** Subrayado está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9438a-116">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="9438a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9438a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9438a-118">Propiedades del control de fuentes</span><span class="sxs-lookup"><span data-stu-id="9438a-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="9438a-119">**\_FONTUNDERLINE de la interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="9438a-119">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="9438a-120">Control de fuentes</span><span class="sxs-lookup"><span data-stu-id="9438a-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 