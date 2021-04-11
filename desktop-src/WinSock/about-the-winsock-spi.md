---
description: Winsock proporciona una interfaz de proveedor de servicios para crear servicios Winsock, lo que se conoce comúnmente como el SPI de Winsock.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: Acerca de Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe70d5d381505085e2794a57a1183e8bec505917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154303"
---
# <a name="about-the-winsock-spi"></a><span data-ttu-id="1e7ff-103">Acerca de Winsock SPI</span><span class="sxs-lookup"><span data-stu-id="1e7ff-103">About the Winsock SPI</span></span>

<span data-ttu-id="1e7ff-104">Winsock proporciona una interfaz de proveedor de servicios para crear servicios Winsock, lo que se conoce comúnmente como el SPI de Winsock.</span><span class="sxs-lookup"><span data-stu-id="1e7ff-104">Winsock provides a Service Provider Interface for creating Winsock services, commonly referred to as the Winsock SPI.</span></span> <span data-ttu-id="1e7ff-105">Existen dos tipos de proveedores de servicios: proveedores de transporte y proveedores de espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="1e7ff-105">Two types of service providers exist: transport providers and namespace providers.</span></span> <span data-ttu-id="1e7ff-106">Entre los ejemplos de proveedores de transporte se incluyen pilas de protocolos como TCP/IP o IPX/SPX, mientras que un ejemplo de proveedor de espacio de nombres sería una interfaz al sistema de nombres de dominio (DNS) de Internet.</span><span class="sxs-lookup"><span data-stu-id="1e7ff-106">Examples of transport providers include protocol stacks such as TCP/IP or IPX/SPX, while an example of a namespace provider would be an interface to the Internet's Domain Naming System (DNS).</span></span> <span data-ttu-id="1e7ff-107">Las secciones independientes de la especificación de la interfaz del proveedor de servicios se aplican a cada tipo de proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="1e7ff-107">Separate sections of the service provider interface specification apply to each type of service provider.</span></span>

<span data-ttu-id="1e7ff-108">Los proveedores de servicios de [transporte](transport-service-providers-2.md) y de [espacio de nombres](name-space-service-providers-2.md) se deben registrar con el \_32.dll Ws2 en el momento en que se instalan.</span><span class="sxs-lookup"><span data-stu-id="1e7ff-108">[Transport](transport-service-providers-2.md) and [namespace](name-space-service-providers-2.md) service providers must be registered with the Ws2\_32.dll at the time they are installed.</span></span> <span data-ttu-id="1e7ff-109">Este registro solo debe realizarse una vez para cada proveedor, ya que la información necesaria se conserva en el almacenamiento persistente.</span><span class="sxs-lookup"><span data-stu-id="1e7ff-109">This registration need only be done once for each provider as the necessary information is retained in persistent storage.</span></span>

 

 



