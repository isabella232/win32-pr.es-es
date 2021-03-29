---
description: Una vez creado el proveedor de red o el administrador de credenciales, debe registrarlo en el sistema.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Registro de proveedores de red y administradores de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277143"
---
# <a name="registering-network-providers-and-credential-managers"></a><span data-ttu-id="5c625-103">Registro de proveedores de red y administradores de credenciales</span><span class="sxs-lookup"><span data-stu-id="5c625-103">Registering Network Providers and Credential Managers</span></span>

<span data-ttu-id="5c625-104">Una vez creado el proveedor de red o el administrador de credenciales, debe registrarlo en el sistema.</span><span class="sxs-lookup"><span data-stu-id="5c625-104">After you have created your network provider or credential manager, you must register it with the system.</span></span> <span data-ttu-id="5c625-105">Esto es necesario para que el MPR sepa qué proveedores de red están instalados.</span><span class="sxs-lookup"><span data-stu-id="5c625-105">This is necessary so the MPR will know what network providers are installed.</span></span> <span data-ttu-id="5c625-106">Cuando se inicia el MPR, comprueba el registro y carga los proveedores de red o administradores de credenciales que encuentra.</span><span class="sxs-lookup"><span data-stu-id="5c625-106">When the MPR starts, it checks the registry and loads any network providers or credential managers it finds.</span></span>

<span data-ttu-id="5c625-107">Dado que los proveedores de red y los administradores de credenciales están relacionados, se registran en las mismas subclaves del registro.</span><span class="sxs-lookup"><span data-stu-id="5c625-107">Because network providers and credential managers are related, they are registered in the same subkeys of the registry.</span></span> <span data-ttu-id="5c625-108">De hecho, las dll de proveedor de red también pueden ser administradores de credenciales.</span><span class="sxs-lookup"><span data-stu-id="5c625-108">In fact, network provider DLLs can also be credential managers.</span></span>

<span data-ttu-id="5c625-109">Para obtener información detallada acerca de las claves del registro que debe crear para el proveedor de red o el administrador de credenciales, consulte [claves del registro de autenticación](authentication-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="5c625-109">For detailed information about the registry keys you should create for your network provider or credential manager, see [Authentication Registry Keys](authentication-registry-keys.md).</span></span>

 

 



