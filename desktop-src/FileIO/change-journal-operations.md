---
description: Códigos de control y estructuras que se usarán con el diario de cambios de número de secuencia de actualización del sistema de archivos NTFS (USN).
ms.assetid: 2215f0d4-6ac8-42a5-87a5-9c76d1fae3ed
title: Operaciones de diario de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87177bc636771c1a02b22fc8ad74cf4c16294e7a3b02e8a366c22c346f511f9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766085"
---
# <a name="change-journal-operations"></a>Operaciones de diario de cambios

En la lista siguiente se identifican los códigos de control que funcionan con el diario de cambios número de secuencia de actualización del sistema de archivos NTFS (USN).

-   [**FSCTL \_ CREATE \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)
-   [**FSCTL \_ DELETE \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal)
-   [**DATOS DE \_ USN DE ENUMERACIÓN DE \_ \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)
-   [**IDENTIFICADOR DE \_ MARCA \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_mark_handle)
-   [**FSCTL \_ QUERY \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)
-   [**FSCTL \_ READ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal)

En la lista siguiente se identifica la información de estructuras relacionada con el diario de cambios USN del sistema de archivos NTFS.

-   [**CREACIÓN DE \_ DATOS DE DIARIO DE USN \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data)
-   [**ELIMINACIÓN \_ DE DATOS DEL DIARIO DE USN \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-delete_usn_journal_data)
-   [**MARCAR INFORMACIÓN \_ DE \_ IDENTIFICADOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-mark_handle_info)
-   [**DATOS DE ENUMERACIÓN DE MFT \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-mft_enum_data_v0)
-   [**LEER \_ DATOS DEL DIARIO DE USN \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0)
-   [**DATOS DEL DIARIO DE USN \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0)
-   [**REGISTRO \_ DE USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)

 

 
