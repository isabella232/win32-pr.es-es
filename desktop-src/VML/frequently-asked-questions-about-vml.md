---
title: Preguntas más frecuentes sobre VML
description: Preguntas más frecuentes sobre VML
ms.assetid: f7f2ce12-facf-4042-b2a7-acaa3e25816a
keywords:
- Lenguaje de marcado de vectores (VML), p + f
- VML (Lenguaje de marcado de vectores), preguntas más frecuentes
- gráficos vectoriales, p + f
- Lenguaje de marcado de vectores (VML), preguntas más frecuentes
- VML (Lenguaje de marcado de vectores), preguntas más frecuentes
- gráficos vectoriales, preguntas más frecuentes
- Lenguaje de marcado de vectores (VML), diferencias de GIF
- VML (Lenguaje de marcado de vectores), diferencias de GIF
- Lenguaje de marcado de vectores (VML), diferencias de PNG
- VML (Lenguaje de marcado de vectores), diferencias de PNG
- gráficos vectoriales, diferencias de formato de tramas
- Lenguaje de marcado de vectores (VML), XML
- VML (Lenguaje de marcado de vectores), XML
- gráficos vectoriales, XML
- Lenguaje de marcado de vectores (VML), animación
- VML (Lenguaje de marcado de vectores), animación
- gráficos vectoriales, animación
- Lenguaje de marcado de vectores (VML), Macromedia Flash
- VML (Lenguaje de marcado de vectores), Macromedia Flash
- gráficos vectoriales, Macromedia Flash
- formatos de trama
- animación
- Macromedia Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e108f2055e7a0fbae1c5ed542fe68c59ec9b212b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995469"
---
# <a name="frequently-asked-questions-about-vml"></a>Preguntas más frecuentes sobre VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

## <a name="does-vml-compete-with-gif-and-png"></a>¿El VML compite con GIF y PNG?

No. Tanto GIF como PNG son formatos de trama (o de mapa de bits) que se pueden usar para almacenar gráficos vectoriales. Los formatos de trama almacenan cada píxel, mientras que los formatos vectoriales como VML usan descripciones matemáticas o esquemas para describir los gráficos. Los gráficos vectoriales almacenados en un formato basado en vectores son más compactos que los almacenados en formatos de trama, lo que da lugar a tiempos de descarga más rápidos para los usuarios Web.

Además, los gráficos VML se entregan en línea a la página HTML en lugar de depender de archivos externos, como es el caso de los formatos GIF y PNG actuales. Esto permite que los gráficos VML escalen e interactúen con otros elementos de la página web a medida que se cambia el tamaño de la página, lo que mejora la experiencia del usuario final.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="why-is-microsoft-supporting-another-xml-based-standard-when-xml-is-hardly-in-use-and-is-young-enough-as-it-is"></a>¿Por qué Microsoft admite otro estándar basado en XML cuando el código XML no está en uso y es lo suficientemente joven como?

XML es una manera eficaz y sencilla de representar datos estructurados en la web y complementa totalmente el HTML para su presentación. VML es un ejemplo de muchos formatos basados en XML específicos de la aplicación que se desarrollarán e implementarán en los próximos meses. Por ejemplo, en la siguiente versión de Office, VML se usará para anotar documentos HTML, para conservar la información de formato de los gráficos de Office Art entre el formato de archivo de Office nativo y HTML, lo que permite a los usuarios de Office cambiar sin problemas entre los dos formatos.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="who-will-support-vml"></a>¿Quién será compatible con VML?

Esperamos que muchos proveedores admitan VML. Por ejemplo, Autodesk, Hewlett-Packard, Macromedia y VISIO han prometido la compatibilidad con VML en versiones futuras de sus productos. Microsoft ha prometido la compatibilidad con VML en versiones futuras de sus plataformas, como Internet Explorer. Además, VML se usará en la próxima generación de Office para habilitar la acción de ida y vuelta entre el formato de Office y HTML.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="does-vml-support-animation"></a>¿Admite VML la animación?

No, actualmente no. Sin embargo, estamos trabajando con nuestros asociados de VML para agregar funcionalidad de animación en el formato VML. Dado que VML se basa en XML, el conjunto de etiquetas se puede extender fácilmente para obtener funcionalidad adicional.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="does-vml-replace-macromedia-flash-didnt-macromedia-just-submit-their-flash-format-for-vector-graphics-to-the-w3c"></a>¿Reemplaza VML Macromedia Flash? ¿No se ha enviado Macromedia el formato Flash para los gráficos vectoriales al W3C?

No. VML es un formato de entrega y de intercambio basado en texto para gráficos vectoriales, mientras que Flash es un formato binario para la entrega de gráficos basados en vectores y animaciones.

Macromedia no ha enviado su formato de archivo al W3C. Sin embargo, abrieron su formato de archivo para los desarrolladores de aplicaciones, los desarrolladores web y los usuarios finales. Consulte <https://www.macromedia.com> para obtener más información.

[Volver a la información general de VML](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

 