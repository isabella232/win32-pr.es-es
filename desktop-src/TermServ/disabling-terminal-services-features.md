---
title: Deshabilitar características de Servicios de Escritorio remoto
description: Para mejorar la seguridad, puede optar por deshabilitar Servicios de Escritorio remoto características.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/01/2020
ms.locfileid: "103995811"
---
# <a name="disabling-remote-desktop-services-features"></a><span data-ttu-id="52fe0-103">Deshabilitar características de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="52fe0-103">Disabling Remote Desktop Services features</span></span>

<span data-ttu-id="52fe0-104">Para mejorar la seguridad, puede optar por deshabilitar Servicios de Escritorio remoto características como el redireccionamiento del portapapeles y la redirección de la impresora para los clientes que se conectan a los servidores host de sesión Escritorio remoto (host de sesión de escritorio remoto) mediante el control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="52fe0-104">For enhanced security, you might choose to disable Remote Desktop Services features such as clipboard redirection and printer redirection for clients that connect to Remote Desktop Session Host (RD Session Host) servers using the Remote Desktop ActiveX Control.</span></span>

<span data-ttu-id="52fe0-105">**Para deshabilitar las características de Servicios de Escritorio remoto**</span><span class="sxs-lookup"><span data-stu-id="52fe0-105">**To disable Remote Desktop Services features**</span></span>

1.  <span data-ttu-id="52fe0-106">Edite el registro del equipo cliente y agregue las claves siguientes:</span><span class="sxs-lookup"><span data-stu-id="52fe0-106">Edit the registry of the client computer and add the following keys:</span></span>

    -   <span data-ttu-id="52fe0-107">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisableClipboardRedirection**</span><span class="sxs-lookup"><span data-stu-id="52fe0-107">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableClipboardRedirection**</span></span>
    -   <span data-ttu-id="52fe0-108">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisableDriveRedirection**</span><span class="sxs-lookup"><span data-stu-id="52fe0-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableDriveRedirection**</span></span>
    -   <span data-ttu-id="52fe0-109">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisablePrinterRedirection**</span><span class="sxs-lookup"><span data-stu-id="52fe0-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisablePrinterRedirection**</span></span>

2.  <span data-ttu-id="52fe0-110">Establezca el valor de ambas claves en **reg \_ DWORD** 1.</span><span class="sxs-lookup"><span data-stu-id="52fe0-110">Set the value of both keys to **REG\_DWORD** 1.</span></span>

 

 




