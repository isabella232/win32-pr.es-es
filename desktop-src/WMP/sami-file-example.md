---
title: Ejemplo de archivo SAMI
description: Ejemplo de archivo SAMI
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Modelo de objetos de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio de multimedia accesible sincronizado (SAMI)
- Windows Media Player Mobile, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX de Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX móvil de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- Control ActiveX, intercambio de multimedia accesible sincronizado (SAMI)
- Intercambio de contenido multimedia accesible sincronizado (SAMI), archivos
- SAMI (intercambio de multimedia accesible sincronizado), archivos
- Intercambio de multimedia accesible sincronizado (SAMI), código de ejemplo
- SAMI (intercambio de multimedia accesible sincronizado), código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9634de52f71b4ca1db151bdf9104c3891c8ce5d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "103914005"
---
# <a name="sami-file-example"></a><span data-ttu-id="2fc00-114">Ejemplo de archivo SAMI</span><span class="sxs-lookup"><span data-stu-id="2fc00-114">SAMI File Example</span></span>

<span data-ttu-id="2fc00-115">El código de ejemplo siguiente es un archivo SAMI completo con un conjunto de texto de subtítulos y varias declaraciones de clase para el estilo de texto y el idioma del título.</span><span class="sxs-lookup"><span data-stu-id="2fc00-115">The following example code is a complete SAMI file with one set of closed caption text and several class declarations for text style and caption language.</span></span>


```C++
<SAMI>
<HEAD>
   <STYLE TYPE = "text/css">
   <!--
   /* P defines the basic style selector for closed caption paragraph text */
   P {font-family:sans-serif; color:white;}
   /* Source, Small, and Big define additional ID selectors for closed caption text */
   #Source {color: orange; font-family: arial; font-size: 12pt;}
   #Small {Name: SmallTxt; font-size: 8pt; color: yellow;}
   #Big {Name: BigTxt; font-size: 12pt; color: magenta;}
   /* ENUSCC and FRFRCC define language class selectors for closed caption text */
   .ENUSCC {Name: 'English Captions'; lang: en-US; SAMIType: CC;}
   .FRFRCC {Name: 'French Captions'; lang: fr-FR; SAMIType: CC;}
   -->
   </STYLE>
</HEAD>
<BODY>
   <!<entity type="mdash"/>- The closed caption text displays at 1000 milliseconds. -->
   <SYNC Start = 1000>
      <!-- English closed captions -->
      <P Class = ENUSCC ID = Source>Narrator
      <P Class = ENUSCC>Great reason to visit Seattle, brought to you by two out-of-staters.
      <!-- French closed captions -->
      <P Class = FRFRCC ID = Source>Narrateur
      <P Class = FRFRCC>Deux personnes ne venant la r&eacute;gion vous donnent de bonnes raisons de visiter Seattle.
</BODY>
</SAMI>

```



<span data-ttu-id="2fc00-116">Los estilos definidos dentro de un archivo SAMI se ajustan a la sintaxis de selector de CSS estándar para elementos, clases e identificadores.</span><span class="sxs-lookup"><span data-stu-id="2fc00-116">Styles defined within a SAMI file conform to standard CSS selector syntax for elements, classes, and IDs.</span></span> <span data-ttu-id="2fc00-117">En el elemento BODY, todos los elementos P tienen el estilo definido para el selector de elementos P en el elemento STYLE.</span><span class="sxs-lookup"><span data-stu-id="2fc00-117">In the BODY element, all P elements have the style defined for the P element selector in the STYLE element.</span></span> <span data-ttu-id="2fc00-118">El atributo class de un elemento especifica el idioma de ese elemento tal y como se define en los selectores de clase en el elemento STYLE (los selectores que comienzan con puntos).</span><span class="sxs-lookup"><span data-stu-id="2fc00-118">The class attribute of an element specifies the language of that element as defined by the class selectors in the STYLE element (the selectors beginning with periods).</span></span> <span data-ttu-id="2fc00-119">Los nombres de idioma especificados por los selectores de clase pueden ser cualquier cadena.</span><span class="sxs-lookup"><span data-stu-id="2fc00-119">The language names specified by the class selectors can be any string.</span></span> <span data-ttu-id="2fc00-120">Los elementos con el atributo ID especificado tienen un estilo adicional aplicado según lo indicado por los selectores de identificador en el elemento STYLE (los selectores precedidos de \# caracteres).</span><span class="sxs-lookup"><span data-stu-id="2fc00-120">Elements with the ID attribute specified have additional styling applied as indicated by the ID selectors in the STYLE element (the selectors prefixed with \# characters).</span></span>

<span data-ttu-id="2fc00-121">Cuando se usa junto con el modelo de objetos de Media Player de Windows, los selectores de clase corresponden a *ClosedCaption*. Propiedad **SAMILang** , que se puede usar para especificar el idioma de los títulos.</span><span class="sxs-lookup"><span data-stu-id="2fc00-121">When used in conjunction with the Windows Media Player object model, the class selectors correspond to the *ClosedCaption*.**SAMILang** property, which can be used to specify the language of the captions.</span></span> <span data-ttu-id="2fc00-122">Los selectores de identificador corresponden a *ClosedCaption*. Propiedad **SAMIStyle** , que se puede usar para especificar el estilo en el que aparecerán los títulos.</span><span class="sxs-lookup"><span data-stu-id="2fc00-122">The ID selectors correspond to the *ClosedCaption*.**SAMIStyle** property, which can be used to specify the style the captions will appear in.</span></span>

<span data-ttu-id="2fc00-123">Para obtener más información acerca de la creación de archivos SAMI, vea Descripción de SAMI 1,0 en el [sitio web de Microsoft](/documentation/).</span><span class="sxs-lookup"><span data-stu-id="2fc00-123">For more information about creating SAMI files, see Understanding SAMI 1.0 at the [Microsoft website](/documentation/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fc00-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2fc00-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fc00-125">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="2fc00-125">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 