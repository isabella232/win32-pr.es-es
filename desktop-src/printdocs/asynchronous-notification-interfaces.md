---
description: Las interfaces siguientes se utilizan en la comunicación asincrónica entre las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión, como los controladores de impresora y los monitores de puerto.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfaces de notificación de impresión asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da8d320b33224e81852542e39f435b45b6dab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817766"
---
# <a name="asynchronous-printing-notification-interfaces"></a><span data-ttu-id="3ee73-103">Interfaces de notificación de impresión asincrónica</span><span class="sxs-lookup"><span data-stu-id="3ee73-103">Asynchronous Printing Notification Interfaces</span></span>

<span data-ttu-id="3ee73-104">Las interfaces siguientes se utilizan en la comunicación asincrónica entre las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión, como los controladores de impresora y los monitores de puerto.</span><span class="sxs-lookup"><span data-stu-id="3ee73-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3ee73-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3ee73-105">In this section</span></span>



| <span data-ttu-id="3ee73-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="3ee73-106">Interface</span></span>                                                                     | <span data-ttu-id="3ee73-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ee73-107">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ee73-108">**IPrintAsyncNotifyCallback**</span><span class="sxs-lookup"><span data-stu-id="3ee73-108">**IPrintAsyncNotifyCallback**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | <span data-ttu-id="3ee73-109">Crea y administra un canal de comunicación que utilizan las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="3ee73-109">Creates and manages a communication channel used by applications and components that are hosted by the print spooler.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="3ee73-110">**IPrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="3ee73-110">**IPrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | <span data-ttu-id="3ee73-111">Representa un canal de comunicación que los componentes hospedados por el administrador de trabajos de impresión usan para enviar notificaciones a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="3ee73-111">Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications.</span></span> <span data-ttu-id="3ee73-112">Si el canal es bidireccional, las aplicaciones pueden usar el mismo canal para devolver respuestas al componente.</span><span class="sxs-lookup"><span data-stu-id="3ee73-112">If the channel is bidirectional, applications can use the same channel to send responses back to the component.</span></span><br/> |
| [<span data-ttu-id="3ee73-113">**IPrintAsyncNotifyDataObject**</span><span class="sxs-lookup"><span data-stu-id="3ee73-113">**IPrintAsyncNotifyDataObject**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | <span data-ttu-id="3ee73-114">Encapsula los datos enviados en un canal de notificación.</span><span class="sxs-lookup"><span data-stu-id="3ee73-114">Encapsulates the data sent in a notification channel.</span></span> <br/>                                                                                                                                                                                             |



 

 

 




