---
description: Si una aplicación solicita bloqueos oportunistas, todos los archivos para los que solicita bloqueos deben abrirse para la entrada y salida superpuestas (asincrónicas) mediante la función CreateFile con la marca de la marca de archivo \_ \_ superpuesta.
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Operaciones de bloqueo oportunista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefd9b292747e89f5ebafd94cb8aa0e38833e8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545542"
---
# <a name="opportunistic-lock-operations"></a><span data-ttu-id="53e8b-103">Operaciones de bloqueo oportunista</span><span class="sxs-lookup"><span data-stu-id="53e8b-103">Opportunistic Lock Operations</span></span>

<span data-ttu-id="53e8b-104">Si una aplicación solicita bloqueos oportunistas, todos los archivos para los que solicita bloqueos deben abrirse para la entrada y salida superpuestas (asincrónicas) mediante la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con la marca de la **marca de archivo \_ \_ superpuesta** .</span><span class="sxs-lookup"><span data-stu-id="53e8b-104">If an application requests opportunistic locks, all files for which it requests locks must be opened for overlapped (asynchronous) input and output by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_OVERLAPPED** flag.</span></span> <span data-ttu-id="53e8b-105">Una vez abiertos los archivos para la operación superpuesta, puede usar la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con uno de los siguientes códigos de control para trabajar con los bloqueos oportunistas de los archivos:</span><span class="sxs-lookup"><span data-stu-id="53e8b-105">After the files are opened for overlapped operation, you can use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with one of the following control codes to work with those files' opportunistic locks:</span></span>

<dl>

[<span data-ttu-id="53e8b-106">**el \_ cierre de ACK OPBATCH de FSCTL está \_ \_ \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="53e8b-106">**FSCTL\_OPBATCH\_ACK\_CLOSE\_PENDING**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[<span data-ttu-id="53e8b-107">**\_Confirmación de interrupción de bloqueo oportunista \_ \_ \_ no \_ 2 de FSCTL**</span><span class="sxs-lookup"><span data-stu-id="53e8b-107">**FSCTL\_OPLOCK\_BREAK\_ACK\_NO\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[<span data-ttu-id="53e8b-108">**\_confirmación de interrupción de bloqueo oportunista de FSCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="53e8b-108">**FSCTL\_OPLOCK\_BREAK\_ACKNOWLEDGE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[<span data-ttu-id="53e8b-109">**\_notificación de interrupción de bloqueo oportunista de FSCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="53e8b-109">**FSCTL\_OPLOCK\_BREAK\_NOTIFY**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[<span data-ttu-id="53e8b-110">**\_ \_ bloqueo oportunista de batch de solicitud de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="53e8b-110">**FSCTL\_REQUEST\_BATCH\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[<span data-ttu-id="53e8b-111">**\_ \_ bloqueo oportunista de filtro de solicitud de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="53e8b-111">**FSCTL\_REQUEST\_FILTER\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[<span data-ttu-id="53e8b-112">**\_bloqueo oportunista de solicitud de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="53e8b-112">**FSCTL\_REQUEST\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[<span data-ttu-id="53e8b-113">**\_ \_ \_ Nivel 1 de bloqueo oportunista de solicitud de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="53e8b-113">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_1**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[<span data-ttu-id="53e8b-114">**\_Nivel 2 de solicitud de \_ bloqueo oportunista de \_ FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="53e8b-114">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
