---
description: Hay dos ingredientes para determinar el comportamiento de la suplantación la autoridad que el cliente concede explícitamente al servidor a través de un nivel de suplantación y la capacidad de los servidores de enmascarar su propia identidad al realizar llamadas en nombre de los clientes.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Afición (servicios de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568057"
---
# <a name="cloaking-component-services"></a>Afición (servicios de componentes)

Hay dos ingredientes para determinar el comportamiento de la suplantación: la autoridad que el cliente concede explícitamente al servidor a través de un nivel de suplantación y la capacidad del servidor para enmascarar su propia identidad al realizar llamadas en nombre del cliente. Esta última funcionalidad se conoce como *"contrabando".* La protección tiene que ver con la identidad de seguridad bajo la que el servidor realiza llamadas.

Cuando el servidor suplanta al cliente, tiene acceso directo a las credenciales de seguridad del cliente. En un sentido muy local, el subproceso de servidor toma la identidad del cliente. Pero cuando el servidor realiza llamadas fuera de su proceso, la identidad del cliente no se proyecta necesariamente como la identidad bajo la que se realiza la llamada.

Cuando la protección está habilitada, las llamadas realizadas por el servidor que suplanta al cliente se pueden realizar bajo la identidad del cliente. Cuando la protección está deshabilitada, las llamadas realizadas por el servidor se realizarán bajo la identidad del servidor.

Además, hay dos formas de desarroba, estática *y* *dinámica,* que se pueden describir de la siguiente manera:

-   Suplantación con la suplantación estática. La identidad de cliente original (realizada como token de subproceso de servidor) se puede presentar una vez a un servidor de bajada en una llamada mediante [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), estableciendo la identidad de cliente original una vez en el proxy y ese token de subproceso se usará en las llamadas de método subsiguientes.
-   Suplantación con el arroba dinámico. La identidad de cliente original se detecta como el token de subproceso de servidor en cada llamada de método al servidor de bajada. En efecto, la identidad que se presenta se puede determinar dinámicamente. La sobrecarga necesaria para hacerlo puede ser considerablemente más costosa.

En el caso de las aplicaciones COM+, la configuración predeterminada es para la funcionalidad de afición dinámica. Esto se puede cambiar mediante programación y de forma administrativa. Aunque la sobrecarga de rendimiento puede tener sobrecarga de rendimiento, proporciona la flexibilidad que normalmente requieren las circunstancias que requieren el uso de la suplantación en primer lugar.

Para obtener más detalles sobre la desadición y las descripciones precisas de los posibles comportamientos, consulte [La desadición](/windows/desktop/com/cloaking) en la documentación de COM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Requisitos del lado cliente para la suplantación](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Requisitos del lado servidor para la suplantación](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
