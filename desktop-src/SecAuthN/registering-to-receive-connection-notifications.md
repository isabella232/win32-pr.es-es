---
description: Después de crear un archivo DLL para recibir notificaciones de conexión, debe registrarlo en el sistema.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Registro para recibir notificaciones de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813587"
---
# <a name="registering-to-receive-connection-notifications"></a><span data-ttu-id="fa2e7-103">Registro para recibir notificaciones de conexión</span><span class="sxs-lookup"><span data-stu-id="fa2e7-103">Registering to Receive Connection Notifications</span></span>

<span data-ttu-id="fa2e7-104">Después de crear un archivo DLL para recibir notificaciones de conexión, debe registrarlo en el sistema.</span><span class="sxs-lookup"><span data-stu-id="fa2e7-104">After you have created a DLL to receive connection notifications, you must register it with the system.</span></span> <span data-ttu-id="fa2e7-105">Para ello, agregue un valor **reg \_ Expand \_** en el</span><span class="sxs-lookup"><span data-stu-id="fa2e7-105">You do this by adding a **REG\_EXPAND\_SZ** value under the</span></span>

<span data-ttu-id="fa2e7-106">**HKEY \_ Sistema \_ del equipo local** NetworkProvider de los \\  \\  \\  \\  \\ **notificantes**</span><span class="sxs-lookup"><span data-stu-id="fa2e7-106">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="fa2e7-107">.</span><span class="sxs-lookup"><span data-stu-id="fa2e7-107">key.</span></span> <span data-ttu-id="fa2e7-108">Este valor especifica la ruta de acceso al archivo DLL que implementa la [API de notificación de conexión](connection-notification-api.md).</span><span class="sxs-lookup"><span data-stu-id="fa2e7-108">This value specifies the path to the DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span>

<span data-ttu-id="fa2e7-109">El valor puede tener cualquier nombre.</span><span class="sxs-lookup"><span data-stu-id="fa2e7-109">The value can have any name.</span></span> <span data-ttu-id="fa2e7-110">Todos los valores de la clave **NotifyTo** se tratan como rutas de acceso a los archivos DLL a los que se notifican los eventos de conexión.</span><span class="sxs-lookup"><span data-stu-id="fa2e7-110">All values under the **Notifyees** key are treated as paths to DLLs that are notified of connection events.</span></span> <span data-ttu-id="fa2e7-111">Se recomienda usar un nombre que identifique el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="fa2e7-111">It is recommended that you use a name that identifies your DLL.</span></span> <span data-ttu-id="fa2e7-112">Esto reduce la posibilidad de un conflicto de nombres con otras aplicaciones de notificación de conexión.</span><span class="sxs-lookup"><span data-stu-id="fa2e7-112">This lessens the chance of a name conflict with other connection notification applications.</span></span>

<span data-ttu-id="fa2e7-113">Para obtener más información sobre cómo crear una aplicación que reciba notificaciones de conexión, consulte [recibir notificaciones de conexión](receiving-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="fa2e7-113">For more information about how to create an application that receives connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md).</span></span>

 

 



