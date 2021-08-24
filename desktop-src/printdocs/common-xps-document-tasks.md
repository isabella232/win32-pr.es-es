---
description: En esta página se enumeran algunas de las tareas de programación que se realizan normalmente con la API de documentos XPS.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Tareas comunes de programación de documentos XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7f71614344968bcc68e658021e1f34296a595d9fbf58be2d544c03c3dc428f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846355"
---
# <a name="common-xps-document-programming-tasks"></a>Tareas comunes de programación de documentos XPS

En esta página se enumeran algunas de las tareas de programación que se realizan normalmente con la API de documentos XPS.

## <a name="common-xps-document-tasks"></a>Tareas comunes del documento XPS

En los ejemplos de código siguientes se muestran algunas de las tareas de programación que se realizan normalmente cuando se usa la API de documentos XPS para trabajar con un OM XPS.

<dl>

[Inicialización de una instancia de XPS OM](xps-object-model-initialization.md)  
[Crear un OM xps en blanco](create-a-blank-xps-om.md)  
[Lectura de un documento XPS en una om xps](read-an-xps-document-into-an-xps-om.md)  
[Navegar por xps om](navigate-the-xps-om.md)  
[Escribir texto en un OM XPS](write-text-to-an-xps-om.md)  
[Dibujar gráficos en un OM XPS](draw-graphics-in-an-xps-om.md)  
[Colocar imágenes en una om xps](place-images-in-an-xps-om.md)  
[Escribir una om xps en un documento XPS](write-an-xps-om-to-an-xps-document.md)  
[Imprimir una OM XPS](print-an-xps-om.md)  
[Trabajar con interfaces de colección de OM xps](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a>Declinación de responsabilidades

Los ejemplos de código no están diseñados para ser programas completos y en funcionamiento. Los ejemplos de código a los que se hace referencia en esta página, por ejemplo, no realizan la comprobación de parámetros, la comprobación de errores o el control de errores. Use estos ejemplos como punto de partida y agregue el código necesario para crear una aplicación sólida. Para obtener más información sobre **los valores devueltos de HRESULT** y las estrategias de control de errores, vea [Control de errores en COM](../com/error-handling-in-com.md).

Para poder usar interfaces XPS OM, COM debe inicializarse en el subproceso, como se muestra en el código de ejemplo siguiente.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Para mayor claridad, estos ejemplos de código usan un OM XPS muy sencillo, que podría no ser lo suficientemente complejo para la aplicación. Por ejemplo, en los ejemplos de código que agregan contenido a una página, los elementos visuales de una página se agregan directamente a la lista de objetos visuales de la página. En la práctica, sin embargo, es posible que desee agrupar objetos visuales en objetos de lienzo, para que se pueda actuar sobre varios objetos como un grupo. Por lo tanto, para habilitar la compatibilidad con el mismo contenido para más de un tamaño de página, podría agrupar el contenido visual de una página en un único objeto de lienzo y, a continuación, aplicar una transformación al lienzo para escalarlo al tamaño de página actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM](../com/error-handling-in-com.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
