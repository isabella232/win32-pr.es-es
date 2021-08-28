---
title: Implementación del modelo de seguridad de Teredo
description: El modelo de seguridad de Teredo se basa en la tecnología Windows Filtering Platform (WFP) integrada en Windows Vista. Como resultado, se recomienda que los firewalls de terceros usen WFP para aplicar el modelo de seguridad de Teredo.
ms.assetid: ee81e5f1-e3e0-440e-a53f-2accced476bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43cad78b7c1512e0f1c632ecd27d0bb9580ac3796d6d36001a1cd19fb72c7b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001753"
---
# <a name="implementing-the-teredo-security-model"></a>Implementación del modelo de seguridad de Teredo

El modelo de seguridad de Teredo se basa en la [tecnología Windows Filtering Platform](/windows/desktop/FWP/windows-filtering-platform-start-page) (WFP) integrada en Windows Vista. Como resultado, se recomienda que los firewalls de terceros usen WFP para aplicar el modelo de [seguridad de Teredo.](about-teredo.md)

La implementación general del [modelo de seguridad de Teredo](the-teredo-security-model.md) requiere lo siguiente:

-   Un firewall de host compatible con IPv6 debe registrarse con Seguridad de Windows Center (WSC) en la máquina. En ausencia de un firewall basado en host o del propio WSC, la interfaz de Teredo no estará disponible para su uso. Este es el único requisito para recibir tráfico solicitado desde Internet a través de la interfaz de Teredo.
-   Cualquier aplicación que reciba tráfico no solicitado de Internet a través de la interfaz de Teredo debe registrarse con un firewall compatible con IPv6, como [Windows Firewall,](/previous-versions/windows/desktop/ics/windows-firewall-start-page)antes de recibir el tráfico no solicitado.

Una dirección de Teredo se volverá inactiva si el tráfico no se ha enviado o recibido a través de la interfaz de Teredo durante una hora y si las aplicaciones que cumplen los criterios de seguridad necesarios para el tráfico no solicitado no se están ejecutando o no tienen sockets de escucha abiertos.

Después del reinicio de una máquina, o si la dirección de Teredo pierde sus calificaciones, Windows Vista calificará automáticamente la dirección y la pondrá a disposición para su uso en cuanto una aplicación se enlace a sockets compatibles con IPv6. Es importante tener en cuenta que la opción "Edge Traversal" de Windows Firewall establecida por una aplicación para permitir el tráfico no solicitado a través de Teredo es persistente en los reinicios.

## <a name="firewall-requirements-for-teredo"></a>Requisitos de firewall para Teredo

Los proveedores de firewall pueden incorporar fácilmente la compatibilidad con Teredo en sus productos y proteger a sus usuarios mediante las funcionalidades de Windows Filtering Platform. Para ello, registre el firewall compatible con IPv6 en el Centro de Seguridad de Windows, agregue las reglas adecuadas en la subcapa teredo de WFP y use las API integradas en Windows para enumerar las aplicaciones que podrían escuchar el tráfico no solicitado a través de Teredo. En situaciones en las que una aplicación no necesita escuchar el tráfico solicitado a través de Teredo, los firewalls no requieren reglas adicionales agregadas al WFP. Sin embargo, un registro de firewall compatible con IPv6 con Seguridad de Windows Center sigue siendo un requisito para que la dirección teredo esté disponible para su uso.

Para admitir este escenario, el firewall debe ser compatible con IPv6 y estar registrado en Seguridad de Windows Center. Además, el firewall no debe cambiar el estado de ejecución o inicio del servicio Seguridad de Windows Center (wscsvc), ya que Teredo depende de la información de estado proporcionada a través de las API de WSC.

La API utilizada para registrar un firewall con WSC se puede obtener si se contacta con Microsoft en wscisv@microsoft.com . Se requiere un acuerdo de confidencialidad (NDA) para la divulgación de esta API debido a problemas de seguridad.

En la siguiente documentación se detallan los filtros y excepciones utilizados para garantizar una compatibilidad óptima con Teredo:

-   [Implementación de filtros de firewall para Teredo](implementing-firewall-filters-for-teredo.md)
-   [Excepciones de firewall necesarias para Teredo](required-firewall-exceptions-for-teredo.md)
-   [Excepciones Windows plataforma de filtrado obligatorio para Teredo](required-windows-filtering-platform-exceptions-for-teredo.md)

## <a name="firewall-requirements-for-other-ipv6-transition-technologies"></a>Requisitos de firewall para otras tecnologías de transición IPv6

Para admitir otras tecnologías de transición IPv6 (como 6to4 e ISATAP), el producto de firewall de host debe ser capaz de procesar el tráfico IPv6. El protocolo IP 41 indica cuándo un encabezado IPv6 sigue un encabezado IPv4. Cuando un firewall de host encuentra el protocolo 41, debe reconocer que el paquete es un paquete encapsulado IPv6 y, como resultado, debe procesar el paquete correctamente y tomar las decisiones de aceptación o denegación según las reglas IPv6 de su directiva.

 

 