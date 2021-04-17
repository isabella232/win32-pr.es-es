---
description: Estructuras NTFS (TxF) transaccionales.
ms.assetid: 85b3cf8e-bff3-4693-b00e-64bf5d1f5065
title: Estructuras TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d490f608ef9ebfa6906d1acffa374a0c9327489b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666703"
---
# <a name="txf-structures"></a>Estructuras TxF

NTFS transaccional (TxF) proporciona las siguientes estructuras.

## <a name="in-this-section"></a>En esta sección



| Estructura                                                                                                    | Descripción                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TXFS \_ crear \_ información de miniversión \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_create_miniversion_info)<br/>                           | Contiene la información de versión sobre la miniversión creada por [**FSCTL \_ TXFS \_ Create \_ miniversión**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion).<br/>                                            |
| [**TXFS \_ obtener \_ información de metadatos de \_ \_ salida**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_metadata_info_out)<br/>                              | Contiene la información de versión sobre la miniversión que se crea.<br/>                                                                                                                 |
| [**identificador de TXF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_id)<br/>                                                                         | Representa un identificador único en el contexto de la Administrador de recursos.<br/>                                                                                                              |
| [**TXFS \_ obtener \_ versión de transacción \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version)<br/>                             | Contiene la información sobre la base y las versiones más recientes del archivo especificado.<br/>                                                                                                      |
| [**TXFS \_ lista \_ de \_ archivos bloqueados de transacciones \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files)<br/>              | Contiene una lista de archivos bloqueados por un escritor de transacciones.<br/>                                                                                                                                 |
| [**TXFS \_ Mostrar la \_ entrada de archivos de transacción \_ bloqueada \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files_entry)<br/> | Contiene información sobre una transacción bloqueada.<br/>                                                                                                                                        |
| [**transacciones de la \_ lista TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions)<br/>                                        | Contiene una lista de transacciones.<br/>                                                                                                                                                        |
| [**entrada de transacciones de la \_ lista TXFS \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions_entry)<br/>                           | Contiene información sobre una transacción.<br/>                                                                                                                                               |
| [**\_ \_ \_ archivo afectado de registro \_ de TxF**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_affected_file)<br/>                          | Contiene información de un archivo que se ve afectado por una transacción.<br/>                                                                                                                     |
| [**\_base de \_ registro de TxF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_base)<br/>                                             | Contiene la información de registro básica.<br/>                                                                                                                                                  |
| [**\_truncamiento de \_ registro de TxF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_truncate)<br/>                                     | Contiene el registro para una operación de truncamiento.<br/>                                                                                                                                           |
| [**\_escritura de \_ registro de TxF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_write)<br/>                                           | Contiene el registro de una operación de escritura.<br/>                                                                                                                                              |
| [**TXFS \_ modificar \_ RM**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_modify_rm)<br/>                                                        | Contiene la información necesaria para modificar los parámetros de registro y el modo de registro para un administrador de recursos secundario.<br/>                                                                      |
| [**TXFS \_ consultar \_ información de RM \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_query_rm_information)<br/>                                 | Contiene información sobre el administrador de recursos (RM).<br/>                                                                                                                                   |
| [**TXFS \_ leer \_ información de copia de seguridad \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/>                  | Contiene una estructura específica NTFS transaccional (TxF). Esta información solo se debe usar al llamar a la [**\_ información de copia de \_ seguridad \_ de TXFS Write**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information).<br/>    |
| [**TXFS \_ información de punto de retorno \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)<br/>                                | La estructura de [**\_ información de punto de \_ retorno \_ de FSCTL TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information) especifica la acción que se va a realizar y en qué transacción.<br/>                                      |
| [**\_ \_ información activa de la transacción TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_transaction_active_info)<br/>                           | Contiene la marca que indica si las transacciones estaban activas o no cuando se tomó una instantánea.<br/>                                                                                     |
| [**TXFS \_ escribir \_ información de copia de seguridad \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>                         | Contiene una estructura específica NTFS transaccional (TxF). Esta información solo se debe usar al llamar a la [**\_ información de copia de \_ seguridad \_ de TXFS Write**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out).<br/> |



 

 

