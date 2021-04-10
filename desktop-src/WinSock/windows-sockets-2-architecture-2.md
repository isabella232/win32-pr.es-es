---
description: La arquitectura de Windows Sockets 2 (Winsock) es compatible con la arquitectura de Windows Open System (WOSA).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Arquitectura de Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155261"
---
# <a name="windows-sockets-2-architecture"></a><span data-ttu-id="98283-103">Arquitectura de Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="98283-103">Windows Sockets 2 Architecture</span></span>

<span data-ttu-id="98283-104">La arquitectura de Windows Sockets 2 es compatible con la arquitectura de Windows Open System (WOSA), como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="98283-104">The Windows Sockets 2 architecture is compliant with the Windows Open System Architecture (WOSA), as illustrated below:</span></span>

![arquitectura de Windows Sockets 2](images/ovrvw2-1.png)

<span data-ttu-id="98283-106">Winsock define una interfaz de proveedor de servicios estándar (SPI) entre la interfaz de programación de aplicaciones (API), con sus funciones exportadas desde WS2 \_32.dll y las pilas de protocolos.</span><span class="sxs-lookup"><span data-stu-id="98283-106">Winsock defines a standard service provider interface (SPI) between the application programming interface (API), with its functions exported from WS2\_32.dll and the protocol stacks.</span></span> <span data-ttu-id="98283-107">Por lo tanto, la compatibilidad con Winsock no se limita a las pilas del protocolo TCP/IP, como es el caso de Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="98283-107">Consequently, Winsock support is not limited to TCP/IP protocol stacks as is the case for Windows Sockets 1.1.</span></span>

<span data-ttu-id="98283-108">Con la arquitectura de Windows Sockets 2, no es necesario o deseable, para que los proveedores de pila suministren su propia implementación de WS2 \_32.dll, ya que un único WS2 \_32.dll debe funcionar en todas las pilas.</span><span class="sxs-lookup"><span data-stu-id="98283-108">With the Windows Sockets 2 architecture, it is not necessary or desirable, for stack vendors to supply their own implementation of WS2\_32.dll, since a single WS2\_32.dll must work across all stacks.</span></span> <span data-ttu-id="98283-109">El \_32.dll WS2 y las correcciones de compatibilidad (shim) se deben ver de la misma manera que un componente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="98283-109">The WS2\_32.dll and compatibility shims should be viewed in the same way as an operating system component.</span></span>

 

 



