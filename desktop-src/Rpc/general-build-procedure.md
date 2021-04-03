---
title: Procedimiento de compilación general
description: Página de navegación para el proceso de creación de una aplicación cliente/servidor mediante la llamada a procedimiento remoto (RPC).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b223bf7482cd7cbb65f5b737c90502a6b6dd3de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075597"
---
# <a name="general-build-procedure"></a><span data-ttu-id="5bde9-103">Procedimiento de compilación general</span><span class="sxs-lookup"><span data-stu-id="5bde9-103">General Build Procedure</span></span>

<span data-ttu-id="5bde9-104">El proceso para crear una aplicación cliente/servidor mediante Microsoft RPC es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="5bde9-104">The process for creating a client/server application using Microsoft RPC is:</span></span>

-   <span data-ttu-id="5bde9-105">Desarrolle la interfaz.</span><span class="sxs-lookup"><span data-stu-id="5bde9-105">Develop the interface.</span></span>
-   <span data-ttu-id="5bde9-106">Desarrolle el servidor que implementa la interfaz.</span><span class="sxs-lookup"><span data-stu-id="5bde9-106">Develop the server that implements the interface.</span></span>
-   <span data-ttu-id="5bde9-107">Desarrolle el cliente que utiliza la interfaz.</span><span class="sxs-lookup"><span data-stu-id="5bde9-107">Develop the client that uses the interface.</span></span>

<span data-ttu-id="5bde9-108">En la ilustración siguiente se muestran estos pasos.</span><span class="sxs-lookup"><span data-stu-id="5bde9-108">The following figure illustrates these steps.</span></span>

![proceso para crear una aplicación cliente-servidor mediante Microsoft RPC](images/appdev.png)

<span data-ttu-id="5bde9-110">Es factible y común desarrollar las aplicaciones cliente y servidor simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="5bde9-110">It is feasible and common to develop the client and server applications concurrently.</span></span> <span data-ttu-id="5bde9-111">Dado que los programas cliente y servidor dependen de la interfaz, sin embargo, la interfaz entre ellos debe desarrollarse antes de que se desarrollen el cliente y el servidor, tal como se muestra en el diagrama anterior.</span><span class="sxs-lookup"><span data-stu-id="5bde9-111">Since both the client and server programs are dependent on the interface, however, the interface between them must be developed before the client and server are developed, as shown in the preceding diagram.</span></span>

<span data-ttu-id="5bde9-112">En esta sección se describen los pasos necesarios para crear una aplicación cliente/servidor con RPC.</span><span class="sxs-lookup"><span data-stu-id="5bde9-112">This section discusses the steps required for building a client/server application with RPC.</span></span> <span data-ttu-id="5bde9-113">La información se presenta en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="5bde9-113">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="5bde9-114">Desarrollo de la interfaz</span><span class="sxs-lookup"><span data-stu-id="5bde9-114">Developing the Interface</span></span>](developing-the-interface.md)
-   [<span data-ttu-id="5bde9-115">Desarrollo del servidor</span><span class="sxs-lookup"><span data-stu-id="5bde9-115">Developing the Server</span></span>](developing-the-server.md)
-   [<span data-ttu-id="5bde9-116">Desarrollo del cliente</span><span class="sxs-lookup"><span data-stu-id="5bde9-116">Developing the Client</span></span>](developing-the-client.md)

 

 




