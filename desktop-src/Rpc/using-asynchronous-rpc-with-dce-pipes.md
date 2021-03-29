---
title: Usar RPC asincrónico con canalizaciones de DCE
description: Microsoft RPC admite el uso de canalizaciones de DCE. Aunque comparten un nombre similar, las canalizaciones de DCE no están relacionadas con las canalizaciones con nombre. Las canalizaciones con nombre son un protocolo de transporte. Las canalizaciones de DCE son un método independiente del Protocolo de comunicación entre cliente y servidor.
ms.assetid: 9de4f6dc-0aa9-446e-b68c-e0d1e247fea7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e9c98f4d4191a064d78cff2c918077f27d676f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075676"
---
# <a name="using-asynchronous-rpc-with-dce-pipes"></a><span data-ttu-id="bfaab-106">Usar RPC asincrónico con canalizaciones de DCE</span><span class="sxs-lookup"><span data-stu-id="bfaab-106">Using Asynchronous RPC with DCE Pipes</span></span>

<span data-ttu-id="bfaab-107">Microsoft RPC admite el uso de canalizaciones de DCE.</span><span class="sxs-lookup"><span data-stu-id="bfaab-107">Microsoft RPC supports the use of DCE pipes.</span></span> <span data-ttu-id="bfaab-108">Aunque comparten un nombre similar, las canalizaciones de DCE no están relacionadas con las [canalizaciones con nombre](asynchronous-rpc-over-the-named-pipe-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="bfaab-108">Although they share a similar name, DCE pipes are unrelated to [named pipes](asynchronous-rpc-over-the-named-pipe-protocol.md).</span></span> <span data-ttu-id="bfaab-109">Las canalizaciones con nombre son un protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="bfaab-109">Named pipes are a transport protocol.</span></span> <span data-ttu-id="bfaab-110">Las canalizaciones de DCE son un método independiente del Protocolo de comunicación entre cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="bfaab-110">DCE pipes are a protocol-independent method of client/server communication.</span></span>

<span data-ttu-id="bfaab-111">En esta sección se presenta una descripción de RPC mediante canalizaciones asincrónicas de DCE.</span><span class="sxs-lookup"><span data-stu-id="bfaab-111">This section presents a discussion of RPC using asynchronous DCE pipes.</span></span> <span data-ttu-id="bfaab-112">Se divide en los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="bfaab-112">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="bfaab-113">Canalizaciones asincrónicas</span><span class="sxs-lookup"><span data-stu-id="bfaab-113">Asynchronous Pipes</span></span>](asynchronous-pipes.md)
-   [<span data-ttu-id="bfaab-114">Declarar canalizaciones asincrónicas</span><span class="sxs-lookup"><span data-stu-id="bfaab-114">Declaring Asynchronous Pipes</span></span>](declaring-asynchronous-pipes.md)
-   [<span data-ttu-id="bfaab-115">Control de canalizaciones asincrónicas en el cliente</span><span class="sxs-lookup"><span data-stu-id="bfaab-115">Client-side Asynchronous Pipe Handling</span></span>](client-side-asynchronous-pipe-handling.md)
-   [<span data-ttu-id="bfaab-116">Control de canalizaciones asincrónicas en el servidor</span><span class="sxs-lookup"><span data-stu-id="bfaab-116">Server-side Asynchronous Pipe Handling</span></span>](server-side-asynchronous-pipe-handling.md)

<span data-ttu-id="bfaab-117">Para obtener una aplicación RPC de canalización asincrónica de ejemplo, vea el ejemplo FileRep en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="bfaab-117">For a sample asynchronous pipe RPC application, see the FileRep sample in the Platform Software Development Kit (SDK).</span></span>

 

 




