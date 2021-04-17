---
description: Windows Server 2008 R2 y Windows 7 presentan los siguientes cambios en el Servicio de instantáneas de volumen.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Novedades: VSS en Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696439"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a>Novedades: VSS en Windows Server 2008 R2 & Windows 7

Windows Server 2008 R2 y Windows 7 presentan los siguientes cambios en el Servicio de instantáneas de volumen.

## <a name="new-vss-interfaces"></a>Nuevas interfaces VSS

<dl>

[**IVssBackupComponentsEx3**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[**IVssComponentEx2**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[**IVssCreateExpressWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[**IVssExpressWriter**](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a>Nuevas clases de VSS

<dl>

[**CVssWriterEx2**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a>Nuevas enumeraciones de VSS

<dl>

[**\_Opciones de recuperación de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a>Nuevas funciones de VSS

<dl>

[**CreateVssExpressWriter**](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a>Modificaciones de la interfaz de VSS existentes

<dl>

Interfaz [**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)<dl> Método agregado: [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Seguimiento y registro de eventos de VSS

A partir de Windows Server 2008 R2 y Windows 7, puede usar la herramienta VssTrace, la herramienta Logman o la herramienta tracelog para recopilar información de seguimiento de la infraestructura de VSS. Para obtener más información, vea [uso de herramientas de seguimiento con VSS](using-tracing-tools-with-vss.md).

## <a name="lun-resynchronization"></a>Resincronización de LUN

En Windows Server 2008 R2 y Windows 7, los solicitantes de VSS pueden usar una característica del proveedor de instantáneas de hardware llamada resincronización de LUN. Se trata de un esquema de recuperación rápida que permite a un administrador de aplicaciones restaurar datos de una instantánea en el número de unidad lógica (LUN) original o en un LUN nuevo. La instantánea puede ser un clon completo o una instantánea diferencial. En ambos casos, al final de la operación de resincronización, el LUN de destino tendrá el mismo contenido que el LUN de instantánea. Durante la operación de resincronización, la matriz realiza una copia del nivel de bloque de la instantánea en el LUN de destino. Para obtener más información, vea lo siguiente:

-   [Resincronización de LUN: un escenario de recuperación rápida en Server 2008 R2](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   "Cómo se usan las instantáneas" en [servicio de instantáneas de volumen](/windows-server/storage/file-server/volume-shadow-copy-service)
-   [Problemas comunes de resincronización de LUN](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a>Escritores de Express

En Windows Server 2008 R2 y Windows 7, la interfaz de VSS Express permite que una aplicación registre la ubicación de sus archivos de datos sin implementar una VSS Writer. Para obtener más información, consulte [escritores de servicio de instantáneas de volumen (VSS) Express](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).

## <a name="new-vss-writers"></a>Nuevos escritores de VSS

Windows Server 2008 R2 y Windows 7 presentan los siguientes escritores de VSS:

-   Escritor de contadores de rendimiento
-   Escritor de Programador de tareas
-   Escritor de almacén de metadatos de VSS

Estos nuevos escritores están documentados en [escritores de VSS en la caja](in-box-vss-writers.md).

 

 
