---
title: Lenguaje de marcado de vectores (VML)
description: Lenguaje de marcado de vectores (VML)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Lenguaje de marcado de vectores (VML), acerca de
- VML (Lenguaje de marcado de vectores), acerca de
- gráficos vectoriales, acerca de
- gráficos vectoriales, Lenguaje de marcado de vectores (VML)
- Lenguaje de marcado de vectores (VML), World Wide Web Consortium (W3C)
- VML (Lenguaje de marcado de vectores), World Wide Web Consortium (W3C)
- gráficos vectoriales, World Wide Web Consortium (W3C)
- gráficos vectoriales, ventajas de VML
- Lenguaje de marcado de vectores (VML), ventajas
- VML (Lenguaje de marcado de vectores), ventajas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ba51fd041f36915eaafe20201876653f597e04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105678614"
---
# <a name="vector-markup-language-vml"></a>Lenguaje de marcado de vectores (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!NOTE]
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

Lenguaje de marcado de vectores (VML) es un formato de intercambio, edición y entrega basado en XML para gráficos vectoriales de alta calidad en la web que satisface las necesidades de los usuarios de productividad y los profesionales de diseño gráfico. XML es un lenguaje emergente sencillo, flexible y abierto basado en texto que complementa HTML. (Vea la [sección XML](/documentation/?frame=true) de MSDN Library para obtener información detallada sobre XML).

VML es compatible actualmente con Microsoft Internet Explorer versión 5,0 o posterior.

VML se ha propuesto al W3C como estándar para los gráficos vectoriales en la web (vea [lenguaje de marcado de vectores (VML)](https://www.w3.org/TR/NOTE-VML)). Microsoft continúa liderando la carga en el desarrollo y la implementación de tecnologías basadas en XML, trabajando con los principales asociados del sector (AutoDesk, Hewlett-Packard, Macromedia, Visio) y el W3C para avanzar en los estándares basados en Web. Esperamos trabajar con el W3C para impulsar en última instancia un formato estándar para los gráficos vectoriales en la Web.

VML también es compatible con Microsoft Office 2000 o posterior. Microsoft Word, Microsoft Excel y Microsoft PowerPoint se pueden usar para crear gráficos VML.

### <a name="using-vml"></a>Usar VML

Para usar VML en las páginas web, use un elemento de estilo para importar el comportamiento de VML, tal y como se muestra en el código siguiente.

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

A continuación, declare el espacio de nombres VML, tal como se muestra en el ejemplo de código siguiente.

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

Por último, agregue elementos VML para definir efectos visuales. Por ejemplo, el siguiente código VML crea un óvalo rojo.

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> Para obtener los mejores resultados cuando se usan documentos en modo Strict, asegúrese de que el marcado es válido y está bien formado. Para obtener más información, vea la. Página de referencia DOCTYPE.


### <a name="benefits-of-vml"></a>Ventajas de VML

-   VML facilita la creación de usuarios y autores de productividad. Facilita el intercambio (a través de cortar y pegar) y la edición posterior de los gráficos vectoriales entre una gran variedad de aplicaciones de productividad y diseño.
-   VML proporciona descargas gráficas más rápidas y una mejor experiencia de usuario. Permite la entrega de gráficos vectoriales escalables completamente integrados y de alta calidad en la web, en un formato basado en texto abierto. En lugar de hacer referencia a gráficos como archivos externos, los gráficos VML se entregan en línea con la página HTML, lo que les permite interactuar y escalar con la interacción del usuario.
-   VML está abierto y basado en estándares. Es un formato basado en XML. XML 1,0 es un lenguaje abierto, simple y basado en texto para describir los datos estructurados en la web y complementa el código HTML para mostrarlo. VML también admite otros estándares del W3C, como Hojas de estilo CSS 2,0 (CSS), que especifica la información de estilo y la posición en 2D, así como el Document Object Model (DOM), que permite a los desarrolladores interactuar de forma coherente con los elementos de la página como objetos.

### <a name="for-additional-information"></a>Para obtener información adicional

Vea los vínculos siguientes:

-   Para obtener respuestas a las preguntas más frecuentes sobre VML, vea las [preguntas más frecuentes sobre VML](frequently-asked-questions-about-vml.md).
-   Para ver un tutorial sobre el uso de VML en páginas web, consulte [Cómo usar VML en páginas web](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), que complementa la [especificación de VML](https://www.w3.org/TR/NOTE-datetime.html) enviada al W3C.
-   Para obtener información sobre los tipos de datos de VML, vea el documento [tipos básicos de VML](basic-vml-types.md) .
-   Para obtener la referencia completa en VML, incluida la información sobre cómo usar VML con etiquetas y scripts, vea la [referencia de VML](msdn-online-vml-introduction.md).