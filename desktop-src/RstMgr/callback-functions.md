---
title: Funciones de devolución de llamada del administrador de reinicio
description: La API del administrador de reinicio utiliza las funciones de devolución de llamada de la tabla siguiente.
ms.assetid: abb78aa5-0487-4e99-85b6-adc38b600c09
keywords:
- Admin. de reinicio del administrador, referencia, funciones de devolución de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c850dd805aeff664e3e09292825e342a6c5603
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793329"
---
# <a name="restart-manager-callback-functions"></a><span data-ttu-id="e316d-104">Funciones de devolución de llamada del administrador de reinicio</span><span class="sxs-lookup"><span data-stu-id="e316d-104">Restart Manager Callback Functions</span></span>

<span data-ttu-id="e316d-105">La API del administrador de reinicio utiliza las funciones de devolución de llamada de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e316d-105">The Restart Manager API uses the callback functions in the following table.</span></span>



| <span data-ttu-id="e316d-106">Función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="e316d-106">Callback Function</span></span>                                               | <span data-ttu-id="e316d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e316d-107">Description</span></span>                                                                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e316d-108">**\_devolución de \_ llamada de estado de escritura de RM \_**</span><span class="sxs-lookup"><span data-stu-id="e316d-108">**RM\_WRITE\_STATUS\_CALLBACK**</span></span>](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) | <span data-ttu-id="e316d-109">La aplicación que inició la sesión del administrador de reinicio puede pasar un puntero a esta función a las funciones del administrador de reinicio para recibir un porcentaje de integridad.</span><span class="sxs-lookup"><span data-stu-id="e316d-109">The application that started the Restart Manager session can pass a pointer to this function to the Restart Manager functions to receive a percentage of completeness.</span></span> |



 

 

 