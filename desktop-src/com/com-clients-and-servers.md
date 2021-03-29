---
title: Clientes y servidores COM
description: Un aspecto fundamental de COM es cómo interactúan los clientes y los servidores.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776506"
---
# <a name="com-clients-and-servers"></a>Clientes y servidores COM

Un aspecto fundamental de COM es cómo interactúan los clientes y los servidores. Un *cliente com* es el código u objeto que obtiene un puntero a un servidor com y utiliza sus servicios llamando a los métodos de sus interfaces. Un *servidor com* es cualquier objeto que proporcione servicios a los clientes; Estos servicios están en forma de implementaciones de interfaz COM a las que puede llamar cualquier cliente que pueda obtener un puntero a una de las interfaces en el objeto de servidor.

Hay dos tipos principales de servidores, *en proceso* y *fuera de proceso*. Los servidores en proceso se implementan en una biblioteca de vínculos dinámicos (DLL) y los servidores fuera de proceso se implementan en un archivo ejecutable (EXE). Los servidores fuera de proceso pueden residir en el equipo local o en un equipo remoto. Además, COM proporciona un mecanismo que permite a un servidor en proceso (un archivo DLL) ejecutarse en un proceso EXE suplente para aprovechar la ventaja de poder ejecutar el proceso en un equipo remoto. Para obtener más información, vea [suplentes de dll](dll-surrogates.md).

Ahora se han ampliado el modelo de programación COM y las construcciones para que los clientes y servidores COM puedan trabajar juntos en la red, no solo dentro de un equipo determinado. Esto permite a las aplicaciones existentes interactuar con nuevas aplicaciones y entre sí entre redes con la administración adecuada y se pueden escribir nuevas aplicaciones para aprovechar las características de red.

No es necesario que las aplicaciones cliente COM sepan cómo se empaquetan los objetos de servidor, si se empaquetan como objetos en proceso (en archivos dll) o como objetos locales o remotos (en exe). COM distribuido permite agregar objetos como aplicaciones de servicio, sincronizando COM con las completas capacidades administrativas y de integración del sistema de Windows.

> [!Note]  
> En esta documentación, el acrónimo COM se usa en preferencia a DCOM. Esto se debe a que DCOM no es independiente; simplemente es COM con una conexión más larga. En los casos en los que lo que se describe es específicamente una operación remota, se usa el término *com distribuido* .

 

COM está diseñado para que sea posible agregar la compatibilidad con la transparencia de ubicación que se extiende a través de una red. Permite que las aplicaciones escritas para equipos individuales se ejecuten a través de una red y proporciona características que amplían estas capacidades y se agregan a la seguridad necesaria en una red. (Para obtener más información, vea [seguridad en com](security-in-com.md)).

COM especifica un mecanismo por el que pueden usar el código de clase muchas aplicaciones diferentes.

Para obtener más información, vea los temas siguientes:

-   [Obtener un puntero a un objeto](getting-a-pointer-to-an-object.md)
-   [Crear un objeto a través de un objeto de clase](creating-an-object-through-a-class-object.md)
-   [Responsabilidades del servidor COM](com-server-responsibilities.md)
-   [Estado del objeto persistente](persistent-object-state.md)
-   [Proporcionar información de clase](providing-class-information.md)
-   [Comunicación entre objetos](inter-object-communication.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sincronización de llamadas](call-synchronization.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




