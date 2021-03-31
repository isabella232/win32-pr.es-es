---
description: Los bloqueos oportunistas se solicitan abriendo primero un archivo con permisos y marcas adecuadas para la aplicación que abre el archivo. Todos los archivos para los que se solicitarán bloqueos oportunistas se deben abrir para una operación superpuesta (asincrónica).
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: Cómo solicitar un bloqueo oportunista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912857"
---
# <a name="how-to-request-an-opportunistic-lock"></a><span data-ttu-id="fbff7-104">Cómo solicitar un bloqueo oportunista</span><span class="sxs-lookup"><span data-stu-id="fbff7-104">How to Request an Opportunistic Lock</span></span>

<span data-ttu-id="fbff7-105">Las aplicaciones cliente solo solicitan directamente bloqueos oportunistas cuando el bloqueo está diseñado para un archivo en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="fbff7-105">Client applications directly request opportunistic locks only when the lock is intended for a file on the local server.</span></span> <span data-ttu-id="fbff7-106">Al tener acceso a los archivos de los servidores remotos, es el redirector de red, no la aplicación cliente, que solicita el bloqueo oportunista desde el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="fbff7-106">When accessing files on remote servers, it is the network redirector, and not the client application, that requests the opportunistic lock from the remote server.</span></span>

<span data-ttu-id="fbff7-107">Los bloqueos oportunistas se solicitan abriendo primero un archivo con permisos y marcas adecuadas para la aplicación que abre el archivo.</span><span class="sxs-lookup"><span data-stu-id="fbff7-107">Opportunistic locks are requested by first opening a file with permissions and flags appropriate to the application opening the file.</span></span> <span data-ttu-id="fbff7-108">Todos los archivos para los que se solicitarán bloqueos oportunistas se deben abrir para una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="fbff7-108">All files for which opportunistic locks will be requested must be opened for overlapped (asynchronous) operation.</span></span> <span data-ttu-id="fbff7-109">Una vez abiertos los archivos para la operación superpuesta, utilice la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con el código de control adecuado para solicitar un bloqueo oportunista.</span><span class="sxs-lookup"><span data-stu-id="fbff7-109">After the files are opened for overlapped operation, use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the appropriate control code to request an opportunistic lock.</span></span> <span data-ttu-id="fbff7-110">Para obtener una lista de las operaciones de bloqueo oportunista, consulte [operaciones de bloqueo oportunista](opportunistic-lock-operations.md).</span><span class="sxs-lookup"><span data-stu-id="fbff7-110">For a list of the opportunistic lock operations, see [Opportunistic Lock Operations](opportunistic-lock-operations.md).</span></span>

<span data-ttu-id="fbff7-111">Las aplicaciones reciben una notificación de que se ha interrumpido un bloqueo oportunista mediante el miembro **hEvent** de la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) asociada con el archivo.</span><span class="sxs-lookup"><span data-stu-id="fbff7-111">Applications are notified that an opportunistic lock is broken by using the **hEvent** member of the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the file.</span></span> <span data-ttu-id="fbff7-112">Las aplicaciones también pueden usar funciones como [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) y [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span><span class="sxs-lookup"><span data-stu-id="fbff7-112">Applications may also use functions such as [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) and [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span></span> <span data-ttu-id="fbff7-113">La aplicación es responsable de asociar el archivo correcto con el bloqueo oportunista roto.</span><span class="sxs-lookup"><span data-stu-id="fbff7-113">The application is responsible for associating the correct file with the broken opportunistic lock.</span></span>

<span data-ttu-id="fbff7-114">Para obtener más información sobre las notificaciones, consulte [Synchronization](/windows/desktop/Sync/synchronization).</span><span class="sxs-lookup"><span data-stu-id="fbff7-114">For more information on notification, see [Synchronization](/windows/desktop/Sync/synchronization).</span></span>

 

 
