---
title: Uso de subprocesos
description: Debe optimizar y equilibrar el uso de subprocesos de aplicación para un entorno de Servicios de Escritorio remoto multiusuario y multiprocesador.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676117"
---
# <a name="thread-usage"></a><span data-ttu-id="bbc20-103">Uso de subprocesos</span><span class="sxs-lookup"><span data-stu-id="bbc20-103">Thread usage</span></span>

<span data-ttu-id="bbc20-104">Los subprocesos proporcionan una forma cómoda de permitir que una aplicación maximice el uso de los recursos de CPU en un sistema, especialmente en una configuración de varios procesadores.</span><span class="sxs-lookup"><span data-stu-id="bbc20-104">Threads provide a convenient way of allowing an application to maximize its usage of CPU resources in a system, especially in a multiple processor configuration.</span></span> <span data-ttu-id="bbc20-105">Sin embargo, en un entorno de Servicios de Escritorio remoto, varios usuarios pueden ejecutar aplicaciones multiproceso y todos los subprocesos de todos los usuarios compiten por los recursos de CPU centrales de ese sistema.</span><span class="sxs-lookup"><span data-stu-id="bbc20-105">In a Remote Desktop Services environment, however, multiple users can be running multithreaded applications, and all of the threads for all of the users compete for the central CPU resources of that system.</span></span> <span data-ttu-id="bbc20-106">Teniendo esto en cuenta, debe optimizar y equilibrar el uso de subprocesos de aplicación para un entorno de Servicios de Escritorio remoto multiusuario y multiprocesador.</span><span class="sxs-lookup"><span data-stu-id="bbc20-106">With this in mind, you should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span> <span data-ttu-id="bbc20-107">Aunque una aplicación multiproceso mal diseñada con subprocesos inactivos o desperdiciados podría funcionar adecuadamente en un equipo cliente, la misma aplicación podría no funcionar bien en un servidor de Servicios de Escritorio remoto multiusuario.</span><span class="sxs-lookup"><span data-stu-id="bbc20-107">While a poorly designed multithreaded application with idle or wasted threads might perform adequately on a client computer, the same application might not perform well on a multiuser Remote Desktop Services server.</span></span>

 

 




