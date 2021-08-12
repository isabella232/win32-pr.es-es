---
title: Introducción a VML
description: Introducción a VML
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Lenguaje de marcado de vectores (VML),reference
- VML (Lenguaje de marcado de vectores),reference
- gráficos vectoriales, referencia de VML
- vector graphics,Lenguaje de marcado de vectores (VML)
- referencia de Lenguaje de marcado de vectores (VML)
- Referencia de VML
- Lenguaje de marcado de vectores (VML), elemento Shape
- VML (Lenguaje de marcado de vectores),Elemento Shape
- gráficos vectoriales, elemento Shape
- Elemento Shape
- Elementos VML, Forma
- Lenguaje de marcado de vectores (VML),VBScript
- VML (Lenguaje de marcado de vectores),VBScript
- Lenguaje de marcado de vectores (VML),Javascript
- VML (Lenguaje de marcado de vectores),Javascript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c694f87cab48a3f5da78db0e32ea576b889dbc3f6e49ba886c56d46b6ca244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600151"
---
# <a name="vml-introduction"></a>Introducción a VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

En este documento se proporciona una referencia detallada completa a la implementación de Lenguaje de marcado de vectores (VML) que se incluye con Microsoft Office 2000. Otras implementaciones pueden variar. Consulte la [especificación de VML](https://www.w3.org/TR/NOTE-datetime.html) para obtener más información sobre VML como estándar.

VML se define como un conjunto de elementos XML y los atributos correspondientes para cada elemento. Puesto que **el elemento Shape** es el bloque de creación básico de VML, haga clic [aquí](shape-element--vml.md) para comenzar la referencia.

Tenga en cuenta que esta referencia contiene varios ejemplos y demostraciones. Debe tener Microsoft Internet Explorer 5.0 o superior instalado para ver la VML en directo.

Además de la información sobre el uso de elementos y atributos como etiquetas XML que extienden HTML, esta referencia contiene sintaxis y ejemplos que muestran cómo usar el scripting y las características Document Object Model de Internet Explorer 5 o superior. El uso de script con VML permite crear elementos "sobre la marcha" y manipular atributos en tiempo real.

En estos ejemplos de esta referencia se usa VBScript y Javascript. Si usa un lenguaje de scripting diferente al que se muestra en un ejemplo, debe coincidir con el caso de todos los nombres de elemento y atributo. La referencia proporciona una sintaxis de scripting que es correcta para lenguajes que distinguen mayúsculas de minúsculas, como JavaScript. Si duda sobre el caso de caracteres correcto, use un explorador de objetos (como OLEView) para explorar el VGX.DLL para determinar el caso exacto de un elemento o atributo. Tenga en cuenta que cuando vml se usa como etiquetas XML, la confidencialidad de mayúsculas y minúsculas depende del tipo de documento subyacente. Si usa un modo strict . DOCTYPE, los elementos y los atributos distinguen mayúsculas de minúsculas.

[Referencia de VML](shape-element--vml.md)

 

 