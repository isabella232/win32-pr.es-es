---
title: Diseño de interfaces remotas
description: Con la llegada del modelo de objetos de componentes distribuidos, es importante que la interfaz personalizada sea remota, incluso si piensa utilizarla solo en proceso.
ms.assetid: 2ee4d950-dfd5-4965-bd77-a600e878be59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3502604d62e6a5129ca3e3538761722909c0198f
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "103904377"
---
# <a name="designing-remotable-interfaces"></a>Diseño de interfaces remotas

Con la llegada del modelo de objetos de componentes distribuidos, es importante que la interfaz personalizada sea remota, incluso si piensa utilizarla solo en proceso.

MIDL es algo más que una manera de generar archivos de encabezado para las interfaces. Es un lenguaje de programación para la comunicación remota que le permite usar las interfaces en los límites del equipo, el proceso y el subproceso. Esto significa que debe comprobar el comportamiento de las interfaces definidas por MIDL bajo esas condiciones antes de lanzar el programa a los clientes. Si ha cometido un error en el IDL y la interfaz no se ha reparado correctamente, puede ser difícil solucionar ese error. Debe revisar la interfaz con un nuevo IID y dejar el anterior en por compatibilidad con versiones anteriores, o bien debe convertir todos los clientes y cada equipo servidor en todas partes al mismo tiempo.

Incluso si la interfaz nunca se va a usar fuera de proceso, se puede usar entre subprocesos. El peor problema de un archivo IDL no comprobado puede producirse para los servidores en proceso que no admiten varios apartamentos de un [solo subproceso](single-threaded-apartments.md)). Un servidor que no especifica un modelo de subprocesos es implícitamente de un solo subproceso. Todo lo marcado con un solo subproceso se fuerza al subproceso que primero llamó a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Si algún otro subproceso era el que activó el objeto, todas las interfaces de ese servidor de un solo subproceso se deben volver a enviar al subproceso de activación, lo que puede dar lugar a una devolución de REGDB \_ E \_ IIDNOTREG en respuesta a una llamada a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))). A menos que pueda validar de forma absoluta que la interfaz está en proceso y que siempre se va a llamar en el mismo subproceso, se le llevará a cabo de forma remota en algún momento.

Por último, como diseñador de la interfaz, debe tener en cuenta el modo en que las aplicaciones cliente usarán la interfaz. Dos cosas, juntas, determinan si una interfaz será eficaz entre los límites del proceso y del equipo: la frecuencia de llamadas a métodos en el límite de la interfaz y la cantidad de datos que se van a transferir en una llamada al método determinada. Aunque COM realiza llamadas entre procesos y entre redes transparentes para los programas, no puede hacer que las llamadas de alta frecuencia y alto ancho de banda sean eficaces en los espacios de direcciones. En algunos casos, es más adecuado diseñar interfaces que normalmente se implementarán solo como servidores en proceso, mientras que otras interfaces son más adecuadas para el uso remoto.

 

 




