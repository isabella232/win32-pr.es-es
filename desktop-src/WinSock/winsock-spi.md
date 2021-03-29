---
description: Interfaz del proveedor de servicios (SPI) de Windows Sockets (Winsock).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: SPI de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652721"
---
# <a name="winsock-spi"></a><span data-ttu-id="76ebb-103">SPI de Winsock</span><span class="sxs-lookup"><span data-stu-id="76ebb-103">Winsock SPI</span></span>

<span data-ttu-id="76ebb-104">La interfaz del proveedor de servicios Winsock, o Winsock SPI, es una disciplina especializada de Winsock que se usa para crear proveedores. los proveedores de transporte, como las pilas de protocolo TCP/IP o IPX/SPX, usan el SPI de Winsock, al igual que los proveedores de espacios de nombres, como el sistema de nombres de dominio (DNS) de Internet.</span><span class="sxs-lookup"><span data-stu-id="76ebb-104">The Winsock Service Provider Interface, or Winsock SPI, is a specialized discipline of Winsock used to create providers; transport providers such as TCP/IP or IPX/SPX protocol stacks use the Winsock SPI, as do namespace providers such as the Internet's Domain Naming System (DNS).</span></span>

<span data-ttu-id="76ebb-105">La programación de red tradicional, como permitir que las aplicaciones se comuniquen a través de la red, no requiere el uso de interfaces de Winsock SPI; Use las interfaces de [Winsock](winsock-reference.md) estándar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="76ebb-105">Traditional network programming, such as enabling applications to communicate over the network, does not require use of Winsock SPI interfaces; use standard [Winsock](winsock-reference.md) interfaces instead.</span></span>

 

<span data-ttu-id="76ebb-106">El SPI de Winsock usa la siguiente Convención de nomenclatura de prefijos de función.</span><span class="sxs-lookup"><span data-stu-id="76ebb-106">The Winsock SPI uses the following function prefix naming convention.</span></span>



| <span data-ttu-id="76ebb-107">Prefijo</span><span class="sxs-lookup"><span data-stu-id="76ebb-107">Prefix</span></span> | <span data-ttu-id="76ebb-108">Significado</span><span class="sxs-lookup"><span data-stu-id="76ebb-108">Meaning</span></span>                          | <span data-ttu-id="76ebb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="76ebb-109">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="76ebb-110">WSP</span><span class="sxs-lookup"><span data-stu-id="76ebb-110">WSP</span></span>    | <span data-ttu-id="76ebb-111">Proveedor de servicios de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="76ebb-111">Windows Sockets Service Provider</span></span> | <span data-ttu-id="76ebb-112">Puntos de entrada del proveedor de servicios de transporte</span><span class="sxs-lookup"><span data-stu-id="76ebb-112">Transport service provider entry points</span></span>           |
| <span data-ttu-id="76ebb-113">WPU</span><span class="sxs-lookup"><span data-stu-id="76ebb-113">WPU</span></span>    | <span data-ttu-id="76ebb-114">Llamada al proveedor de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="76ebb-114">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="76ebb-115">Ws2 \_32.dll puntos de entrada para proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="76ebb-115">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="76ebb-116">WSC</span><span class="sxs-lookup"><span data-stu-id="76ebb-116">WSC</span></span>    | <span data-ttu-id="76ebb-117">Configuración de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="76ebb-117">Windows Sockets Configuration</span></span>    | <span data-ttu-id="76ebb-118">WS2 \_32.dll puntos de entrada para applets de instalación</span><span class="sxs-lookup"><span data-stu-id="76ebb-118">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="76ebb-119">NSP</span><span class="sxs-lookup"><span data-stu-id="76ebb-119">NSP</span></span>    | <span data-ttu-id="76ebb-120">Proveedor de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="76ebb-120">Namespace Provider</span></span>               | <span data-ttu-id="76ebb-121">Puntos de entrada del proveedor de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="76ebb-121">Namespace provider entry points</span></span>                   |



 

 

 



