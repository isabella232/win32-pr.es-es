---
description: Obtenga información sobre las interfaces que se usan en la comunicación asincrónica entre aplicaciones y componentes hospedados por el colador de impresión.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfaces de notificación de impresión asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe0de2cf8510b1bb039907067b62fce08a4145
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396100"
---
# <a name="asynchronous-printing-notification-interfaces"></a><span data-ttu-id="aa9f5-103">Interfaces de notificación de impresión asincrónica</span><span class="sxs-lookup"><span data-stu-id="aa9f5-103">Asynchronous Printing Notification Interfaces</span></span>

<span data-ttu-id="aa9f5-104">Las interfaces siguientes se usan en la comunicación asincrónica entre aplicaciones y componentes hospedados por el colador de impresión, como controladores de impresora y monitores de puerto.</span><span class="sxs-lookup"><span data-stu-id="aa9f5-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aa9f5-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="aa9f5-105">In this section</span></span>



| <span data-ttu-id="aa9f5-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="aa9f5-106">Interface</span></span>                                                                     | <span data-ttu-id="aa9f5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa9f5-107">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa9f5-108">**IPrintAsyncNotifyCallback**</span><span class="sxs-lookup"><span data-stu-id="aa9f5-108">**IPrintAsyncNotifyCallback**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | <span data-ttu-id="aa9f5-109">Crea y administra un canal de comunicación utilizado por las aplicaciones y los componentes hospedados por el cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="aa9f5-109">Creates and manages a communication channel used by applications and components that are hosted by the print spooler.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="aa9f5-110">**IPrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="aa9f5-110">**IPrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | <span data-ttu-id="aa9f5-111">Representa un canal de comunicación que los componentes hospedados por el colador de impresión usan para enviar notificaciones a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="aa9f5-111">Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications.</span></span> <span data-ttu-id="aa9f5-112">Si el canal es bidireccional, las aplicaciones pueden usar el mismo canal para enviar respuestas de vuelta al componente.</span><span class="sxs-lookup"><span data-stu-id="aa9f5-112">If the channel is bidirectional, applications can use the same channel to send responses back to the component.</span></span><br/> |
| [<span data-ttu-id="aa9f5-113">**IPrintAsyncNotifyDataObject**</span><span class="sxs-lookup"><span data-stu-id="aa9f5-113">**IPrintAsyncNotifyDataObject**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | <span data-ttu-id="aa9f5-114">Encapsula los datos enviados en un canal de notificación.</span><span class="sxs-lookup"><span data-stu-id="aa9f5-114">Encapsulates the data sent in a notification channel.</span></span> <br/>                                                                                                                                                                                             |



 

 

 




