---
description: Las siguientes funciones se usan con el registro de eventos.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Funciones de registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687380"
---
# <a name="event-logging-functions"></a><span data-ttu-id="35300-103">Funciones de registro de eventos</span><span class="sxs-lookup"><span data-stu-id="35300-103">Event Logging Functions</span></span>

<span data-ttu-id="35300-104">Las siguientes funciones se usan con el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="35300-104">The following functions are used with event logging.</span></span>



| <span data-ttu-id="35300-105">Función</span><span class="sxs-lookup"><span data-stu-id="35300-105">Function</span></span>                                                         | <span data-ttu-id="35300-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="35300-106">Description</span></span>                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35300-107">**BackupEventLog**</span><span class="sxs-lookup"><span data-stu-id="35300-107">**BackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | <span data-ttu-id="35300-108">Guarda el registro de eventos especificado en un archivo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="35300-108">Saves the specified event log to a backup file.</span></span>                                                     |
| [<span data-ttu-id="35300-109">**ClearEventLog**</span><span class="sxs-lookup"><span data-stu-id="35300-109">**ClearEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | <span data-ttu-id="35300-110">Borra el registro de eventos especificado y, opcionalmente, guarda la copia actual del registro en un archivo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="35300-110">Clears the specified event log, and optionally saves the current copy of the log to a backup file.</span></span>  |
| [<span data-ttu-id="35300-111">**CloseEventLog**</span><span class="sxs-lookup"><span data-stu-id="35300-111">**CloseEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | <span data-ttu-id="35300-112">Cierra un identificador de lectura para el registro de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="35300-112">Closes a read handle to the specified event log.</span></span>                                                    |
| [<span data-ttu-id="35300-113">**DeregisterEventSource**</span><span class="sxs-lookup"><span data-stu-id="35300-113">**DeregisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | <span data-ttu-id="35300-114">Cierra un identificador de escritura en el registro de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="35300-114">Closes a write handle to the specified event log.</span></span>                                                   |
| [<span data-ttu-id="35300-115">**GetEventLogInformation**</span><span class="sxs-lookup"><span data-stu-id="35300-115">**GetEventLogInformation**</span></span>](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | <span data-ttu-id="35300-116">Recupera información sobre el registro de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="35300-116">Retrieves information about the specified event log.</span></span>                                                |
| [<span data-ttu-id="35300-117">**GetNumberOfEventLogRecords**</span><span class="sxs-lookup"><span data-stu-id="35300-117">**GetNumberOfEventLogRecords**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | <span data-ttu-id="35300-118">Recupera el número de registros del registro de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="35300-118">Retrieves the number of records in the specified event log.</span></span>                                         |
| [<span data-ttu-id="35300-119">**GetOldestEventLogRecord**</span><span class="sxs-lookup"><span data-stu-id="35300-119">**GetOldestEventLogRecord**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | <span data-ttu-id="35300-120">Recupera el número de registro absoluto del registro más antiguo en el registro de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="35300-120">Retrieves the absolute record number of the oldest record in the specified event log.</span></span>               |
| [<span data-ttu-id="35300-121">**NotifyChangeEventLog**</span><span class="sxs-lookup"><span data-stu-id="35300-121">**NotifyChangeEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | <span data-ttu-id="35300-122">Permite a una aplicación recibir una notificación cuando se escribe un evento en el registro de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="35300-122">Enables an application to receive notification when an event is written to the specified event log.</span></span> |
| [<span data-ttu-id="35300-123">**OpenBackupEventLog**</span><span class="sxs-lookup"><span data-stu-id="35300-123">**OpenBackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | <span data-ttu-id="35300-124">Abre un identificador de un registro de eventos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="35300-124">Opens a handle to a backup event log.</span></span>                                                               |
| [<span data-ttu-id="35300-125">**OpenEventLog**</span><span class="sxs-lookup"><span data-stu-id="35300-125">**OpenEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | <span data-ttu-id="35300-126">Abre un identificador del registro de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="35300-126">Opens a handle to the specified event log.</span></span>                                                          |
| [<span data-ttu-id="35300-127">**ReadEventLog**</span><span class="sxs-lookup"><span data-stu-id="35300-127">**ReadEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | <span data-ttu-id="35300-128">Lee un número entero de entradas del registro de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="35300-128">Reads a whole number of entries from the specified event log.</span></span>                                       |
| [<span data-ttu-id="35300-129">**RegisterEventSource**</span><span class="sxs-lookup"><span data-stu-id="35300-129">**RegisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | <span data-ttu-id="35300-130">Recupera un identificador registrado en el registro de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="35300-130">Retrieves a registered handle to the specified event log.</span></span>                                           |
| [<span data-ttu-id="35300-131">**ReportEvent**</span><span class="sxs-lookup"><span data-stu-id="35300-131">**ReportEvent**</span></span>](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | <span data-ttu-id="35300-132">Escribe una entrada al final del registro de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="35300-132">Writes an entry at the end of the specified event log.</span></span>                                              |



 

 

 



