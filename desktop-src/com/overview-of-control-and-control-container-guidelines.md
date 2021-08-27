---
title: Información general sobre las directrices del contenedor de controles y controles
description: Información general sobre las directrices del contenedor de controles y controles
ms.assetid: c4cf2409-0085-43e6-afa2-f9c03cc50565
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2658c691e13b0a78da82fa006ed22142082e2f7eb8b04d78992943a024487a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120465"
---
# <a name="overview-of-control-and-control-container-guidelines"></a>Información general sobre las directrices del contenedor de controles y controles

Un ActiveX control es básicamente un objeto OLE simple que admite la [**interfaz IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Normalmente admitirá más interfaces para ofrecer funcionalidad, pero todas las interfaces adicionales se pueden ver como opcionales y, como tal, un contenedor de control no debe basarse en ninguna interfaz adicional que se admita. Al no especificar interfaces adicionales que un control debe admitir, un control puede dirigirse eficazmente a un área determinada de funcionalidad sin tener que admitir interfaces concretas para calificarse como control. Como siempre con OLE, ya sea en un control o en un contenedor de controles, nunca se debe suponer que una interfaz está disponible y que siempre se deben seguir las convenciones de comprobación de devolución estándar. Es importante que un contenedor de control o control se degrade correctamente y ofrezca funcionalidad alternativa si no hay disponible una interfaz necesaria.

Un ActiveX de control debe ser capaz de hospedar un control de ActiveX mínimo; también admitirá varias interfaces adicionales, como se especifica en [Contenedores](containers.md). Hay una serie de interfaces y métodos que un contenedor puede admitir opcionalmente, que se agrupan en áreas funcionales conocidas como categorías *de componentes*. Un contenedor puede admitir cualquier combinación de categorías de componentes, por ejemplo, existe una categoría de componentes para el enlace de datos y un contenedor puede admitir o no la funcionalidad de enlace de datos, en función de las necesidades de mercado del contenedor. Si un control necesita compatibilidad con el enlace de datos de un contenedor para funcionar, escribirá este requisito en el Registro. Esto permite que un contenedor de controles solo ofrezca para la inserción los controles que sabe que puede hospedar correctamente. Es importante tener en cuenta que las categorías de componentes se especifican como parte de OLE y no son específicas de los controles de ActiveX, la arquitectura de controles usa categorías de componentes para identificar las áreas de funcionalidad que un componente OLE puede admitir. Las categorías de componentes no son acumulativas ni exclusivas, por lo que un contenedor de controles puede admitir una categoría sin admitir necesariamente otra.

Es importante que los controles que requieren características opcionales o características específicas de un determinado contenedor se empaqueten y comercialmente con claridad con esos requisitos. De forma similar, los contenedores que ofrecen determinadas características o categorías de componentes se deben comercializar y empaquetar para ofrecer esos niveles de compatibilidad al hospedar controles ActiveX componentes. Se recomienda controlar el destino y la prueba con tantos contenedores como sea posible y degradar correctamente para ofrecer una funcionalidad menor o alternativa si las interfaces o los métodos no están disponibles. En una situación en la que un control no puede realizar su función de trabajo designada sin la compatibilidad de una categoría de componente, esa categoría debe especificarse como requisito en el Registro para evitar que el control se inserte en un contenedor inadecuado.

Estas instrucciones definen esas interfaces y métodos que un control puede esperar que admita un contenedor de controles, aunque como siempre un control debe comprobar los valores devueltos al usar [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) u otros métodos para obtener punteros a estas interfaces. Un contenedor no debe esperar que un control admita algo más que la interfaz [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) y estas directrices identifican qué interfaces puede admitir un control y lo que significa la presencia de una interfaz determinada.

## <a name="why-the-activex-control-and-control-container-guidelines-are-important"></a>Por qué las ActiveX control y control de contenedores son importantes

ActiveX Los controles se han convertido en la arquitectura principal para desarrollar componentes de software programables para su uso en una variedad de contenedores diferentes, desde herramientas de desarrollo de software hasta herramientas de productividad del usuario final. Para que un control funcione bien en una variedad de contenedores, el control debe ser capaz de asumir algún nivel mínimo de funcionalidad en el que pueda confiar en todos los contenedores.

Al seguir estas directrices, los desarrolladores de controles y contenedores hacen que sus controles y contenedores sean más confiables e interoperables y, en última instancia, componentes mejores y más utilizables para crear soluciones basadas en componentes.

## <a name="what-to-do-when-an-interface-you-need-is-not-available"></a>Qué hacer cuando una interfaz que necesita no está disponible

Los programas OLE deben [**usar QueryInterface para**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) adquirir punteros de interfaz y deben comprobar el valor devuelto. Las aplicaciones OLE no pueden asumir de forma segura **que QueryInterface** se realizará correctamente.

Este requisito se aplica a todas las aplicaciones OLE. Si la interfaz solicitada no está disponible (es decir, [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) devuelve E NOINTERFACE), el control o contenedor debe degradarse correctamente, incluso si eso significa que no puede realizar su función de \_ trabajo designada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ActiveX Directrices para controlar y controlar contenedores](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




