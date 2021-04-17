---
title: ButtonText (Elemento)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. | Elemento ButtonText
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- Elemento ButtonText Windows Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700414"
---
# <a name="buttontext-element"></a><span data-ttu-id="b0b91-105">ButtonText (Elemento)</span><span class="sxs-lookup"><span data-stu-id="b0b91-105">ButtonText Element</span></span>

> [!Note]  
> <span data-ttu-id="b0b91-106">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="b0b91-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b0b91-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="b0b91-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b0b91-108">El elemento **ButtonText** especifica la cadena de texto que Windows Media Player muestra para un botón del panel de tareas.</span><span class="sxs-lookup"><span data-stu-id="b0b91-108">The **ButtonText** element specifies the text string that Windows Media Player displays for a task pane button.</span></span>

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a><span data-ttu-id="b0b91-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="b0b91-109">Attributes</span></span>

<span data-ttu-id="b0b91-110">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="b0b91-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b0b91-111">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="b0b91-111">Parent/Child Elements</span></span>



| <span data-ttu-id="b0b91-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="b0b91-112">Hierarchy</span></span>       | <span data-ttu-id="b0b91-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="b0b91-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="b0b91-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b0b91-114">Parent elements</span></span> | <span data-ttu-id="b0b91-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="b0b91-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="b0b91-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b0b91-116">Child elements</span></span>  | <span data-ttu-id="b0b91-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b0b91-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="b0b91-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0b91-118">Remarks</span></span>

<span data-ttu-id="b0b91-119">Este elemento es necesario para cada instancia de **ServiceTask1**, **ServiceTask2** o **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="b0b91-119">This element is required for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span>

> [!Note]  
> <span data-ttu-id="b0b91-120">Windows Media Player 10 tiene tres paneles de tareas en los que una tienda en línea puede mostrar sus páginas Web.</span><span class="sxs-lookup"><span data-stu-id="b0b91-120">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="b0b91-121">La tienda en línea puede elegir usar uno, dos o los tres paneles de tareas.</span><span class="sxs-lookup"><span data-stu-id="b0b91-121">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="b0b91-122">Windows Media Player 11 solo tiene un panel de tareas, que el usuario puede ver haciendo clic en la pestaña **tiendas en línea** . Windows Media Player 11 omite los elementos **ServiceTask2** y **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="b0b91-122">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="b0b91-123">Windows Media Player puede recortar el texto del botón para ajustarse al espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="b0b91-123">Windows Media Player may crop button text to fit the available space.</span></span> <span data-ttu-id="b0b91-124">El reproductor siempre usa la fuente Tahoma de 8 puntos de negrita para este texto.</span><span class="sxs-lookup"><span data-stu-id="b0b91-124">The Player always uses the Tahoma bold 8-point font for this text.</span></span> <span data-ttu-id="b0b91-125">Hay dos líneas disponibles para mostrar el texto del botón, pero el reproductor no ajusta automáticamente el texto de la primera línea al segundo.</span><span class="sxs-lookup"><span data-stu-id="b0b91-125">There are two lines available to display button text, but the Player does not automatically wrap text from the first line to the second.</span></span> <span data-ttu-id="b0b91-126">Para especificar un salto de línea en el texto del botón, inserte la nueva secuencia de escape de línea " \\ n" en la cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="b0b91-126">To specify a line break in the button text, insert the new line escape sequence "\\n" in your text string.</span></span>

<span data-ttu-id="b0b91-127">La cadena de texto también se muestra en el menú **ir** en la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b0b91-127">The text string is also displayed in the **GoTo** menu in the Windows Media Player user interface.</span></span>

<span data-ttu-id="b0b91-128">Debe probar la tienda en línea con una variedad de opciones de visualización para asegurarse de que el texto se muestre como se espera.</span><span class="sxs-lookup"><span data-stu-id="b0b91-128">You should test your online store using a variety of display settings to ensure that text displays as you expect.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b91-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0b91-129">Requirements</span></span>



| <span data-ttu-id="b0b91-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0b91-130">Requirement</span></span> | <span data-ttu-id="b0b91-131">Value</span><span class="sxs-lookup"><span data-stu-id="b0b91-131">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="b0b91-132">Versión</span><span class="sxs-lookup"><span data-stu-id="b0b91-132">Version</span></span><br/> | <span data-ttu-id="b0b91-133">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b0b91-133">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0b91-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0b91-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b91-135">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="b0b91-135">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="b0b91-136">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="b0b91-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="b0b91-137">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b0b91-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





