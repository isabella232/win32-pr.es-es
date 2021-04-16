---
description: La forma más sencilla de e/s en Windows Sockets 2 es el bloqueo de e/s.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Bloqueo de entrada/salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696405"
---
# <a name="blocking-inputoutput"></a><span data-ttu-id="d5ddb-103">Bloqueo de entrada/salida</span><span class="sxs-lookup"><span data-stu-id="d5ddb-103">Blocking Input/Output</span></span>

<span data-ttu-id="d5ddb-104">La forma más sencilla de e/s en Windows Sockets 2 es el bloqueo de e/s.</span><span class="sxs-lookup"><span data-stu-id="d5ddb-104">The simplest form of I/O in Windows Sockets 2 is blocking I/O.</span></span> <span data-ttu-id="d5ddb-105">Como se mencionó en [modos y marcas de atributo de socket](socket-attribute-flags-and-modes-2.md), los sockets se crean de forma predeterminada en modo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="d5ddb-105">As mentioned in [Socket Attribute Flags and Modes](socket-attribute-flags-and-modes-2.md), sockets are created in blocking mode by default.</span></span> <span data-ttu-id="d5ddb-106">Cualquier operación de e/s con un socket de bloqueo no volverá hasta que la operación se haya completado completamente.</span><span class="sxs-lookup"><span data-stu-id="d5ddb-106">Any I/O operation with a blocking socket will not return until the operation has been fully completed.</span></span> <span data-ttu-id="d5ddb-107">Por lo tanto, cualquier subproceso solo puede ejecutar una operación de e/s a la vez.</span><span class="sxs-lookup"><span data-stu-id="d5ddb-107">Thus, any thread can only execute one I/O operation at a time.</span></span> <span data-ttu-id="d5ddb-108">Por ejemplo, si un subproceso emite una operación de recepción y no hay ningún dato disponible actualmente, el subproceso se bloqueará hasta que los datos estén disponibles y se coloquen en el búfer del subproceso.</span><span class="sxs-lookup"><span data-stu-id="d5ddb-108">For example, if a thread issues a receive operation and no data is currently available, the thread will block until data becomes available and is placed into the thread's buffer.</span></span> <span data-ttu-id="d5ddb-109">Aunque esto es sencillo, no es necesariamente la manera más eficaz de realizar operaciones de e/s (consulte [pseudo bloqueo y bloqueo real](pseudo-vs--true-blocking-2.md) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="d5ddb-109">Although this is simple, it is not necessarily the most efficient way to do I/O (see [Pseudo Blocking and True Blocking](pseudo-vs--true-blocking-2.md) for more information).</span></span>

 

 



