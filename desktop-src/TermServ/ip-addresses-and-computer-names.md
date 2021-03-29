---
title: Direcciones IP y nombres de equipo
description: No es seguro suponer que el nombre del equipo o la dirección IP que se asignen al equipo se asocian a un único usuario, dado que varios usuarios pueden iniciar sesión a la vez en un servidor host de sesión de Escritorio remoto.
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359327"
---
# <a name="ip-addresses-and-computer-names"></a><span data-ttu-id="f2c4e-103">Direcciones IP y nombres de equipo</span><span class="sxs-lookup"><span data-stu-id="f2c4e-103">IP addresses and computer names</span></span>

<span data-ttu-id="f2c4e-104">Varios usuarios pueden iniciar sesión simultáneamente en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="f2c4e-104">Multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="f2c4e-105">Por lo tanto, no es seguro suponer que el nombre del equipo o la dirección IP asignada al equipo están asociados a un solo usuario.</span><span class="sxs-lookup"><span data-stu-id="f2c4e-105">Consequently, it is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user.</span></span> <span data-ttu-id="f2c4e-106">Esto difiere de un entorno de Windows de un solo usuario, en el que solo un usuario inicia sesión a la vez.</span><span class="sxs-lookup"><span data-stu-id="f2c4e-106">This differs from a single-user Windows environment, in which only one user is logged on at a time.</span></span>

<span data-ttu-id="f2c4e-107">Las aplicaciones que usan el nombre de equipo o la dirección IP para las licencias o como medio para identificar una iteración de la aplicación en la red no funcionarán correctamente en un entorno de Servicios de Escritorio remoto, porque el nombre de equipo o la dirección IP del servidor se pueden asociar a muchos usuarios.</span><span class="sxs-lookup"><span data-stu-id="f2c4e-107">Applications that use the computer name or IP address for licensing or as a means of identifying an iteration of the application on the network will not work properly in a Remote Desktop Services environment, because the server's computer name or IP address can be associated with many users.</span></span>

<span data-ttu-id="f2c4e-108">En un entorno de Servicios de Escritorio remoto, cada terminal de cliente o emulador de terminal tiene una dirección IP y un nombre de equipo independientes.</span><span class="sxs-lookup"><span data-stu-id="f2c4e-108">In a Remote Desktop Services environment, each client terminal or terminal emulator has a separate IP address and computer name.</span></span> <span data-ttu-id="f2c4e-109">Para recuperar la dirección IP y el nombre de equipo de un cliente, llame a la función [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) .</span><span class="sxs-lookup"><span data-stu-id="f2c4e-109">To retrieve the IP address and computer name of a client, call the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span> <span data-ttu-id="f2c4e-110">Otras funciones que recuperan estas direcciones de red y nombres de equipo recuperan el nombre y la dirección del servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f2c4e-110">Other functions that retrieve these network addresses and computer names retrieve the name and address of the RD Session Host server.</span></span> <span data-ttu-id="f2c4e-111">Por ejemplo, la función [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) devuelve el nombre de equipo del servidor.</span><span class="sxs-lookup"><span data-stu-id="f2c4e-111">For example, the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function returns the computer name of the server.</span></span>

 

 