---
description: Hyper-V usa el Servicio de instantáneas de volumen (VSS) para realizar copias de seguridad y restaurar máquinas virtuales.
ms.assetid: 94C67F22-658D-49DD-9588-6BB4FCF7ADA9
title: Copia de seguridad y restauración de máquinas virtuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf5a0db5bf6956557c22445d5745dbaede03389cf6ead7467b32b65e76c59b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914045"
---
# <a name="backing-up-and-restoring-virtual-machines"></a>Copia de seguridad y restauración de máquinas virtuales

Hyper-V usa el Servicio de instantáneas de volumen (VSS) para realizar copias de seguridad y restaurar máquinas virtuales. Si los servicios de integración de copia de seguridad (instantánea de volumen) están instalados en el sistema operativo invitado, se instala un solicitante de VSS que permitirá a los escritores de VSS del sistema operativo invitado participar en la copia de seguridad de la máquina virtual. Para más información, consulte las secciones siguientes:

-   [Copia de seguridad de las máquinas virtuales](#backing-up-the-virtual-machines)
-   [Restauración de las máquinas virtuales](#restoring-the-virtual-machines)
-   [Clústeres de conmutación por error y VSS de Hyper-V](#failover-clustering-and-hyper-v-vss)
-   [Detalles sobre VSS Writer de Hyper-V](#details-on-the-hyper-v-vss-writer)
-   [Temas relacionados](#related-topics)

## <a name="backing-up-the-virtual-machines"></a>Copia de seguridad de las máquinas virtuales

Hyper-V usa uno de los dos mecanismos para hacer una copia de seguridad de cada máquina virtual. El mecanismo de copia de seguridad predeterminado se denomina método "Saved State", donde la máquina virtual se coloca en un estado guardado durante el procesamiento del evento PrepareForSnapshot, se toman instantáneas de los volúmenes adecuados y la máquina virtual se devuelve al estado anterior durante el procesamiento del evento PostSnapshot.

El otro mecanismo de copia de seguridad se denomina método "Instantánea de máquina virtual secundaria", que usa VSS dentro de la máquina virtual secundaria para participar en la copia de seguridad. Para que se pueda usar el método "Instantánea de máquina virtual secundaria", se deben cumplir todas las condiciones siguientes:

-   El servicio de integración de copia de seguridad (instantánea de volumen) está instalado y en ejecución en la máquina virtual secundaria. El nombre del servicio es "Solicitante de instantáneas de volumen de Hyper-V".
-   La máquina virtual secundaria debe estar en estado de ejecución.
-   La ubicación del archivo de instantáneas de la máquina virtual se establece para que sea el mismo volumen del sistema operativo host que los archivos VHD de la máquina virtual.
-   Todos los volúmenes de la máquina virtual secundaria son discos básicos y no hay discos dinámicos.
-   Todos los discos de la máquina virtual secundaria deben usar un sistema de archivos que admita instantáneas (por ejemplo, NTFS).

En general, el proceso de copia de seguridad de máquinas virtuales es el mismo que se describe en Información general sobre el procesamiento de una copia [de seguridad en VSS.](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss) El comportamiento único se produce cuando vsS Writer de Hyper-V (parte del servicio "Administración de máquinas virtuales de Hyper-V") procesa el evento PrepareForSnapshot. Si la copia de seguridad se ha realizado mediante el método "Instantánea de máquina virtual secundaria", se realiza un procesamiento adicional, pero no es visible para la máquina virtual secundaria.

En el procedimiento siguiente se describe cómo hacer una copia de seguridad de máquinas virtuales.

**Para hacer una copia de seguridad de máquinas virtuales**

1.  Para cada máquina virtual de los metadatos del escritor, si se usa el método "Saved State", la máquina virtual se coloca en un estado guardado. En el caso de las máquinas virtuales que usan el método "Instantánea de máquina virtual secundaria", el servicio solicitante de instantáneas de volumen de Hyper-V de la máquina virtual secundaria procesa la copia de seguridad como se detalla en Información general sobre el procesamiento de una copia de seguridad en [VSS.](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss) Todos los eventos de VSS de la máquina virtual secundaria se producen durante el procesamiento del sistema operativo host del evento PrepareForSnapshot.
2.  Una vez que todas las máquinas virtuales se han puesto en el estado guardado o se han tomado instantáneas, vsS Writer de Hyper-V vuelve del evento PrepareForSnapshot. VsS Writer de Hyper-V no realiza ningún procesamiento durante los eventos Freeze y Thaw.
3.  Cuando VSS Writer de Hyper-V procesa el evento PostSnapshot, las máquinas virtuales de las que se ha hecho una copia de seguridad mediante el método "Saved State" y que vsS Writer de Hyper-V han guardado se devuelven al estado en el que se encontraban antes de que se iniciara la copia de seguridad. En el caso de las máquinas virtuales de las que se ha realizado una copia de seguridad mediante el método "Instantánea de máquina virtual secundaria", la imagen de host de los archivos VHD que tenían las instantáneas tomadas se revierte a la instantánea tomada durante el procesamiento del evento PrepareForSnapshot. Este procesamiento se realiza independientemente de los escritores de VSS en las máquinas virtuales secundarias, por lo que las instantáneas tomadas deben ser recuperables automáticamente. (**VSS \_ VOLSNAP \_ ATTR \_ NO \_ AUTORECOVERY** no está establecido en el contexto).

No se admiten copias de seguridad parciales. Si alguna máquina virtual no puede crear una instantánea, no se realizará una copia de seguridad de ninguna máquina virtual.

> [!Note]  
> Los discos iSCSI y de paso a través no son visibles para el sistema operativo host y, por lo tanto, no son de copia de seguridad de VsS Writer de Hyper-V. Las copias de seguridad de estos volúmenes deben realizarse completamente en la máquina virtual.

 

## <a name="restoring-the-virtual-machines"></a>Restauración de las máquinas virtuales

La restauración de las máquinas virtuales la realiza completamente el sistema operativo host; los escritores de VSS en las máquinas virtuales secundarias no están implicados.

En el procedimiento siguiente se describe cómo restaurar máquinas virtuales.

**Para restaurar máquinas virtuales**

1.  Durante el procesamiento del evento PreRestore, VSS Writer de Hyper-V se desactiva y elimina las máquinas virtuales que están a punto de restaurarse.
2.  Una vez que todos los escritores de VSS han procesado el evento PreRestore, se restauran los archivos.
3.  Durante el procesamiento del evento PostRestore, vsS Writer de Hyper-V llama al método [**IVssComponent::GetFileRestoreStatus.**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) Si la devolución no es **VSS \_ RS \_ ALL,** vss writer de Hyper-V llama al método [**SetWriterFailure**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure) y devuelve **False** desde el [**método OnPostRestore.**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore)
4.  Para cada máquina virtual restaurada, vsS Writer de Hyper-V registra la máquina virtual con el servicio de administración de Hyper-V. Si la máquina virtual se restaura en una ubicación no predeterminada, se crea un vínculo simbólico en la ubicación predeterminada que vincula a esa ubicación.
5.  Para cada VHD que se restauró, la ubicación se compara con la especificada para esa máquina virtual. Si la ubicación es diferente, la configuración se actualiza con la ubicación adecuada.
6.  La configuración de red se actualiza. Si los conmutadores virtuales a los que se conectó la máquina virtual cuando se creó una copia de seguridad siguen saliendo, se crean nuevos puertos y se conectan a la máquina virtual.

## <a name="failover-clustering-and-hyper-v-vss"></a>Clústeres de conmutación por error y VSS de Hyper-V

VsS Writer de Hyper-V no tiene en cuenta las máquinas virtuales que forman parte de un clúster de conmutación por error. Durante las copias de seguridad del método "Estado guardado" y todas las restauraciones, la máquina virtual se colocaría en el estado guardado o se eliminaría por completo. Esto se vería como un error por parte del servicio de agrupación en clústeres y provocaría la conmutación por error de las aplicaciones de esos nodos a otros nodos. Para evitar esto durante las copias de seguridad de "Estado guardado", el estado de la máquina virtual debe guardarse mediante el servicio de agrupación en clústeres. Para evitar esto durante una restauración, los recursos de la máquina virtual tendrían que desconectarse.

## <a name="details-on-the-hyper-v-vss-writer"></a>Detalles sobre VSS Writer de Hyper-V

Nombre del escritor: Microsoft Hyper-V VSS Writer

Identificador de escritor: 66841cd4-6ded-4f4b-8f17-fd23f8ddc3de

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre el procesamiento de una copia de seguridad en VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)
</dt> <dt>

[Información general sobre el procesamiento de una restauración en VSS](/windows/desktop/VSS/overview-of-processing-a-restore-under-vss)
</dt> </dl>

 

 
