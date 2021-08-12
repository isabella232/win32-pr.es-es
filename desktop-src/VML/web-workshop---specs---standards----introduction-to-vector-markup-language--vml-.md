---
title: Lenguaje de marcado de vectores (VML)
description: Lenguaje de marcado de vectores (VML)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Lenguaje de marcado de vectores (VML),about
- VML (Lenguaje de marcado de vectores),about
- gráficos vectoriales, acerca de
- vector graphics,Lenguaje de marcado de vectores (VML)
- Lenguaje de marcado de vectores (VML),World Wide Web Consortium (W3C)
- VML (Lenguaje de marcado de vectores),World Wide Web Consortium (W3C)
- vector graphics,World Wide Web Consortium (W3C)
- gráficos vectoriales, ventajas de VML
- Lenguaje de marcado de vectores (VML), ventajas
- VML (Lenguaje de marcado de vectores),benefits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6199b481c58bbc5cd769ba43e614f21ae0105b4ef703858b559cdd76ff5516bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596071"
---
# <a name="vector-markup-language-vml"></a>Lenguaje de marcado de vectores (VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!NOTE]
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

Lenguaje de marcado de vectores (VML) es un formato de intercambio, edición y entrega basado en XML para gráficos vectoriales de alta calidad en la Web que satisface las necesidades tanto de los usuarios de productividad como de los profesionales del diseño gráfico. XML es un lenguaje emergente basado en texto simple, flexible y abierto que complementa a HTML. (Consulte la [sección XML](/documentation/?frame=true) de MSDN Library para obtener información detallada sobre XML).

VmL es compatible actualmente con Microsoft Internet Explorer versión 5.0 o posterior.

VmL se ha propuesto al W3C como un estándar para gráficos vectoriales en la Web (consulte Lenguaje de marcado de vectores [(VML)](https://www.w3.org/TR/NOTE-VML)). Microsoft sigue a la cabeza en el desarrollo y la implementación de tecnologías basadas en XML, trabajando con asociados líderes del sector (AutoDesk, Autodesk-Pcl, Macromedia, Visio) y el W3C para avanzar en los estándares basados en web. Esperamos trabajar con el W3C para, en última instancia, llevar a un formato estándar para gráficos vectoriales en la Web.

VML también es compatible con Microsoft Office 2000 o posterior. Microsoft Word, Microsoft Excel y Microsoft PowerPoint se pueden usar para crear gráficos VML.

### <a name="using-vml"></a>Uso de VML

Para usar VML en las páginas web, use un elemento de estilo para importar el comportamiento de VML, como se muestra en el código siguiente.

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

A continuación, declare el espacio de nombres VML, como se muestra en el ejemplo de código siguiente.

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

Por último, agregue elementos VML para definir los efectos de los objetos visuales. Por ejemplo, el siguiente código VML crea un óvalo rojo.

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> Para obtener mejores resultados al usar documentos en modo estricto, asegúrese de que el marcado es válido y correcto. Para obtener más información, vea ! Página de referencia de DOCTYPE.


### <a name="benefits-of-vml"></a>Ventajas de VML

-   VML facilita la creación a los usuarios y autores de productividad. Facilita el intercambio (mediante cortar y pegar) y la posterior edición de gráficos vectoriales entre una amplia variedad de aplicaciones de productividad y diseño.
-   VML proporciona descargas gráficas más rápidas y una mejor experiencia de usuario. Permite la entrega de gráficos vectoriales escalables, totalmente integrados y de alta calidad a la Web, en un formato abierto basado en texto. En lugar de hacer referencia a gráficos como archivos externos, los gráficos VML se entregan en línea con la página HTML, lo que les permite interactuar y escalar con la interacción del usuario.
-   VML está abierto y está basado en estándares. Es un formato basado en XML. XML 1.0 es un lenguaje abierto, sencillo y basado en texto para describir datos estructurados en la Web y complementa HTML para su presentación. VML también admite otros estándares W3C, como Hojas de estilo CSS 2.0 (CSS), que especifica información de estilo y posicionamiento 2D, así como el Document Object Model (DOM), que permite a los desarrolladores interactuar de forma coherente con los elementos de página como objetos.

### <a name="for-additional-information"></a>Para obtener información adicional

Consulte los vínculos siguientes:

-   Para obtener respuestas a las preguntas más frecuentes sobre VML, consulte las preguntas más frecuentes [sobre VML.](frequently-asked-questions-about-vml.yml)
-   Para ver un tutorial sobre el uso de VML en páginas web, consulte Uso de VML en [Páginas web,](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)que complementa la especificación [de VML](https://www.w3.org/TR/NOTE-datetime.html) enviada al W3C.
-   Para obtener información sobre los tipos de datos de VML, consulte el [documento Tipos básicos de VML.](basic-vml-types.md)
-   Para obtener una referencia completa sobre VML, incluida información sobre cómo usar VML con etiquetas, así como scripting, consulte la referencia [de VML](msdn-online-vml-introduction.md).