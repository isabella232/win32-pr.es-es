---
description: .
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Usar la etiqueta meta para garantizar compatibilidad futura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e965711053a7108c69295ac737953a05536a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717301"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a>Usar la etiqueta meta para garantizar compatibilidad futura

Windows Internet Explorer 8 le permite controlar los modos de compatibilidad de documentos, por lo que puede indicar al explorador que represente las páginas web de la misma manera que las versiones anteriores del explorador. También puede elegir cuándo actualizar la página web, mientras sigue siendo utilizable y funcionar correctamente.

## <a name="setting-the-meta-element"></a>Establecer el elemento meta

El elemento **meta** incluye un atributo de **contenido** que le permite especificar el modo en el que se representa el contenido para la página web, como se muestra en la tabla siguiente.



| Value | Modo de representación                                                 |
|-------|----------------------------------------------------------------|
| IE = 9  | Usar el modo de representación de estándares de Windows Internet Explorer 9   |
| IE = 8  | Usar el modo de representación de estándares de Internet Explorer 8           |
| IE = 7  | Usar el modo de representación de estándares de Windows Internet Explorer 7   |
| IE=5  | Usar el modo de representación de estándares de Microsoft Internet Explorer 5 |



 

Para obtener más información sobre la compatibilidad y el encabezado X-UA-compatible, vea [definir la compatibilidad de documentos](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) en MSDN Library.

En el ejemplo de código siguiente se muestra cómo forzar la representación de una página web en el modo Internet Explorer 8.


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a>Usar un encabezado HTTP

Muchos sitios web contienen miles (o decenas de miles) de páginas web individuales, por lo que no resulta práctico establecer el elemento **meta** en cada documento. Si desea establecer el elemento **meta** para todas las páginas o una colección de páginas seleccionadas por carpeta, puede ajustar la configuración del servidor en su lugar y agregar los metadatos compatibles con X-UA en el [encabezado HTTP](/previous-versions/cc817572(v=msdn.10)).

En el caso de los sitios que requieren diferentes valores de elemento **meta** para las páginas del mismo servidor, hay varias herramientas que generan e insertan automáticamente el elemento **meta** adecuado. Por ejemplo, la utilidad de [herramientas Web de ArtInSoft](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) de Aggiorno inserta y quita la característica de etiqueta de compatibilidad de Internet Explorer 8 y puede ayudar a su sitio a cumplir estándares de compatibilidad específicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
