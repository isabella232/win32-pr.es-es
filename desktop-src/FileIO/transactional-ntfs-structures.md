---
description: Estructuras NTFS transaccionales (TxF).
ms.assetid: 85b3cf8e-bff3-4693-b00e-64bf5d1f5065
title: Estructuras txf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d490f608ef9ebfa6906d1acffa374a0c9327489b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069819"
---
# <a name="txf-structures"></a>Estructuras txf

NTFS transaccional (TxF) proporciona las siguientes estructuras.

## <a name="in-this-section"></a>En esta sección



| Estructura                                                                                                    | Descripción                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TXFS \_ CREATE \_ MINIVERSION \_ INFO**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_create_miniversion_info)<br/>                           | Contiene la información de versión sobre la miniversión creada por [**FSCTL \_ TXFS \_ CREATE \_ MINIVERSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion).<br/>                                            |
| [**TXFS \_ GET \_ METADATA \_ INFO \_ OUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_metadata_info_out)<br/>                              | Contiene la información de versión sobre la miniversión que se crea.<br/>                                                                                                                 |
| [**Identificador de \_ TXF**](/windows/desktop/api/TxfW32/ns-txfw32-txf_id)<br/>                                                                         | Representa un identificador único dentro del contexto del Resource Manager.<br/>                                                                                                              |
| [**TXFS \_ GET \_ TRANSACTED \_ VERSION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version)<br/>                             | Contiene la información sobre la base y las versiones más recientes del archivo especificado.<br/>                                                                                                      |
| [**LISTA DE ARCHIVOS \_ \_ BLOQUEADOS DE \_ TRANSACCIONES DE \_ TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files)<br/>              | Contiene una lista de archivos bloqueados por un escritor de transacciones.<br/>                                                                                                                                 |
| [**ENTRADA DE ARCHIVOS \_ \_ BLOQUEADOS DE LA LISTA \_ DE \_ \_ TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files_entry)<br/> | Contiene información sobre una transacción bloqueada.<br/>                                                                                                                                        |
| [**TXFS \_ LIST \_ TRANSACTIONS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions)<br/>                                        | Contiene una lista de transacciones.<br/>                                                                                                                                                        |
| [**ENTRADA TXFS \_ LIST \_ TRANSACTIONS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions_entry)<br/>                           | Contiene información sobre una transacción.<br/>                                                                                                                                               |
| [**ARCHIVO AFECTADO DE \_ \_ REGISTRO DE \_ TXF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_affected_file)<br/>                          | Contiene información de un archivo afectado por una transacción.<br/>                                                                                                                     |
| [**BASE DE REGISTROS DE TXF \_ \_ \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_base)<br/>                                             | Contiene la información básica del registro.<br/>                                                                                                                                                  |
| [**TRUNCAMIENTO DE \_ LA ENTRADA DE REGISTRO \_ \_ DE TXF**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_truncate)<br/>                                     | Contiene el registro de una operación de truncamiento.<br/>                                                                                                                                           |
| [**ESCRITURA DE REGISTROS \_ \_ TXF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_write)<br/>                                           | Contiene el registro de una operación de escritura.<br/>                                                                                                                                              |
| [**TXFS \_ MODIFY \_ RM**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_modify_rm)<br/>                                                        | Contiene la información necesaria al modificar los parámetros de registro y el modo de registro de un administrador de recursos secundario.<br/>                                                                      |
| [**INFORMACIÓN DE \_ RM DE CONSULTA DE \_ \_ TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_query_rm_information)<br/>                                 | Contiene información sobre el administrador de recursos (RM).<br/>                                                                                                                                   |
| [**TXFS \_ READ \_ BACKUP \_ INFORMATION \_ OUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/>                  | Contiene una estructura específica ntfs transaccional (TxF). Esta información solo debe usarse al llamar a [**TXFS \_ WRITE BACKUP \_ \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information).<br/>    |
| [**INFORMACIÓN DE TXFS \_ \_ SAVEPOINT**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)<br/>                                | La [**estructura FSCTL \_ TXFS \_ SAVEPOINT \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information) especifica la acción que se va a realizar y en qué transacción.<br/>                                      |
| [**INFORMACIÓN ACTIVA DE \_ TRANSACCIÓN \_ DE TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_transaction_active_info)<br/>                           | Contiene la marca que indica si las transacciones estaban activas o no cuando se tomó una instantánea.<br/>                                                                                     |
| [**INFORMACIÓN DE COPIA DE \_ SEGURIDAD DE ESCRITURA DE \_ \_ TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>                         | Contiene una estructura específica ntfs transaccional (TxF). Esta información solo debe usarse al llamar a [**TXFS \_ WRITE BACKUP \_ \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out).<br/> |



 

 

