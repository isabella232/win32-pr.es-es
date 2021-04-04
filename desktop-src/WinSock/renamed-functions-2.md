---
description: En dos casos, era necesario cambiar el nombre de las funciones que se usan en los sockets de Berkeley para evitar conflictos con otras funciones de la API de Microsoft Windows.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Funciones cuyo nombre ha cambiado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908573"
---
# <a name="renamed-functions"></a><span data-ttu-id="33f6d-103">Funciones cuyo nombre ha cambiado</span><span class="sxs-lookup"><span data-stu-id="33f6d-103">Renamed Functions</span></span>

<span data-ttu-id="33f6d-104">En dos casos, era necesario cambiar el nombre de las funciones que se usan en los sockets de Berkeley para evitar conflictos con otras funciones de la API de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="33f6d-104">In two cases it was necessary to rename functions that are used in Berkeley Sockets in order to avoid clashes with other Microsoft Windows API functions.</span></span>

## <a name="close-and-closesocket"></a><span data-ttu-id="33f6d-105">Close y closesocket</span><span class="sxs-lookup"><span data-stu-id="33f6d-105">Close and Closesocket</span></span>

<span data-ttu-id="33f6d-106">Los descriptores de archivo estándar representan los sockets en sockets de Berkeley, por lo que se puede usar la función **Close** para cerrar sockets, así como archivos normales.</span><span class="sxs-lookup"><span data-stu-id="33f6d-106">Sockets are represented by standard file descriptors in Berkeley Sockets, so the **close** function can be used to close sockets as well as regular files.</span></span> <span data-ttu-id="33f6d-107">Aunque nada en Windows Sockets impide que una implementación use identificadores de archivos normales para identificar sockets, nada lo requiere.</span><span class="sxs-lookup"><span data-stu-id="33f6d-107">While nothing in Windows Sockets prevents an implementation from using regular file handles to identify sockets, nothing requires it either.</span></span> <span data-ttu-id="33f6d-108">En Windows, los sockets deben cerrarse mediante la rutina [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) .</span><span class="sxs-lookup"><span data-stu-id="33f6d-108">On Windows, sockets must be closed by using the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) routine.</span></span> <span data-ttu-id="33f6d-109">EN Windows, el uso de la función **Close** para cerrar un socket es incorrecto y los efectos de hacerlo no están definidos por esta especificación.</span><span class="sxs-lookup"><span data-stu-id="33f6d-109">ON Windows, using the **close** function to close a socket is incorrect and the effects of doing so are undefined by this specification.</span></span>

## <a name="ioctl-and-ioctlsocketwsaioctl"></a><span data-ttu-id="33f6d-110">Ioctl y Ioctlsocket/WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="33f6d-110">Ioctl and Ioctlsocket/WSAIoctl</span></span>

<span data-ttu-id="33f6d-111">Varios sistemas en tiempo de ejecución de lenguaje C usan el ioctl para fines no relacionados con Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="33f6d-111">Various C language run-time systems use the IOCTLs for purposes unrelated to Windows Sockets.</span></span> <span data-ttu-id="33f6d-112">Como consecuencia, la función [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) y la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) se definieron para controlar las funciones de socket realizadas por **ioctl** y **fcntl** en la distribución de software Berkeley.</span><span class="sxs-lookup"><span data-stu-id="33f6d-112">As a consequence, the [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) function and the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function were defined to handle socket functions that were performed by **IOCTL** and **fcntl** in the Berkeley Software Distribution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33f6d-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33f6d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33f6d-114">**closesocket**</span><span class="sxs-lookup"><span data-stu-id="33f6d-114">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="33f6d-115">**ioctlsocket**</span><span class="sxs-lookup"><span data-stu-id="33f6d-115">**ioctlsocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[<span data-ttu-id="33f6d-116">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="33f6d-116">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="33f6d-117">Consideraciones sobre la programación de Winsock</span><span class="sxs-lookup"><span data-stu-id="33f6d-117">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="33f6d-118">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="33f6d-118">**WSAIoctl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



