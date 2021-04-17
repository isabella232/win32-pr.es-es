---
description: Hyper-V usa el Servicio de instantáneas de volumen (VSS) para realizar copias de seguridad y restaurar máquinas virtuales.
ms.assetid: 94C67F22-658D-49DD-9588-6BB4FCF7ADA9
title: Copia de seguridad y restauración de máquinas virtuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9cf6d5b80a4c7392fb38e893a4fafad3f90435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687528"
---
# <a name="backing-up-and-restoring-virtual-machines"></a>Copia de seguridad y restauración de máquinas virtuales

Hyper-V usa el Servicio de instantáneas de volumen (VSS) para realizar copias de seguridad y restaurar máquinas virtuales. Si los servicios de integración de copia de seguridad (instantánea de volumen) están instalados en el sistema operativo invitado, se instala un solicitante de VSS que permitirá a los escritores de VSS en el sistema operativo invitado participar en la copia de seguridad de la máquina virtual. Para obtener más información, consulte las siguientes secciones:

-   [Copia de seguridad de las máquinas virtuales](#backing-up-the-virtual-machines)
-   [Restauración de las máquinas virtuales](#restoring-the-virtual-machines)
-   [Clústeres de conmutación por error y Hyper-V VSS](#failover-clustering-and-hyper-v-vss)
-   [Detalles sobre VSS Writer de Hyper-V](#details-on-the-hyper-v-vss-writer)
-   [Temas relacionados](#related-topics)

## <a name="backing-up-the-virtual-machines"></a>Copia de seguridad de las máquinas virtuales

Hyper-V usa uno de los dos mecanismos para realizar una copia de seguridad de cada máquina virtual. El mecanismo de copia de seguridad predeterminado se denomina método "estado guardado", en el que la máquina virtual se coloca en un estado guardado durante el procesamiento del evento PrepareForSnapshot, se toman las instantáneas de los volúmenes adecuados y la máquina virtual se vuelve al estado anterior durante el procesamiento del evento de instantáneas.

El otro mecanismo de copia de seguridad se denomina método "instantánea de máquina virtual secundaria", que usa VSS dentro de la máquina virtual secundaria para participar en la copia de seguridad. Para que se admita el método "instantánea de máquina virtual secundaria", deben cumplirse todas las condiciones siguientes:

-   El servicio de integración de copia de seguridad (instantánea de volumen) está instalado y ejecutándose en la máquina virtual secundaria. El nombre del servicio es "solicitante de instantáneas de volumen de Hyper-V".
-   La máquina virtual secundaria debe estar en el estado en ejecución.
-   La ubicación del archivo de instantáneas de la máquina virtual está configurada para que sea el mismo volumen en el sistema operativo host que los archivos VHD de la máquina virtual.
-   Todos los volúmenes de la máquina virtual secundaria son discos básicos y no hay ningún disco dinámico.
-   Todos los discos de la máquina virtual secundaria deben usar un sistema de archivos que admita instantáneas (por ejemplo, NTFS).

En general, el proceso de copia de seguridad de máquinas virtuales es el mismo que se describe en [información general sobre el procesamiento de una copia de seguridad en VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss). El comportamiento único se produce cuando el VSS Writer de Hyper-V (parte del servicio de administración de máquinas virtuales de Hyper-V) procesa el evento PrepareForSnapshot. Si la copia de seguridad se realizó con el método "instantánea de máquina virtual secundaria", se realiza un procesamiento adicional pero no es visible para la máquina virtual secundaria.

En el procedimiento siguiente se describe cómo realizar copias de seguridad de máquinas virtuales.

**Para realizar copias de seguridad de máquinas virtuales**

1.  Para cada máquina virtual en los metadatos del sistema de escritura, si se usa el método "estado guardado", la máquina virtual se coloca en un estado guardado. En el caso de las máquinas virtuales que usan el método "instantánea de VM secundaria", el servicio solicitante de instantáneas de volumen de Hyper-V de la máquina virtual secundaria procesa la copia de seguridad como se detalla en [información general sobre el procesamiento de una copia de seguridad en VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss). Todos los eventos de VSS en la máquina virtual secundaria se producen durante el procesamiento del sistema operativo host del evento PrepareForSnapshot.
2.  Después de que todas las máquinas virtuales se hayan puesto en el estado guardado o se hayan tomado instantáneas, el VSS Writer de Hyper-V vuelve del evento PrepareForSnapshot. La VSS Writer de Hyper-V no realiza ningún procesamiento durante los eventos Freeze y reanudación.
3.  Cuando el VSS Writer de Hyper-V procesa el evento de instantáneas, las máquinas virtuales de las que se realizó una copia de seguridad mediante el método "estado guardado" y que se pusieron en estado guardado por el VSS Writer de Hyper-V se devuelven al estado en que se encontraban antes de que se iniciara la copia de seguridad. En el caso de las máquinas virtuales de las que se realizó una copia de seguridad mediante el método "instantánea de máquina virtual secundaria", la imagen de host de los archivos VHD que tenían las instantáneas tomadas se revierte a la instantánea tomada durante el procesamiento del evento PrepareForSnapshot. Este procesamiento se realiza de forma independiente de los escritores de VSS en las máquinas virtuales secundarias, por lo que las instantáneas tomadas deben ser recuperables automáticamente. (**VSS \_ VOLSNAP \_ ATTR \_ \_** no se ha establecido la Autorrecuperación en el contexto).

No se admiten copias de seguridad parciales. Si se produce un error en una máquina virtual para crear una instantánea, no se hará ninguna copia de seguridad de las máquinas virtuales.

> [!Note]  
> Los discos de paso a través e iSCSI no son visibles para el sistema operativo host y, por lo tanto, no se realiza una copia de seguridad del VSS Writer de Hyper-V. Las copias de seguridad de estos volúmenes deben realizarse en su totalidad en la máquina virtual.

 

## <a name="restoring-the-virtual-machines"></a>Restauración de las máquinas virtuales

La restauración de las máquinas virtuales se realiza por completo en el sistema operativo host; los escritores de VSS en las máquinas virtuales secundarias no están implicados.

En el procedimiento siguiente se describe cómo restaurar máquinas virtuales.

**Para restaurar máquinas virtuales**

1.  Durante el procesamiento del evento de prerestauración, el VSS Writer de Hyper-V se apaga y elimina todas las máquinas virtuales que se van a restaurar.
2.  Después de que todos los escritores de VSS hayan procesado el evento prerestore, se restauran los archivos.
3.  Durante el procesamiento del evento postrestore, el VSS Writer de Hyper-V llama al método [**IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) . Si el valor devuelto no es **VSS \_ RS \_ ALL**, el VSS Writer de Hyper-V llama al método [**SetWriterFailure**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure) y devuelve **false** desde el método [**OnPostRestore**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore) .
4.  Para cada máquina virtual restaurada, la VSS Writer de Hyper-V registra la máquina virtual con el servicio de administración de Hyper-V. Si la máquina virtual se restaura en una ubicación no predeterminada, se crea un vínculo simbólico en la ubicación predeterminada que se vincula a esa ubicación.
5.  Para cada VHD que se restauró, la ubicación se compara con la especificada para esa máquina virtual. Si la ubicación es diferente, la configuración se actualiza con la ubicación adecuada.
6.  Se actualiza la configuración de red. Si los conmutadores virtuales a los que estaba conectada la máquina virtual cuando se hizo la copia de seguridad todavía salen, se crean nuevos puertos y se conectan a la máquina virtual.

## <a name="failover-clustering-and-hyper-v-vss"></a>Clústeres de conmutación por error y Hyper-V VSS

La VSS Writer de Hyper-V no da ninguna consideración a las máquinas virtuales que forman parte de un clúster de conmutación por error. Durante las copias de seguridad del método "estado guardado" y todas las restauraciones, la máquina virtual se colocará en el estado guardado o se eliminará completamente. Esto se vería como un error en el servicio de agrupación en clústeres y hace que las aplicaciones de esos nodos se conmuten por error a otros nodos. Para evitar esto durante las copias de seguridad de "estado guardado", el estado de la máquina virtual se debe guardar mediante el servicio de agrupación en clústeres. Para evitar esto durante una restauración, los recursos de la máquina virtual deberán dejarse sin conexión.

## <a name="details-on-the-hyper-v-vss-writer"></a>Detalles sobre VSS Writer de Hyper-V

Nombre del escritor: Microsoft Hyper-V VSS Writer

ID. de escritor: 66841cd4-6ded-4f4b-8f17-fd23f8ddc3de

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre el procesamiento de una copia de seguridad en VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)
</dt> <dt>

[Información general sobre el procesamiento de una restauración en VSS](/windows/desktop/VSS/overview-of-processing-a-restore-under-vss)
</dt> </dl>

 

 
