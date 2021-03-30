---
title: Información general sobre las instrucciones de contenedor de control y control
description: Información general sobre las instrucciones de contenedor de control y control
ms.assetid: c4cf2409-0085-43e6-afa2-f9c03cc50565
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd72851775898f4fd140c7d101d72993c34e3eb
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "103785589"
---
# <a name="overview-of-control-and-control-container-guidelines"></a>Información general sobre las instrucciones de contenedor de control y control

Un control ActiveX es esencialmente un objeto OLE simple que admite la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Normalmente, admite más interfaces para ofrecer funcionalidad, pero todas las interfaces adicionales se pueden ver como opcionales y, como tal, un contenedor de control no debe basarse en cualquier interfaz adicional que se admita. Si no se especifican interfaces adicionales que un control debe admitir, un control puede dirigirse eficazmente a un área determinada de funcionalidad sin tener que admitir interfaces determinadas para calificar como un control. Como siempre con OLE, ya sea en un contenedor de control o de control, nunca se debe suponer que una interfaz está disponible y siempre deben seguirse las convenciones estándar de comprobación de devolución. Es importante que un contenedor de control o control se reduzca correctamente y ofrezca funcionalidad alternativa si no está disponible una interfaz necesaria.

Un contenedor de controles ActiveX debe ser capaz de hospedar un control ActiveX mínimo; también admite varias interfaces adicionales, como se especifica en [contenedores](containers.md). Hay una serie de interfaces y métodos que un contenedor puede admitir opcionalmente, que se agrupan en áreas funcionales conocidas como *categorías de componentes*. Un contenedor puede admitir cualquier combinación de categorías de componentes, por ejemplo, existe una categoría de componente para el enlace de los DataBindings y un contenedor puede o no admitir la funcionalidad de enlace de los enlaces, en función de las necesidades de mercado del contenedor. Si un control necesita compatibilidad con el enlace de los enlaces de un contenedor para que funcione, se especificará este requisito en el registro. Esto permite que un contenedor de control solo ofrezca la inserción de aquellos controles que sepa que puede hospedar correctamente. Es importante tener en cuenta que las categorías de componentes se especifican como parte de OLE y no son específicas de los controles ActiveX, la arquitectura de los controles utiliza categorías de componentes para identificar las áreas de funcionalidad que puede admitir un componente OLE. Las categorías de componentes no son acumulativas ni exclusivas, por lo que un contenedor de control puede admitir una categoría sin que sea necesaria la compatibilidad con otra.

Es importante para los controles que requieren características opcionales, o características específicas de un determinado contenedor que se van a empaquetar y comercializar claramente con esos requisitos. De igual forma, los contenedores que ofrecen ciertas características o categorías de componentes deben comercializarse y empaquetarse como si ofrecieran los niveles de soporte técnico al hospedar controles ActiveX. Se recomienda que controle el destino y la prueba con tantos contenedores como sea posible y que se reduzca correctamente para ofrecer una funcionalidad menos o alternativa si no están disponibles las interfaces o los métodos. En una situación en la que un control no puede realizar su función de trabajo designada sin la compatibilidad de una categoría de componente, esa categoría debe especificarse como un requisito en el registro para evitar que el control se inserte en un contenedor inadecuado.

Estas instrucciones definen las interfaces y los métodos que un control puede esperar que admita un contenedor de control, aunque como siempre un control debe comprobar los valores devueltos cuando se usa [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) u otros métodos para obtener punteros a estas interfaces. Un contenedor no debe esperar que un control admita algo más que la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , y estas instrucciones identifican qué interfaces puede admitir un control y qué significa la presencia de una interfaz determinada.

## <a name="why-the-activex-control-and-control-container-guidelines-are-important"></a>¿Por qué son importantes las directrices del control ActiveX y del contenedor de controles?

Los controles ActiveX se han convertido en la arquitectura principal para el desarrollo de componentes de software programables para su uso en diversos contenedores distintos, desde herramientas de desarrollo de software hasta herramientas de productividad del usuario final. Para que un control funcione correctamente en varios contenedores, el control debe ser capaz de asumir el nivel mínimo de funcionalidad que puede utilizar en todos los contenedores.

Siguiendo estas directrices, los desarrolladores de controles y contenedores hacen que sus controles y contenedores sean más confiables e interoperables y, en última instancia, componentes más útiles y más fáciles de usar para compilar soluciones basadas en componentes.

## <a name="what-to-do-when-an-interface-you-need-is-not-available"></a>Qué hacer cuando una interfaz que necesita no está disponible

Los programas OLE deben usar [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para adquirir punteros de interfaz y deben comprobar el valor devuelto. Las aplicaciones OLE no pueden suponer con seguridad que **QueryInterface** se realizará correctamente.

Este requisito se aplica a todas las aplicaciones OLE. Si la interfaz solicitada no está disponible (es decir, [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) devuelve E \_ nointerface), el control o el contenedor deben degradarse correctamente, incluso si eso significa que no puede realizar su función de trabajo designada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices para el contenedor de controles y controles ActiveX](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




