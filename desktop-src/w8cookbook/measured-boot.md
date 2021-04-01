---
title: Arranque medido
description: Arranque medido
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccbba6e5f96fd91c00c295c4b15cab8849f11dc
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794205"
---
# <a name="measured-boot"></a>Arranque medido

## <a name="platforms"></a>Plataformas

 **Clientes** : Windows 8  
**Servidores** : Windows Server 2012  



## <a name="description"></a>Descripción

A medida que el software antimalware (AM) es mejor y mejor en la detección de malware en tiempo de ejecución, los atacantes también se están volviendo mejor en la creación de rootkits que pueden ocultarse de la detección. La detección de malware que se inicia al principio del ciclo de arranque es un desafío que la mayoría de los proveedores de AM se direccionan diligentemente. Normalmente, crean hackers del sistema que no son compatibles con el sistema operativo host y, en realidad, pueden poner el equipo en un estado inestable. Hasta este punto, Windows no ha proporcionado una buena forma de que AM detecte y resuelva estas amenazas de arranque iniciales. Windows 8 presenta una nueva característica denominada arranque medido, que mide cada componente, desde el firmware hasta los controladores de inicio de arranque, almacena esas mediciones en el Módulo de plataforma segura (TPM) del equipo y, a continuación, pone a disposición un registro que se puede probar de forma remota para comprobar el estado de arranque del cliente.

## <a name="manifestation"></a>Manifestación

La característica de arranque medido proporciona el software AM con un registro de confianza (resistente a la suplantación y manipulación) de todos los componentes de arranque que se iniciaron antes del software de AM. El software AM puede utilizar el registro para determinar si los componentes que se ejecutaron antes de ser de confianza o si están infectados con malware. El software AM del equipo local puede enviar el registro a un servidor remoto para su evaluación. El servidor remoto puede iniciar acciones correctivas interactuando con el software del cliente o a través de mecanismos fuera de banda, según corresponda.

## <a name="mitigation"></a>Mitigación

En escenarios empresariales, el administrador del sistema controla cómo se usa la información de arranque medida. En escenarios de usuario final, por ejemplo, banca en línea), el consumidor debe optar por usar el arranque medido para el servicio específico.

## <a name="solution"></a>Solución

Se está preparando una nota del producto que detalla las API y las llamadas a funciones que se deben realizar para varios escenarios de arranque medidos.

 

 




