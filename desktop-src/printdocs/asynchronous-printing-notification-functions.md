---
description: Las interfaces siguientes se utilizan en la comunicación asincrónica entre las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión, como los controladores de impresora y los monitores de puerto.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Funciones de notificación de impresión asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7b0b61de15af9f7117e7c36104eb51abbb7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697669"
---
# <a name="asynchronous-printing-notification-functions"></a><span data-ttu-id="91f4d-103">Funciones de notificación de impresión asincrónica</span><span class="sxs-lookup"><span data-stu-id="91f4d-103">Asynchronous Printing Notification Functions</span></span>

<span data-ttu-id="91f4d-104">Las interfaces siguientes se utilizan en la comunicación asincrónica entre las aplicaciones y los componentes que se hospedan en el administrador de trabajos de impresión, como los controladores de impresora y los monitores de puerto.</span><span class="sxs-lookup"><span data-stu-id="91f4d-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="91f4d-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="91f4d-105">In this section</span></span>



| <span data-ttu-id="91f4d-106">Función</span><span class="sxs-lookup"><span data-stu-id="91f4d-106">Function</span></span>                                                                                        | <span data-ttu-id="91f4d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="91f4d-107">Description</span></span>                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91f4d-108">**CreatePrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="91f4d-108">**CreatePrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | <span data-ttu-id="91f4d-109">Crea un canal de comunicación entre un componente de impresión hospedado en el administrador de trabajos de impresión, como un controlador de impresión o un monitor de puerto, y una aplicación que recibe notificaciones del componente.</span><span class="sxs-lookup"><span data-stu-id="91f4d-109">Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.</span></span><br/> |
| [<span data-ttu-id="91f4d-110">**RegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="91f4d-110">**RegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | <span data-ttu-id="91f4d-111">Permite a una aplicación registrarse para recibir notificaciones de los componentes de impresión hospedados en el administrador de trabajos de impresión, como controladores de impresora, procesadores de impresión y monitores de puerto.</span><span class="sxs-lookup"><span data-stu-id="91f4d-111">Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.</span></span><br/>                              |
| [<span data-ttu-id="91f4d-112">**UnRegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="91f4d-112">**UnRegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | <span data-ttu-id="91f4d-113">Habilita una aplicación que se ha registrado para recibir notificaciones de los componentes de impresión hospedados en el administrador de trabajos de impresión para anular el registro.</span><span class="sxs-lookup"><span data-stu-id="91f4d-113">Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.</span></span><br/>                                                              |



 

 

 




