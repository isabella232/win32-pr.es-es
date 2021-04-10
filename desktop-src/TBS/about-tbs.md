---
title: Acerca de TBS
description: Servicio del sistema que permite el uso compartido transparente de los recursos de Módulo de plataforma segura (TPM).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- Servicios base de TPM TBS, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104270745"
---
# <a name="about-tbs"></a>Acerca de TBS

La característica servicios base de TPM (TBS) es un servicio del sistema que permite el uso compartido transparente de los recursos de Módulo de plataforma segura (TPM). Comparte simultáneamente los recursos de TPM entre varias aplicaciones en el mismo equipo físico, incluso si esas aplicaciones se ejecutan en máquinas virtuales diferentes. A partir de Windows 8 y Windows Server 2012, TBS viene preinstalado en todos los sistemas con un TPM.

El Trusted Computing Group (TCG) define un Módulo de plataforma segura que proporciona funciones criptográficas diseñadas para proporcionar confianza en la plataforma. Dado que el TPM está implementado en hardware, tiene recursos finitos. El TCG también define una pila de software que hace uso de estos recursos para proporcionar operaciones de confianza para el software de la aplicación. Sin embargo, no se realiza ninguna disposición para ejecutar una implementación de TSS en paralelo con el software del sistema operativo que también puede usar recursos de TPM. La característica TBS resuelve este problema habilitando cada pila de software que se comunica con TBS para usar la comprobación de recursos de TPM para cualquier otra pila de software que pueda estar ejecutándose en la máquina.

La especificación del TPM y la especificación de la pila de software de TCG (TSS) están disponibles en [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .

TBS se implementa como un servicio fuera de proceso que acepta comandos que usan un servicio RPC. Una biblioteca vinculada dinámicamente presenta la interfaz del lenguaje C y se comunica con el servicio TBS.

> [!Note]  
> El servicio TBS solo acepta solicitudes RPC del equipo local.

 

Los objetivos principales de TBS son los siguientes:

-   Proporcionan un uso compartido eficaz de los recursos de TPM limitados, como las ranuras de claves, las ranuras de las sesiones de autorización y las ranuras de transporte.
-   Proporcionar acceso con prioridad y sincronizado a los recursos de TPM entre varias instancias de pilas de software de TPM.
-   Proporcione la administración adecuada de los recursos de TPM a través de los Estados de energía.
-   Impedir que las pilas de software de TPM tengan acceso a los comandos de TPM que se deben restringir, ya sea debido a limitaciones de plataforma o requisitos administrativos.

En la ilustración siguiente se muestra la relación entre TBS y el TPM.

![relación de TBS en modo de usuario con el TPM en modo kernel](images/tbs-block-diagram-as11601.png)

 

 




