---
title: Modelo de objetos de texto
description: Esta sección contiene información sobre los elementos de programación utilizados con el modelo de objetos de texto (TOM).
ms.assetid: vs|controls|~\controls\richedit\textobjectmodel.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7625ca7772da7f4e10aa7d64159971ee0e259d2a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103904874"
---
# <a name="text-object-model"></a><span data-ttu-id="928fd-103">Modelo de objetos de texto</span><span class="sxs-lookup"><span data-stu-id="928fd-103">Text Object Model</span></span>

<span data-ttu-id="928fd-104">Esta sección contiene información sobre los elementos de programación utilizados con el modelo de objetos de texto (TOM).</span><span class="sxs-lookup"><span data-stu-id="928fd-104">This section contains information about the programming elements used with the Text Object Model (TOM).</span></span>

<span data-ttu-id="928fd-105">TOM define un conjunto considerable de interfaces de manipulación de texto.</span><span class="sxs-lookup"><span data-stu-id="928fd-105">The TOM defines a substantial set of text manipulation interfaces.</span></span> <span data-ttu-id="928fd-106">Las soluciones de texto como Microsoft Word y los controles Rich Edit admiten el conjunto de características TOM.</span><span class="sxs-lookup"><span data-stu-id="928fd-106">Text solutions such as Microsoft Word and rich edit controls support the TOM feature set.</span></span> <span data-ttu-id="928fd-107">Los TOM se han influenciado en gran medida en WordBasic (el lenguaje de programación usado para Word) y es fácil de usar en Microsoft Visual Basic para Aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="928fd-107">TOM was greatly influenced by WordBasic (the programming language used for Word) and it is easy to use from Microsoft Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="928fd-108">Esta compatibilidad tiene varias ventajas:</span><span class="sxs-lookup"><span data-stu-id="928fd-108">This compatibility has several advantages:</span></span>

-   <span data-ttu-id="928fd-109">El código se puede migrar fácilmente de una solución a otra.</span><span class="sxs-lookup"><span data-stu-id="928fd-109">Code can migrate fairly easily from one solution to another.</span></span>
-   <span data-ttu-id="928fd-110">Se puede usar un lenguaje para compartir información de texto entre distintos motores de texto.</span><span class="sxs-lookup"><span data-stu-id="928fd-110">One language can be used to share text information between different text engines.</span></span>
-   <span data-ttu-id="928fd-111">Reduce la necesidad de documentación y código en comparación con las interfaces independientes del modelo de objetos componentes (COM) de bajo nivel y de VBA.</span><span class="sxs-lookup"><span data-stu-id="928fd-111">It reduces the need for documentation and code compared to the separate low-level Component Object Model (COM) and VBA interfaces.</span></span>

<span data-ttu-id="928fd-112">Sin embargo, puede ser menos eficaz para los fines de C/C++ que el uso de interfaces COM de nivel inferior más generales.</span><span class="sxs-lookup"><span data-stu-id="928fd-112">However, it can be less efficient for C/C++ purposes than the use of more general lower level COM interfaces.</span></span>

<span data-ttu-id="928fd-113">TOM es un conjunto sencillo de interfaces que se implementan para sus soluciones de texto principal, Word y controles Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="928fd-113">TOM is a straightforward set of interfaces to implement for its primary text solutions, Word and rich edit controls.</span></span> <span data-ttu-id="928fd-114">Sin embargo, para las aplicaciones que imponen un énfasis menor en el texto, es mejor proporcionar interfaces TOM mediante la transferencia del texto a un control de edición que admita TOM.</span><span class="sxs-lookup"><span data-stu-id="928fd-114">However, for applications that place minor emphasis on text, it is better to provide TOM interfaces by transferring the text to an edit control that supports TOM.</span></span> <span data-ttu-id="928fd-115">Dado que los controles de edición enriquecida se distribuyen con los sistemas operativos de Microsoft, son el medio estándar para obtener la funcionalidad de TOM.</span><span class="sxs-lookup"><span data-stu-id="928fd-115">Since rich edit controls ship with Microsoft operating systems, they are the standard means of obtaining TOM functionality.</span></span>

### <a name="overviews"></a><span data-ttu-id="928fd-116">Temas de introducción</span><span class="sxs-lookup"><span data-stu-id="928fd-116">Overviews</span></span>



| <span data-ttu-id="928fd-117">Tema</span><span class="sxs-lookup"><span data-stu-id="928fd-117">Topic</span></span>                                                          | <span data-ttu-id="928fd-118">Contenido</span><span class="sxs-lookup"><span data-stu-id="928fd-118">Contents</span></span>                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="928fd-119">Acerca del modelo de objetos de texto</span><span class="sxs-lookup"><span data-stu-id="928fd-119">About Text Object Model</span></span>](about-text-object-model.md)         | <span data-ttu-id="928fd-120">El objeto del modelo de objetos de texto (TOM) de nivel superior se define mediante la interfaz [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) , que tiene métodos para crear y recuperar objetos inferiores en la jerarquía de objetos.</span><span class="sxs-lookup"><span data-stu-id="928fd-120">The top-level Text Object Model (TOM) object is defined by the [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) interface, which has methods for creating and retrieving objects lower in the object hierarchy.</span></span><br/> |
| [<span data-ttu-id="928fd-121">Usar el modelo de objetos de texto</span><span class="sxs-lookup"><span data-stu-id="928fd-121">Using The Text Object Model</span></span>](using-the-text-object-model.md) | <span data-ttu-id="928fd-122">Los ejemplos de código de este documento muestran varios aspectos del uso del modelo de objetos de texto (TOM).</span><span class="sxs-lookup"><span data-stu-id="928fd-122">The code samples in this document show various aspects of using the Text Object Model (TOM).</span></span><br/>                                                                                                          |



 

