---
title: UI_PKEY_LabelDescription
description: Identifica la propiedad LabelDescription de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb81e723d5f55dcfd63f1bb89bff4741b4e088e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903609"
---
# <a name="ui_pkey_labeldescription"></a><span data-ttu-id="f305c-103">UI \_ PKEY \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="f305c-103">UI\_PKEY\_LabelDescription</span></span>

<span data-ttu-id="f305c-104">Identifica la propiedad LabelDescription de PKEY de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f305c-104">Identifies the UI\_PKEY\_LabelDescription property.</span></span>

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="f305c-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f305c-105">Remarks</span></span>

<span data-ttu-id="f305c-106">\_ \_ Una aplicación usa la interfaz de usuario PKEY LabelDescription para consultar la descripción asociada a [una \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f305c-106">UI\_PKEY\_LabelDescription is used by an application to query the description associated with a [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span>

<span data-ttu-id="f305c-107">El valor de propiedad es una cadena restringida a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="f305c-107">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="f305c-108">Use la referencia de caracteres XML del juego de caracteres universal (UCS) `&#xA;` para especificar un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="f305c-108">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="f305c-109">La longitud máxima es sin límite.</span><span class="sxs-lookup"><span data-stu-id="f305c-109">The maximum length is unbounded.</span></span>

<span data-ttu-id="f305c-110">No se admite la alineación derecha.</span><span class="sxs-lookup"><span data-stu-id="f305c-110">Right alignment is not supported.</span></span>

<span data-ttu-id="f305c-111">En la captura de pantalla siguiente se muestra el uso de una etiqueta y una descripción de etiqueta asociada en un menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f305c-111">The following screen shot illustrates the use of a label and an associated label description in an Application Menu.</span></span>

![captura de pantalla que muestra una etiqueta y una descripción de etiqueta asociada en un menú de la aplicación.](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a><span data-ttu-id="f305c-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f305c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f305c-114">Propiedades de recursos</span><span class="sxs-lookup"><span data-stu-id="f305c-114">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="f305c-115">**Comando. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="f305c-115">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[<span data-ttu-id="f305c-116">\_Etiqueta PKEY de IU \_</span><span class="sxs-lookup"><span data-stu-id="f305c-116">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 




