---
title: Modelo de objetos de texto
description: Esta sección contiene información sobre los elementos de programación usados con El modelo de objetos de texto (TOM).
ms.assetid: vs|controls|~\controls\richedit\textobjectmodel.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cec69cb8f35d9125df561aa45771f0ca32aef67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166054"
---
# <a name="text-object-model"></a>Modelo de objetos de texto

Esta sección contiene información sobre los elementos de programación usados con El modelo de objetos de texto (TOM).

TOM define un conjunto sustancial de interfaces de manipulación de texto. Las soluciones de texto, como Microsoft Word controles de edición enriquecidos y de texto completo, admiten el conjunto de características TOM. TOM se vio muy influenciado por WordBasic (el lenguaje de programación que se usa para Word) y es fácil de usar desde Microsoft Visual Basic para Aplicaciones (VBA). Esta compatibilidad tiene varias ventajas:

-   El código puede migrarse con bastante facilidad de una solución a otra.
-   Se puede usar un idioma para compartir información de texto entre distintos motores de texto.
-   Reduce la necesidad de documentación y código en comparación con las interfaces independientes de modelo de objetos componentes (COM) y VBA de bajo nivel.

Sin embargo, puede ser menos eficaz para C/C++ que el uso de interfaces COM de nivel inferior más generales.

TOM es un conjunto sencillo de interfaces que se implementan para sus soluciones de texto principal, word y controles de edición enriquecciones. Sin embargo, para las aplicaciones que dan un énfasis menor al texto, es mejor proporcionar interfaces TOM transfiriendo el texto a un control de edición que admita TOM. Dado que los controles de edición enriquecidos se envían con sistemas operativos de Microsoft, son el medio estándar para obtener la funcionalidad TOM.

### <a name="overviews"></a>Temas de introducción



| Tema                                                          | Contenido                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca del modelo de objetos de texto](about-text-object-model.md)         | El objeto Modelo de objetos de texto (TOM) de nivel superior se define mediante la interfaz [**ITextDocument,**](/windows/desktop/api/Tom/nn-tom-itextdocument) que tiene métodos para crear y recuperar objetos inferiores en la jerarquía de objetos.<br/> |
| [Usar el modelo de objetos de texto](using-the-text-object-model.md) | Los ejemplos de código de este documento muestran varios aspectos del uso del Modelo de objetos de texto (TOM).<br/>                                                                                                          |



 

### <a name="interfaces"></a>Interfaces




| Tema | Contenido | 
|-------|----------|
| <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> | La <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>interfaz ITextDocument</strong></a> es la interfaz de nivel superior de TOM, que recupera los objetos de selección y rango activos para cualquier caso del documento, ya sea activo o no. Permite que la aplicación:<ul><li>Abra y guarde documentos.</li><li>Controlar el comportamiento de deshacer y la actualización de pantalla.</li><li>Busque un intervalo desde una posición de pantalla.</li><li>Obtiene un <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>enumerador de historias de ITextStoryRanges.</strong></a></li></ul><br /><strong>Cuándo implementar</strong><br /> Las aplicaciones normalmente no implementan la <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>interfaz ITextDocument.</strong></a> Las soluciones de texto de Microsoft, como los controles de edición enriquecidos, implementan <strong>ITextDocument</strong> como parte de su implementación de TOM. <br /><strong>Cuándo usar</strong><br /> Las aplicaciones pueden recuperar un <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>puntero ITextDocument</strong></a> de un control de edición enriquecido. Para ello, envíe un mensaje <a href="em-getoleinterface.md"><strong>de EM_GETOLEINTERFACE</strong></a> para recuperar un <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>objeto IRichEditOle</strong></a> de un control de edición enriquecido. A continuación, llame al método <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown::QueryInterface</strong></a> del objeto para recuperar un <strong>puntero ITextDocument.</strong><br /> | 
| <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> | Se accede a los atributos de intervalo de texto enriquecido de TOM a través de un par de interfaces duales, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>e ITextPara</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a> | Se accede a los atributos de intervalo de texto enriquecido de TOM a través de un par de interfaces duales, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>e ITextPara</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> | Los <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>objetos ITextRange</strong></a> son eficaces herramientas de edición y enlace de datos que permiten a un programa seleccionar texto en un caso y, a continuación, examinar o cambiar ese texto.<br /> | 
| <a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a> | Una selección de texto es un intervalo de texto con resaltado de selección.<br /> | 
| <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> | El propósito de la <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>interfaz ITextStoryRanges</strong></a> es enumerar los casos de <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>un objeto ITextDocument.</strong></a><br /> | 




 

 

