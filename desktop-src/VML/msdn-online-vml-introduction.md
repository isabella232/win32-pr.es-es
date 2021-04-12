---
title: Introducción a VML
description: Introducción a VML
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Lenguaje de marcado de vectores (VML), referencia
- VML (Lenguaje de marcado de vectores), referencia
- gráficos vectoriales, referencia de VML
- gráficos vectoriales, Lenguaje de marcado de vectores (VML)
- referencia de Lenguaje de marcado de vectores (VML)
- Referencia de VML
- Lenguaje de marcado de vectores (VML), elemento de forma
- VML (Lenguaje de marcado de vectores), elemento de forma
- gráficos vectoriales, elemento de forma
- Elemento de forma
- Elementos VML, forma
- Lenguaje de marcado de vectores (VML), VBScript
- VML (Lenguaje de marcado de vectores), VBScript
- Lenguaje de marcado de vectores (VML), JavaScript
- VML (Lenguaje de marcado de vectores), JavaScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7a370519e3f173e7418f1aa0510cac768ff46c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420871"
---
# <a name="vml-introduction"></a>Introducción a VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

En este documento se proporciona una referencia detallada completa de la implementación del Lenguaje de marcado de vectores (VML) que se incluye con Microsoft Office 2000. Otras implementaciones pueden variar. Consulte la [especificación de VML](https://www.w3.org/TR/NOTE-datetime.html) para obtener más información sobre VML como estándar.

VML se define como un conjunto de elementos XML y los atributos correspondientes para cada elemento. Dado que el elemento de **forma** es el bloque de creación básico de VML, haga clic [aquí](shape-element--vml.md) para comenzar la referencia.

Tenga en cuenta que esta referencia contiene varios ejemplos y demostraciones. Debe tener Microsoft Internet Explorer 5,0 o posterior instalado para ver el VML en directo.

Además de la información sobre el uso de elementos y atributos como etiquetas XML que amplían HTML, esta referencia contiene sintaxis y ejemplos que muestran cómo usar las características de scripting y Document Object Model de Internet Explorer 5 o posterior. El uso de scripts con VML le permite crear elementos "sobre la marcha" y manipular atributos en tiempo real.

En este ejemplo se usa VBScript y JavaScript. Si utiliza un lenguaje de scripting diferente del que se muestra en un ejemplo, debe coincidir con las mayúsculas y minúsculas de todos los nombres de elementos y atributos. La referencia proporciona sintaxis de scripting que es correcta para los lenguajes que distinguen mayúsculas de minúsculas, como JavaScript. Si duda sobre el caso de caracteres correctos, use un examinador de objetos (por ejemplo, OLEView) para explorar el VGX.DLL para determinar el uso exacto de un elemento o atributo. Tenga en cuenta que cuando se usa VML como etiquetas XML, la distinción de mayúsculas y minúsculas depende del tipo de documento del documento subyacente. Si usa un modo STRICT. DOCTYPE, Elements y Attributes distinguirán mayúsculas de minúsculas.

[Referencia de VML](shape-element--vml.md)

 

 