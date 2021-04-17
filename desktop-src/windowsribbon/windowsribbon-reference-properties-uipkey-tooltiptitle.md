---
title: UI_PKEY_TooltipTitle
description: Identifica la propiedad TooltipTitle de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704729"
---
# <a name="ui_pkey_tooltiptitle"></a><span data-ttu-id="367bc-103">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="367bc-103">UI\_PKEY\_TooltipTitle</span></span>

<span data-ttu-id="367bc-104">Identifica la propiedad TooltipTitle de PKEY de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="367bc-104">Identifies the UI\_PKEY\_TooltipTitle property.</span></span>

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="367bc-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="367bc-105">Remarks</span></span>

<span data-ttu-id="367bc-106">\_ \_ Una aplicación usa la interfaz de usuario PKEY TooltipTitle para consultar la información sobre herramientas, grupos, botones, elementos de la galería y otros controles de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="367bc-106">UI\_PKEY\_TooltipTitle is used by an application to query the tooltip of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

<span data-ttu-id="367bc-107">El valor de propiedad es una cadena restringida a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="367bc-107">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="367bc-108">Use la referencia de caracteres XML del juego de caracteres universal (UCS) `&#xA;` para especificar un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="367bc-108">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="367bc-109">No se admite la alineación derecha.</span><span class="sxs-lookup"><span data-stu-id="367bc-109">Right alignment is not supported.</span></span>

<span data-ttu-id="367bc-110">La longitud máxima del TooltipTitle de PKEY de la interfaz de usuario \_ \_ no está enlazada.</span><span class="sxs-lookup"><span data-stu-id="367bc-110">The maximum length of UI\_PKEY\_TooltipTitle is unbounded.</span></span>

<span data-ttu-id="367bc-111">Para mostrar una y comercial en una información sobre herramientas, escape la designación de carácter especial con un signo de y comercial ( `&&` ) como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="367bc-111">To display an ampersand in a tooltip, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a><span data-ttu-id="367bc-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="367bc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="367bc-113">Propiedades de recursos</span><span class="sxs-lookup"><span data-stu-id="367bc-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="367bc-114">**Comando. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="367bc-114">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[<span data-ttu-id="367bc-115">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="367bc-115">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




