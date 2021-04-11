---
title: Obtención del estado de una operación del administrador de reinicio
description: Cuando se debe apagar o reiniciar muchas aplicaciones y servicios, la operación del administrador de reinicio puede tardar un período de tiempo prolongado. El método siguiente se puede utilizar para obtener el estado de la operación actual.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa5f329a8f21aa625c5c7b61a3e65b2c907bbf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149541"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a><span data-ttu-id="45698-104">Obtención del estado de una operación del administrador de reinicio</span><span class="sxs-lookup"><span data-stu-id="45698-104">Getting the Status of a Restart Manager Operation</span></span>

<span data-ttu-id="45698-105">Cuando se debe apagar o reiniciar muchas aplicaciones y servicios, la operación del administrador de reinicio puede tardar un período de tiempo prolongado.</span><span class="sxs-lookup"><span data-stu-id="45698-105">When many applications and services must be shut down or restarted, the Restart Manager operation can take an extended period of time.</span></span> <span data-ttu-id="45698-106">El método siguiente se puede utilizar para obtener el estado de la operación actual.</span><span class="sxs-lookup"><span data-stu-id="45698-106">The following method can be used to obtain the status of the current operation.</span></span>

<span data-ttu-id="45698-107">**Para obtener el estado de la operación actual del administrador de reinicio**</span><span class="sxs-lookup"><span data-stu-id="45698-107">**To get the status of the current Restart Manager operation**</span></span>

1.  <span data-ttu-id="45698-108">El instalador debe implementar una función de [**devolución de llamada de estado de escritura de RM \_ \_ \_**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) que determine el estado de las aplicaciones que se han cerrado o reiniciado.</span><span class="sxs-lookup"><span data-stu-id="45698-108">The installer should implement a [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function that determines the status of the applications that have been shut down or restarted.</span></span> <span data-ttu-id="45698-109">La función puede proporcionar la información a la interfaz de usuario o al registro.</span><span class="sxs-lookup"><span data-stu-id="45698-109">The function can provide the information to the user interface or log.</span></span>
2.  <span data-ttu-id="45698-110">El instalador pasa el puntero a la función de [**devolución de llamada de estado de \_ escritura \_ \_ de RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) al llamar a la función [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .</span><span class="sxs-lookup"><span data-stu-id="45698-110">The installer passes the pointer to the [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function when calling the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>

 

 