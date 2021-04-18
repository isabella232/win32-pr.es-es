---
title: Administración de energía (servicios base de TPM)
description: El TBS recibe los eventos de administración de energía.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "105665771"
---
# <a name="power-management-tpm-base-services"></a><span data-ttu-id="64de4-103">Administración de energía (servicios base de TPM)</span><span class="sxs-lookup"><span data-stu-id="64de4-103">Power Management (TPM Base Services)</span></span>

<span data-ttu-id="64de4-104">El TBS recibe los eventos de administración de energía.</span><span class="sxs-lookup"><span data-stu-id="64de4-104">The TBS receives power management events.</span></span> <span data-ttu-id="64de4-105">Cuando se recibe una indicación de que el TPM u otras partes de la plataforma están a punto de entrar en un estado de energía en el que se interrumpirá la ejecución o se perderá el estado de TPM, el TBS realiza comprobaciones para determinar si es probable que finalice el comando que se está ejecutando antes de que el sistema se apague.</span><span class="sxs-lookup"><span data-stu-id="64de4-105">When an indication is received that the TPM or other parts of the platform are about to enter a power state in which execution will be interrupted or TPM state will be lost, the TBS checks to determine whether the currently executing command is likely to finish before the system powers down.</span></span> <span data-ttu-id="64de4-106">En general, el TBS permite finalizar los comandos de duración corta y media, pero cancela los comandos de larga duración.</span><span class="sxs-lookup"><span data-stu-id="64de4-106">In general, the TBS allows short and medium duration commands to finish, but cancels long duration commands.</span></span> <span data-ttu-id="64de4-107">Una vez que se ha devuelto el comando, el TBS detiene el envío de nuevos comandos al TPM y se prepara para la hibernación.</span><span class="sxs-lookup"><span data-stu-id="64de4-107">After the command has returned, the TBS stops sending new commands to the TPM and prepares itself for hibernation.</span></span> <span data-ttu-id="64de4-108">Cuando se restaura la alimentación, el TBS devuelve el resultado del comando al autor de la llamada y, a continuación, continúa con el procesamiento de los comandos TBS pendientes.</span><span class="sxs-lookup"><span data-stu-id="64de4-108">When power is restored, the TBS returns the result of the command to the caller, and then proceeds with processing pending TBS commands.</span></span> <span data-ttu-id="64de4-109">El código de administración de energía de TBS se ejecuta de forma asincrónica, por lo que puede controlar las solicitudes de administración de energía, incluso si el TPM está procesando un comando largo.</span><span class="sxs-lookup"><span data-stu-id="64de4-109">The TBS power management code runs asynchronously, so it can handle power management requests even if the TPM is processing a long command.</span></span>

<span data-ttu-id="64de4-110">Cuando un equipo entra en Estados de suspensión, incluido S3 (suspensión) y S4 (hibernación), el TPM se apaga.</span><span class="sxs-lookup"><span data-stu-id="64de4-110">When a computer enters sleep states, including S3 (sleep) and S4 (hibernation), the TPM is powered off.</span></span> <span data-ttu-id="64de4-111">Por lo tanto, se pierden todos los Estados de TPM no persistentes.</span><span class="sxs-lookup"><span data-stu-id="64de4-111">Thus, all nonpersistent TPM states are lost.</span></span> <span data-ttu-id="64de4-112">Antes de entrar en estos Estados, se espera que el software de aplicación se prepare para la pérdida de Estados de TPM volátiles.</span><span class="sxs-lookup"><span data-stu-id="64de4-112">Before entering these states, application software is expected to prepare for the loss of volatile TPM states.</span></span> <span data-ttu-id="64de4-113">Cuando el sistema vuelve de un estado de suspensión, el TBS se sincroniza con el TPM para que el estado de TBS sea coherente con el estado de TPM.</span><span class="sxs-lookup"><span data-stu-id="64de4-113">When the system returns from a sleep state, the TBS synchronizes with the TPM so that the TBS state is consistent with the TPM state.</span></span> <span data-ttu-id="64de4-114">Es posible que el software de la aplicación tenga que volver a emitir los comandos que se han interrumpido.</span><span class="sxs-lookup"><span data-stu-id="64de4-114">Application software may need to reissue commands that were interrupted.</span></span>

 

 




