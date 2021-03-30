---
description: Hay dos ingredientes a la hora de determinar el comportamiento de la suplantación de la autoridad que el cliente concede explícitamente al servidor a través de un nivel de suplantación y la capacidad de los servidores de enmascarar su propia identidad al realizar llamadas en los clientes.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Cloaking (servicios de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807213"
---
# <a name="cloaking-component-services"></a>Cloaking (servicios de componentes)

Hay dos ingredientes a la hora de determinar el comportamiento de la suplantación: la autoridad que el cliente concede explícitamente al servidor a través de un nivel de suplantación y la capacidad del servidor de enmascarar su propia identidad al realizar llamadas en el nombre del cliente. Esta última funcionalidad se conoce como *Cloaking*. La ocultación tiene que hacer con la identidad de seguridad en la que el servidor realiza llamadas.

Cuando el servidor suplanta al cliente, tiene acceso directo a las credenciales de seguridad del cliente. En un sentido muy local, el subproceso de servidor toma la identidad del cliente. Pero cuando el servidor realiza llamadas fuera de su proceso, la identidad del cliente no se proyectará necesariamente como la identidad en la que se realiza la llamada.

Cuando está habilitada la ocultación, las llamadas realizadas por el servidor que suplanta al cliente pueden realizarse en la identidad del cliente. Cuando se deshabilita la ocultación, las llamadas realizadas por el servidor se realizarán en la identidad del servidor.

Además, hay dos formas de Cloaking, ocultación *estática* y *ocultación dinámica*, que se puede describir de la siguiente manera:

-   Suplantación con Cloaking estático. La identidad del cliente original (realizada como el token de subproceso de servidor) se puede presentar una vez a un servidor de nivel inferior en una llamada mediante [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), estableciendo la identidad del cliente original una vez en el proxy y ese token de subproceso se usará en las llamadas de método posteriores.
-   Suplantación con Cloaking dinámico. La identidad del cliente original se detecta como el token del subproceso del servidor en cada llamada al método en el servidor que sigue en la cadena. En efecto, la identidad que se presenta se puede determinar de forma dinámica. La sobrecarga necesaria para ello puede ser considerablemente más costosa.

En el caso de las aplicaciones COM+, la configuración predeterminada es para la funcionalidad de ocultación dinámica. Esto se puede cambiar mediante programación y administrativamente. Aunque el Cloaking dinámico puede suponer una sobrecarga de rendimiento, proporciona la flexibilidad que normalmente requiere la realización de las circunstancias que requieren el uso de la suplantación en primer lugar.

Para obtener más información acerca de la ocultación y descripciones precisas de posibles comportamientos, vea [cloakinging](/windows/desktop/com/cloaking) en la documentación de com.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Requisitos del cliente para la suplantación](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Requisitos del servidor para la suplantación](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
