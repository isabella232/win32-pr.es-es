---
title: Error de TabIndex de ARIA
description: Error de TabIndex de ARIA
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104078541"
---
# <a name="aria-tabindex-error"></a><span data-ttu-id="d295d-104">Error de TabIndex de ARIA</span><span class="sxs-lookup"><span data-stu-id="d295d-104">ARIA Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="d295d-105">Texto</span><span class="sxs-lookup"><span data-stu-id="d295d-105">Text</span></span>

<span data-ttu-id="d295d-106">El elemento no está deshabilitado y tiene un controlador de eventos **click** pero tiene **TabIndex** < 0 y no está en el orden de tabulación de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d295d-106">Element is not disabled and has a **click** event handler but it has **tabIndex** < 0 and is not in the tab order by default.</span></span>

## <a name="type"></a><span data-ttu-id="d295d-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d295d-107">Type</span></span>

<span data-ttu-id="d295d-108">Error</span><span class="sxs-lookup"><span data-stu-id="d295d-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="d295d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d295d-109">Description</span></span>

<span data-ttu-id="d295d-110">Este error se aplica a los elementos que tienen un controlador de eventos click y no están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="d295d-110">This error applies to elements that have a click event handler and are not disabled.</span></span> <span data-ttu-id="d295d-111">Estos elementos deben estar en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="d295d-111">These elements must be in the tab order.</span></span> <span data-ttu-id="d295d-112">Esto garantiza que se puede obtener acceso a un elemento mediante la tecla Tab, que es la forma en que los usuarios del lector de pantalla navegan por la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d295d-112">This ensures that an element can be reached using the Tab key, which is how screen reader users typically navigate the UI.</span></span>

<span data-ttu-id="d295d-113">Para corregir este error, establezca el atributo [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) en un valor que sea igual o mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="d295d-113">To fix this error, set the [**tabindex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) attribute to a value that is equal to or greater than 0.</span></span> <span data-ttu-id="d295d-114">No es necesario establecer explícitamente el atributo **TabIndex** para las etiquetas que se encuentran en el orden de tabulación de forma predeterminada, como [**un**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (con el atributo [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) ), el [**botón**](https://developer.mozilla.org/docs/Web/HTML/Element/button), la [**entrada**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (excepto "Hidden"), [**Select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**TextArea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)y [**Area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (como parte del mapa de imágenes).</span><span class="sxs-lookup"><span data-stu-id="d295d-114">You do not need to explicitly set the **tabindex** attribute for tags that are in the tab order by default, such as [**a**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (with [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) attribute), [**button**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**input**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (excluding "hidden"), [**select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea), and [**area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (as part of the image map).</span></span>

## <a name="example"></a><span data-ttu-id="d295d-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d295d-115">Example</span></span>


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




