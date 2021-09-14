---
description: Enumeraciones usadas en la administración de archivos.
ms.assetid: 14b1cfff-5e47-4309-8e62-fb5c8da9ce97
title: Enumeraciones de administración de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b53d8f53bf9dbe16c15d21171e52ea3dd0015d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069963"
---
# <a name="file-management-enumerations"></a>Enumeraciones de administración de archivos

Las enumeraciones siguientes se usan en la administración de archivos.

## <a name="in-this-section"></a>En esta sección



| Enumeración                                                                   | Descripción                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FASE DE COPIA DE COPYFILE2 \_ \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_copy_phase)<br/>             | Indica la fase de una copia en el momento de un error.<br/>                                                                                                                                                                           |
| [**ACCIÓN DE MENSAJE \_ COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_action)<br/>     | Devuelto por la función de devolución de llamada [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) para indicar qué acción se debe realizar para la operación de copia pendiente.<br/>                                                             |
| [**COPYFILE2 \_ MESSAGE \_ TYPE**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_type)<br/>         | Indica el tipo de mensaje pasado en la [**estructura COPYFILE2 \_ MESSAGE**](/windows/desktop/api/WinBase/ns-winbase-copyfile2_message) a la función de devolución de llamada [*CopyFile2ProgressRoutine.*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine)<br/>                                       |
| [**CSV \_ CONTROL \_ OP**](/windows/desktop/api/WinIoCtl/ne-winioctl-csv_control_op)<br/>                         | Especifica el tipo de operación de control CSV que se usará con el código [**de control FSCTL \_ CSV \_ CONTROL.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control)<br/>                                                                                                       |
| [**TIPO DE \_ IDENTIFICADOR \_ DE ARCHIVO**](/windows/desktop/api/WinBase/ne-winbase-file_id_type)<br/>                             | Discriminador por la unión en la [**estructura DEL DESCRIPTOR DEL IDENTIFICADOR \_ \_ DE**](/windows/desktop/api/WinBase/ns-winbase-file_id_descriptor) ARCHIVO.<br/>                                                                                                                                 |
| [**INFORMACIÓN DE \_ ARCHIVO POR CLASE DE \_ \_ \_ IDENTIFICADOR**](/windows/win32/api/minwinbase/ne-minwinbase-file_info_by_handle_class)<br/> | Identifica el tipo de información de archivo que [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) debe recuperar o [**setFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle) debe establecer.<br/>                |
| [**NIVELES DE INFORMACIÓN \_ DE \_ FINDEX**](/windows/win32/api/minwinbase/ne-minwinbase-findex_info_levels)<br/>             | Define los valores que se usan con [**la función FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) para especificar el nivel de información de los datos devueltos.<br/>                                                                                 |
| [**OPERACIONES DE BÚSQUEDA DE FINDEX \_ \_**](/windows/win32/api/minwinbase/ne-minwinbase-findex_search_ops)<br/>               | Define los valores que se usan con [**la función FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) para especificar el tipo de filtrado que se debe realizar.<br/>                                                                                           |
| [**OBTENER NIVELES \_ DE INFORMACIÓN \_ DE \_ FILEEX**](/windows/win32/api/minwinbase/ne-minwinbase-get_fileex_info_levels)<br/>        | Define los valores que se usan con las funciones [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) y [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda) para especificar el nivel de información de los datos devueltos.<br/> |
| [**SUGERENCIA DE \_ PRIORIDAD**](/windows/desktop/api/WinBase/ne-winbase-priority_hint)<br/>                            | Define los valores que se usan con la estructura [**FILE IO PRIORITY HINT \_ \_ \_ \_ INFO**](/windows/desktop/api/WinBase/ns-winbase-file_io_priority_hint_info) para especificar la sugerencia de prioridad para una operación de E/S de archivo.<br/>                                                      |
| [**NIVELES DE \_ INFORMACIÓN DE \_ STREAMING**](/windows/desktop/api/fileapi/ne-fileapi-stream_info_levels)<br/>                 | Define los valores que se usan con [**la función FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) para especificar el nivel de información de los datos devueltos.<br/>                                                                               |



 

 

