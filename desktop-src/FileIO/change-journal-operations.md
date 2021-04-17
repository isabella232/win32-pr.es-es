---
description: Códigos y estructuras de control que se usarán con el diario de cambios del número de secuencias actualizadas (USN) del sistema de archivos NTFS.
ms.assetid: 2215f0d4-6ac8-42a5-87a5-9c76d1fae3ed
title: Cambiar operaciones de diario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52cda51d0efc4cbae1333fc197f42d6a5cc0f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688475"
---
# <a name="change-journal-operations"></a><span data-ttu-id="940d5-103">Cambiar operaciones de diario</span><span class="sxs-lookup"><span data-stu-id="940d5-103">Change Journal Operations</span></span>

<span data-ttu-id="940d5-104">En la lista siguiente se identifican los códigos de control que funcionan con el diario de cambios del número de secuencias actualizadas (USN) del sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="940d5-104">The following list identifies the control codes that work with the NTFS file system update sequence number (USN) change journal.</span></span>

-   [<span data-ttu-id="940d5-105">**\_diario de creación de \_ USN de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="940d5-105">**FSCTL\_CREATE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)
-   [<span data-ttu-id="940d5-106">**\_diario de eliminación de \_ USN de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="940d5-106">**FSCTL\_DELETE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal)
-   [<span data-ttu-id="940d5-107">**\_datos de \_ USN \_ enum de FSCTL**</span><span class="sxs-lookup"><span data-stu-id="940d5-107">**FSCTL\_ENUM\_USN\_DATA**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)
-   [<span data-ttu-id="940d5-108">**\_identificador de marca de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="940d5-108">**FSCTL\_MARK\_HANDLE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_mark_handle)
-   [<span data-ttu-id="940d5-109">**\_diario de \_ USN de consulta de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="940d5-109">**FSCTL\_QUERY\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)
-   [<span data-ttu-id="940d5-110">**\_diario de lectura de \_ USN de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="940d5-110">**FSCTL\_READ\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal)

<span data-ttu-id="940d5-111">La lista siguiente identifica la información de estructuras relacionada con el diario de cambios USN del sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="940d5-111">The following list identifies the structures information that relates to the NTFS file system USN change journal.</span></span>

-   [<span data-ttu-id="940d5-112">**CREAR \_ \_ datos de diario USN \_**</span><span class="sxs-lookup"><span data-stu-id="940d5-112">**CREATE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data)
-   [<span data-ttu-id="940d5-113">**ELIMINAR \_ \_ datos de diario USN \_**</span><span class="sxs-lookup"><span data-stu-id="940d5-113">**DELETE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-delete_usn_journal_data)
-   [<span data-ttu-id="940d5-114">**MARCAR \_ información de identificador \_**</span><span class="sxs-lookup"><span data-stu-id="940d5-114">**MARK\_HANDLE\_INFO**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mark_handle_info)
-   [<span data-ttu-id="940d5-115">**\_datos de enumeración de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="940d5-115">**MFT\_ENUM\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mft_enum_data_v0)
-   [<span data-ttu-id="940d5-116">**LEER \_ \_ datos del diario USN \_**</span><span class="sxs-lookup"><span data-stu-id="940d5-116">**READ\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0)
-   [<span data-ttu-id="940d5-117">**\_datos de diario USN \_**</span><span class="sxs-lookup"><span data-stu-id="940d5-117">**USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0)
-   [<span data-ttu-id="940d5-118">**\_registro USN**</span><span class="sxs-lookup"><span data-stu-id="940d5-118">**USN\_RECORD**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)

 

 
