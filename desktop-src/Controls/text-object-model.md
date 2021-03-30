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
# <a name="text-object-model"></a>Modelo de objetos de texto

Esta sección contiene información sobre los elementos de programación utilizados con el modelo de objetos de texto (TOM).

TOM define un conjunto considerable de interfaces de manipulación de texto. Las soluciones de texto como Microsoft Word y los controles Rich Edit admiten el conjunto de características TOM. Los TOM se han influenciado en gran medida en WordBasic (el lenguaje de programación usado para Word) y es fácil de usar en Microsoft Visual Basic para Aplicaciones (VBA). Esta compatibilidad tiene varias ventajas:

-   El código se puede migrar fácilmente de una solución a otra.
-   Se puede usar un lenguaje para compartir información de texto entre distintos motores de texto.
-   Reduce la necesidad de documentación y código en comparación con las interfaces independientes del modelo de objetos componentes (COM) de bajo nivel y de VBA.

Sin embargo, puede ser menos eficaz para los fines de C/C++ que el uso de interfaces COM de nivel inferior más generales.

TOM es un conjunto sencillo de interfaces que se implementan para sus soluciones de texto principal, Word y controles Rich Edit. Sin embargo, para las aplicaciones que imponen un énfasis menor en el texto, es mejor proporcionar interfaces TOM mediante la transferencia del texto a un control de edición que admita TOM. Dado que los controles de edición enriquecida se distribuyen con los sistemas operativos de Microsoft, son el medio estándar para obtener la funcionalidad de TOM.

### <a name="overviews"></a>Temas de introducción



| Tema                                                          | Contenido                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca del modelo de objetos de texto](about-text-object-model.md)         | El objeto del modelo de objetos de texto (TOM) de nivel superior se define mediante la interfaz [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) , que tiene métodos para crear y recuperar objetos inferiores en la jerarquía de objetos.<br/> |
| [Usar el modelo de objetos de texto](using-the-text-object-model.md) | Los ejemplos de código de este documento muestran varios aspectos del uso del modelo de objetos de texto (TOM).<br/>                                                                                                          |



 

### <a name="interfaces"></a>Interfaces



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></td>
<td>La interfaz <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> es la interfaz de nivel superior Tom, que recupera los objetos de selección e intervalo activos de cualquier caso en el documento, ya sea activo o no. Permite que la aplicación:
<ul>
<li>Abrir y guardar documentos.</li>
<li>Controlar el comportamiento de deshacer y la actualización de la pantalla.</li>
<li>Buscar un intervalo desde una posición de la pantalla.</li>
<li>Obtiene un enumerador de casos <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> .</li>
</ul>
<br/> <strong>Cuándo implementar</strong><br/> Normalmente, las aplicaciones no implementan la interfaz <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> . Las soluciones de texto de Microsoft, como los controles Rich Edit, implementan <strong>ITextDocument</strong> como parte de su implementación de Tom. <br/> <strong>Cuándo usar</strong><br/> Las aplicaciones pueden recuperar un puntero <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> de un control Rich Edit. Para ello, envíe un mensaje de <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> para recuperar un objeto <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> de un control Rich Edit. A continuación, llame al método <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown:: QueryInterface</strong></a> del objeto para recuperar un puntero <strong>ITextDocument</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></td>
<td>Se obtiene acceso a los atributos de intervalo de texto enriquecido TOM a través de un par de interfaces duales, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> y <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></td>
<td>Se obtiene acceso a los atributos de intervalo de texto enriquecido TOM a través de un par de interfaces duales, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> y <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></td>
<td>Los objetos <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> son eficaces herramientas de edición y enlace de datos que permiten a un programa Seleccionar texto en un caso y, a continuación, examinar o cambiar el texto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></td>
<td>Una selección de texto es un intervalo de texto con resaltado de selección.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></td>
<td>El propósito de la interfaz <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> es enumerar los casos de un <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

