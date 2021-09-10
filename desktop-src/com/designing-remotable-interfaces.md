---
title: Diseño de interfaces remotas
description: Con la llegada del modelo de objetos de componentes distribuidos, es importante que la interfaz personalizada sea remotable, incluso si piensa usarlo solo en proceso.
ms.assetid: 2ee4d950-dfd5-4965-bd77-a600e878be59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3502604d62e6a5129ca3e3538761722909c0198f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369792"
---
# <a name="designing-remotable-interfaces"></a>Diseño de interfaces remotas

Con la llegada del modelo de objetos de componentes distribuidos, es importante que la interfaz personalizada sea remotable, incluso si piensa usarlo solo en proceso.

MIDL es algo más que una forma de generar archivos de encabezado para las interfaces. Es un lenguaje de programación para la comunicación remota que permite usar las interfaces a través de los límites de la máquina, el proceso y los subprocesos. Esto significa que debe comprobar el comportamiento de las interfaces definidas por MIDL en esas condiciones antes de lanzar el programa a los clientes. Si ha cometido un error en el IDL y la interfaz no está remota correctamente, puede ser difícil solucionar ese error. Tiene que revisar la interfaz con un nuevo IID y dejar el antiguo en por compatibilidad con versiones anteriores o tiene que convertir todos los clientes y todos los equipos de servidor en todas partes al mismo tiempo.

Incluso si la interfaz nunca se usará fuera de proceso, se puede usar entre subprocesos. El peor problema para un archivo IDL no desactivado puede surgir para los servidores en proceso que no admiten varios servidores de un solo [subproceso](single-threaded-apartments.md)). Un servidor que no especifica un modelo de subprocesos es implícitamente de un solo subproceso. Todo lo marcado como de subproceso único se fuerza al subproceso que primero llamó [**a CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) Si algún otro subproceso fue el que activó el objeto , todas las interfaces de ese servidor de un solo subproceso se deben volver remotas al subproceso de activación, lo que puede dar lugar a una devolución de REGDB \_ E IIDNOTREG en respuesta a una llamada \_ a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))). A menos que pueda aserr absolutamente que la interfaz está en proceso y que siempre se va a llamar en el mismo subproceso, se le remoto en algún momento.

Por último, como diseñador de interfaces, debe tener en cuenta cómo las aplicaciones cliente usarán la interfaz. Dos cosas, juntas, determinan si una interfaz será eficaz a través de los límites del proceso y de la máquina: la frecuencia de las llamadas a métodos a través del límite de la interfaz y la cantidad de datos que se van a transferir en una llamada de método determinada. Aunque COM hace que las llamadas entre procesos y entre redes son transparentes para los programas, no puede hacer eficientes las llamadas de alta frecuencia y ancho de banda en los espacios de direcciones. En algunos casos, es más adecuado diseñar interfaces que normalmente se implementarán solo como servidores en proceso, mientras que otras interfaces son más adecuadas para el uso remoto.

 

 




