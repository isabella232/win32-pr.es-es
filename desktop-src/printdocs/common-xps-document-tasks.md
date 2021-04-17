---
description: En esta página se enumeran algunas de las tareas de programación que se suelen realizar con la API de documentos XPS.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Tareas comunes de programación de documentos XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c40ee0c901b9d906d4d59c69bab4cfc22d8208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677785"
---
# <a name="common-xps-document-programming-tasks"></a>Tareas comunes de programación de documentos XPS

En esta página se enumeran algunas de las tareas de programación que se suelen realizar con la API de documentos XPS.

## <a name="common-xps-document-tasks"></a>Tareas comunes de documentos XPS

En los siguientes ejemplos de código se muestran algunas de las tareas de programación que normalmente se realizan cuando se usa la API de documento XPS para trabajar con un OM XPS.

<dl>

[Inicializar un OM XPS](xps-object-model-initialization.md)  
[Crear un OM XPS en blanco](create-a-blank-xps-om.md)  
[Leer un documento XPS en un OM XPS](read-an-xps-document-into-an-xps-om.md)  
[Navegar por el OM de XPS](navigate-the-xps-om.md)  
[Escribir texto en un OM XPS](write-text-to-an-xps-om.md)  
[Dibujar gráficos en un OM XPS](draw-graphics-in-an-xps-om.md)  
[Colocar imágenes en un OM XPS](place-images-in-an-xps-om.md)  
[Escribir un OM XPS en un documento XPS](write-an-xps-om-to-an-xps-document.md)  
[Imprimir un OM XPS](print-an-xps-om.md)  
[Trabajar con interfaces de colección de XPS OM](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a>Declinación de responsabilidades

Los ejemplos de código no pretenden ser completos ni programas de trabajo. Los ejemplos de código a los que se hace referencia en esta página, por ejemplo, no realizan la comprobación de parámetros, la comprobación de errores ni el control de errores. Use estos ejemplos como punto de partida y, a continuación, agregue el código necesario para crear una aplicación sólida. Para obtener más información sobre los valores devueltos **HRESULT** y las estrategias de control de errores, vea [control de errores en com](../com/error-handling-in-com.md).

Antes de poder usar las interfaces XPS OM, se debe inicializar COM en el subproceso, tal como se muestra en el código de ejemplo siguiente.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Para mayor claridad, en estos ejemplos de código se usa un modelo de objetos de XPS muy sencillo, uno que podría no ser suficientemente complejo para la aplicación. Como punto, en los ejemplos de código que agregan contenido a una página, los elementos visuales de una página se agregan directamente a la lista de objetos visuales de la página. en la práctica, sin embargo, es posible que desee agrupar objetos visuales en objetos de lienzo, de modo que se pueda actuar como grupo en varios objetos. Por lo tanto, para habilitar la compatibilidad del mismo contenido con más de un tamaño de página, puede agrupar el contenido visual de una página en un solo objeto Canvas y, a continuación, aplicar una transformación al lienzo para escalarlo al tamaño de página actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM](../com/error-handling-in-com.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
