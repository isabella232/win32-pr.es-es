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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466264"
---
# <a name="thin-provisioning-of-logical-units"></a>Aprovisionamiento fino de unidades lógicas

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

Windows El aprovisionamiento fino es una interfaz para la solución de aprovisionamiento de almacenamiento de un extremo a otro. Para ofrecer un servicio de aprovisionamiento de almacenamiento de alta disponibilidad, escalable y fácil de usar, se necesitan implementaciones sólidas desde el host del servidor al dispositivo de destino de almacenamiento. La característica de aprovisionamiento fino de Windows proporciona una vista sincrónica de los dispositivos de almacenamiento de aprovisionamiento fino al administrador del sistema, al administrador de TI y al administrador de almacenamiento mediante la identificación de la unidad lógica (LUN) de aprovisionamiento fino, la notificación de umbral, el control del agotamiento de recursos, la recuperación de espacio y la recuperación del estado del direccionamiento de bloque lógico (LBA). La Windows de aprovisionamiento fino presenta un sólido modelo de servicio de aprovisionamiento de almacenamiento que se puede aplicar a sistemas de almacenamiento cliente-servidor, almacenamiento de virtualización y servicios de almacenamiento en la nube. Microsoft garantizará la alta calidad de la característica de aprovisionamiento fino al aplicar los requisitos del Kit de certificación de hardware de aprovisionamiento fino de Windows para los productos de la matriz de almacenamiento.

La solución Windows de almacenamiento de aprovisionamiento fino:

-   Permite a los administradores de almacenamiento crear un LUN mayor con menos recursos de disco físico
-   Agrega o quita el recurso de disco físico sin interrumpir el servicio de aprovisionamiento de almacenamiento.
-   Alerta a los usuarios sobre el uso del volumen de almacenamiento a través de la configuración de umbral.
-   Admite el aprovisionamiento de almacenamiento a través de la configuración del grupo de almacenamiento compartido.
-   Aumenta o disminuye el tamaño del grupo de almacenamiento según la demanda y el uso del espacio de almacenamiento.

Resumen de las características de Windows thin provisioning:

-   Identificación de LUN de aprovisionamiento fino
-   Identificadores de notificación de umbral, agotamiento temporal de recursos y agotamiento permanente de recursos
-   Storage recuperación de espacio de almacenamiento
-   Asignación de consultas de estado de bloques lógicos

## <a name="manifestation"></a>Manifestación

Sin la comprensión adecuada de los identificadores Windows para el LUN de aprovisionamiento fino, la aplicación podría producir un comportamiento inesperado o una causa desconocida.

## <a name="using-thin-provisioning-luns"></a>Uso de LUN de aprovisionamiento fino

Para usar LUN con aprovisionamiento fino en Windows 8 o Windows Server 2012, los administradores del sistema y del almacenamiento deben tener en cuenta estos aspectos:

-   Identificación de LUN de aprovisionamiento fino; los administradores del sistema o los usuarios finales pueden usar Defrag y la utilidad Storage Optimizer para identificar el tipo de medio del dispositivo de almacenamiento.
-   Cuando se alcanza un umbral o un evento de agotamiento de recursos permanente, Windows registrará un evento del sistema para alertar al administrador del sistema.
-   Storage recuperación de espacio se puede realizar de forma manual o automática mediante la notificación de eliminación de archivos o el programador del optimizador de almacenamiento.
-   Storage administrador debe implementar la notificación de umbral para alertar al administrador del sistema o al usuario final y evitar cualquier interrupción inesperada del servicio de almacenamiento.

## <a name="tests"></a>Pruebas

-   Storage matriz debe recibir Windows 8 certificado de aprovisionamiento fino para admitir Windows características de aprovisionamiento fino
-   Windows El Kit de certificación de hardware de aprovisionamiento fino para la matriz de almacenamiento será una herramienta de prueba útil para comprobar la funcionalidad de la matriz de almacenamiento para la compatibilidad Windows características de aprovisionamiento fino
-   Windows espera que el LUN de aprovisionamiento fino y el LUN de aprovisionamiento completo funcionen en el mismo sistema sin ningún problema.

## <a name="resources"></a>Recursos

-   [Especificación de comandos de bloque SCSI T10 (SBC3r27)](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [Servicios de panel de hardware](/windows-hardware/drivers/dashboard/)

 

 