---
description: Windows Server 2008 R2 y Windows 7 presentan los siguientes cambios en el Servicio de instantáneas de volumen.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Novedades: VSS en Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eeaaf42a82e13c5766ee3cfa6ba9fe73a36a783824497482ac97fc20d058a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121531"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a>Novedades: VSS en Windows Server 2008 R2 & Windows 7

Windows Server 2008 R2 y Windows 7 presentan los siguientes cambios en el Servicio de instantáneas de volumen.

## <a name="new-vss-interfaces"></a>Nuevas interfaces de VSS

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

[**OPCIONES DE \_ RECUPERACIÓN DE VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a>Nuevas funciones de VSS

<dl>

[**CreateVssExpressWriter**](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a>Modificaciones existentes de la interfaz de VSS

<dl>

[**Interfaz IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)<dl> Método agregado: [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Registro y seguimiento de eventos de VSS

A partir de Windows Server 2008 R2 y Windows 7, puede usar la herramienta VssTrace, la herramienta Logman o la herramienta Tracelog para recopilar información de seguimiento de la infraestructura de VSS. Para obtener más información, [vea Usar herramientas de seguimiento con VSS.](using-tracing-tools-with-vss.md)

## <a name="lun-resynchronization"></a>Resincronización de LUN

En Windows Server 2008 R2 y Windows 7, los solicitantes de VSS pueden usar una característica del proveedor de instantáneas de hardware llamada resincronización de LUN. Se trata de un esquema de recuperación rápida que permite a un administrador de aplicaciones restaurar datos desde una instantánea al número de unidad lógica (LUN) original o a un lun nuevo. La instantánea puede ser un clon completo o una instantánea diferencial. En ambos casos, al final de la operación de resincronización, el LUN de destino tendrá el mismo contenido que el LUN de instantánea. Durante la operación de resincronización, la matriz realiza una copia del nivel de bloque de la instantánea en el LUN de destino. Para obtener más información, vea lo siguiente:

-   [Resincronización de LUN: un escenario de recuperación rápida en Server 2008 R2](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   "Cómo se usan las instantáneas" [en Servicio de instantáneas de volumen](/windows-server/storage/file-server/volume-shadow-copy-service)
-   [Gotchas comunes de resincronización de LUN](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a>Escritores rápidos

En Windows Server 2008 R2 y Windows 7, la interfaz express de VSS permite a una aplicación registrar la ubicación de sus archivos de datos sin implementar vsS Writer. Para obtener más información, [vea Servicio de instantáneas de volumen (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).

## <a name="new-vss-writers"></a>Nuevos vss writers

Windows Server 2008 R2 y Windows 7 presentan los siguientes vss writers:

-   Escritor de contadores de rendimiento
-   Programador de tareas Writer
-   Escritor del almacén de metadatos de VSS

Estos nuevos escritores se documentan en [In-Box VSS Writers](in-box-vss-writers.md).

 

 
