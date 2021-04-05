---
title: Aprovisionamiento fino de unidades lógicas
description: Aprovisionamiento fino de unidades lógicas
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- LBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078507"
---
# <a name="thin-provisioning-of-logical-units"></a>Aprovisionamiento fino de unidades lógicas

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

El aprovisionamiento fino de Windows es una interfaz para la solución de aprovisionamiento de almacenamiento de un extremo a otro. Para ofrecer un servicio de aprovisionamiento de almacenamiento de alta disponibilidad, escalable y fácil de usar, se necesitan implementaciones sólidas desde el host del servidor al dispositivo de destino de almacenamiento. La característica de aprovisionamiento fino de Windows proporciona una vista sincrónica de los dispositivos de almacenamiento de aprovisionamiento fino al administrador del sistema, el administrador de ti y el administrador de almacenamiento a través de la identificación de la unidad lógica (LUN) de aprovisionamiento fino, la notificación de umbrales, el control de agotamiento de recursos, la recuperación de espacio y la recuperación de estado del direccionamiento de bloque lógico (LBA) La característica de aprovisionamiento fino de Windows presenta un sólido modelo de servicio de aprovisionamiento de almacenamiento que se puede aplicar a los sistemas de almacenamiento cliente-servidor, almacenamiento de virtualización y servicios de almacenamiento en la nube. Microsoft garantizará la alta calidad de la característica de aprovisionamiento fino aplicando los requisitos del kit de certificación de hardware de aprovisionamiento fino de Windows para los productos de la matriz de almacenamiento.

La solución de almacenamiento de aprovisionamiento fino de Windows:

-   Permite a los administradores de almacenamiento crear un LUN mayor con menos recursos de disco físico.
-   Agrega o quita un recurso de disco físico sin interrumpir el servicio de aprovisionamiento de almacenamiento
-   Alerta a los usuarios del uso del volumen de almacenamiento a través de la configuración de umbral
-   Admite el aprovisionamiento de almacenamiento a través de la configuración del grupo de almacenamiento compartido
-   Aumenta o disminuye el tamaño del grupo de almacenamiento en función de la demanda y el uso del espacio de almacenamiento

Resumen de las características de aprovisionamiento fino de Windows:

-   Identificación de LUN de aprovisionamiento fino
-   Identificadores para la notificación de umbrales, el agotamiento de recursos temporal y el agotamiento de recursos permanente
-   Recuperación del espacio de almacenamiento
-   Asignación de consultas de estado de bloques lógicos

## <a name="manifestation"></a>Manifestación

Sin la comprensión adecuada de los identificadores de Windows para el LUN de aprovisionamiento fino, la aplicación podría generar un error inesperado o una causa desconocida.

## <a name="using-thin-provisioning-luns"></a>Uso de LUN de aprovisionamiento fino

Para usar LUN con aprovisionamiento fino en Windows 8 o Windows Server 2012, los administradores de sistemas y almacenamiento deben tener en cuenta estos aspectos:

-   Identificación de LUN de aprovisionamiento fino; los administradores del sistema o los usuarios finales pueden usar Defrag y la utilidad del optimizador de almacenamiento para identificar el tipo de medio del dispositivo de almacenamiento.
-   Cuando se alcanza un umbral o un evento de agotamiento de recursos permanente, Windows registra un evento del sistema para alertar al administrador del sistema
-   La recuperación de espacio de almacenamiento se puede realizar manual o automáticamente mediante la notificación de eliminación de archivo o el programador del optimizador de almacenamiento
-   El administrador de almacenamiento debe implementar la notificación de umbral para alertar al administrador del sistema o al usuario final y evitar cualquier interrupción del servicio de almacenamiento inesperada.

## <a name="tests"></a>Pruebas

-   La matriz de almacenamiento debe recibir el certificado de aprovisionamiento fino de Windows 8 para admitir las características de aprovisionamiento fino de Windows
-   El kit de certificación de hardware de aprovisionamiento fino de Windows para la matriz de almacenamiento será una herramienta de prueba útil para comprobar la capacidad de la matriz de almacenamiento para la compatibilidad con las características de aprovisionamiento fino de Windows
-   Windows espera que el LUN de aprovisionamiento fino y el LUN de aprovisionamiento completo funcionen en el mismo sistema sin ningún problema

## <a name="resources"></a>Recursos

-   [Especificación del comando de bloque SCSI de T10 (SBC3r27)](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [Servicios del panel de hardware](/windows-hardware/drivers/dashboard/)

 

 