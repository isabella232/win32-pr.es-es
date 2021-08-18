---
description: Uso de la etiqueta meta para garantizar la compatibilidad futura
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Uso de la etiqueta meta para garantizar la compatibilidad futura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0cff3dab146d67303d57c97b2298614c5ae0142b18a3bd2d141fbf90e86ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994595"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a>Uso de la etiqueta meta para garantizar la compatibilidad futura

Windows Internet Explorer 8 permite controlar los modos de compatibilidad de documentos, por lo que puede indicar al explorador que represente las páginas web de la misma manera que las versiones anteriores del explorador. También puede elegir cuándo actualizar la página web, mientras sigue siendo utilizable y funciona correctamente.

## <a name="setting-the-meta-element"></a>Establecer el elemento Meta

El **meta** elemento incluye un **atributo content** que permite especificar el modo en el que se representa el contenido para la página web, como se muestra en la tabla siguiente.



| Value | Modo de representación                                                 |
|-------|----------------------------------------------------------------|
| IE=9  | Uso del modo de representación Windows Internet Explorer estándares 9   |
| IE=8  | Uso del modo de representación Internet Explorer estándares 8           |
| IE=7  | Usar el modo de representación Windows Internet Explorer estándares 7   |
| IE=5  | Uso del modo de representación Internet Explorer estándares de Microsoft Internet Explorer 5 |



 

Para obtener más información sobre la compatibilidad y el encabezado compatible con X-UA, vea Definir la compatibilidad [de documentos](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) en MSDN Library.

En el ejemplo de código siguiente se muestra cómo forzar que una página web se represente en Internet Explorer modo 8.


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



## <a name="using-an-http-header"></a>Uso de un encabezado HTTP

Muchos sitios web contienen miles (o decenas de miles) de páginas web individuales, por lo que establecer el **meta** elemento en cada documento no es práctico. Si desea establecer el **meta** elemento para todas las páginas o una colección de páginas seleccionadas por carpeta, puede ajustar la configuración del servidor en su lugar y agregar los metadatos compatibles con X-UA en el [encabezado HTTP](/previous-versions/cc817572(v=msdn.10)).

Para los sitios que requieren valores de **meta** element diferentes para las páginas del mismo servidor, hay varias herramientas que generan e insertan automáticamente el **meta** elemento adecuado. Por ejemplo, la utilidad [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) de Aprocesamiento inserta y quita la característica de etiqueta de compatibilidad Internet Explorer 8 y puede ayudar a su sitio a cumplir estándares de compatibilidad específicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
