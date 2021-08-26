---
title: E/S de múltiples rutas ahora admite bloques de solicitud de almacenamiento extendido
description: E/S de múltiples rutas ahora admite bloques de solicitud de almacenamiento extendido
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b3a5ce3050bf7fddc2bd77da30e766c7b9cd67a8c4f49c753da5302b104c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932215"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a>E/S de múltiples rutas ahora admite bloques de solicitud de almacenamiento extendido

## <a name="platforms"></a>Plataformas

**Servidores:** Windows Server 2012 

## <a name="description"></a>Descripción

En Windows Server 2012, una nueva estructura, STORAGE REQUEST BLOCK (SRB extendido) reemplaza el bloque de solicitud \_ \_ SCSI \_ (SRB heredado) en la pila \_ de almacenamiento principal. Las SRB extendidas replican la funcionalidad de las SRB heredadas, pero también son extensibles y escalables.

E/S de múltiples rutas (MPIO) admite SRB extendidos y permite que los módulos específicos del dispositivo (DSM) especifiquen también compatibilidad con SRB extendida. Sin embargo, para que la pila de almacenamiento de un dispositivo de múltiples rutas use SRB extendidas, todos los componentes de la pila deben admitir **SRB extendidos,** incluido DSM . Tenga en cuenta que el DSM de Microsoft, MSDSM, admite SRB extendidos.

La estructura SCSI PASS THROUGH EX no forma parte de la estructura de paso a través de MPIO extendida, ya que el paso a través de SCSI extendido puede ser de un tamaño variable, dependiendo del depurador de la línea de comandos \_ \_ \_ (CDB). En su lugar, el paso extendido de MPIO tiene un campo que describe el desplazamiento desde el principio de la estructura de paso a través de MPIO extendida a la estructura \_ SCSI PASS \_ THROUGH \_ EX. El autor de la llamada debe asegurarse de asignar un búfer del tamaño adecuado y establecer correctamente el desplazamiento de paso a través SCSI. Siempre que el autor de la llamada siga las reglas para los pasos SCSI extendidos, no debería haber ningún trabajo adicional para que usen el paso extendido de MPIO.

> [!Note]  
> Si el DSM no admite SRB extendidos, MPIO producirá un error en las solicitudes de paso a través de MPIO extendidas que tengan establecida la marca \_ MPIO IOCTL \_ FLAG INVOLVE \_ \_ DSM.

 

## <a name="manifestation"></a>Manifestación

Si alguna parte de la pila de almacenamiento del dispositivo, incluido DSM, no admite SRB extendidas, la pila de almacenamiento revertirá al uso de SRB heredados.

## <a name="solution"></a>Solución

Solo hay dos requisitos de MPIO para que dsm admita bloques de \_ solicitud de \_ almacenamiento:

-   El DSM debe notificar su tipo como DsmType6
-   Dsm debe proporcionar la función DSM \_ ADDRESS \_ TYPE \_ SUPPORTED

Si DSM no notifica DsmType6 o si notifica DsmType6 pero no proporciona la función DSM ADDRESS TYPE SUPPORTED, MPIO asumirá que DSM no admite \_ \_ \_ SRB extendidas.

La función DSM \_ ADDRESS TYPE SUPPORTED acepta dos \_ \_ parámetros, uno de los cuales es un tipo de dirección. Este tipo de dirección debe ser uno de los valores de STORAGE \_ ADDRESS \_ TYPE \_ \* definidos en srb.h. Dsm debe devolver TRUE si admite el tipo de dirección especificado y FALSE si no lo hace. La definición de "compatibilidad" es en última instancia del DSM. MPIO usa esta función para asegurarse de que el DSM no se comportará mal si se le entrega un SRB extendido con una estructura \_ STOR ADDRESS del tipo especificado. Por lo tanto, MPIO normalmente llama a esta función cuando se enumera un dispositivo de múltiples rutas, pero se puede llamar a la función en cualquier momento.

Si un DSM nunca toca la dirección DE STOR de un SRB extendido, puede devolver TRUE para cualquier \_ valor de TIPO DE DIRECCIÓN DE ALMACENAMIENTO \_ \_ \_ \* válido. Revise el DSM de ejemplo en wdk.

**Otras notas importantes**

-   Los DSM que admiten SRB extendidos deben ser capaces de controlar las estructuras SCSI \_ REQUEST BLOCK y STORAGE REQUEST \_ \_ \_ BLOCK. El hecho de que un DSM informe de que admite SRB extendidos no significa que recibirá exclusivamente SRB extendidas. Todavía puede recibir cualquier número de SRB heredadas además de las SRB extendidas y, por tanto, debe ser capaz de controlar ambas.
-   Hemos proporcionado un archivo de encabezado en el WDK denominado srbhelper.h que contiene funciones insertadas para ayudar a los controladores que deben controlar las SRB extendidas y heredadas. Nuestro DSM de ejemplo usa este encabezado para que pueda usarlo como ejemplo de cómo usar estas funciones.
-   Un DSM que no admita srbs extendidos nunca tendrá que controlar las SRB extendidas.
-   Es posible que un MPIO haga que la pila de almacenamiento se retrase en las SRB heredadas en caso de que DSM no admita un tipo de DIRECCIÓN DE ALMACENAMIENTO determinado (pero, de lo contrario, admita \_ \_ \_ \* SRB extendidos).
-   "BTL8" es el único TIPO DE DIRECCIÓN DE ALMACENAMIENTO definido \_ \_ actualmente para \_ \* Windows Server 2012.

 

 




