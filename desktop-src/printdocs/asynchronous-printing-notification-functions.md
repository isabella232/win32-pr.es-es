---
description: Obtenga información sobre las funciones que se usan en la comunicación asincrónica entre aplicaciones y componentes hospedados por el colador de impresión.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Funciones de notificación de impresión asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc9a404d1675c8ee87be31c7c57dd14a370697c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394860"
---
# <a name="asynchronous-printing-notification-functions"></a><span data-ttu-id="2c9fd-103">Funciones de notificación de impresión asincrónica</span><span class="sxs-lookup"><span data-stu-id="2c9fd-103">Asynchronous Printing Notification Functions</span></span>

<span data-ttu-id="2c9fd-104">Las siguientes funciones se usan en la comunicación asincrónica entre aplicaciones y componentes hospedados por el cola de impresión, como controladores de impresora y monitores de puerto.</span><span class="sxs-lookup"><span data-stu-id="2c9fd-104">The following functions are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2c9fd-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2c9fd-105">In this section</span></span>



| <span data-ttu-id="2c9fd-106">Función</span><span class="sxs-lookup"><span data-stu-id="2c9fd-106">Function</span></span>                                                                                        | <span data-ttu-id="2c9fd-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c9fd-107">Description</span></span>                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c9fd-108">**CreatePrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="2c9fd-108">**CreatePrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | <span data-ttu-id="2c9fd-109">Crea un canal de comunicación entre un componente de impresión hospedado en Administrador de trabajos de impresión, como un controlador de impresión o un monitor de puerto, y una aplicación que recibe notificaciones del componente.</span><span class="sxs-lookup"><span data-stu-id="2c9fd-109">Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.</span></span><br/> |
| [<span data-ttu-id="2c9fd-110">**RegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="2c9fd-110">**RegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | <span data-ttu-id="2c9fd-111">Permite que una aplicación se registre para recibir notificaciones de los componentes de impresión hospedados en El cola de impresión, como controladores de impresora, procesadores de impresión y monitores de puerto.</span><span class="sxs-lookup"><span data-stu-id="2c9fd-111">Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.</span></span><br/>                              |
| [<span data-ttu-id="2c9fd-112">**UnRegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="2c9fd-112">**UnRegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | <span data-ttu-id="2c9fd-113">Permite que una aplicación que se ha registrado reciba notificaciones de los componentes de impresión hospedados por el cola de impresión para anular el registro.</span><span class="sxs-lookup"><span data-stu-id="2c9fd-113">Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.</span></span><br/>                                                              |



 

 

 




