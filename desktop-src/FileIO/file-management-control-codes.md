---
description: Códigos de control usados en la administración de archivos.
ms.assetid: e27ded4b-d104-4244-b38e-5fed10d32e1e
title: Códigos de control de administración de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cb3baf78c4066a640242afe8465592bc9a6f8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912861"
---
# <a name="file-management-control-codes"></a>Códigos de control de administración de archivos

Los siguientes códigos de control se usan en la administración de archivos.

## <a name="in-this-section"></a>En esta sección



| Código de control                                                                                    | Descripción                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ permitir \_ \_ \_ e/s de DASD extendida**](/windows/win32/api/winioctl/ni-winioctl-fsctl_allow_extended_dasd_io)<br/>             | Indica al controlador del sistema de archivos que no realice comprobaciones de límite de e/s en las llamadas de lectura o escritura de la partición.<br/>                                                                                  |
| [**\_ \_ identificador de objeto de creación u \_ obtención de \_ FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)<br/>          | Recupera el identificador de objeto para el archivo o directorio especificado. Si no existe ningún identificador de objeto, al usar **FSCTL \_ Create \_ u \_ obtener el \_ \_ ID. de objeto** se crea uno.<br/>                           |
| [**\_control CSV de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control)<br/>                                     | Recupera los resultados de una operación de control de CSV.<br/>                                                                                                                                        |
| [**\_ \_ ID. de objeto de eliminación de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)<br/>                          | Quita el identificador de objeto de un archivo o directorio especificado.<br/>                                                                                                                        |
| [**\_elementos duplicados \_ \_ de extensiones de FSCTL en el \_ archivo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)<br/>       | Indica al sistema de archivos que copie un intervalo de bytes de archivo en nombre de una aplicación.<br/>                                                                                                     |
| [**recorte de \_ nivel de archivo FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_file_level_trim)<br/>                            | Indica al sistema de almacenamiento qué intervalos del archivo no es necesario almacenar.<br/>                                                                                                    |
| [**\_ \_ obtener estadísticas del sistema de archivos FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics)<br/>        | Recupera la información de varios contadores de rendimiento del sistema de archivos.<br/>                                                                                                                 |
| [**\_sistema de archivos FSCTL \_ obtener \_ estadísticas \_ ex**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics_ex)<br/> | Recupera la información de varios contadores de rendimiento del sistema de archivos.<br/> Compatibilidad con este código de control iniciado con Windows 10.<br/>                                               |
| [**FSCTL \_ Buscar \_ archivos \_ por \_ SID**](/windows/win32/api/winioctl/ni-winioctl-fsctl_find_files_by_sid)<br/>                       | Busca un directorio para un archivo cuyo propietario de creador coincide con el SID especificado.<br/>                                                                                                           |
| [**compresión de FSCTL \_ obtener \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)<br/>                             | Recupera el estado de compresión actual de un archivo o directorio en un volumen cuyo sistema de archivos admite la compresión por secuencia.<br/>                                                            |
| [**\_registro de \_ \_ archivos NTFS obtención de \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record)<br/>                 | Recupera el primer registro de archivo que está en uso y tiene un valor ordinal menor o igual que el número de referencia de archivo solicitado.<br/>                                                    |
| [**\_identificador de \_ objeto de obtención de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)<br/>                                | Recupera el identificador de objeto para el archivo o directorio especificado.<br/>                                                                                                                     |
| [**Cómo \_ obtener \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)<br/>                                       | Recupera información sobre el mecanismo de recuperación automática del sistema de archivos NTFS.<br/>                                                                                                               |
| [**FSCTL \_ iniciar \_ reparación**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)<br/>                             | Desencadena el sistema de archivos NTFS para iniciar un ciclo de recuperación automática en un único archivo.<br/>                                                                                                            |
| [**FSCTL \_ hacer \_ \_ compatible con medios**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)<br/>                | Cierra una sesión de UDF abierta en un medio de escritura de una vez para que la ROM de medios sea compatible.<br/>                                                                                                         |
| [**el \_ cierre de ACK OPBATCH de FSCTL está \_ \_ \_ pendiente**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)<br/>       | Notifica a un servidor que una aplicación cliente está lista para cerrar un archivo.<br/>                                                                                                                    |
| [**\_Confirmación de interrupción de bloqueo oportunista \_ \_ \_ no \_ 2 de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)<br/>              | Responde a la notificación de que un bloqueo oportunista en un archivo está a punto de ser interrumpido. Use esta operación para desbloquear todos los bloqueos oportunistas en el archivo, pero mantenga abierto el archivo.<br/>            |
| [**\_confirmación de interrupción de bloqueo oportunista de FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)<br/>          | Responde a la notificación de que un bloqueo oportunista exclusivo en un archivo está a punto de ser interrumpido. Use esta operación para indicar que el archivo debe recibir un bloqueo oportunista de nivel 2.<br/> |
| [**\_notificación de interrupción de bloqueo oportunista de FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)<br/>                    | Permite que la aplicación que realiza la llamada espere a que finalice una interrupción del bloqueo oportunista.<br/>                                                                                                   |
| [**\_ \_ intervalos asignados de consulta de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)<br/>              | Examina un archivo o una secuencia alternativa buscando rangos que pueden contener datos distintos de cero.<br/>                                                                                                       |
| [**\_consulta \_ de FSCTL \_ en \_ información de volumen de disco \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)<br/>      | Solicita información de volumen específica de UDF.<br/>                                                                                                                                                |
| [**\_información de \_ reserva de consulta de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)<br/>                      | Recupera las propiedades de administración de defectos del volumen. Se usa para sistemas de archivos UDF.<br/>                                                                                                     |
| [**\_archivo de recuperación de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_recall_file)<br/>                                     | Recupera un archivo de medios de almacenamiento administrados por el almacenamiento remoto, que es el software de administración de almacenamiento jerárquico.<br/>                                                                    |
| [**\_ \_ bloqueo oportunista de batch de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)<br/>                  | Solicita un bloqueo oportunista de batch en un archivo.<br/>                                                                                                                                           |
| [**\_ \_ bloqueo oportunista de filtro de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)<br/>                | Solicita un bloqueo oportunista de filtro en un archivo.<br/>                                                                                                                                          |
| [**\_bloqueo oportunista de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)<br/>                               | Solicita un bloqueo oportunista (oportunista) en un archivo y confirma que se ha producido una interrupción de bloqueo oportunista.<br/>                                                                                    |
| [**\_ \_ \_ Nivel 1 de bloqueo oportunista de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)<br/>             | Solicita un bloqueo oportunista de nivel 1 en un archivo.<br/>                                                                                                                                         |
| [**\_Nivel 2 de solicitud de \_ bloqueo oportunista de \_ FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)<br/>             | Solicita un bloqueo oportunista de nivel 2 en un archivo.<br/>                                                                                                                                         |
| [**\_configuración de \_ compresión de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                             | Establece el estado de compresión de un archivo o directorio en un volumen cuyo sistema de archivos admite la compresión por archivo y por directorio.<br/>                                                         |
| [**\_configuración de \_ Administración de defectos de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)<br/>                | Establece el estado de administración de defectos de software para el archivo especificado. Se usa para sistemas de archivos UDF.<br/>                                                                                             |
| [**\_identificador de \_ objeto de conjunto de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)<br/>                                | Establece el identificador de objeto para el archivo o directorio especificado.<br/>                                                                                                                          |
| [**identificador de objeto de conjunto de FSCTL \_ \_ \_ \_ extendido**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)<br/>             | Modifica los datos de usuario asociados al identificador de objeto para el archivo o directorio especificado.<br/>                                                                                            |
| [**configuración de la reparación de FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)<br/>                                       | Establece el modo de la capacidad de recuperación automática del sistema de archivos NTFS.<br/>                                                                                                                          |
| [**FSCTL \_ set \_ Sparse**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)<br/>                                       | Marca el archivo indicado como disperso o no disperso. En un archivo disperso, es posible que los intervalos grandes de ceros no requieran la asignación de disco.<br/>                                                               |
| [**FSCTL \_ establecer \_ \_ datos cero**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)<br/>                                | Rellena un intervalo especificado de un archivo con ceros (0).<br/>                                                                                                                                        |
| [**FSCTL \_ set \_ Zero \_ on \_ desasignación**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_on_deallocation)<br/>         | Indica que un identificador de archivo del sistema de archivos NTFS debe tener sus clústeres rellenados con ceros cuando se cancela la asignación.<br/>                                                                             |
| [**\_espera \_ de \_ reparación de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)<br/>                            | Devuelve cuando se completan las reparaciones especificadas.<br/>                                                                                                                                        |



 

Los siguientes códigos de control se usan con la [compresión y descompresión de archivos](file-compression-and-decompression.md).

<dl>

[**compresión de FSCTL \_ obtener \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)  
[**\_configuración de \_ compresión de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)  
</dl>

Los siguientes códigos de control se utilizan con [identificadores de objeto](distributed-link-tracking-and-object-identifiers.md).

<dl>

[**\_ \_ identificador de objeto de creación u \_ obtención de \_ FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)  
[**\_ \_ ID. de objeto de eliminación de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)  
[**\_identificador de \_ objeto de obtención de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)  
[**\_identificador de \_ objeto de conjunto de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)  
[**identificador de objeto de conjunto de FSCTL \_ \_ \_ \_ extendido**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)  
</dl>

Los siguientes códigos de control se usan con [bloqueos oportunistas](opportunistic-locks.md).

<dl>

[**el \_ cierre de ACK OPBATCH de FSCTL está \_ \_ \_ pendiente**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**\_Confirmación de interrupción de bloqueo oportunista \_ \_ \_ no \_ 2 de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**\_confirmación de interrupción de bloqueo oportunista de FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**\_notificación de interrupción de bloqueo oportunista de FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**\_ \_ bloqueo oportunista de batch de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**\_ \_ bloqueo oportunista de filtro de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**\_bloqueo oportunista de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**\_ \_ \_ Nivel 1 de bloqueo oportunista de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**\_Nivel 2 de solicitud de \_ bloqueo oportunista de \_ FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

Los siguientes códigos de control se utilizan con [archivos dispersos](sparse-files.md).

<dl>

[**\_ \_ intervalos asignados de consulta de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)  
[**FSCTL \_ set \_ Sparse**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)  
[**FSCTL \_ establecer \_ \_ datos cero**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)  
</dl>

Los siguientes códigos de control se utilizan con el mecanismo de recuperación automática de NTFS.

<dl>

[**Cómo \_ obtener \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)  
[**FSCTL \_ iniciar \_ reparación**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)  
[**configuración de la reparación de FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)  
[**\_espera \_ de \_ reparación de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)  
</dl>

Los siguientes códigos de control se usan con UDF.

<dl>

[**FSCTL \_ hacer \_ \_ compatible con medios**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)  
[**\_consulta \_ de FSCTL \_ en \_ información de volumen de disco \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)  
[**\_información de \_ reserva de consulta de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)  
[**\_configuración de \_ Administración de defectos de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de control de administración de directorios](directory-management-control-codes.md)
</dt> <dt>

[Códigos de control de administración del volumen](volume-management-control-codes.md)
</dt> </dl>

 

