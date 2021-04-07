---
title: UI_PKEY_Label
description: Identifica la \_ propiedad de etiqueta PKEY de la interfaz de usuario \_ .
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245ce8d239e1a0893c907a047aa9a48996cbf606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903610"
---
# <a name="ui_pkey_label"></a><span data-ttu-id="d0019-103">\_Etiqueta PKEY de IU \_</span><span class="sxs-lookup"><span data-stu-id="d0019-103">UI\_PKEY\_Label</span></span>

<span data-ttu-id="d0019-104">Identifica la \_ propiedad de etiqueta PKEY de la interfaz de usuario \_ .</span><span class="sxs-lookup"><span data-stu-id="d0019-104">Identifies the UI\_PKEY\_Label property.</span></span>

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="d0019-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0019-105">Remarks</span></span>

<span data-ttu-id="d0019-106">\_ \_ La etiqueta PKEY de la interfaz de usuario se usa en una aplicación para consultar el texto de la etiqueta de pestañas, grupos, botones, elementos de la galería y otros controles de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="d0019-106">UI\_PKEY\_Label is used by an application to query the label text of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

> [!Note]  
> <span data-ttu-id="d0019-107">Windows 8 y versiones más recientes: imagen del botón de menú de la [aplicación](windowsribbon-controls-applicationmenu.md) cambiada a etiqueta: **archivo**.</span><span class="sxs-lookup"><span data-stu-id="d0019-107">Windows 8 and newer: [Application Menu](windowsribbon-controls-applicationmenu.md) button image changed to label: **File**.</span></span> <span data-ttu-id="d0019-108">Se recomienda no usar archivo como etiqueta para ninguna de sus propias pestañas.</span><span class="sxs-lookup"><span data-stu-id="d0019-108">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

<span data-ttu-id="d0019-109">El valor de propiedad es una cadena restringida a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="d0019-109">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="d0019-110">Use la referencia de caracteres XML del juego de caracteres universal (UCS) `&#xA;` para especificar un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="d0019-110">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="d0019-111">No se admite la alineación derecha.</span><span class="sxs-lookup"><span data-stu-id="d0019-111">Right alignment is not supported.</span></span>

<span data-ttu-id="d0019-112">La longitud máxima de la etiqueta PKEY de la interfaz de usuario \_ \_ no está enlazada.</span><span class="sxs-lookup"><span data-stu-id="d0019-112">The maximum length of UI\_PKEY\_Label is unbounded.</span></span>

<span data-ttu-id="d0019-113">Si un comando se expone a través de un elemento de menú y el valor de la etiqueta [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o UI \_ PKEY \_ contiene una letra precedida por un símbolo de y comercial, como se muestra en el ejemplo siguiente, esta letra se trata como un KeyTip y una tecla de aceleración para ese comando por el marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="d0019-113">If a Command is exposed through a menu item and the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or UI\_PKEY\_Label contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="d0019-114">Para mostrar una y comercial en una etiqueta, escape la designación de carácter especial con un signo de y comercial ( `&&` ), tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d0019-114">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a><span data-ttu-id="d0019-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0019-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0019-116">Propiedades de recursos</span><span class="sxs-lookup"><span data-stu-id="d0019-116">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="d0019-117">**Comando. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="d0019-117">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[<span data-ttu-id="d0019-118">UI \_ PKEY \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="d0019-118">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




