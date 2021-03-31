---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Novedades de VSS en Windows Server 2008 y Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f053e327a7a54a9597bc06836b37c00effc62f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154326"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a>Novedades de VSS en Windows Server 2008 y Windows Vista SP1

Windows Server 2008 y Windows Vista con Service Pack 1 (SP1) presentan los siguientes cambios en el Servicio de instantáneas de volumen.

> [!Note]  
> Todos los cambios de Windows Vista se aplican a Windows Server 2008 y Windows Vista con SP1. Para obtener más información sobre estos cambios, consulte [novedades de VSS en Windows Vista](what-s-new-in-vss-in-windows-vista.md).

 

-   [Nuevas interfaces VSS](#new-vss-interfaces)
-   [Nuevas enumeraciones de VSS](#new-vss-enumerations)
-   [Nuevas estructuras de VSS](#new-vss-structures)
-   [Modificaciones de la enumeración de VSS existentes](#existing-vss-enumeration-modifications)
-   [Modificaciones de la interfaz de VSS existentes](#existing-vss-interface-modifications)
-   [Nuevos escritores de VSS](#new-vss-writers)

## <a name="new-vss-interfaces"></a>Nuevas interfaces VSS

<dl>

[**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a>Nuevas enumeraciones de VSS

<dl>

[**\_\_Opciones de hardware de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[**\_error de protección de VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[**\_nivel de protección de VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a>Nuevas estructuras de VSS

<dl>

[**\_información de \_ protección de volumen de VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a>Modificaciones de la enumeración de VSS existentes

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Enumeración de esquema de copia de seguridad
</dt> <dd>

<dl> <dt>

<span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Valor agregado:
</dt> <dd>

VSS \_ BS \_ Writer \_ admite \_ \_ restauraciones en paralelo

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeración de [**\_ \_ atributos de \_ instantánea \_ de volumen de VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

postinstantánea de \_ atributo VOLSNAP de VSS de VSS \_ \_ \_

\_recuperación de \_ TxF de atributo VOLSNAP \_ de VSS \_

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a>Modificaciones de la interfaz de VSS existentes

<dl> <dt>

<span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>Interfaz [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
</dt> <dd>

<dl> <dt>

<span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Método agregado:
</dt> <dd>

[**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a>Nuevos escritores de VSS

Windows Server 2008 y Windows Vista con SP1 presentan los siguientes escritores de VSS:

-   Escritor de configuración de IIS
-   Escritor de metabase de IIS
-   VSS Writer de NPS
-   VSS Writer de puerta de enlace de Servicios de Escritorio remoto (Terminal Services)
-   Escritor de VSS para licencias de Servicios de Escritorio remoto (Terminal Services)

Estos escritores están documentados en [escritores de VSS en la caja](in-box-vss-writers.md).

 

 



