---
description: El enrutador de proveedor múltiple (MPR) llama a las funciones de notificación de conexión cuando se conecta o desconecta un recurso de red. Para recibir estas notificaciones, puede implementar estas funciones en un archivo DLL.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: API de notificación de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 352d5cb09923a666e3fe1474e9fd2ebe033f05be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155904"
---
# <a name="connection-notification-api"></a><span data-ttu-id="852a7-104">API de notificación de conexión</span><span class="sxs-lookup"><span data-stu-id="852a7-104">Connection Notification API</span></span>

<span data-ttu-id="852a7-105">El [*enrutador de proveedor múltiple*](/windows/desktop/SecGloss/m-gly) (MPR) llama a las funciones de notificación de conexión cuando se conecta o desconecta un recurso de red.</span><span class="sxs-lookup"><span data-stu-id="852a7-105">The [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the connection notification functions when it connects or disconnects a network resource.</span></span> <span data-ttu-id="852a7-106">Para recibir estas notificaciones, puede implementar estas funciones en un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="852a7-106">To receive such notifications, you can implement these functions in a DLL.</span></span>

<span data-ttu-id="852a7-107">El MPR llama a la función [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) antes y después de intentar cada operación Add-Connection ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)o [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span><span class="sxs-lookup"><span data-stu-id="852a7-107">The MPR calls the [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) function before and after attempting each add-connection operation ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a), or [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span></span> <span data-ttu-id="852a7-108">No se llama a esta función cuando el MPR está restaurando automáticamente las conexiones de red.</span><span class="sxs-lookup"><span data-stu-id="852a7-108">This function is not called when the MPR is automatically restoring network connections.</span></span>

<span data-ttu-id="852a7-109">El MPR llama a la función [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) antes y después de intentar cada operación de cancelación de conexión ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) o [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).</span><span class="sxs-lookup"><span data-stu-id="852a7-109">The MPR calls the [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) function before and after attempting each cancel-connection operation ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) or [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).</span></span>

<span data-ttu-id="852a7-110">Para obtener más información acerca de las funciones de WNet, consulte [redes de Windows](/windows/desktop/WNet/windows-networking-wnet-).</span><span class="sxs-lookup"><span data-stu-id="852a7-110">For more information about WNet functions, see [Windows Networking](/windows/desktop/WNet/windows-networking-wnet-).</span></span>

<span data-ttu-id="852a7-111">Para obtener más información acerca de cómo crear y registrar una aplicación que recibe notificaciones de conexión de red, consulte recepción de notificaciones de [conexión](receiving-connection-notifications.md) y [registro para recibir notificaciones de conexión](registering-to-receive-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="852a7-111">For more information about how to create and register an application that receives network connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md) and [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 
