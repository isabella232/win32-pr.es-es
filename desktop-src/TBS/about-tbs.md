---
title: Acerca de TBS
description: Un servicio del sistema que permite el uso compartido transparente de los Módulo de plataforma segura (TPM).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- TPM Base Services TBS , acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4997bf6181a1da7aabaf811d0f1d0cf3e3ca813bb11a8f2d73b3b286e4e5ebde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954462"
---
# <a name="about-tbs"></a>Acerca de TBS

La característica Servicios base de TPM (TBS) es un servicio del sistema que permite el uso compartido transparente de los recursos Módulo de plataforma segura (TPM). Comparte simultáneamente los recursos de TPM entre varias aplicaciones en la misma máquina física, incluso si esas aplicaciones se ejecutan en máquinas virtuales diferentes. A partir Windows 8 y Windows Server 2012, TBS viene preinstalado en todos los sistemas con un TPM.

El Trusted Computing Group (TCG) define un Módulo de plataforma segura que proporciona funciones criptográficas diseñadas para proporcionar confianza en la plataforma. Dado que el TPM se implementa en hardware, tiene recursos finitos. El TCG también define una pila de software que usa estos recursos para proporcionar operaciones de confianza para el software de aplicación. Sin embargo, no se realiza ninguna aprovisionamiento para ejecutar una implementación de TSS en paralelo con software del sistema operativo que también puede estar usando recursos de TPM. La característica TBS resuelve este problema habilitando cada pila de software que se comunica con TBS para usar los recursos de TPM que comprueban si hay otras pilas de software que se puedan ejecutar en la máquina.

La especificación de TPM y la especificación de tcg software stack (TSS) están disponibles en [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .

TBS se implementa como un servicio fuera de proceso que acepta comandos que usan un servicio RPC. Una biblioteca vinculada dinámicamente presenta la interfaz del lenguaje C y se comunica con el servicio TBS.

> [!Note]  
> El servicio TBS solo acepta solicitudes RPC del equipo local.

 

Los objetivos principales de TBS son:

-   Proporcione un uso compartido eficaz de recursos de TPM limitados, como ranuras de clave, ranuras de sesiones de autorización y ranuras de transporte.
-   Proporcione acceso con prioridad y sincronizado a los recursos de TPM entre varias instancias de pilas de software de TPM.
-   Proporcione la administración adecuada de los recursos de TPM en todos los estados de energía.
-   Impedir que las pilas de software de TPM accedan a los comandos de TPM que deben estar restringidos, ya sea debido a limitaciones de la plataforma o a requisitos administrativos.

En la ilustración siguiente se muestra la relación del TBS con el TPM.

![relación de los tb en modo de usuario con el tpm en modo kernel](images/tbs-block-diagram-as11601.png)

 

 




