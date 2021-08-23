---
description: Un proveedor de instantáneas debe cumplir las directrices para garantizar la compatibilidad del solicitante.
ms.assetid: 49baeb89-1dc9-45c2-a532-071085a8e52f
title: Comportamientos necesarios para los proveedores de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97153d3780701fce6edcde4a4a7740ae1d296b58b2bb44ea38c51f3ab1204499
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056393"
---
# <a name="required-behaviors-for-shadow-copy-providers"></a>Comportamientos necesarios para los proveedores de instantáneas

Un proveedor de instantáneas debe cumplir las directrices para garantizar la compatibilidad del solicitante. En tiempo de ejecución, una aplicación de copia de seguridad o cualquier otro solicitante que use instantáneas debe funcionar correctamente sin tener conocimiento de detalles específicos de implementación del proveedor.

## <a name="automagic-resource-management"></a>Administración de recursos de Automagic

Debe ser posible que el solicitante simplemente agregue un volumen a un conjunto de instantáneas. El solicitante puede especificar atributos de instantáneas como **VSS \_ VOLSNAP \_ ATTR \_ TRANSPORTABLE,** **VSS \_ VOLSNAP \_ ATTR \_ DIFFERENTIAL** o **VSS \_ VOLSNAP \_ ATTR \_ PLEX** en EL CONTEXTO DE INSTANTÁNEA [**\_ DE VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context). El proveedor debe respetar esos atributos. Si no puede respetar esos atributos, debe indicar que no se admite el conjunto de instantáneas estableciendo \* *pbIsSupported* en [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported) en **FALSE.**

El proveedor nunca debe aceptar admitir una instantánea que no pueda crear. Si el solicitante no especifica un atributo plex o diferencial, el proveedor debe incluir lógica de automagic para asignar espacio del subsistema para la instantánea y crear la instantánea mediante el método más adecuado. El proveedor de hardware no debe incluir una API específica del proveedor para administrar las propiedades de instantáneas necesarias.

## <a name="created-shadow-copy-volumes-are-read-only-and-hidden"></a>Los volúmenes de instantáneas creados Read-Only y ocultos

VSS establece marcas en cada LUN afectado de forma que los volúmenes de instantáneas resultantes se ocultarán y serán de solo lectura cuando lo detecte un equipo que ejecuta Windows Server 2003. Las letras de unidad y las carpetas montadas no se asignan automáticamente. VSS mantiene estas marcas a lo largo del ciclo de vida de una instantánea.

## <a name="hardware-shadow-copy-luns-must-be-readwrite"></a>Los LUN de instantáneas de hardware deben ser de lectura y escritura

VSS solo admite instantáneas de hardware donde el LUN subyacente se asigna como lectura/escritura. Esto debe hacerse antes de crear la instantánea. no se puede hacer después del hecho. Los proveedores de hardware no deben modificar estas marcas. Para obtener más información sobre cómo VSS usa estas marcas, vea [The Shadow Copy Creation Process](the-shadow-copy-creation-process.md).

## <a name="auto-import-hardware-shadow-copies-are-not-supported-on-windows-cluster-service"></a>No se admiten instantáneas de hardware de importación automática en Windows servicio de clúster

