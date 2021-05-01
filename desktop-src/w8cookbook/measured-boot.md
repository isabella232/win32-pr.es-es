---
title: Arranque medido
description: Arranque medido
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d728a1980bc9a461e6383b1dea2bd7eb4aab461
ms.sourcegitcommit: f14de4414da072d5a761e946aedfde24d8b65102
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2021
ms.locfileid: "108314346"
---
# <a name="measured-boot"></a>Arranque medido

## <a name="platforms"></a>Plataformas

 **Clientes:** Windows 8  
**Servidores:** Windows Server 2012  



## <a name="description"></a>Descripción

A medida que el software antimalware (AM) se ha vuelto mejor y mejor en la detección de malware en tiempo de ejecución, los atacantes también están mejorando en la creación de rootkits que pueden ocultarse de la detección. Detectar malware que se inicia al principio del ciclo de arranque es un desafío que la mayoría de los proveedores de AM abordan diligentemente. Normalmente, crean hacks del sistema que no son compatibles con el sistema operativo host y pueden dar lugar realmente a la colocación del equipo en un estado inestable. Hasta este momento, Windows no ha proporcionado una buena manera de que AM detecte y resuelva estas amenazas de arranque temprano. Windows 8 presenta una nueva característica denominada Arranque medido, que mide cada componente, desde el firmware hasta los controladores de inicio de arranque, almacena esas medidas en el Módulo de plataforma segura (TPM) en la máquina y, a continuación, pone a disposición un registro que se puede probar de forma remota para comprobar el estado de arranque del cliente.

## <a name="manifestation"></a>Manifestación

La Arranque medido proporciona software de AM con un registro de confianza (resistente a la suplantación y manipulación) de todos los componentes de arranque que se iniciaron antes del software de AM. El software de AM puede usar el registro para determinar si los componentes que se han ejecutado antes son de confianza o si están infectados con malware. El software am del equipo local puede enviar el registro a un servidor remoto para su evaluación. El servidor remoto puede iniciar acciones de corrección mediante la interacción con el software en el cliente o a través de mecanismos fuera de banda, según corresponda.

## <a name="mitigation"></a>Mitigación

En escenarios empresariales, el administrador del sistema tiene el control de Arranque medido se usa la información. En escenarios de usuario final, por ejemplo, la banca en línea), el consumidor debe optar por usar Arranque medido para el servicio específico.

## <a name="solution"></a>Solución

Se está preparando una documentación que detalla las API y las llamadas de función que se deben realizar para varios Arranque medido escenarios.

 

 




