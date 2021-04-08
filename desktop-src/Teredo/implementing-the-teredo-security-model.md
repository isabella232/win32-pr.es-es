---
title: Implementar el modelo de seguridad de Teredo
description: El modelo de seguridad de Teredo se basa en la tecnología de la plataforma de filtrado de Windows (WFP) integrada en Windows Vista. Como resultado, se recomienda que los firewalls de terceros usen WFP para aplicar el modelo de seguridad de Teredo.
ms.assetid: ee81e5f1-e3e0-440e-a53f-2accced476bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a39668f8e1c86e0cd5b12056df5eb9a5fd9cd3ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792939"
---
# <a name="implementing-the-teredo-security-model"></a>Implementar el modelo de seguridad de Teredo

El modelo de seguridad de Teredo se basa en la tecnología de la [plataforma de filtrado de Windows](/windows/desktop/FWP/windows-filtering-platform-start-page) (WFP) integrada en Windows Vista. Como resultado, se recomienda que los firewalls de terceros usen WFP para aplicar el modelo de seguridad de [Teredo](about-teredo.md) .

La implementación general del [modelo de seguridad de Teredo](the-teredo-security-model.md) requiere lo siguiente:

-   Un firewall de host compatible con IPv6 se debe registrar con Windows Security Center (WSC) en la máquina. En ausencia de un firewall basado en host, o el propio WSC, la interfaz Teredo no estará disponible para su uso. Este es el único requisito para recibir el tráfico solicitado desde Internet a través de la interfaz Teredo.
-   Cualquier aplicación que reciba tráfico no solicitado de Internet a través de la interfaz Teredo debe registrarse en un firewall compatible con IPv6, como [firewall de Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page), antes de recibir el tráfico no solicitado.

Una dirección Teredo entrará en estado inactivo si no se ha enviado o recibido tráfico a través de la interfaz Teredo durante una hora y si las aplicaciones que cumplen los criterios de seguridad necesarios para el tráfico no solicitado no se están ejecutando o no tienen Sockets en escucha abiertos.

Después del reinicio de una máquina, o si la dirección Teredo pierde sus calificaciones, Windows Vista calificará automáticamente la dirección y estará disponible para su uso en cuanto una aplicación se enlace a Sockets compatibles con IPv6. Es importante tener en cuenta que la opción "cruce seguro" del firewall de Windows establecida por una aplicación para permitir el tráfico no solicitado a través de Teredo es persistente en los reinicios.

## <a name="firewall-requirements-for-teredo"></a>Requisitos de Firewall para Teredo

Los proveedores de Firewall pueden incorporar fácilmente compatibilidad con Teredo en sus productos y proteger a sus usuarios mediante las capacidades de la plataforma de filtrado de Windows. Esto puede realizarse registrando el Firewall compatible con IPv6 con la Security Center de Windows, agregando las reglas adecuadas a la subcapa Teredo de WFP y usando las API integradas en Windows para enumerar las aplicaciones que pueden escuchar el tráfico no solicitado a través de Teredo. En situaciones en las que una aplicación no necesita escuchar el tráfico solicitado a través de Teredo, los firewalls no requieren reglas adicionales agregadas a la WFP. Sin embargo, un registro de Firewall compatible con IPv6 con Windows Security Center sigue siendo un requisito para que la dirección Teredo esté disponible para su uso.

Con el fin de admitir este escenario, el Firewall debe ser compatible con IPv6 y registrarse con el Security Center de Windows. Además, el Firewall no debe cambiar el estado de ejecución o de inicio del servicio Security Center de Windows (wscsvc), ya que Teredo depende de la información de estado proporcionada a través de las API de WSC.

La API utilizada para registrar un firewall con el WSC se puede obtener poniéndose en contacto con Microsoft en wscisv@microsoft.com . Se requiere un acuerdo de CONFIDENCIALidad para la divulgación de esta API debido a problemas de seguridad.

La siguiente documentación detalla los filtros y las excepciones que se usan para garantizar la compatibilidad óptima con Teredo:

-   [Implementación de filtros de Firewall para Teredo](implementing-firewall-filters-for-teredo.md)
-   [Excepciones de Firewall necesarias para Teredo](required-firewall-exceptions-for-teredo.md)
-   [Excepciones de plataforma de filtrado de Windows necesarias para Teredo](required-windows-filtering-platform-exceptions-for-teredo.md)

## <a name="firewall-requirements-for-other-ipv6-transition-technologies"></a>Requisitos de Firewall para otras tecnologías de transición de IPv6

Con el fin de admitir otras tecnologías de transición de IPv6 (como 6to4 e ISATAP), el producto de Firewall de host debe ser capaz de procesar el tráfico IPv6. El protocolo IP 41 indica cuando un encabezado IPv6 sigue a un encabezado IPv4. Cuando un firewall de host encuentra el protocolo 41, debe reconocer que el paquete es un paquete encapsulado en IPv6 y, como resultado, debe procesar el paquete adecuadamente y tomar las decisiones de aceptación o denegación en función de las reglas de IPv6 en su Directiva.

 

 