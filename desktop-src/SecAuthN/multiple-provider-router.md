---
description: El enrutador de varios proveedores (MPR) controla la comunicación entre el sistema operativo Windows y los proveedores de red instalados. Permite a Windows presentar al usuario una red integrada.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Enrutador de varios proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911865"
---
# <a name="multiple-provider-router"></a><span data-ttu-id="aaadc-104">Enrutador de varios proveedores</span><span class="sxs-lookup"><span data-stu-id="aaadc-104">Multiple Provider Router</span></span>

<span data-ttu-id="aaadc-105">El [*enrutador de varios proveedores*](../secgloss/m-gly.md) (MPR) controla la comunicación entre el sistema operativo Windows y los proveedores de red instalados.</span><span class="sxs-lookup"><span data-stu-id="aaadc-105">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication between the Windows operating system and the installed network providers.</span></span> <span data-ttu-id="aaadc-106">Permite a Windows presentar al usuario una red integrada.</span><span class="sxs-lookup"><span data-stu-id="aaadc-106">It enables Windows to present an integrated network to the user.</span></span>

<span data-ttu-id="aaadc-107">Cuando se inicia el MPR, comprueba el registro para determinar qué proveedores de red están instalados en el sistema y el orden en el que deben recorrerse.</span><span class="sxs-lookup"><span data-stu-id="aaadc-107">When the MPR starts, it checks the registry to determine which network providers are installed on the system and the order they should be cycled through.</span></span> <span data-ttu-id="aaadc-108">Carga todas las dll de proveedor de red registradas y las utiliza para procesar las llamadas de WNet posteriores realizadas por la interfaz de usuario u otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="aaadc-108">It loads all registered network provider DLLs and uses them to process subsequent WNet calls made by the user interface or other applications.</span></span>

<span data-ttu-id="aaadc-109">Para obtener más información acerca de las funciones de WNet, consulte [redes de Windows](../wnet/windows-networking-wnet-.md).</span><span class="sxs-lookup"><span data-stu-id="aaadc-109">For more information about WNet functions, see [Windows Networking](../wnet/windows-networking-wnet-.md).</span></span>

 

 
