---
title: El modelo RPC
description: La llamada a procedimiento remoto (RPC) para los lenguajes de programación C y C++ está diseñada para ayudar a satisfacer las necesidades de los desarrolladores que trabajan en la próxima generación de software para Windows sistemas operativos.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- Llamada a procedimiento remoto RPC , descrito, el modelo RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244436"
---
# <a name="the-rpc-model"></a>El modelo RPC

La llamada a procedimiento remoto (RPC) para los lenguajes de programación C y C++ está diseñada para ayudar a satisfacer las necesidades de los desarrolladores que trabajan en la próxima generación de software para Windows sistemas operativos.

RPC es un mecanismo de comunicación entre procesos (IPC) eficaz, sólido, eficaz y seguro que permite el intercambio de datos y la invocación de funcionalidad que reside en un proceso diferente. Ese proceso diferente puede estar en la misma máquina, en la red de área local o a través de Internet. En esta sección se explica el modelo de programación RPC y el modelo para sistemas distribuidos que se pueden implementar mediante RPC.

RPC es totalmente compatible con archivos de 64 Windows. Hay tres tipos de procesos: procesos nativos de 32 bits, procesos nativos de 64 bits y procesos de 32 bits que se ejecutan en el emulador de procesos de 32 bits en un sistema de 64 bits (a menudo denominados procesos WOW64). Para obtener más información sobre WOW64, vea [Running 32-bit Applications](/windows/desktop/WinProg64/running-32-bit-applications). Mediante RPC, los desarrolladores pueden comunicarse de forma transparente entre diferentes tipos de proceso. RPC administra automáticamente las diferencias de proceso en segundo plano.

RPC se desarrolló inicialmente como una extensión de RPC de OSF. A excepción de algunas de sus características avanzadas, RPC es interoperable con las implementaciones de RPC de OSF de otros proveedores.

En esta sección también se proporciona información general sobre los componentes rpc y su funcionamiento. La información se presenta en los temas siguientes:

-   [El modelo de programación](the-programming-model.md)
-   [Modelo para sistemas distribuidos](the-model-for-distributed-systems.md)
-   [Funcionamiento de RPC](how-rpc-works.md)
-   [Componentes RPC de Microsoft](microsoft-rpc-components.md)

 

 