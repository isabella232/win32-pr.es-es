---
description: Códigos de control usados en la administración de archivos.
ms.assetid: e27ded4b-d104-4244-b38e-5fed10d32e1e
title: Códigos de control de administración de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cb3baf78c4066a640242afe8465592bc9a6f8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069966"
---
# <a name="file-management-control-codes"></a>Códigos de control de administración de archivos

Los siguientes códigos de control se usan en la administración de archivos.

## <a name="in-this-section"></a>En esta sección



| Código de control                                                                                    | Descripción                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ ALLOW \_ EXTENDED \_ DASD \_ IO**](/windows/win32/api/winioctl/ni-winioctl-fsctl_allow_extended_dasd_io)<br/>             | Indica al controlador del sistema de archivos que no realice ninguna comprobación de límites de E/S en las llamadas de lectura o escritura de la partición.<br/>                                                                                  |
| [**FSCTL \_ CREATE U GET OBJECT \_ \_ \_ \_ ID**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)<br/>          | Recupera el identificador de objeto para el archivo o directorio especificado. Si no existe ningún identificador de objeto, **el uso de FSCTL CREATE U \_ GET OBJECT \_ \_ \_ \_ ID** crea uno.<br/>                           |
| [**CONTROL CSV \_ DE \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control)<br/>                                     | Recupera los resultados de una operación de control CSV.<br/>                                                                                                                                        |
| [**FSCTL \_ DELETE \_ OBJECT \_ ID**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)<br/>                          | Quita el identificador de objeto de un archivo o directorio especificado.<br/>                                                                                                                        |
| [**EXTENSIONES DUPLICADAS DE FSCTL \_ \_ PARA \_ \_ ARCHIVO**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)<br/>       | Indica al sistema de archivos que copie un intervalo de bytes de archivo en nombre de una aplicación.<br/>                                                                                                     |
| [**RECORTE DE NIVEL \_ \_ DE ARCHIVO DE \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_file_level_trim)<br/>                            | Indica al sistema de almacenamiento qué intervalos del archivo no son necesarios para almacenarse.<br/>                                                                                                    |
| [**FSCTL \_ FILESYSTEM \_ GET \_ STATISTICS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics)<br/>        | Recupera la información de varios contadores de rendimiento del sistema de archivos.<br/>                                                                                                                 |
| [**FSCTL \_ FILESYSTEM \_ GET \_ STATISTICS \_ EX**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics_ex)<br/> | Recupera la información de varios contadores de rendimiento del sistema de archivos.<br/> La compatibilidad con este código de control se inició con Windows 10.<br/>                                               |
| [**FSCTL \_ FIND \_ FILES \_ BY \_ SID**](/windows/win32/api/winioctl/ni-winioctl-fsctl_find_files_by_sid)<br/>                       | Busca en un directorio un archivo cuyo propietario del creador coincide con el SID especificado.<br/>                                                                                                           |
| [**COMPRESIÓN GET \_ DE \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)<br/>                             | Recupera el estado de compresión actual de un archivo o directorio en un volumen cuyo sistema de archivos admite la compresión por secuencia.<br/>                                                            |
| [**FSCTL \_ GET \_ NTFS \_ FILE \_ RECORD**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record)<br/>                 | Recupera el primer registro de archivo que está en uso y tiene un valor ordinal menor o igual que el número de referencia de archivo solicitado.<br/>                                                    |
| [**FSCTL \_ GET \_ OBJECT \_ ID**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)<br/>                                | Recupera el identificador de objeto para el archivo o directorio especificado.<br/>                                                                                                                     |
| [**FSCTL \_ GET \_ REPAIR**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)<br/>                                       | Recupera información sobre el mecanismo de recuperación automática del sistema de archivos NTFS.<br/>                                                                                                               |
| [**REPARACIÓN DE INICIO DE FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)<br/>                             | Desencadena el sistema de archivos NTFS para iniciar un ciclo de recuperación automática en un solo archivo.<br/>                                                                                                            |
| [**FSCTL \_ MAKE \_ MEDIA \_ COMPATIBLE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)<br/>                | Cierra una sesión udF abierta en los medios de escritura una vez para que la ROM multimedia sea compatible.<br/>                                                                                                         |
| [**FSCTL \_ OPBATCH \_ ACK \_ CLOSE \_ PENDING**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)<br/>       | Notifica a un servidor que una aplicación cliente está lista para cerrar un archivo.<br/>                                                                                                                    |
| [**FSCTL \_ OPLOCK \_ BREAK \_ ACK NO \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)<br/>              | Responde a la notificación de que un bloqueo oportunista en un archivo está a punto de romperse. Use esta operación para desbloquear todos los bloqueos oportunistas del archivo, pero mantenga el archivo abierto.<br/>            |
| [**CONFIRMACIÓN DE \_ INTERRUPCIÓN DEL BLOQUEO DE OPERACIÓN \_ DE FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)<br/>          | Responde a la notificación de que un bloqueo oportunista exclusivo en un archivo está a punto de romperse. Use esta operación para indicar que el archivo debe recibir un bloqueo oportunista de nivel 2.<br/> |
| [**NOTIFICACIÓN DE \_ INTERRUPCIÓN DEL BLOQUEO \_ DE OPERACIÓN \_ DE FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)<br/>                    | Permite que la aplicación que realiza la llamada espere a que se complete una interrupción de bloqueo oportunista.<br/>                                                                                                   |
| [**INTERVALOS \_ \_ ASIGNADOS DE CONSULTA \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)<br/>              | Examina un archivo o secuencia alternativa en busca de intervalos que pueden contener datos distintos de cero.<br/>                                                                                                       |
| [**CONSULTA FSCTL \_ EN LA INFORMACIÓN DEL VOLUMEN DE \_ \_ \_ \_ DISCO**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)<br/>      | Solicita información de volumen específica de udF.<br/>                                                                                                                                                |
| [**INFORMACIÓN DE \_ LA \_ SPARING DE CONSULTA \_ DE FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)<br/>                      | Recupera las propiedades de administración de defectos del volumen. Se usa para sistemas de archivos UDF.<br/>                                                                                                     |
| [**ARCHIVO DE \_ RECUPERACIÓN DE \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_recall_file)<br/>                                     | Recupera un archivo de medios de almacenamiento que Storage administración remota, que es el software de administración de almacenamiento jerárquico.<br/>                                                                    |
| [**FSCTL \_ REQUEST \_ BATCH \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)<br/>                  | Solicita un bloqueo oportunista por lotes en un archivo.<br/>                                                                                                                                           |
| [**FSCTL \_ REQUEST \_ FILTER \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)<br/>                | Solicita un bloqueo oportunista de filtro en un archivo.<br/>                                                                                                                                          |
| [**FSCTL \_ REQUEST \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)<br/>                               | Solicita un bloqueo oportunista (oplock) en un archivo y confirma que se ha producido una interrupción del bloqueo.<br/>                                                                                    |
| [**FSCTL \_ REQUEST \_ OPLOCK LEVEL \_ \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)<br/>             | Solicita un bloqueo oportunista de nivel 1 en un archivo.<br/>                                                                                                                                         |
| [**FSCTL \_ REQUEST \_ OPLOCK LEVEL \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)<br/>             | Solicita un bloqueo oportunista de nivel 2 en un archivo.<br/>                                                                                                                                         |
| [**COMPRESIÓN DE CONJUNTO \_ DE \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                             | Establece el estado de compresión de un archivo o directorio en un volumen cuyo sistema de archivos admite la compresión por archivo y por directorio.<br/>                                                         |
| [**ADMINISTRACIÓN DE \_ DEFECTOS DEL CONJUNTO \_ DE \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)<br/>                | Establece el estado de administración de defectos de software para el archivo especificado. Se usa para sistemas de archivos UDF.<br/>                                                                                             |
| [**FSCTL \_ SET \_ OBJECT \_ ID**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)<br/>                                | Establece el identificador de objeto para el archivo o directorio especificado.<br/>                                                                                                                          |
| [**FSCTL \_ SET \_ OBJECT \_ ID \_ EXTENDED**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)<br/>             | Modifica los datos de usuario asociados al identificador de objeto para el archivo o directorio especificado.<br/>                                                                                            |
| [**FSCTL \_ SET \_ REPAIR**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)<br/>                                       | Establece el modo de la funcionalidad de recuperación automática de un sistema de archivos NTFS.<br/>                                                                                                                          |
| [**FSCTL \_ SET \_ SPARSE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)<br/>                                       | Marca el archivo indicado como disperso o no disperso. En un archivo disperso, es posible que los intervalos grandes de ceros no requieran asignación de disco.<br/>                                                               |
| [**FSCTL \_ SET \_ ZERO \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)<br/>                                | Rellena un intervalo especificado de un archivo con ceros (0).<br/>                                                                                                                                        |
| [**FSCTL \_ SET \_ ZERO \_ ON \_ DEALLOCATION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_on_deallocation)<br/>         | Indica que un identificador de archivo del sistema de archivos NTFS debe tener sus clústeres rellenos de ceros cuando se desasigna.<br/>                                                                             |
| [**FSCTL \_ WAIT \_ FOR \_ REPAIR**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)<br/>                            | Devuelve cuando se completan las reparaciones especificadas.<br/>                                                                                                                                        |



 

Los siguientes códigos de control se usan con [compresión de archivos y descompresión.](file-compression-and-decompression.md)

<dl>

[**COMPRESIÓN GET \_ DE \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)  
[**COMPRESIÓN DE CONJUNTO \_ DE \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)  
</dl>

Los siguientes códigos de control se usan con [identificadores de objeto](distributed-link-tracking-and-object-identifiers.md).

<dl>

[**FSCTL \_ CREATE U GET OBJECT \_ \_ \_ \_ ID**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)  
[**FSCTL \_ DELETE \_ OBJECT \_ ID**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)  
[**FSCTL \_ GET \_ OBJECT \_ ID**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)  
[**FSCTL \_ SET \_ OBJECT \_ ID**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)  
[**FSCTL \_ SET \_ OBJECT \_ ID \_ EXTENDED**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)  
</dl>

Los siguientes códigos de control se usan con [bloqueos oportunistas](opportunistic-locks.md).

<dl>

[**FSCTL \_ OPBATCH \_ ACK \_ CLOSE \_ PENDING**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**FSCTL \_ OPLOCK \_ BREAK \_ ACK NO \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**CONFIRMACIÓN DE \_ INTERRUPCIÓN DEL BLOQUEO DE OPERACIÓN \_ DE FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**NOTIFICACIÓN DE \_ INTERRUPCIÓN DEL BLOQUEO \_ DE OPERACIÓN \_ DE FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**FSCTL \_ REQUEST \_ BATCH \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**FSCTL \_ REQUEST \_ FILTER \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**FSCTL \_ REQUEST \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**FSCTL \_ REQUEST \_ OPLOCK LEVEL \_ \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**FSCTL \_ REQUEST \_ OPLOCK LEVEL \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

Los siguientes códigos de control se usan [con archivos dispersos](sparse-files.md).

<dl>

[**INTERVALOS \_ \_ ASIGNADOS DE CONSULTA \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)  
[**FSCTL \_ SET \_ SPARSE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)  
[**FSCTL \_ SET \_ ZERO \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)  
</dl>

Los siguientes códigos de control se usan con el mecanismo de recuperación automática de NTFS.

<dl>

[**FSCTL \_ GET \_ REPAIR**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)  
[**REPARACIÓN DE INICIO DE FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)  
[**FSCTL \_ SET \_ REPAIR**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)  
[**FSCTL \_ WAIT \_ FOR \_ REPAIR**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)  
</dl>

Los siguientes códigos de control se usan con UDF.

<dl>

[**FSCTL \_ MAKE \_ MEDIA \_ COMPATIBLE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)  
[**CONSULTA FSCTL \_ EN LA INFORMACIÓN DEL VOLUMEN DE \_ \_ \_ \_ DISCO**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)  
[**INFORMACIÓN DE \_ LA \_ SPARING DE CONSULTA \_ DE FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)  
[**ADMINISTRACIÓN DE \_ DEFECTOS DEL CONJUNTO \_ DE \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de control de administración de directorios](directory-management-control-codes.md)
</dt> <dt>

[Códigos de control de administración del volumen](volume-management-control-codes.md)
</dt> </dl>

 

