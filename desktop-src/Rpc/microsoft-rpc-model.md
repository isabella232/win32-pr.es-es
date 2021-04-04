---
title: El modelo RPC
description: La llamada a procedimiento remoto (RPC) para los lenguajes de programación C y C++ está diseñada para ayudar a satisfacer las necesidades de los programadores que trabajan en la próxima generación de software para los sistemas operativos Windows.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- RPC llamada a procedimiento remoto, descrito, el modelo RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793210"
---
# <a name="the-rpc-model"></a>El modelo RPC

La llamada a procedimiento remoto (RPC) para los lenguajes de programación C y C++ está diseñada para ayudar a satisfacer las necesidades de los programadores que trabajan en la próxima generación de software para los sistemas operativos Windows.

RPC es un mecanismo de comunicación entre procesos (IPC) eficaz, sólido, eficiente y seguro que permite el intercambio de datos y la invocación de funciones que residen en un proceso diferente. Ese proceso diferente puede estar en el mismo equipo, en la red de área local o a través de Internet. En esta sección se explica el modelo de programación RPC y el modelo para sistemas distribuidos que se pueden implementar con RPC.

RPC es totalmente compatible con Windows de 64 bits. Hay tres tipos de procesos: procesos nativos de 32 bits, procesos nativos de 64 bits y procesos de 32 bits que se ejecutan en el emulador de proceso de 32 bits en un sistema de 64 bits (a menudo denominados procesos WOW64). Para obtener más información sobre WOW64, vea [ejecutar aplicaciones de 32 bits](/windows/desktop/WinProg64/running-32-bit-applications). Con RPC, los desarrolladores pueden comunicarse de forma transparente entre distintos tipos de procesos; RPC administra automáticamente las diferencias en los procesos en segundo plano.

RPC se desarrolló inicialmente como una extensión para la RPC de OSF. Con la excepción de algunas de sus características avanzadas, RPC es interoperable con las implementaciones de otros proveedores de la RPC de OSF.

En esta sección también se proporciona información general sobre los componentes de RPC y su funcionamiento. La información se presenta en los temas siguientes:

-   [Modelo de programación](the-programming-model.md)
-   [El modelo para sistemas distribuidos](the-model-for-distributed-systems.md)
-   [Cómo funciona RPC](how-rpc-works.md)
-   [Componentes de Microsoft RPC](microsoft-rpc-components.md)

 

 