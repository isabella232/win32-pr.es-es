---
title: E/S de múltiples rutas ahora admite bloques de solicitud de almacenamiento extendidos
description: E/S de múltiples rutas ahora admite bloques de solicitud de almacenamiento extendidos
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f558f8088b5066b51447c5f2ea23edd5154d5c10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247653"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a>E/S de múltiples rutas ahora admite bloques de solicitud de almacenamiento extendidos

## <a name="platforms"></a>Plataformas

**Servidores:** Windows Server 2012 

## <a name="description"></a>Descripción

En Windows Server 2012, una nueva estructura, STORAGE REQUEST BLOCK (SRB extendido) reemplaza el bloque de solicitud \_ \_ SCSI \_ (SRB heredado) en la pila de \_ almacenamiento principal. Las SRB extendidas replican la funcionalidad de las SRB heredadas, pero también son extensibles y escalables.

E/S de múltiples rutas (MPIO) admite SRB extendidos y permite que los módulos específicos del dispositivo (HSM) especifiquen también compatibilidad con SRB extendida. Sin embargo, para que la pila de almacenamiento de un dispositivo de múltiples rutas use SRB extendidos, todos los componentes de la pila deben admitir **SRB extendidos,** incluido DSM . Tenga en cuenta que microsoft in-box DSM, MSDSM, admite SRB extendidos.

La estructura SCSI PASS THROUGH EX no forma parte de la estructura de paso a través de MPIO extendida, ya que el paso SCSI extendido puede ser de un tamaño variable, dependiendo del depurador de la línea de \_ \_ comandos \_ (CDB). En su lugar, el paso extendido de MPIO tiene un campo que describe el desplazamiento desde el principio de la estructura de paso a través de MPIO extendida a la estructura \_ SCSI PASS \_ THROUGH \_ EX. El autor de la llamada debe asegurarse de que asigna un búfer del tamaño adecuado y establece correctamente el desplazamiento de paso a través SCSI. Siempre que el autor de la llamada siga las reglas para los pasos SCSI extendidos, no debería haber ningún trabajo adicional para que usen el paso extendido de MPIO.

> [!Note]  
> Si DSM no admite SRB extendidos, MPIO producirá un error en las solicitudes de paso de MPIO extendidas que tengan establecida la marca \_ MPIO IOCTL \_ FLAG INVOLVE \_ \_ DSM.

 

## <a name="manifestation"></a>Manifestación

Si alguna parte de la pila de almacenamiento del dispositivo, incluido DSM, no admite SRB extendidas, la pila de almacenamiento volverá al uso de SRB heredados.

## <a name="solution"></a>Solución

Solo hay dos requisitos de MPIO para que DSM admita BLOQUES \_ DE SOLICITUD \_ DE ALMACENAMIENTO:

-   DSM debe notificar su tipo como DsmType6
-   DSM debe proporcionar la función DSM \_ ADDRESS \_ TYPE \_ SUPPORTED

Si DSM no notifica DsmType6 o si notifica DsmType6 pero no proporciona la función DSM ADDRESS TYPE SUPPORTED, MPIO supondrá que DSM no admite \_ \_ \_ SRB extendidos.

La función DSM \_ ADDRESS TYPE SUPPORTED acepta dos \_ \_ parámetros, uno de los cuales es un tipo de dirección. Este tipo de dirección debe ser uno de los valores de STORAGE \_ ADDRESS \_ TYPE \_ \* definidos en srb.h. DSM debe devolver TRUE si admite el tipo de dirección especificado y FALSE si no lo hace. La definición de "soporte" es en última instancia el DSM. MPIO usa esta función para asegurarse de que el DSM no se comportará mal si se le entrega un SRB extendido con una estructura \_ STOR ADDRESS del tipo especificado. Por lo tanto, MPIO normalmente llama a esta función cuando se enumera un dispositivo de múltiples rutas, pero se puede llamar a la función en cualquier momento.

Si un DSM nunca toca la dirección DE STOR de un SRB extendido, puede devolver TRUE para cualquier valor de TIPO DE DIRECCIÓN DE ALMACENAMIENTO \_ \_ \_ \_ \* válido. Revise el DSM de ejemplo en WDK.

**Otras notas importantes**

-   Los DSM que admiten SRB extendidos deben ser capaces de controlar tanto las estructuras SCSI REQUEST BLOCK como \_ las estructuras STORAGE REQUEST \_ \_ \_ BLOCK. El hecho de que un DSM informe de que admite SRB extendidos no significa que recibirá exclusivamente srbs extendidos. Puede seguir recibiendo cualquier número de SRB heredados además de los SRB extendidos y, por lo tanto, debe ser capaz de controlar ambos.
-   Hemos proporcionado un archivo de encabezado en la WDK denominado srbhelper.h que contiene funciones insertadas para ayudar a los controladores que deben controlar las SRB extendidas y heredadas. Nuestro DSM de ejemplo usa este encabezado para que pueda usarlo como ejemplo de cómo usar estas funciones.
-   Un DSM que no admita SRB extendidos nunca tendrá que controlar las SRB extendidas.
-   Es posible que un MPIO haga que la pila de almacenamiento se retrase en srbs heredados en caso de que DSM no admita un tipo de DIRECCIÓN DE ALMACENAMIENTO determinado (pero, de lo contrario, admita \_ \_ \_ \* SRB extendidos).
-   "BTL8" es el único TIPO DE DIRECCIÓN DE ALMACENAMIENTO definido \_ \_ actualmente para \_ \* Windows Server 2012.

 

 




