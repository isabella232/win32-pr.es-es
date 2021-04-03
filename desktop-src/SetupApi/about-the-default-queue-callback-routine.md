---
description: La rutina de devolución de llamada de cola predeterminada controla las notificaciones enviadas por SetupCommitFileQueue de forma genérica.
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: Acerca de la rutina de devolución de llamada de cola predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907855"
---
# <a name="about-the-default-queue-callback-routine"></a><span data-ttu-id="c9035-103">Acerca de la rutina de devolución de llamada de cola predeterminada</span><span class="sxs-lookup"><span data-stu-id="c9035-103">About the Default Queue Callback Routine</span></span>

<span data-ttu-id="c9035-104">La rutina de devolución de llamada de cola predeterminada controla las notificaciones enviadas por [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) de forma genérica.</span><span class="sxs-lookup"><span data-stu-id="c9035-104">The default queue callback routine handles notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) in a generic manner.</span></span> <span data-ttu-id="c9035-105">Mediante el uso de la rutina predeterminada, obtiene una interfaz de usuario preparada para crear cuadros de diálogo de instalación comunes.</span><span class="sxs-lookup"><span data-stu-id="c9035-105">By using the default routine, you get a ready-made user interface to create common setup dialog boxes.</span></span> <span data-ttu-id="c9035-106">Se recomienda usar la rutina de devolución de llamada de cola predeterminada, tanto para facilitar el uso como para garantizar una apariencia y un comportamiento coherentes de los cuadros de diálogo generados durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="c9035-106">It is recommended that you use the default queue callback routine, both for ease of use, and to ensure a consistent appearance and behavior of dialog boxes generated during the installation.</span></span>

<span data-ttu-id="c9035-107">La rutina de devolución de llamada predeterminada requiere una estructura de contexto para mantener el registro interno.</span><span class="sxs-lookup"><span data-stu-id="c9035-107">The default callback routine requires a context structure for internal record keeping.</span></span> <span data-ttu-id="c9035-108">Además, la cola pasa información adicional relevante a la notificación actual en un conjunto de parámetros, *Param1* y *Param2*.</span><span class="sxs-lookup"><span data-stu-id="c9035-108">In addition, the queue passes additional information relevant to the current notification in a set of parameters, *Param1* and *Param2*.</span></span>

<span data-ttu-id="c9035-109">Por ejemplo, si la cola envía una notificación de SPFILENOTIFY \_ NEEDMEDIA a la rutina de devolución de llamada predeterminada, *Param1* apunta a una estructura de [**\_ medios de origen**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) que contiene información sobre los medios necesarios y *Param2* apunta a una matriz de caracteres que puede recibir información de la ruta de acceso del usuario.</span><span class="sxs-lookup"><span data-stu-id="c9035-109">For example, if the queue sends an SPFILENOTIFY\_NEEDMEDIA notification to the default callback routine, *Param1* points to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure that contains information about the media needed, and *Param2* points to a character array that can receive new path information from the user.</span></span>

<span data-ttu-id="c9035-110">La rutina de devolución de llamada predeterminada usa esta información para pedir al usuario que inserte los medios de origen necesarios, especifique una nueva ruta de acceso, omita la copia del archivo actual o cancele la operación actual.</span><span class="sxs-lookup"><span data-stu-id="c9035-110">The default callback routine uses this information to prompt the user to either insert the needed source media, specify a new path, skip copying the current file, or cancel the current operation.</span></span> <span data-ttu-id="c9035-111">La rutina de devolución de llamada de cola predeterminada devuelve FILEOP \_ NEWPATH, FILEOP \_ doit, FILEOP \_ SKIP o FILEOP \_ Abort a la cola, dependiendo de la acción realizada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c9035-111">The default queue callback routine returns FILEOP\_NEWPATH, FILEOP\_DOIT , FILEOP\_SKIP, or FILEOP\_ABORT to the queue, depending on which action the user took.</span></span>

<span data-ttu-id="c9035-112">Para obtener información sobre cómo la rutina de devolución de llamada de cola predeterminada controla cada notificación de cola, vea [notificaciones de cola de archivos](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c9035-112">For information on how the default queue callback routine handles each queue notification, see [File Queue Notifications](file-queue-notifications.md).</span></span>

<span data-ttu-id="c9035-113">Para obtener información sobre las rutinas de devolución de llamada de cola personalizadas, vea [crear una rutina de devolución de llamada de cola personalizada](creating-a-custom-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="c9035-113">For information on custom queue callback routines, see [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



