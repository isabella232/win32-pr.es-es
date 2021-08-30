---
title: Arranque medido
description: Arranque medido
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27be1890773f705f7f663655a91858125b58160eb6dbe02378e7bb79fa24ad2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815185"
---
# <a name="measured-boot"></a>Arranque medido

## <a name="platforms"></a>Plataformas

 **Clientes:** Windows 8  
**Servidores:** Windows Server 2012  



## <a name="description"></a>Descripción

A medida que el software antimalware (AM) se ha vuelto mejor y mejor en la detección de malware en tiempo de ejecución, los atacantes también están mejorando en la creación de rootkits que pueden ocultarse de la detección. Detectar malware que se inicia al principio del ciclo de arranque es un desafío que la mayoría de los proveedores de AM abordan diligentemente. Normalmente, crean ataques informáticos del sistema que no son compatibles con el sistema operativo host y pueden dar lugar a la colocación del equipo en un estado inestable. Hasta este punto, Windows ha proporcionado una buena manera de que AM detecte y resuelva estas amenazas de arranque temprano. Windows 8 presenta una nueva característica denominada Arranque medido, que mide cada componente, desde el firmware hasta los controladores de inicio de arranque, almacena esas medidas en el Módulo de plataforma segura (TPM) en la máquina y, a continuación, pone a disposición de los usuarios un registro que se puede probar de forma remota para comprobar el estado de arranque del cliente.

## <a name="manifestation"></a>Manifestación

La Arranque medido proporciona a am software un registro de confianza (resistente a la suplantación y manipulación) de todos los componentes de arranque que se iniciaron antes del software am. El software am puede usar el registro para determinar si los componentes que se han ejecutado antes son de confianza o si están infectados con malware. El software am de la máquina local puede enviar el registro a un servidor remoto para su evaluación. El servidor remoto puede iniciar acciones de corrección mediante la interacción con el software en el cliente o a través de mecanismos fuera de banda, según corresponda.

## <a name="mitigation"></a>Mitigación

En escenarios empresariales, el administrador del sistema tiene el control de Arranque medido se usa la información. En escenarios de usuario final, por ejemplo, la banca en línea), el consumidor debe optar por usar Arranque medido para el servicio específico.

## <a name="solution"></a>Solución

Se está preparando un documento técnico que detalla las API y las llamadas de función que se deben realizar para varios Arranque medido escenarios.

 

 




