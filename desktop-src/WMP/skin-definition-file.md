---
title: Archivo de definición de máscara
description: Archivo de definición de máscara
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Aspectos de Windows Media Player, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd06708a99a15dc9a8266278850c0507007f058
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704725"
---
# <a name="skin-definition-file"></a><span data-ttu-id="4281f-107">Archivo de definición de máscara</span><span class="sxs-lookup"><span data-stu-id="4281f-107">Skin Definition File</span></span>

<span data-ttu-id="4281f-108">Los archivos de definición de máscara contienen las instrucciones básicas sobre lo que hace la máscara y dónde se pueden encontrar otros archivos usados por la máscara.</span><span class="sxs-lookup"><span data-stu-id="4281f-108">Skin definition files contain the basic instructions for what the skin does and where other files used by the skin can be found.</span></span> <span data-ttu-id="4281f-109">Solo puede haber un archivo de definición de máscara para una máscara y una extensión de nombre de archivo. WMS.</span><span class="sxs-lookup"><span data-stu-id="4281f-109">There can only be one skin definition file for a skin, and it has a .wms file name extension.</span></span>

<span data-ttu-id="4281f-110">Las instrucciones del archivo de definición de máscara se escriben en lenguaje de marcado extensible (XML), que es similar a HTML.</span><span class="sxs-lookup"><span data-stu-id="4281f-110">The instructions in the skin definition file are written in Extensible Markup Language (XML), which is similar to HTML.</span></span> <span data-ttu-id="4281f-111">Si ha usado HTML para crear páginas web, verá que XML resulta familiar.</span><span class="sxs-lookup"><span data-stu-id="4281f-111">If you have used HTML to create webpages, you will find that XML looks familiar.</span></span>

<span data-ttu-id="4281f-112">El XML en el archivo de definición de máscara utiliza un conjunto de etiquetas de elementos especiales para definir partes de la interfaz de usuario de máscara.</span><span class="sxs-lookup"><span data-stu-id="4281f-112">The XML in the skin definition file uses a set of special element tags to define parts of the skin user interface.</span></span> <span data-ttu-id="4281f-113">Por ejemplo, el elemento [Button](button-element.md) define cómo se comportará un botón, dónde irá y cuál será el aspecto.</span><span class="sxs-lookup"><span data-stu-id="4281f-113">For example, the [BUTTON](button-element.md) element defines how a button will behave, where it will go, and what it will look like.</span></span>

<span data-ttu-id="4281f-114">Cada etiqueta de elemento tiene atributos específicos.</span><span class="sxs-lookup"><span data-stu-id="4281f-114">Each element tag has specific attributes.</span></span> <span data-ttu-id="4281f-115">Por ejemplo, el elemento [Button](button-element.md) tiene un atributo **Image** que define dónde se puede encontrar la imagen del botón.</span><span class="sxs-lookup"><span data-stu-id="4281f-115">For example, the [BUTTON](button-element.md) element has an **image** attribute that defines where the picture for the button can be found.</span></span> <span data-ttu-id="4281f-116">Esto es similar a HTML, donde el elemento BODY tendrá un atributo **bgcolor** que define el color de fondo de la página HTML.</span><span class="sxs-lookup"><span data-stu-id="4281f-116">This is similar to HTML, where the BODY element will have a **bgcolor** attribute that defines the background color of the HTML page.</span></span> <span data-ttu-id="4281f-117">En la sección [referencia de programación](skin-programming-reference.md) de la máscara se incluye información detallada sobre todos los elementos de máscara y sus atributos.</span><span class="sxs-lookup"><span data-stu-id="4281f-117">Detailed information about all skin elements and their attributes is included in the [Skin Programming Reference](skin-programming-reference.md) section.</span></span>

<span data-ttu-id="4281f-118">XML tiene algunas reglas sencillas que debe conocer para crear máscaras.</span><span class="sxs-lookup"><span data-stu-id="4281f-118">XML has a few simple rules that you need to know to create skins.</span></span> <span data-ttu-id="4281f-119">A diferencia de HTML, XML requiere que siga las reglas exactamente.</span><span class="sxs-lookup"><span data-stu-id="4281f-119">Unlike HTML, XML requires you to follow the rules exactly.</span></span>

## <a name="enclose-elements-with-angle-brackets"></a><span data-ttu-id="4281f-120">Incluir elementos con corchetes angulares</span><span class="sxs-lookup"><span data-stu-id="4281f-120">Enclose Elements with Angle Brackets</span></span>

<span data-ttu-id="4281f-121">Todos los elementos se incluyen entre corchetes angulares. por ejemplo, el elemento de **botón** se escribe de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="4281f-121">All elements are enclosed by angle brackets; for example, the **BUTTON** element is typed like this:</span></span>


```C++
<BUTTON>

```



<span data-ttu-id="4281f-122">No es necesario escribir la palabra "BUTTON" en mayúsculas, pero la Convención de escribir nombres de elementos en mayúsculas se usa en el código de ejemplo de este SDK.</span><span class="sxs-lookup"><span data-stu-id="4281f-122">You do not need to type the word "BUTTON" in all uppercase letters, but the convention of typing element names in all uppercase is used in the example code of this SDK.</span></span>

## <a name="put-attributes-before-the-closing-bracket"></a><span data-ttu-id="4281f-123">Colocar atributos antes del corchete de cierre</span><span class="sxs-lookup"><span data-stu-id="4281f-123">Put Attributes Before the Closing Bracket</span></span>

<span data-ttu-id="4281f-124">Todos los atributos de un elemento determinado deben incluirse antes del corchete angular de cierre.</span><span class="sxs-lookup"><span data-stu-id="4281f-124">All attributes for a particular element must be included before the closing angle bracket.</span></span> <span data-ttu-id="4281f-125">Un atributo consta del nombre del atributo seguido de un signo igual (=) y el valor del atributo entre comillas.</span><span class="sxs-lookup"><span data-stu-id="4281f-125">An attribute consists of the attribute name followed by an equal sign (=) and the value of the attribute in quotes.</span></span>


