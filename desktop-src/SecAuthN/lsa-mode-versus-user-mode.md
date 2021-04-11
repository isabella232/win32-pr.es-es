---
description: Cuando un paquete de seguridad SSP/AP funciona como un paquete de autenticación, se carga en el espacio de procesos de la autoridad de seguridad local (LSA) y se dice que está en modo LSA.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: Modo LSA frente al modo usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8fadde30fe60c38a2b8ccb1f158d94ec7d5603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083154"
---
# <a name="lsa-mode-vs-user-mode"></a><span data-ttu-id="cbd31-103">Modo LSA frente al modo usuario</span><span class="sxs-lookup"><span data-stu-id="cbd31-103">LSA Mode vs. User Mode</span></span>

<span data-ttu-id="cbd31-104">Cuando un [*paquete de seguridad*](../secgloss/s-gly.md) SSP/AP funciona como un [*paquete de autenticación*](../secgloss/a-gly.md), se carga en el espacio de procesos de la autoridad de [*seguridad local*](../secgloss/l-gly.md) (LSA) y se dice que está en modo LSA.</span><span class="sxs-lookup"><span data-stu-id="cbd31-104">When an SSP/AP [*security package*](../secgloss/s-gly.md) is functioning as an [*authentication package*](../secgloss/a-gly.md), it is loaded into the process space of the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) and is said to be in LSA mode.</span></span> <span data-ttu-id="cbd31-105">Las aplicaciones de inicio de sesión acceden a la funcionalidad del paquete de autenticación mediante las [funciones de inicio de sesión](authentication-functions.md)</span><span class="sxs-lookup"><span data-stu-id="cbd31-105">Logon applications access authentication package functionality using the [LSA Logon Functions](authentication-functions.md).</span></span> <span data-ttu-id="cbd31-106">Los desarrolladores pueden usar funciones de compatibilidad con LSA disponibles únicamente para los paquetes de seguridad de modo LSA para implementar paquetes de autenticación más sofisticados que los admitidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="cbd31-106">Developers can use LSA support functions available only to LSA-mode security packages to implement more sophisticated authentication packages than previously supported.</span></span>

<span data-ttu-id="cbd31-107">Cuando un [*paquete de seguridad*](../secgloss/s-gly.md) proporciona servicios de seguridad a una aplicación cliente/servidor, se carga en los procesos de cliente y servidor y se dice que está en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="cbd31-107">When a [*security package*](../secgloss/s-gly.md) provides security services to a client/server application, it is loaded into the client and server processes and is said to be in user mode.</span></span> <span data-ttu-id="cbd31-108">Las aplicaciones cliente/servidor obtienen acceso a los servicios de soporte técnico de seguridad del paquete de seguridad mediante la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cbd31-108">Client/server applications access the security package's security support services using Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI).</span></span>

<span data-ttu-id="cbd31-109">La compatibilidad de LSA con SSP/APs incluye funciones que las instancias del modo de usuario y el modo LSA de un paquete de seguridad pueden usar para comunicarse.</span><span class="sxs-lookup"><span data-stu-id="cbd31-109">LSA support for SSP/APs includes functions that the LSA-mode and user-mode instances of a security package can use to communicate.</span></span> <span data-ttu-id="cbd31-110">Además, la instancia de modo de usuario de un paquete de seguridad puede delegar las solicitudes seleccionadas de información en la instancia de modo LSA del paquete.</span><span class="sxs-lookup"><span data-stu-id="cbd31-110">Additionally, the user-mode instance of a security package can delegate selected requests for information to the LSA-mode instance of the package.</span></span>

<span data-ttu-id="cbd31-111">Para obtener más información sobre cómo se inicializan los paquetes de seguridad para cada modo, consulte [inicialización en modo LSA](lsa-mode-initialization.md) y [inicialización en modo usuario](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="cbd31-111">For details about how security packages are initialized for each mode, see [LSA-mode Initialization](lsa-mode-initialization.md) and [User-mode Initialization](user-mode-initialization.md).</span></span>

 

 