### <a name="interfaces"></a><span data-ttu-id="928fd-123">Interfaces</span><span class="sxs-lookup"><span data-stu-id="928fd-123">Interfaces</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="928fd-124">Tema</span><span class="sxs-lookup"><span data-stu-id="928fd-124">Topic</span></span></th>
<th><span data-ttu-id="928fd-125">Contenido</span><span class="sxs-lookup"><span data-stu-id="928fd-125">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="928fd-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="928fd-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span></span></td>
<td><span data-ttu-id="928fd-127">La interfaz <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> es la interfaz de nivel superior Tom, que recupera los objetos de selección e intervalo activos de cualquier caso en el documento, ya sea activo o no.</span><span class="sxs-lookup"><span data-stu-id="928fd-127">The <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface is the TOM top-level interface, which retrieves the active selection and range objects for any story in the document whether active or not.</span></span> <span data-ttu-id="928fd-128">Permite que la aplicación:</span><span class="sxs-lookup"><span data-stu-id="928fd-128">It enables the application to:</span></span>
<ul>
<li><span data-ttu-id="928fd-129">Abrir y guardar documentos.</span><span class="sxs-lookup"><span data-stu-id="928fd-129">Open and save documents.</span></span></li>
<li><span data-ttu-id="928fd-130">Controlar el comportamiento de deshacer y la actualización de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="928fd-130">Control undo behavior and screen updating.</span></span></li>
<li><span data-ttu-id="928fd-131">Buscar un intervalo desde una posición de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="928fd-131">Find a range from a screen position.</span></span></li>
<li><span data-ttu-id="928fd-132">Obtiene un enumerador de casos <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="928fd-132">Get an <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> story enumerator.</span></span></li>
</ul>
<br/> <span data-ttu-id="928fd-133"><strong>Cuándo implementar</strong></span><span class="sxs-lookup"><span data-stu-id="928fd-133"><strong>When to Implement</strong></span></span><br/> <span data-ttu-id="928fd-134">Normalmente, las aplicaciones no implementan la interfaz <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="928fd-134">Applications typically do not implement the <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface.</span></span> <span data-ttu-id="928fd-135">Las soluciones de texto de Microsoft, como los controles Rich Edit, implementan <strong>ITextDocument</strong> como parte de su implementación de Tom.</span><span class="sxs-lookup"><span data-stu-id="928fd-135">Microsoft text solutions, such as rich edit controls, implement <strong>ITextDocument</strong> as part of their TOM implementation.</span></span> <br/> <span data-ttu-id="928fd-136"><strong>Cuándo usar</strong></span><span class="sxs-lookup"><span data-stu-id="928fd-136"><strong>When to Use</strong></span></span><br/> <span data-ttu-id="928fd-137">Las aplicaciones pueden recuperar un puntero <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="928fd-137">Applications can retrieve an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> pointer from a rich edit control.</span></span> <span data-ttu-id="928fd-138">Para ello, envíe un mensaje de <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> para recuperar un objeto <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="928fd-138">To do this, send an <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> message to retrieve an <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> object from a rich edit control.</span></span> <span data-ttu-id="928fd-139">A continuación, llame al método <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown:: QueryInterface</strong></a> del objeto para recuperar un puntero <strong>ITextDocument</strong> .</span><span class="sxs-lookup"><span data-stu-id="928fd-139">Then, call the object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown::QueryInterface</strong></a> method to retrieve an <strong>ITextDocument</strong> pointer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="928fd-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span><span class="sxs-lookup"><span data-stu-id="928fd-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span></span></td>
<td><span data-ttu-id="928fd-141">Se obtiene acceso a los atributos de intervalo de texto enriquecido TOM a través de un par de interfaces duales, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> y <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="928fd-141">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="928fd-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span><span class="sxs-lookup"><span data-stu-id="928fd-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span></span></td>
<td><span data-ttu-id="928fd-143">Se obtiene acceso a los atributos de intervalo de texto enriquecido TOM a través de un par de interfaces duales, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> y <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="928fd-143">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="928fd-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="928fd-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span></span></td>
<td><span data-ttu-id="928fd-145">Los objetos <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> son eficaces herramientas de edición y enlace de datos que permiten a un programa Seleccionar texto en un caso y, a continuación, examinar o cambiar el texto.</span><span class="sxs-lookup"><span data-stu-id="928fd-145">The <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> objects are powerful editing and data-binding tools that allow a program to select text in a story and then examine or change that text.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="928fd-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="928fd-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span></span></td>
<td><span data-ttu-id="928fd-147">Una selección de texto es un intervalo de texto con resaltado de selección.</span><span class="sxs-lookup"><span data-stu-id="928fd-147">A text selection is a text range with selection highlighting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="928fd-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span><span class="sxs-lookup"><span data-stu-id="928fd-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span></span></td>
<td><span data-ttu-id="928fd-149">El propósito de la interfaz <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> es enumerar los casos de un <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="928fd-149">The purpose of the <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> interface is to enumerate the stories in an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