```C++
<BUTTON image="mypic.jpg">

```



<span data-ttu-id="4281f-126">No es necesario escribir la palabra "imagen" en minúsculas, pero la Convención de escribir nombres de atributo en minúsculas se usa en el código de ejemplo de este SDK.</span><span class="sxs-lookup"><span data-stu-id="4281f-126">You do not need to type the word "image" in lowercase, but the convention of typing attribute names in lowercase is used in the example code of this SDK.</span></span> <span data-ttu-id="4281f-127">Tenga en cuenta también que el valor del atributo está entre comillas.</span><span class="sxs-lookup"><span data-stu-id="4281f-127">Also note that the value of the attribute is enclosed in quotation marks.</span></span>

## <a name="opening-and-closing-elements"></a><span data-ttu-id="4281f-128">Abrir y cerrar elementos</span><span class="sxs-lookup"><span data-stu-id="4281f-128">Opening and Closing Elements</span></span>

<span data-ttu-id="4281f-129">Algunos elementos se agrupan dentro de otro elemento.</span><span class="sxs-lookup"><span data-stu-id="4281f-129">Some elements are grouped together inside another element.</span></span> <span data-ttu-id="4281f-130">Por ejemplo, el elemento **BUTTONGROUP** no tiene mucho sentido a menos que use uno o varios elementos **BUTTONELEMENT** con él.</span><span class="sxs-lookup"><span data-stu-id="4281f-130">For example, the **BUTTONGROUP** element does not make a lot of sense unless you use one or more **BUTTONELEMENT** elements with it.</span></span> <span data-ttu-id="4281f-131">Para que la agrupación sea clara, debe tener una etiqueta de apertura y de cierre para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="4281f-131">To make the grouping clear, you need to have an opening and closing tag for each element.</span></span> <span data-ttu-id="4281f-132">La etiqueta de apertura es solo el nombre de elemento y los atributos relacionados, rodeados por corchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="4281f-132">The opening tag is just the element name and any related attributes, surrounded by angle brackets.</span></span> <span data-ttu-id="4281f-133">La etiqueta de cierre es el nombre del elemento, precedido por una barra diagonal (/) y, a continuación, entre corchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="4281f-133">The closing tag is the element name, preceded by a forward slash (/), and then enclosed by angle brackets.</span></span> <span data-ttu-id="4281f-134">Por ejemplo, la etiqueta de apertura del elemento **BUTTONGROUP** tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="4281f-134">For example, the **BUTTONGROUP** element opening tag looks like this:</span></span>


```C++
<BUTTONGROUP>

```



<span data-ttu-id="4281f-135">La etiqueta **BUTTONGROUP** de cierre tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="4281f-135">The closing **BUTTONGROUP** tag looks like this:</span></span>


```C++
</BUTTONGROUP>

```



<span data-ttu-id="4281f-136">Colocaría las etiquetas **BUTTONELEMENT** entre las etiquetas de elemento **BUTTONGROUP** de apertura y cierre.</span><span class="sxs-lookup"><span data-stu-id="4281f-136">You would put the **BUTTONELEMENT** tags between the opening and closing **BUTTONGROUP** element tags.</span></span> <span data-ttu-id="4281f-137">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4281f-137">For example:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a><span data-ttu-id="4281f-138">Cerrar elementos</span><span class="sxs-lookup"><span data-stu-id="4281f-138">Closing Off Elements</span></span>

<span data-ttu-id="4281f-139">Si un elemento no tiene ningún otro elemento dentro de él, debe colocar una barra diagonal al final del nombre del elemento justo antes del corchete angular de cierre.</span><span class="sxs-lookup"><span data-stu-id="4281f-139">If an element has no other elements inside it, you must put a forward slash at the end of the element name just before the closing angle bracket.</span></span> <span data-ttu-id="4281f-140">Por ejemplo, en el código anterior, cada elemento **BUTTONELEMENT** tiene una barra diagonal para indicar que no hay otros elementos anidados en él.</span><span class="sxs-lookup"><span data-stu-id="4281f-140">For example, in the code above, each **BUTTONELEMENT** element has a forward slash to indicate that there are no other elements nested within it.</span></span>

<span data-ttu-id="4281f-141">En otras palabras, debe tener una etiqueta de elemento de cierre o cerrar el elemento con una barra diagonal.</span><span class="sxs-lookup"><span data-stu-id="4281f-141">In other words, you must either have a closing element tag or close off your element with a forward slash.</span></span>

<span data-ttu-id="4281f-142">Esto es correcto:</span><span class="sxs-lookup"><span data-stu-id="4281f-142">This is correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="4281f-143">Esto no es correcto:</span><span class="sxs-lookup"><span data-stu-id="4281f-143">This is not correct:</span></span>


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="4281f-144">Esto tampoco es correcto:</span><span class="sxs-lookup"><span data-stu-id="4281f-144">This is also not correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



<span data-ttu-id="4281f-145">En la sección siguiente se proporciona más información acerca de los archivos de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="4281f-145">The following section provides more information about skin definition files:</span></span>

-   [<span data-ttu-id="4281f-146">Estructura del archivo de definición de máscara</span><span class="sxs-lookup"><span data-stu-id="4281f-146">Skin Definition File Structure</span></span>](skin-definition-file-structure.md)

## <a name="related-topics"></a><span data-ttu-id="4281f-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4281f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4281f-148">**Archivos de máscara**</span><span class="sxs-lookup"><span data-stu-id="4281f-148">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




