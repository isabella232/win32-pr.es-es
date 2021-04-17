---
description: Las enumeraciones siguientes se definen en la API de instantáneas de volumen.
ms.assetid: f2f09791-b17e-4f54-9d29-83a4189bffc1
title: Enumeraciones de la API de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ade0af4637e9c057c9743dfaf0778e86b3d81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696482"
---
# <a name="volume-shadow-copy-api-enumerations"></a>Enumeraciones de la API de instantáneas de volumen

Las enumeraciones siguientes se definen en la API de instantáneas de volumen.



| Nombre                                                                           | Descripción                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Estado de \_ escritor \_ alternativo de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_alternate_writer_state)            | Define el conjunto de Estados válidos que se usa para indicar si un escritor tiene un escritor alternativo asociado.                                                              |
| [**\_nivel de aplicación de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_application_level)                       | Define el conjunto de niveles de aplicación válidos.                                                                                                                       |
| [**esquema de copia de seguridad de VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)                               | Define el conjunto de esquemas de copia de seguridad: las operaciones en las que puede participar un escritor.                                                                                          |
| [**tipo de copia de seguridad de VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)                                   | Define el conjunto de tipos de copia de seguridad.                                                                                                                                   |
| [**\_marcas de componentes de VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)                           | Indica compatibilidad con la recuperación automática.                                                                                                                               |
| [**\_tipo de componente de VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)                             | Define el conjunto de tipos de componente.                                                                                                                                |
| [**\_Estado de \_ restauración de archivos VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_file_restore_status)                  | Define el conjunto de Estados de una operación de restauración de archivos.                                                                                                           |
| [**\_tipo de \_ copia de seguridad de especificación de archivo VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)             | Define el conjunto de operaciones de copia de seguridad admitidas por escritores.                                                                                                         |
| [**\_\_Opciones de hardware de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)                      | Define las marcas de LUN de instantánea.                                                                                                                                     |
| [**\_tipo de \_ objeto de administración de VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_mgmt_object_type)                        | Discriminante para la Unión de [**\_ \_ objetos \_ de administración de VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001) en la estructura [**\_ \_ \_ Prop del objeto de administración de VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) . |
| [**\_tipo de objeto de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_object_type)                                   | Se usa para identificar un objeto como un conjunto de instantáneas, una instantánea o un proveedor.                                                                                         |
| [**\_error de protección de VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)                         | Define el conjunto de errores de protección de instantáneas.                                                                                                                  |
| [**\_nivel de protección de VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)                         | Define el conjunto de niveles de protección de instantáneas de volumen.                                                                                                           |
| [**\_capacidades del proveedor de VSS \_**](/windows/desktop/api/vss/ne-vss-vss_provider_capabilities)              | Reservado para uso futuro.                                                                                                                                           |
| [**\_tipo de proveedor de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_provider_type)                               | Define el conjunto de tipos de proveedor.                                                                                                                                 |
| [**\_Opciones de recuperación de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)                         | Lo utiliza un solicitante para especificar cómo se va a realizar una operación de resincronización.                                                                               |
| [**\_destino de restauración de VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)                             | Define el conjunto de destinos de restauración.                                                                                                                                |
| [**\_tipo de restauración de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)                                 | Define el conjunto de operaciones de restauración que se va a realizar.                                                                                                              |
| [**\_enumeración RESTOREMETHOD de VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)                     | Define el conjunto de métodos de restauración de archivos predeterminados para un escritor.                                                                                                      |
| [**tipo de puesta al día de VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)                         | Lo utiliza un solicitante para indicar el tipo de operación de puesta al día que se va a realizar.                                                                         |
| [**\_compatibilidad con instantáneas de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_compatibility)             | Define el conjunto de operaciones de control de volumen o de e/s de archivos que se pueden deshabilitar para un volumen del que se ha realizado una copia sombra.                                            |
| [**\_\_contexto de instantánea de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)                      | Especifica cómo se va a crear, consultar o eliminar una instantánea y el grado de implicación del escritor.                                                            |
| [**\_Estado de instantánea de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)                             | Define el conjunto de Estados de una operación de instantánea.                                                                                                              |
| [**\_tipo de origen de VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)                                   | Define el conjunto de tipos de datos que puede administrar un escritor.                                                                                                         |
| [**\_máscara de suscripción de VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_subscribe_mask)                             | Define el conjunto de eventos que puede recibir un escritor.                                                                                                               |
| [**\_tipo de uso de VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)                                     | Especifica cómo utiliza el sistema host los datos administrados por un escritor.                                                                                                   |
| [**\_\_atributos de \_ instantáneas de volumen de VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) | Define el conjunto de atributos de una instantánea.                                                                                                                    |
| [**Estado de VSS \_ Writer \_**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)                                 | Define el conjunto de Estados del escritor.                                                                                                                           |
| [**\_enumeración WRITERRESTORE de VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)                     | Define el conjunto de condiciones bajo las que un escritor controlará los eventos generados durante una operación de restauración.                                                        |



 

 

 



