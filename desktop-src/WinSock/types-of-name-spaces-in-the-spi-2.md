---
description: Los tres tipos de espacios de nombres de Windows Sockets (Winsock) SPI incluyen espacios de nombres dinámicos, estáticos y persistentes.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Tipos de espacios de nombres en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697481"
---
# <a name="types-of-namespaces-in-the-spi"></a><span data-ttu-id="1f833-103">Tipos de espacios de nombres en el SPI</span><span class="sxs-lookup"><span data-stu-id="1f833-103">Types of Namespaces in the SPI</span></span>

<span data-ttu-id="1f833-104">Hay tres tipos diferentes de espacios de nombres en los que se puede registrar un servicio:</span><span class="sxs-lookup"><span data-stu-id="1f833-104">There are three different types of namespaces in which a service could be registered:</span></span>

-   <span data-ttu-id="1f833-105">Dinámica</span><span class="sxs-lookup"><span data-stu-id="1f833-105">Dynamic</span></span>
-   <span data-ttu-id="1f833-106">estática</span><span class="sxs-lookup"><span data-stu-id="1f833-106">Static</span></span>
-   <span data-ttu-id="1f833-107">Persistente</span><span class="sxs-lookup"><span data-stu-id="1f833-107">Persistent</span></span>

<span data-ttu-id="1f833-108">Los espacios de nombres dinámicos permiten que los servicios se registren en el espacio de nombres sobre la marcha y para que los clientes detecten los servicios disponibles en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="1f833-108">Dynamic namespaces allow services to register with the namespace on the fly, and for clients to discover the available services at run time.</span></span> <span data-ttu-id="1f833-109">Los espacios de nombres dinámicos suelen basarse en difusiones para indicar la disponibilidad continua de un servicio de red.</span><span class="sxs-lookup"><span data-stu-id="1f833-109">Dynamic namespaces frequently rely on broadcasts to indicate the continued availability of a network service.</span></span> <span data-ttu-id="1f833-110">Algunos ejemplos de espacios de nombres dinámicos incluyen el espacio de nombres de SAP que se usa en un entorno de NetWare y el espacio de nombres NBP que usa AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="1f833-110">Examples of dynamic namespaces include the SAP namespace used within a NetWare environment and the NBP namespace used by AppleTalk.</span></span>

<span data-ttu-id="1f833-111">Los espacios de nombres estáticos requieren que todos los servicios se registren con anterioridad, es decir, cuando se crea el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="1f833-111">Static namespaces require all of the services to be registered ahead of time, that is, when the namespace is created.</span></span> <span data-ttu-id="1f833-112">El DNS es un ejemplo de un espacio de nombres estático.</span><span class="sxs-lookup"><span data-stu-id="1f833-112">The DNS is an example of a static namespace.</span></span> <span data-ttu-id="1f833-113">Aunque hay una manera de resolver nombres mediante programación, no hay ninguna manera de registrar los nombres mediante programación.</span><span class="sxs-lookup"><span data-stu-id="1f833-113">Although there is a programmatic way to resolve names, there is no programmatic way to register names.</span></span>

<span data-ttu-id="1f833-114">Los espacios de nombres persistentes permiten que los servicios se registren con el espacio de nombres sobre la marcha.</span><span class="sxs-lookup"><span data-stu-id="1f833-114">Persistent namespaces allow services to register with the namespace on the fly.</span></span> <span data-ttu-id="1f833-115">Sin embargo, a diferencia de los espacios de nombres dinámicos, los espacios de nombres persistentes conservan la información de registro en un almacenamiento no volátil donde permanece hasta el momento en que el servicio solicita que se quite.</span><span class="sxs-lookup"><span data-stu-id="1f833-115">Unlike dynamic namespaces however, persistent namespaces retain the registration information in nonvolatile storage where it remains until such time as the service requests that it be removed.</span></span> <span data-ttu-id="1f833-116">Los espacios de nombres persistentes son typified por servicios de directorio como X. 500 y NDS (servicio de directorio NetWare).</span><span class="sxs-lookup"><span data-stu-id="1f833-116">Persistent namespaces are typified by directory services such as X.500 and the NDS (NetWare Directory Service).</span></span> <span data-ttu-id="1f833-117">Estos entornos permiten agregar, eliminar y modificar las propiedades del servicio.</span><span class="sxs-lookup"><span data-stu-id="1f833-117">These environments allow the adding, deleting, and modification of service properties.</span></span> <span data-ttu-id="1f833-118">Además, el objeto de servicio que representa el servicio dentro del servicio de directorio podría tener una variedad de atributos asociados al servicio.</span><span class="sxs-lookup"><span data-stu-id="1f833-118">In addition, the service object representing the service within the directory service could have a variety of attributes associated with the service.</span></span> <span data-ttu-id="1f833-119">El atributo más importante para las aplicaciones cliente es la información de direccionamiento del servicio.</span><span class="sxs-lookup"><span data-stu-id="1f833-119">The most important attribute for client applications is the service's addressing information.</span></span>

 

 



