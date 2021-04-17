---
description: Un proceso puede llamar a WSPCloseSocket en un socket duplicado y el descriptor se desasignará. Sin embargo, el socket subyacente permanecerá abierto hasta que se llame a WSPCloseSocket en el último descriptor restante.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Recuento de referencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72d9ef7b3e5e31cc7941d30c47f107fc068489ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696808"
---
# <a name="reference-counting"></a><span data-ttu-id="4b94e-104">Recuento de referencias</span><span class="sxs-lookup"><span data-stu-id="4b94e-104">Reference Counting</span></span>

<span data-ttu-id="4b94e-105">Un proceso puede llamar a [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) en un socket duplicado y el descriptor se desasignará.</span><span class="sxs-lookup"><span data-stu-id="4b94e-105">A process may call [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) on a duplicated socket and the descriptor will become deallocated.</span></span> <span data-ttu-id="4b94e-106">Sin embargo, el socket subyacente permanecerá abierto hasta que se llame a **WSPCloseSocket** en el último descriptor restante.</span><span class="sxs-lookup"><span data-stu-id="4b94e-106">The underlying socket, however, will remain open until **WSPCloseSocket** is called on the last remaining descriptor.</span></span>

 

 
