---
title: Clientes y servidores COM
description: Un aspecto crítico de COM es cómo interactúan los clientes y los servidores.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369447"
---
# <a name="com-clients-and-servers"></a>Clientes y servidores COM

Un aspecto crítico de COM es cómo interactúan los clientes y los servidores. Un *cliente COM* es cualquier código u objeto que obtiene un puntero a un servidor COM y usa sus servicios llamando a los métodos de sus interfaces. Un *servidor COM* es cualquier objeto que proporciona servicios a los clientes; Estos servicios están en forma de implementaciones de interfaz COM a las que puede llamar cualquier cliente que pueda obtener un puntero a una de las interfaces del objeto de servidor.

Hay dos tipos principales de servidores, *en proceso* y fuera *de proceso.* Los servidores en proceso se implementan en una biblioteca vinculada dinámica (DLL) y los servidores fuera de proceso se implementan en un archivo ejecutable (EXE). Los servidores fuera de proceso pueden residir en el equipo local o en un equipo remoto. Además, COM proporciona un mecanismo que permite que un servidor en proceso (un archivo DLL) se ejecute en un proceso EXE suplente para aprovechar la ventaja de poder ejecutar el proceso en un equipo remoto. Para obtener más información, vea [Suplentes de DLL.](dll-surrogates.md)

El modelo de programación COM y las construcciones se han ampliado para que los clientes y servidores COM puedan trabajar juntos en la red, no solo dentro de un equipo determinado. Esto permite que las aplicaciones existentes interactúen con nuevas aplicaciones y entre sí a través de redes con una administración adecuada, y se pueden escribir nuevas aplicaciones para aprovechar las características de red.

No es necesario que las aplicaciones cliente COM sean conscientes de cómo se empaquetan los objetos de servidor, si se empaquetan como objetos en proceso (en archivos DLL) o como objetos locales o remotos (en E/S POR). COM distribuido permite además empaquetar objetos como aplicaciones de servicio, sincronizando COM con las completas funcionalidades administrativas y de integración del sistema de Windows.

> [!Note]  
> En esta documentación, el acrónimo COM se usa en lugar de DCOM. Esto se debe a que DCOM no es independiente; es simplemente COM con una conexión más larga. En los casos en los que lo que se describe es específicamente una operación remota, se usa el término *COM* distribuido.

 

COM está diseñado para que sea posible agregar la compatibilidad con la transparencia de ubicación que se extiende a través de una red. Permite que las aplicaciones escritas para equipos individuales se ejecuten a través de una red y proporciona características que amplían estas funcionalidades y agregan a la seguridad necesaria en una red. (Para obtener más información, vea [Seguridad en COM).](security-in-com.md)

COM especifica un mecanismo por el que muchas aplicaciones diferentes pueden usar el código de clase.

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

 

 




