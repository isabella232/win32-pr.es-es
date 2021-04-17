---
description: 'Hay dos tipos distintos de aplicaciones de red de socket: servidor y cliente.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: Acerca de los servidores y clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a951d23ba1c6ad4f0f5ffd1f674b056a36c3f8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696408"
---
# <a name="about-servers-and-clients"></a><span data-ttu-id="bcbf3-103">Acerca de los servidores y clientes</span><span class="sxs-lookup"><span data-stu-id="bcbf3-103">About Servers and Clients</span></span>

<span data-ttu-id="bcbf3-104">Hay dos tipos distintos de aplicaciones de red de socket: servidor y cliente.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-104">There are two distinct types of socket network applications: Server and Client.</span></span>

<span data-ttu-id="bcbf3-105">Los servidores y los clientes tienen distintos comportamientos. por lo tanto, el proceso de crearlos es diferente.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-105">Servers and Clients have different behaviors; therefore, the process of creating them is different.</span></span> <span data-ttu-id="bcbf3-106">A continuación se muestra el modelo general para crear un cliente y un servidor TCP/IP de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-106">What follows is the general model for creating a streaming TCP/IP Server and Client.</span></span>

## <a name="server"></a><span data-ttu-id="bcbf3-107">Servidor</span><span class="sxs-lookup"><span data-stu-id="bcbf3-107">Server</span></span>

1.  <span data-ttu-id="bcbf3-108">Inicialice Winsock.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-108">Initialize Winsock.</span></span>
2.  <span data-ttu-id="bcbf3-109">Cree un socket.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-109">Create a socket.</span></span>
3.  <span data-ttu-id="bcbf3-110">Enlazar el socket.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-110">Bind the socket.</span></span>
4.  <span data-ttu-id="bcbf3-111">Escuche en el socket para un cliente.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-111">Listen on the socket for a client.</span></span>
5.  <span data-ttu-id="bcbf3-112">Acepte una conexión desde un cliente.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-112">Accept a connection from a client.</span></span>
6.  <span data-ttu-id="bcbf3-113">Recibir y enviar datos.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-113">Receive and send data.</span></span>
7.  <span data-ttu-id="bcbf3-114">Desconectarte.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-114">Disconnect.</span></span>

## <a name="client"></a><span data-ttu-id="bcbf3-115">Remoto</span><span class="sxs-lookup"><span data-stu-id="bcbf3-115">Client</span></span>

1.  <span data-ttu-id="bcbf3-116">Inicialice Winsock.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-116">Initialize Winsock.</span></span>
2.  <span data-ttu-id="bcbf3-117">Cree un socket.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-117">Create a socket.</span></span>
3.  <span data-ttu-id="bcbf3-118">Conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-118">Connect to the server.</span></span>
4.  <span data-ttu-id="bcbf3-119">Enviar y recibir datos.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-119">Send and receive data.</span></span>
5.  <span data-ttu-id="bcbf3-120">Desconectarte.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-120">Disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="bcbf3-121">Algunos de los pasos son los mismos para un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-121">Some of the steps are the same for a client and a server.</span></span> <span data-ttu-id="bcbf3-122">Estos pasos se implementan casi exactamente igual.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-122">These steps are implemented almost exactly alike.</span></span> <span data-ttu-id="bcbf3-123">Algunos de los pasos de esta guía serán específicos para el tipo de aplicación que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="bcbf3-123">Some of the steps in this guide will be specific to the type of application being created.</span></span>

 

<span data-ttu-id="bcbf3-124">Primer paso: [creación de una aplicación de Winsock básica](creating-a-basic-winsock-application.md)</span><span class="sxs-lookup"><span data-stu-id="bcbf3-124">First Step: [Creating a Basic Winsock Application](creating-a-basic-winsock-application.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="bcbf3-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bcbf3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcbf3-126">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="bcbf3-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



