---
description: Un proveedor de instantáneas debe cumplir las directrices para garantizar la compatibilidad del solicitante.
ms.assetid: 49baeb89-1dc9-45c2-a532-071085a8e52f
title: Comportamientos necesarios para los proveedores de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f451dea7154a313cd64a3a46fbcc3b5fe663ec12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696977"
---
# <a name="required-behaviors-for-shadow-copy-providers"></a>Comportamientos necesarios para los proveedores de instantáneas

Un proveedor de instantáneas debe cumplir las directrices para garantizar la compatibilidad del solicitante. En tiempo de ejecución, una aplicación de copia de seguridad o cualquier otro solicitante que use instantáneas debe funcionar correctamente sin tener que conocer los detalles de implementación de un proveedor concreto.

## <a name="automagic-resource-management"></a>Administración de recursos automagic

Debe ser posible que el solicitante simplemente agregue un volumen a un conjunto de instantáneas. El solicitante puede especificar atributos de instantáneas, como **VSS \_ volsnap \_ ATTR \_ transportable**, la **\_ diferencia de \_ atributo \_ volsnap de VSS** de VSS o el **\_ \_ \_ Plex de atributo volsnap de VSS** en el contexto de la [**\_ \_ instantánea \_ de VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context). El proveedor debe cumplir esos atributos. Si no puede respetar esos atributos, debe indicar que no se admite el conjunto de instantáneas estableciendo \* *PbIsSupported* en [**IVssHardwareSnapshotProvider:: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported) en **false**.

El proveedor no debe aceptar nunca que admita una instantánea que no pueda crear. Si el solicitante no especifica un atributo complejo o diferencial, el proveedor debe incluir la lógica automágica para asignar el espacio del subsistema de la instantánea y crear la instantánea con el método más apropiado. El proveedor de hardware no debe incluir una API específica del proveedor para administrar las propiedades de instantánea necesarias.

## <a name="created-shadow-copy-volumes-are-read-only-and-hidden"></a>Los volúmenes de instantáneas creados están Read-Only y ocultos

VSS establece marcas en cada LUN afectado de modo que los volúmenes de instantáneas resultantes estén ocultos y sean de solo lectura cuando se detecten en un equipo con Windows Server 2003. Las letras de unidad y las carpetas montadas no se asignan automáticamente. VSS mantiene estas marcas a lo largo del ciclo de vida de una instantánea.

## <a name="hardware-shadow-copy-luns-must-be-readwrite"></a>Los LUN de instantáneas de hardware deben ser de lectura/escritura

VSS admite instantáneas de hardware solo cuando el LUN subyacente se asigna como lectura y escritura. Esto debe hacerse antes de crear la instantánea; no se puede hacer después del hecho. Los proveedores de hardware no deben modificar estas marcas. Para obtener más información sobre cómo usa VSS estas marcas, vea [el proceso de creación de instantáneas](the-shadow-copy-creation-process.md).

## <a name="auto-import-hardware-shadow-copies-are-not-supported-on-windows-cluster-service"></a>No se admite la importación automática de instantáneas de hardware en el servicio de Cluster Server de Windows

Windows Servicio de clúster no puede alojar LUN con firmas duplicadas y diseño de particiones. Los LUN de instantánea deben transportarse a un host fuera del clúster. Para obtener más información, consulte [recuperación rápida mediante el uso de volúmenes de instantáneas transportables](fast-recovery-using-transportable-shadow-copied-volumes.md).

## <a name="shadow-copies-that-contain-dynamic-disks-must-be-transported-to-a-different-host"></a>Las instantáneas que contienen discos dinámicos deben transportarse a un host diferente

**Antes de Windows Server 2008:** La compatibilidad nativa con los discos dinámicos no puede alojar LUN con firmas duplicadas y contenido de base de datos de configuración. Los LUN de instantánea deben transportarse a un host diferente. VSS lo exige al no permitir la importación automática de instantáneas de discos dinámicos. Un solicitante no debe importar una instantánea transportable de nuevo en el mismo host.

**A partir de Windows Server 2008:** Esta limitación se ha quitado.

## <a name="providers-are-out-of-process"></a>Los proveedores están fuera de proceso

Todos los proveedores deben implementarse como componentes COM fuera de proceso.

## <a name="time-critical-operations"></a>Operaciones de Time-Critical

Las operaciones largas, como la sincronización de complejos, deben iniciarse en [**IVssHardwareSnapshotProvider:: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot). Esta función debe iniciar el trabajo de preparación asincrónica y volver rápidamente. [**IVssProviderCreateSnapshotSet:: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) actúa como una función "Rendezvous": el proveedor puede esperar sincrónicamente en este método para completar el trabajo de preparación Iniciado por **BeginPrepareSnapshot**.

Los proveedores no deben agregar retrasos en [**IVssProviderCreateSnapshotSet::P recommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**IVssProviderCreateSnapshotSet:: CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)o [**IVssProviderCreateSnapshotSet::P ostcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) cuando las aplicaciones se inmovilizan durante estas llamadas. **CommitSnapshots** debe volver en segundos, ya que se llama a este método durante la ventana de vaciado y retención, y el soporte del kernel de VSS cancelará el vaciado y se conservará si la versión no se recibe en 10 segundos, lo que haría que VSS produjera un error en el proceso de creación de la instantánea. Si el proveedor tarda más de unos segundos en completar esta llamada, hay una alta probabilidad de que se produzca un error en la creación de la instantánea.

## <a name="careful-io-during-commitsnapshots"></a>E/s cuidadosa durante CommitSnapshots

Los proveedores de hardware no deben tener que realizar ninguna e/s en los volúmenes implicados en la instantánea durante la [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots). Si se requiere una e/s, los proveedores no deben iniciar ninguna e/s en un volumen original mientras se controla el método **CommitSnapshots** .

Durante [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots), los controladores de soporte del kernel de VSS bloquean la e/s en los volúmenes originales en los que se están realizando instantáneas. Si el proveedor usa e/s sincrónica para un volumen que está en el conjunto de instantáneas, se bloqueará la e/s y se producirá un interbloqueo del proceso de confirmación de la instantánea. El proveedor no debe llamar a ninguna API de Win32 durante **CommitSnapshots** , ya que tendrá una gran probabilidad de producir e/s y un interbloqueo. El tiempo de espera de compatibilidad del kernel de VSS interrumpirá este interbloqueo después de 10 segundos, pero esto hará que se produzca un error en la creación de la instantánea.

Si se debe intentar e/s, se debe realizar de forma asincrónica. La e/s no se completará hasta que se hayan devuelto todos los proveedores de sus métodos [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) . En general, es mejor realizar estas operaciones en la llamada a [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) .

## <a name="readwrite-shadow-copy-luns"></a>LUN de lectura/escritura de instantáneas

En esta versión, VSS solo admite LUN de lectura/escritura, aunque los volúmenes se expongan como de solo lectura. La razón es que el sistema necesita cambiar estructuras de datos en el disco, como:

-   Firma de disco, que cambia durante el proceso de instantáneas
-   Las estructuras de datos relacionadas con las particiones, incluidas las que indican que la partición es de solo lectura, está oculta, una instantánea y no deben tener asignada una letra de unidad.

## <a name="unique-page-83-information"></a>Página única 83 información

Tanto el LUN original como el LUN de instantánea recién creado deben tener al menos un identificador de almacenamiento único en la página 83 datos. Al menos un identificador de almacenamiento \_ con un tipo de 1, 2, 3 u 8, y una asociación de 0 debe ser única en el LUN original y el LUN de instantánea recién creado.

 

 



