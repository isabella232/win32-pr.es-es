---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Novedades de VSS en Windows Server 2008 y Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ee109eec31c084dc43fb9e0cc6341f443a16e6aa06ac989a7f328d9bb3011f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006125"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a>Novedades de VSS en Windows Server 2008 y Windows Vista SP1

Windows Server 2008 y Windows Vista con Service Pack 1 (SP1) presentan los siguientes cambios en el Servicio de instantáneas de volumen.

> [!Note]  
> Todos los cambios de Windows Vista se aplican a Windows Server 2008 y Windows Vista con SP1. Para obtener más información sobre esos cambios, vea [Novedades de VSS en Windows Vista](what-s-new-in-vss-in-windows-vista.md).

 

-   [Nuevas interfaces vss](#new-vss-interfaces)
-   [Nuevas enumeraciones de VSS](#new-vss-enumerations)
-   [Nuevas estructuras de VSS](#new-vss-structures)
-   [Modificaciones de enumeración de VSS existentes](#existing-vss-enumeration-modifications)
-   [Modificaciones existentes de la interfaz de VSS](#existing-vss-interface-modifications)
-   [Nuevos vss writers](#new-vss-writers)

## <a name="new-vss-interfaces"></a>Nuevas interfaces vss

<dl>

[**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a>Nuevas enumeraciones de VSS

<dl>

[**\_OPCIONES DE HARDWARE DE VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[**ERROR DE \_ VSS \_ PROTECTION**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[**NIVEL DE PROTECCIÓN DE VSS \_ \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a>Nuevas estructuras de VSS

<dl>

[**INFORMACIÓN DE PROTECCIÓN \_ POR \_ VOLUMEN DE \_ VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a>Modificaciones de enumeración de VSS existentes

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ BACKUP \_ SCHEMA (enumeración)**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Valor agregado:
</dt> <dd>

VSS \_ BS \_ WRITER ADMITE \_ \_ \_ RESTAURACIONES PARALELAS

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ ENUMERACIÓN \_ DE ATRIBUTOS DE \_ INSTANTÁNEAS DE VOLUMEN \_ DE VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ DELAYED \_ POSTSNAPSHOT

RECUPERACIÓN DE TXF DE VSS \_ VOLSNAP \_ ATTR \_ \_

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a>Modificaciones existentes de la interfaz de VSS

<dl> <dt>

<span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2 (interfaz)**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
</dt> <dd>

<dl> <dt>

<span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Método agregado:
</dt> <dd>

[**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a>Nuevos vss writers

Windows Server 2008 y Windows Vista con SP1 presentan los siguientes vss writers:

-   Escritor de configuración de IIS
-   Escritor de metabase de IIS
-   NPS VSS Writer
-   vsS Writer de puerta de enlace de Servicios de Escritorio remoto (Terminal Services)
-   Servicios de Escritorio remoto (Terminal Services) Licencias de VSS Writer

Estos escritores se documentan en [In-Box VSS Writers](in-box-vss-writers.md).

 

 