Windows Servicio de clúster pueden alojar LUN con firmas duplicadas y diseño de partición. Los LUN de instantáneas se deben transportar a un host fuera del clúster. Para obtener más información, vea [Recuperación rápida mediante volúmenes de instantáneas transportables.](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copies-that-contain-dynamic-disks-must-be-transported-to-a-different-host"></a>Las instantáneas que contienen discos dinámicos deben transportarse a otro host

**Antes de Windows Server 2008:** La compatibilidad nativa con discos dinámicos no puede dar cabida a LUN con firmas duplicadas y contenido de la base de datos de configuración. Los LUN de instantáneas deben transportarse a otro host. VSS aplica esto al no permitir la importación automática de instantáneas de discos dinámicos. Un solicitante no debe importar una instantánea transportable de vuelta al mismo host.

**A partir de Windows Server 2008:** Esta limitación se quita.

## <a name="providers-are-out-of-process"></a>Los proveedores están fuera de proceso

Todos los proveedores deben implementarse como componentes COM fuera de proceso.

## <a name="time-critical-operations"></a>Time-Critical operaciones

Las operaciones largas, como sincronizar plexos, deben iniciarse en [**IVssHardwareSnapshotProvider::BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot). Esta función debe iniciar el trabajo de preparación asincrónica y devolver rápidamente. [**IVssProviderCreateSnapshotSet::EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) actúa como una función "rendezvous": el proveedor puede esperar sincrónicamente en este método para la finalización del trabajo de preparación iniciado por **BeginPrepareSnapshot.**

Los proveedores no deben agregar retrasos en [**IVssProviderCreateSnapshotSet::P reCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**IVssProviderCreateSnapshotSet::CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)o [**IVssProviderCreateSnapshotSet::P ostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) a medida que las aplicaciones se inmovilizan durante estas llamadas. **CommitSnapshots** debe devolverse en cuestión de segundos, ya que se llama a esto durante la ventana Vaciar y mantener, y la compatibilidad con kernel de VSS cancelará el vaciado y la retención si la versión no se recibe en 10 segundos, lo que provocaría un error en VSS en el proceso de creación de instantáneas. Si el proveedor tarda más de unos segundos en completar esta llamada, existe una alta probabilidad de que se producirá un error en la creación de la instantánea.

## <a name="careful-io-during-commitsnapshots"></a>E/S cuidadosa durante commitSnapshots

Los proveedores de hardware no deben tener que realizar ninguna E/S en los volúmenes implicados en la instantánea durante [**CommitSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) Si se requiere alguna E/S, los proveedores no deben iniciar ninguna E/S en un volumen original mientras se administra **el método CommitSnapshots.**

Durante [**CommitSnapshots,**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)los controladores de compatibilidad con kernel de VSS bloquean la E/S en los volúmenes originales que se están copiando en la sombra. Si el proveedor usa E/S sincrónica en un volumen que se encuentra en el conjunto de instantáneas, esa E/S se bloqueará y el proceso de confirmación de instantáneas se interbloqueará. El proveedor no debe llamar a ninguna API de Win32 durante **CommitSnapshots,** ya que tendrá una alta probabilidad de provocar E/S y un interbloqueo. El tiempo de espera de compatibilidad con kernel de VSS interrumpirá este interbloqueo después de 10 segundos, pero esto provocará un error en la creación de instantáneas.

Si se debe intentar la E/S, se debe realizar de forma asincrónica. La E/S no se completará hasta que todos los proveedores devuelvan sus [**métodos CommitSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) En general, es mejor realizar estas operaciones en la [**llamada PostCommitSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots)

## <a name="readwrite-shadow-copy-luns"></a>LUN de instantáneas de lectura y escritura

En esta versión, VSS solo admite LUN de instantáneas de lectura y escritura, incluso si los volúmenes se exponen como de solo lectura. El motivo es que el sistema debe cambiar las estructuras de datos en disco, como:

-   Firma de disco, que cambia durante el proceso de instantáneas
-   Las estructuras de datos relacionadas con particiones, incluidas las que indican que la partición es de solo lectura, oculta, una instantánea y no deben tener asignada una letra de unidad.

## <a name="unique-page-83-information"></a>Información de la página 83 única

Tanto el LUN original como el LUN de instantáneas recién creado deben tener al menos un identificador de almacenamiento único en los datos de la página 83. Al menos un IDENTIFICADOR DE ALMACENAMIENTO con un tipo de 1, 2, 3 o 8, y una asociación de 0 debe ser única en el LUN original y el LUN de instantáneas recién \_ creado.

 

 



