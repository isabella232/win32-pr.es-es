---
title: Operaciones de red de Windows
description: Una aplicación puede usar las funciones de WNet para examinar, agregar o cancelar conexiones de red en cualquier parte de la jerarquía de red.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30326d9ad1299e577c65586cff3df3010c086f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359085"
---
# <a name="windows-networking-operations"></a><span data-ttu-id="05b76-103">Operaciones de red de Windows</span><span class="sxs-lookup"><span data-stu-id="05b76-103">Windows Networking Operations</span></span>

<span data-ttu-id="05b76-104">Una aplicación puede usar las funciones de WNet para examinar, agregar o cancelar conexiones de red en cualquier parte de la jerarquía de red.</span><span class="sxs-lookup"><span data-stu-id="05b76-104">An application can use the WNet functions to browse, add, or cancel network connections anywhere in the network hierarchy.</span></span>

<span data-ttu-id="05b76-105">Una *conexión persistente* es una conexión de red que el sistema restaura automáticamente cuando el usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="05b76-105">A *persistent connection* is a network connection that the system automatically restores when the user logs on.</span></span> <span data-ttu-id="05b76-106">Puede llamar a las funciones [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (o [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) y [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) para controlar si una conexión de red es persistente de una sesión a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="05b76-106">You can call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (or [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) and [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) functions to control whether a network connection is persistent from one session to the next.</span></span>

<span data-ttu-id="05b76-107">Para buscar el nombre de usuario predeterminado o el nombre de usuario que se usa para establecer una conexión de red, llame a la función [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .</span><span class="sxs-lookup"><span data-stu-id="05b76-107">To find the default user name or the user name used to establish a network connection, call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="05b76-108">Además de llamar a las funciones de WNet, un proceso también puede utilizar los procesadores de elementos y canalizaciones con nombre para comunicarse con otro proceso.</span><span class="sxs-lookup"><span data-stu-id="05b76-108">In addition to calling the WNet functions, a process can also use mailslots and named pipes to communicate with another process.</span></span> <span data-ttu-id="05b76-109">Para obtener más información, consulte [procesadores de buzones](/windows/desktop/ipc/mailslots) y [canalizaciones](/windows/desktop/ipc/pipes).</span><span class="sxs-lookup"><span data-stu-id="05b76-109">For more information, see [Mailslots](/windows/desktop/ipc/mailslots) and [Pipes](/windows/desktop/ipc/pipes).</span></span>

 

 