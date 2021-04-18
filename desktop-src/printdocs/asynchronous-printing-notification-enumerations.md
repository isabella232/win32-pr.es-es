---
description: Las enumeraciones siguientes se utilizan en la comunicación asincrónica entre las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión, como los controladores de impresora y los monitores de puerto.
ms.assetid: 732a552b-caf9-45da-9a9e-a325c4f6341b
title: Enumeraciones de notificación de impresión asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e2baf2a4476ac858a883dda55b2864a79d78cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706298"
---
# <a name="asynchronous-printing-notification-enumerations"></a><span data-ttu-id="bb9b9-103">Enumeraciones de notificación de impresión asincrónica</span><span class="sxs-lookup"><span data-stu-id="bb9b9-103">Asynchronous Printing Notification Enumerations</span></span>

<span data-ttu-id="bb9b9-104">Las enumeraciones siguientes se utilizan en la comunicación asincrónica entre las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión, como los controladores de impresora y los monitores de puerto.</span><span class="sxs-lookup"><span data-stu-id="bb9b9-104">The following enumerations are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bb9b9-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bb9b9-105">In this section</span></span>



| <span data-ttu-id="bb9b9-106">Enumeración</span><span class="sxs-lookup"><span data-stu-id="bb9b9-106">Enumeration</span></span>                                                                               | <span data-ttu-id="bb9b9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb9b9-107">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb9b9-108">**PrintAsyncNotifyConversationStyle**</span><span class="sxs-lookup"><span data-stu-id="bb9b9-108">**PrintAsyncNotifyConversationStyle**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle)<br/> | <span data-ttu-id="bb9b9-109">Especifica si la comunicación es bidireccional o unidireccional entre aplicaciones y componentes hospedados en el administrador de trabajos de impresión, como controladores de impresora, procesadores de impresión y monitores de puerto.</span><span class="sxs-lookup"><span data-stu-id="bb9b9-109">Specifies whether communication is bidirectional or unidirectional between applications and Print Spooler-hosted components such as printer drivers, print processors, and port monitors.</span></span><br/>           |
| [<span data-ttu-id="bb9b9-110">**PrintAsyncNotifyError**</span><span class="sxs-lookup"><span data-stu-id="bb9b9-110">**PrintAsyncNotifyError**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)<br/>                         | <span data-ttu-id="bb9b9-111">Especifica la parte del código de error del **HRESULT** devuelto después de un error de notificación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="bb9b9-111">Specifies the error code portion of the **HRESULT** returned after an asynchronous notification failure.</span></span><br/>                                                                                            |
| [<span data-ttu-id="bb9b9-112">**PrintAsyncNotifyUserFilter**</span><span class="sxs-lookup"><span data-stu-id="bb9b9-112">**PrintAsyncNotifyUserFilter**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)<br/>               | <span data-ttu-id="bb9b9-113">Especifica si las notificaciones solo van a las aplicaciones de escucha asociadas al mismo usuario que el remitente hospedado en el administrador de trabajos de impresión, o bien, van a un conjunto más amplio de aplicaciones de escucha.</span><span class="sxs-lookup"><span data-stu-id="bb9b9-113">Specifies whether notifications will go only to listening applications that are associated with the same user as the Print Spooler-hosted sender, or go to a broader set of listening applications.</span></span><br/> |



 

 

 




