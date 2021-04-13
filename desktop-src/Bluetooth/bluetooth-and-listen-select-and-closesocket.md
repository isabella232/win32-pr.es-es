---
title: Bluetooth y escuchar, seleccionar y closesocket
description: Bluetooth usa las funciones Listen, SELECT y closesocket sin ninguna modificación de la programación estándar de Windows Sockets.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- closesocket
- listen
- select
- Bluetooth y escuchar
- Bluetooth y escuchar, seleccione
- Bluetooth y escuchar, seleccionar y closesocket
- listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487914"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a><span data-ttu-id="3cdb5-111">Bluetooth y escuchar, seleccionar y closesocket</span><span class="sxs-lookup"><span data-stu-id="3cdb5-111">Bluetooth and listen, select, and closesocket</span></span>

<span data-ttu-id="3cdb5-112">Bluetooth usa las funciones [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**Select**](/windows/desktop/api/winsock2/nf-winsock2-select)y [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) sin ninguna modificación de la programación estándar de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="3cdb5-112">Bluetooth uses the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select), and [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) functions without any modification from standard Windows Sockets programming.</span></span>

<span data-ttu-id="3cdb5-113">Al igual que con Windows Sockets, la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) libera los recursos asociados al socket.</span><span class="sxs-lookup"><span data-stu-id="3cdb5-113">As with Windows Sockets, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function frees resources associated with the socket.</span></span>

<span data-ttu-id="3cdb5-114">Cuando se llama a la función [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) , se recomienda encarecidamente que se use un valor bajo para el parámetro de *trabajo pendiente* (normalmente de 2 a 4), ya que solo se aceptan algunas conexiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="3cdb5-114">When calling the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) function, it is strongly recommended that a low value is used for the *backlog* parameter (typically 2 to 4), since only a few client connections are accepted.</span></span> <span data-ttu-id="3cdb5-115">Esto reduce los recursos del sistema que se asignan para su uso por el socket de escucha.</span><span class="sxs-lookup"><span data-stu-id="3cdb5-115">This reduces the system resources that are allocated for use by the listening socket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cdb5-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3cdb5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cdb5-117">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="3cdb5-117">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="3cdb5-118">**closesocket**</span><span class="sxs-lookup"><span data-stu-id="3cdb5-118">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="3cdb5-119">**escuchar**</span><span class="sxs-lookup"><span data-stu-id="3cdb5-119">**listen**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[<span data-ttu-id="3cdb5-120">**no**</span><span class="sxs-lookup"><span data-stu-id="3cdb5-120">**select**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 