---
description: Por lo general, se considera más fácil de ver en la red que una difusión de todas las rutas, una difusión dirigida se limita a la red local que especifique.
ms.assetid: e2358580-5a65-434d-ba4c-a6b0615bccc3
title: Difusión dirigida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3a47bd47e9800e1f9c93cffa555b76feb77373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705633"
---
# <a name="directed-broadcast"></a><span data-ttu-id="b7cde-103">Difusión dirigida</span><span class="sxs-lookup"><span data-stu-id="b7cde-103">Directed Broadcast</span></span>

<span data-ttu-id="b7cde-104">Por lo general, se considera más fácil de ver en la red que una difusión de todas las rutas, una difusión dirigida se limita a la red local que especifique.</span><span class="sxs-lookup"><span data-stu-id="b7cde-104">Generally considered more network friendly than an all-routes broadcast, a directed broadcast limits itself to the local network that you specify.</span></span> <span data-ttu-id="b7cde-105">Rellene **SA \_ netnum** con el número de red de destino y **SA \_ nodenum** con binarios.</span><span class="sxs-lookup"><span data-stu-id="b7cde-105">Fill **sa\_netnum** with the target network number and **sa\_nodenum** with binary ones.</span></span> <span data-ttu-id="b7cde-106">Los enrutadores reenvían esta solicitud a la red de destino, donde se convierte en una difusión local.</span><span class="sxs-lookup"><span data-stu-id="b7cde-106">Routers forward this request to the destination network where it becomes a local broadcast.</span></span> <span data-ttu-id="b7cde-107">Las redes intermedias no ven este paquete como una difusión.</span><span class="sxs-lookup"><span data-stu-id="b7cde-107">Intermediate networks do not see this packet as a broadcast.</span></span>

 

 



