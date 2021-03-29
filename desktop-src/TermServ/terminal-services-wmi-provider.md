---
title: Servicios de Escritorio remoto proveedor WMI
description: El proveedor WMI de Servicios de Escritorio remoto proporciona acceso mediante programación a la información y la configuración que se exponen en el complemento configuración/conexiones de Microsoft Management Console (MMC) de Servicios de Escritorio remoto.
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de Servicios de Escritorio remoto, proveedor WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d947db18c0cde63bcb6c4c3954fc9811e0f0f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077915"
---
# <a name="remote-desktop-services-wmi-provider"></a><span data-ttu-id="5c233-104">Servicios de Escritorio remoto proveedor WMI</span><span class="sxs-lookup"><span data-stu-id="5c233-104">Remote Desktop Services WMI provider</span></span>

<span data-ttu-id="5c233-105">El proveedor WMI de Servicios de Escritorio remoto proporciona acceso mediante programación a la información y la configuración que se exponen en el complemento configuración/conexiones de Microsoft Management Console (MMC) de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5c233-105">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

<span data-ttu-id="5c233-106">El proceso de administración de Windows (Winmgmt.exe) carga la DLL del proveedor cuando un cliente realiza una solicitud al servidor.</span><span class="sxs-lookup"><span data-stu-id="5c233-106">The provider DLL is loaded by the Windows Management process (Winmgmt.exe) when a client makes a request to the server.</span></span> <span data-ttu-id="5c233-107">La administración es posible mediante el uso de los métodos de proveedor.</span><span class="sxs-lookup"><span data-stu-id="5c233-107">Administration is possible by using the provider methods.</span></span> <span data-ttu-id="5c233-108">El proveedor se registra como una instancia de y un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="5c233-108">The provider is registered as both an instance and a method provider.</span></span>

<span data-ttu-id="5c233-109">El proveedor de WMI Servicios de Escritorio remoto se ha implementado como un proveedor dinámico derivado de la clase base del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) , heredando todas sus propiedades y métodos, y una biblioteca de vínculos dinámicos en proceso.</span><span class="sxs-lookup"><span data-stu-id="5c233-109">The Remote Desktop Services WMI provider has been implemented as a dynamic provider derived from the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) base class, inheriting all of its properties and methods, and an in-process dynamic link library.</span></span>

<span data-ttu-id="5c233-110">Para obtener más información, vea la [Referencia del proveedor de WMI de servicios de escritorio remoto](terminal-services-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="5c233-110">For more information, see the [Remote Desktop Services WMI Provider reference](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c233-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c233-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c233-112">Servicios de Escritorio remoto referencia del proveedor WMI</span><span class="sxs-lookup"><span data-stu-id="5c233-112">Remote Desktop Services WMI Provider Reference</span></span>](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 