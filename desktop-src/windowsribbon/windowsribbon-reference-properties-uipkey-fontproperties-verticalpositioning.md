---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifica la propiedad \_ PKEY \_ FontProperties \_ VerticalPositioning de la interfaz de usuario.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954b01ff3271b9f74fac2c130c697a70e910fc93
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444306"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a><span data-ttu-id="cab33-103">UI \_ PKEY \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="cab33-103">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>

<span data-ttu-id="cab33-104">Identifica la propiedad \_ PKEY \_ FontProperties \_ VerticalPositioning de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="cab33-104">Identifies the UI\_PKEY\_FontProperties\_VerticalPositioning property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a><span data-ttu-id="cab33-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cab33-105">Remarks</span></span>

<span data-ttu-id="cab33-106">La propiedad FontProperties VerticalPositioning de ui PKEY la usa una aplicación para consultar el valor de \_ \_ los controles \_ **Superíndice** **y Subíndice.**</span><span class="sxs-lookup"><span data-stu-id="cab33-106">UI\_PKEY\_FontProperties\_VerticalPositioning is used by an application to query the value of the **Superscript** and **Subscript** controls.</span></span>

<span data-ttu-id="cab33-107">El valor de propiedad es de la [**\_ enumeración FONTVERTICALPOSITION de**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="cab33-107">The property value is from the [**UI\_FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) enumeration.</span></span>

<span data-ttu-id="cab33-108">El valor predeterminado es `UI_FONTVERTICALPOSITION_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="cab33-108">The default value is `UI_FONTVERTICALPOSITION_NOTSET`.</span></span>

<span data-ttu-id="cab33-109">En la siguiente captura de pantalla se muestran **los botones Superíndice** y **Subíndice** del [**control FontControl de la cinta**](windowsribbon-element-fontcontrol.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="cab33-109">The following screen shot shows the **Superscript** and **Subscript** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-subsuper.png)

<span data-ttu-id="cab33-111">En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="cab33-111">The following table describes the properties and the UI result.</span></span>



|     <span data-ttu-id="cab33-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cab33-112">Property</span></span>                           |          <span data-ttu-id="cab33-113">Resultado de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="cab33-113">UI Result</span></span>                                                                             |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | <span data-ttu-id="cab33-114">**Los botones** **de superíndice** y subíndice están deshabilitados y solo los puede establecer la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cab33-114">**Superscript** and **Subscript** buttons are disabled and can only be set by the application.</span></span> |
| `UI_FONTVERTICALPOSITION_NOTSET`       | <span data-ttu-id="cab33-115">**Los botones** **De superíndice y Subíndice** no están seleccionados.</span><span class="sxs-lookup"><span data-stu-id="cab33-115">**Superscript** and **Subscript** buttons are not selected.</span></span>                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | <span data-ttu-id="cab33-116">**El botón Superíndice** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="cab33-116">**Superscript** button is selected.</span></span>                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | <span data-ttu-id="cab33-117">**El botón De subíndice** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="cab33-117">**Subscript** button is selected.</span></span>                                                              |



 

> [!Note]  
> <span data-ttu-id="cab33-118">Los **botones Superíndice** **y Subíndice** no se pueden seleccionar.</span><span class="sxs-lookup"><span data-stu-id="cab33-118">The **Superscript** and **Subscript** buttons cannot both be selected.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cab33-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cab33-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cab33-120">Propiedades del control de fuentes</span><span class="sxs-lookup"><span data-stu-id="cab33-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="cab33-121">**UI \_ FONTVERTICALPOSITION**</span><span class="sxs-lookup"><span data-stu-id="cab33-121">**UI\_FONTVERTICALPOSITION**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[<span data-ttu-id="cab33-122">Control de fuentes</span><span class="sxs-lookup"><span data-stu-id="cab33-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 