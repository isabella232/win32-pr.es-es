---
title: Completar y cancelar un trabajo
description: Para completar un trabajo de transferencia, llame al método IBackgroundCopyJob complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- transferir BITS de trabajo, cancelar
- cancelar los BITS de un trabajo
- transferir BITS de trabajo, completar
- completar BITS de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486651"
---
# <a name="completing-and-canceling-a-job"></a><span data-ttu-id="51eaa-107">Completar y cancelar un trabajo</span><span class="sxs-lookup"><span data-stu-id="51eaa-107">Completing and Canceling a Job</span></span>

<span data-ttu-id="51eaa-108">Para completar un trabajo de transferencia, llame al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="51eaa-108">To complete a transfer job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="51eaa-109">En el caso de los trabajos de descarga, puede llamar al método **Complete** antes de que se transfieran todos los archivos del trabajo (antes de que el estado del trabajo sea transferencia de estado del trabajo de BG \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="51eaa-109">For download jobs, you can call the **Complete** method before all files in the job have been transferred (before the job's state is BG\_JOB\_STATE\_TRANSFERRED).</span></span> <span data-ttu-id="51eaa-110">Solo los archivos que BITS se transfirieron correctamente al cliente antes de llamar al método **Complete** están disponibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="51eaa-110">Only those files that BITS successfully transferred to the client before you called the **Complete** method are available to the user.</span></span>

<span data-ttu-id="51eaa-111">En el caso de los trabajos de carga, llame al método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) solo si el estado del trabajo es el estado del trabajo de BG \_ \_ \_ transferido.</span><span class="sxs-lookup"><span data-stu-id="51eaa-111">For upload jobs, call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method only if the job's state is BG\_JOB\_STATE\_TRANSFERRED.</span></span> <span data-ttu-id="51eaa-112">Para determinar cuándo se transfiere el estado del trabajo \_ \_ \_ , transfiera el estado del trabajo, [sondee](polling-for-the-status-of-the-job.md) la propiedad de estado del trabajo o regístrese para recibir la notificación de eventos del trabajo de notificación de BG \_ \_ \_ transferida. [](registering-a-com-callback.md)</span><span class="sxs-lookup"><span data-stu-id="51eaa-112">To determine when the job's state is BG\_JOB\_STATE\_TRANSFERRED, [poll](polling-for-the-status-of-the-job.md) the job's state property or register to receive BG\_NOTIFY\_JOB\_TRANSFERRED [event notification](registering-a-com-callback.md).</span></span>

<span data-ttu-id="51eaa-113">Para cancelar un trabajo de transferencia, llame al método [**IBackgroundCopyJob:: CANCEL**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="51eaa-113">To cancel a transfer job, call the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span> <span data-ttu-id="51eaa-114">El método **Cancel** quita el trabajo de la cola de transferencia y quita los archivos temporales del cliente.</span><span class="sxs-lookup"><span data-stu-id="51eaa-114">The **Cancel** method removes the job from the transfer queue and removes the temporary files from the client.</span></span> <span data-ttu-id="51eaa-115">Normalmente, se llama a este método si no se puede resolver un error asociado al trabajo.</span><span class="sxs-lookup"><span data-stu-id="51eaa-115">Typically, you call this method if you are unable to resolve an error associated with the job.</span></span>

<span data-ttu-id="51eaa-116">El método [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) cancela una carga si la carga no se ha completado.</span><span class="sxs-lookup"><span data-stu-id="51eaa-116">The [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method cancels an upload if the upload is not complete.</span></span> <span data-ttu-id="51eaa-117">Si la carga se ha completado y el trabajo es de tipo BG \_ Job \_ Type \_ upload \_ , el método cancela la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51eaa-117">If the upload is complete, and the job is of type BG\_JOB\_TYPE\_UPLOAD\_REPLY, the method cancels the reply.</span></span>

<span data-ttu-id="51eaa-118">Si no llama al método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o al método [**IBackgroundCopyJob:: CANCEL**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) en 90 días (el valor predeterminado de [valor jobinactivitytimeout](group-policies.md) Directiva de grupo), el servicio cancela el trabajo.</span><span class="sxs-lookup"><span data-stu-id="51eaa-118">If you do not call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method within 90 days (default [JobInactivityTimeout](group-policies.md) Group Policy), the service cancels the job.</span></span> <span data-ttu-id="51eaa-119">Si el servicio cancela el trabajo, los archivos descargados y el archivo de respuesta no están disponibles para el cliente; la cancelación del trabajo no afecta a los archivos que se han cargado correctamente.</span><span class="sxs-lookup"><span data-stu-id="51eaa-119">If the service cancels the job, the downloaded files and the reply file are not available to the client; job cancellation does not affect files that have been successfully uploaded.</span></span> <span data-ttu-id="51eaa-120">Siempre debe llamar al método **Complete** o **Cancel** y no confiar en la Directiva valor jobinactivitytimeout para limpiar los trabajos.</span><span class="sxs-lookup"><span data-stu-id="51eaa-120">You should always call the **Complete** or the **Cancel** method and not rely on the JobInactivityTimeout policy to cleanup your jobs.</span></span> <span data-ttu-id="51eaa-121">Los trabajos que quedan en la cola pueden impedir que los usuarios creen otros trabajos si se alcanza el límite de la Directiva MaxJobsPerUser o MaxJobsPerMachine.</span><span class="sxs-lookup"><span data-stu-id="51eaa-121">Jobs left in the queue may prevent users from creating other jobs if the MaxJobsPerUser or MaxJobsPerMachine policy limit is reached.</span></span>

 

 




