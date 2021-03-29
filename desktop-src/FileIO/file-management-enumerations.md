---
description: Enumeraciones usadas en la administración de archivos.
ms.assetid: 14b1cfff-5e47-4309-8e62-fb5c8da9ce97
title: Enumeraciones de administración de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b53d8f53bf9dbe16c15d21171e52ea3dd0015d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002863"
---
# <a name="file-management-enumerations"></a>Enumeraciones de administración de archivos

Las enumeraciones siguientes se usan en la administración de archivos.

## <a name="in-this-section"></a>En esta sección



| Enumeración                                                                   | Descripción                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Fase de copia de COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_copy_phase)<br/>             | Indica la fase de una copia en el momento de un error.<br/>                                                                                                                                                                           |
| [**\_Acción del mensaje COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_action)<br/>     | Devuelto por la función de devolución de llamada [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) para indicar qué acción se debe realizar para la operación de copia pendiente.<br/>                                                             |
| [**\_Tipo de mensaje COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_type)<br/>         | Indica el tipo de mensaje que se pasa en la estructura del [**\_ mensaje COPYFILE2**](/windows/desktop/api/WinBase/ns-winbase-copyfile2_message) a la función de devolución de llamada [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) .<br/>                                       |
| [**\_operación de control de CSV \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-csv_control_op)<br/>                         | Especifica el tipo de operación de control de CSV que se va a usar con el código de control de [**\_ \_ control CSV de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control) .<br/>                                                                                                       |
| [**\_tipo de ID. de archivo \_**](/windows/desktop/api/WinBase/ne-winbase-file_id_type)<br/>                             | Discriminador de la Unión en la estructura del [**\_ \_ descriptor de ID**](/windows/desktop/api/WinBase/ns-winbase-file_id_descriptor) . de archivo.<br/>                                                                                                                                 |
| [**\_información \_ de archivo \_ por \_ clase de identificador**](/windows/win32/api/minwinbase/ne-minwinbase-file_info_by_handle_class)<br/> | Identifica el tipo de información de archivo que [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) debe recuperar o [**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle) debe establecer.<br/>                |
| [**\_niveles de información de FINDEX \_**](/windows/win32/api/minwinbase/ne-minwinbase-findex_info_levels)<br/>             | Define los valores que se utilizan con la función [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) para especificar el nivel de información de los datos devueltos.<br/>                                                                                 |
| [**\_operaciones de búsqueda de FINDEX \_**](/windows/win32/api/minwinbase/ne-minwinbase-findex_search_ops)<br/>               | Define los valores que se usan con la función [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) para especificar el tipo de filtrado que se va a realizar.<br/>                                                                                           |
| [**OBTENER \_ \_ los niveles de información de FILEEX \_**](/windows/win32/api/minwinbase/ne-minwinbase-get_fileex_info_levels)<br/>        | Define los valores que se usan con las funciones [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) y [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda) para especificar el nivel de información de los datos devueltos.<br/> |
| [**sugerencia de prioridad \_**](/windows/desktop/api/WinBase/ne-winbase-priority_hint)<br/>                            | Define los valores que se utilizan con la estructura de información de la [**sugerencia de prioridad de e/s de archivo \_ \_ \_ \_**](/windows/desktop/api/WinBase/ns-winbase-file_io_priority_hint_info) para especificar la sugerencia de prioridad para una operación de e/s de archivo.<br/>                                                      |
| [**\_niveles de información de secuencia \_**](/windows/desktop/api/fileapi/ne-fileapi-stream_info_levels)<br/>                 | Define los valores que se utilizan con la función [**FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) para especificar el nivel de información de los datos devueltos.<br/>                                                                               |



 

 

