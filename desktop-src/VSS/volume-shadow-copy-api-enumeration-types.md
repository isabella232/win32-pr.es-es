---
description: Las enumeraciones siguientes se definen en la API de instantáneas de volumen.
ms.assetid: f2f09791-b17e-4f54-9d29-83a4189bffc1
title: Enumeraciones de Api de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451aec8bf8ef95f8ac86d6a0b496a3205c90d94215cecd044707af5502e50b79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866185"
---
# <a name="volume-shadow-copy-api-enumerations"></a>Enumeraciones de Api de instantáneas de volumen

Las enumeraciones siguientes se definen en la API de instantáneas de volumen.



| Nombre                                                                           | Descripción                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VSS \_ ALTERNATE \_ WRITER \_ STATE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_alternate_writer_state)            | Define el conjunto de estados válidos utilizados para indicar si un escritor tiene un escritor alternativo asociado.                                                              |
| [**NIVEL DE APLICACIÓN \_ DE \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_application_level)                       | Define el conjunto de niveles de aplicación válidos.                                                                                                                       |
| [**ESQUEMA DE COPIA \_ DE SEGURIDAD DE \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)                               | Define el conjunto de esquemas de copia de seguridad: operaciones en las que puede participar un escritor.                                                                                          |
| [**TIPO DE COPIA DE SEGURIDAD DE VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)                                   | Define el conjunto de tipos de copia de seguridad.                                                                                                                                   |
| [**MARCAS DE COMPONENTES \_ \_ DE VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)                           | Indica la compatibilidad con la recuperación automática.                                                                                                                               |
| [**TIPO DE COMPONENTE DE VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)                             | Define el conjunto de tipos de componentes.                                                                                                                                |
| [**ESTADO DE \_ RESTAURACIÓN DE \_ ARCHIVOS DE VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_file_restore_status)                  | Define el conjunto de estados de una operación de restauración de archivos.                                                                                                           |
| [**TIPO DE COPIA DE \_ SEGURIDAD DE \_ ESPECIFICACIÓN DE ARCHIVO \_ VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)             | Define el conjunto de operaciones de copia de seguridad que admiten los escritores.                                                                                                         |
| [**\_OPCIONES DE HARDWARE DE VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)                      | Define marcas LUN de instantáneas.                                                                                                                                     |
| [**TIPO DE \_ OBJETO MGMT \_ DE VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_mgmt_object_type)                        | Discriminante para la [**unión de \_ VSS MGMT \_ OBJECT \_ UNION**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001) dentro de la estructura [**\_ VSS MGMT \_ OBJECT \_ PROP.**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) |
| [**TIPO DE OBJETO DE VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_object_type)                                   | Se usa para identificar un objeto como un conjunto de instantáneas, una instantánea o un proveedor.                                                                                         |
| [**ERROR DE PROTECCIÓN DE VSS \_ \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)                         | Define el conjunto de errores de protección de instantáneas.                                                                                                                  |
| [**NIVEL DE PROTECCIÓN DE VSS \_ \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)                         | Define el conjunto de niveles de protección de instantáneas de volumen.                                                                                                           |
| [**FUNCIONALIDADES DEL PROVEEDOR DE VSS \_ \_**](/windows/desktop/api/vss/ne-vss-vss_provider_capabilities)              | Reservado para uso futuro.                                                                                                                                           |
| [**TIPO DE PROVEEDOR DE VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_provider_type)                               | Define el conjunto de tipos de proveedor.                                                                                                                                 |
| [**OPCIONES DE \_ RECUPERACIÓN DE VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)                         | Lo usa un solicitante para especificar cómo se va a realizar una operación de resincronización.                                                                               |
| [**DESTINO DE \_ RESTAURACIÓN DE VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)                             | Define el conjunto de destinos de restauración.                                                                                                                                |
| [**TIPO DE \_ RESTAURACIÓN DE VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)                                 | Define el conjunto de operaciones de restauración que se va a realizar.                                                                                                              |
| [**ENUMERACIÓN \_ RESTOREMETHOD DE VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)                     | Define el conjunto de métodos de restauración de archivos predeterminados para un escritor.                                                                                                      |
| [**VSS \_ ROLLFORWARD \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)                         | Lo usa un solicitante para indicar el tipo de operación de reversión que está a punto de realizar.                                                                         |
| [**COMPATIBILIDAD CON INSTANTÁNEAS DE VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_compatibility)             | Define el conjunto de operaciones de E/S de archivos o control de volumen que se pueden deshabilitar para un volumen que se ha copiado de forma instantánea.                                            |
| [**\_CONTEXTO DE INSTANTÁNEA DE VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)                      | Especifica cómo se va a crear, consultar o eliminar una instantánea y el grado de participación del escritor.                                                            |
| [**ESTADO DE INSTANTÁNEA DE VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)                             | Define el conjunto de estados de una operación de instantánea.                                                                                                              |
| [**TIPO DE ORIGEN DE VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)                                   | Define el conjunto de tipos de datos que un escritor puede administrar.                                                                                                         |
| [**VSS \_ SUBSCRIBE \_ MASK**](/windows/desktop/api/VsWriter/ne-vswriter-vss_subscribe_mask)                             | Define el conjunto de eventos que un escritor puede recibir.                                                                                                               |
| [**TIPO DE USO DE VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)                                     | Especifica cómo el sistema host usa los datos administrados por un escritor.                                                                                                   |
| [**\_ATRIBUTOS DE INSTANTÁNEAS \_ DE \_ VOLUMEN DE \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) | Define el conjunto de atributos de una instantánea.                                                                                                                    |
| [**ESTADO DE VSS \_ \_ WRITER**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)                                 | Define el conjunto de estados del sistema de escritura.                                                                                                                           |
| [**ENUMERACIÓN \_ VSS \_ WRITERRESTORE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)                     | Define el conjunto de condiciones en las que un escritor controlará los eventos generados durante una operación de restauración.                                                        |



 

 

 



