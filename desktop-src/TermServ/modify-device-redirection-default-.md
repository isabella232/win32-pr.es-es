---
title: Modificar el valor predeterminado de redirección del dispositivo
description: Dado que Escritorio remoto servidores de puerta de enlace intentan exigir directivas de redirección de dispositivos seguras antes de pasar la conexión de cliente a un servidor host de sesión Escritorio remoto, puede que tenga que deshabilitar este valor predeterminado en algunos casos.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903548"
---
# <a name="modify-device-redirection-default"></a><span data-ttu-id="b8719-103">Modificar el valor predeterminado de redirección del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b8719-103">Modify Device Redirection Default</span></span>

<span data-ttu-id="b8719-104">Dado que Escritorio remoto servidores de puerta de enlace intentan exigir directivas de redirección de dispositivos seguras antes de pasar la conexión de cliente a un servidor host de sesión Escritorio remoto, puede que tenga que deshabilitar este valor predeterminado en algunos casos.</span><span class="sxs-lookup"><span data-stu-id="b8719-104">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

<span data-ttu-id="b8719-105">En Windows Server 2008 R2 y versiones posteriores, los servidores de puerta de enlace de Escritorio remoto de forma predeterminada intentarán aplicar directivas seguras de redireccionamiento de dispositivos antes de pasar la conexión de cliente a un servidor host de sesión Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b8719-105">On Windows Server 2008 R2 and later, Remote Desktop Gateway servers will by default attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server.</span></span> <span data-ttu-id="b8719-106">Sin embargo, esta característica no es compatible con algunos servidores.</span><span class="sxs-lookup"><span data-stu-id="b8719-106">However, this feature is not supported by some servers.</span></span> <span data-ttu-id="b8719-107">Por ejemplo, esto no se admite para las conexiones a las sesiones de la consola de Hyper-V y es posible que sea necesario deshabilitar el valor predeterminado para admitir la autenticación federada.</span><span class="sxs-lookup"><span data-stu-id="b8719-107">For example, this is not supported for connections to Hyper-V console sessions, and it may be necessary to disable the default to support federated authentication.</span></span> <span data-ttu-id="b8719-108">En estos casos, esta característica puede deshabilitarse mediante la creación de la siguiente clave del registro para permitir que las conexiones pasen.</span><span class="sxs-lookup"><span data-stu-id="b8719-108">In these cases, this feature can be disabled by creating the following registry key to allow connections to go through.</span></span>

<span data-ttu-id="b8719-109">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server Gateway \\ preRDPDisableRegKey**</span><span class="sxs-lookup"><span data-stu-id="b8719-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server Gateway\\preRDPDisableRegKey**</span></span>

<span data-ttu-id="b8719-110">Cuando exista esta clave, la puerta de enlace de Escritorio remoto no aplicará la redirección de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b8719-110">When this key exists, the Remote Desktop Gateway will not enforce device redirection.</span></span>

 

 




