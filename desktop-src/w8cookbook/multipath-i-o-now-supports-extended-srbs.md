---
title: E/s de múltiples rutas admite ahora bloques de solicitud de almacenamiento extendido
description: E/s de múltiples rutas admite ahora bloques de solicitud de almacenamiento extendido
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f558f8088b5066b51447c5f2ea23edd5154d5c10
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "104359481"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a>E/s de múltiples rutas admite ahora bloques de solicitud de almacenamiento extendido

## <a name="platforms"></a>Plataformas

**Servidores** : Windows Server 2012 

## <a name="description"></a>Descripción

En Windows Server 2012, una nueva estructura, el bloque de solicitud de almacenamiento \_ \_ (SRB extendido) reemplaza \_ el \_ bloque de solicitud SCSI (SRB) en la pila de almacenamiento principal. Extended SRBs Replica la funcionalidad de la SRBs heredada, pero también es extensible y escalable.

E/s de múltiples rutas (MPIO) admite SRBs extendidos y permite que los módulos específicos del dispositivo (DSM) especifiquen también la compatibilidad con SRB extendida. Sin embargo, para que la pila de almacenamiento de un dispositivo de múltiples rutas use SRBss extendidos, **todos los componentes de la pila deben admitir SRBs extendidos, incluido DSM**. Tenga en cuenta que el DSM de Microsoft en Box, MSDSM, admite SRBs extendido.

La \_ estructura de paso \_ a través \_ de SCSI no forma parte de la estructura de paso a través de MPIO extendido, ya que el paso de SCSI extendido puede ser de un tamaño variable, según el depurador de la línea de comandos (CDB). En su lugar, el pase de MPIO extendido tiene un campo que describe el desplazamiento desde el principio de la estructura de paso a través de MPIO extendido hasta la \_ estructura de paso \_ a través de SCSI \_ . El llamador debe asegurarse de que asignan un búfer con el tamaño adecuado y establecen el desplazamiento correcto del SCSI. Siempre que el autor de la llamada siga las reglas de paso a través de SCSI extendido, no debería haber ningún trabajo adicional para que use el paso de MPIO extendido.

> [!Note]  
> Si el DSM no es compatible con SRBs extendidos, MPIO producirá un error en las solicitudes de paso a través de MPIO extendidas que tienen la marca de ioctl MPIO establecida en la \_ \_ \_ \_ marca DSM.

 

## <a name="manifestation"></a>Manifestación

Si alguna parte de la pila de almacenamiento del dispositivo, incluido DSM, no admite SRBs extendidos, la pila de almacenamiento revertirá al uso de SRBs heredadas.

## <a name="solution"></a>Solución

Solo hay dos requisitos de MPIO para que DSM admita bloques de \_ solicitud de almacenamiento \_ :

-   DSM debe notificar su tipo como DsmType6
-   DSM debe proporcionar la \_ \_ \_ función compatible con el tipo de dirección de DSM

Si el DSM no notifica DsmType6 o si informa de DsmType6, pero no proporciona la \_ función compatible con el tipo de dirección de DSM \_ \_ , MPIO ASUMIrá que DSM no admite SRBs extendido.

La \_ función compatible con el tipo de dirección DSM \_ \_ acepta dos parámetros, uno de los cuales es un tipo de dirección. Este tipo de dirección debe ser uno de los \_ valores de tipo de dirección de almacenamiento \_ \_ \* definidos en SRB. h. El DSM debe devolver TRUE si admite el tipo de dirección dado y FALSE si no es así. La definición de "soporte" es en última instancia hasta el DSM. MPIO usa esta función para asegurarse de que el DSM no se comportará correctamente si se le entrega una SRB extendida con una \_ estructura de dirección Stor del tipo dado. Como tal, MPIO normalmente llama a esta función cuando se está enumerando un dispositivo de múltiples rutas, pero se puede llamar a la función en cualquier momento.

Si un DSM no toca nunca una dirección de almacenamiento de información de SRB extendida \_ , puede devolver true para cualquier valor de tipo de dirección de almacenamiento válido \_ \_ \_ \* . Revise el DSM de ejemplo en el WDK.

**Otras notas importantes**

-   Los DSM que admiten SRBs extendidos deben ser capaces de \_ administrar \_ estructuras de bloques de solicitud SCSI y estructuras de bloques de solicitud de almacenamiento \_ \_ . El hecho de que un DSM informe de que admite SRBs extendidos no significa que recibirá de forma exclusiva SRBs extendido. Todavía puede recibir cualquier número de SRBs heredados además de SRBs extendido y, por tanto, debe ser capaz de controlar ambos.
-   Hemos proporcionado un archivo de encabezado en el WDK llamado srbhelper. h que contiene funciones insertadas para ayudar a los controladores que deben controlar los SRBs extendidos y heredados. Nuestro ejemplo DSM usa este encabezado para que pueda usarlo como ejemplo de cómo usar estas funciones.
-   Un DSM que no admita SRBs extendidos nunca tendrá que administrar SRBs extendidos.
-   Es posible que un MPIO cause que la pila de almacenamiento revierta en SRBs heredados en caso de que el DSM no admita un tipo de dirección de almacenamiento determinado \_ \_ \_ \* (pero, de lo contrario, admita SRBs extendido).
-   "BTL8" es el único \_ \_ tipo de dirección \_ \* de almacenamiento definido actualmente para Windows Server 2012.

 

 




