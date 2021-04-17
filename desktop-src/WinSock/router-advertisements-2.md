---
description: El contenido de los anuncios de enrutador IPv6 se deriva automáticamente de las rutas publicadas en la tabla de enrutamiento. Las rutas no publicadas se usan para el enrutamiento, pero se omiten cuando se crean anuncios de enrutador.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: Anuncios de enrutador IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706186"
---
# <a name="ipv6-router-advertisements"></a><span data-ttu-id="0e377-104">Anuncios de enrutador IPv6</span><span class="sxs-lookup"><span data-stu-id="0e377-104">IPv6 Router Advertisements</span></span>

<span data-ttu-id="0e377-105">El contenido de los anuncios de enrutador IPv6 se deriva automáticamente de las rutas publicadas en la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="0e377-105">The content of IPv6 router advertisements is automatically derived from the published routes in the routing table.</span></span> <span data-ttu-id="0e377-106">Las rutas no publicadas se usan para el enrutamiento, pero se omiten cuando se crean anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="0e377-106">Nonpublished routes are used for routing but are ignored when constructing router advertisements.</span></span>

<span data-ttu-id="0e377-107">Los anuncios de enrutador para IPv6 siempre contienen una opción de dirección de nivel de vínculo de origen y una opción de MTU.</span><span class="sxs-lookup"><span data-stu-id="0e377-107">Router advertisements for IPv6 always contain a source link-layer address option and an MTU option.</span></span> <span data-ttu-id="0e377-108">El valor de la opción MTU se toma de la MTU de vínculo actual de la interfaz de envío.</span><span class="sxs-lookup"><span data-stu-id="0e377-108">The value for the MTU option is taken from the sending interface's current link MTU.</span></span> <span data-ttu-id="0e377-109">Este valor se puede cambiar con el comando IFC MTU de IPv6.</span><span class="sxs-lookup"><span data-stu-id="0e377-109">This value can be changed with the ipv6 ifc mtu command.</span></span>

<span data-ttu-id="0e377-110">El anuncio de enrutador solo tiene una duración de enrutador distinto de cero si hay una ruta predeterminada publicada.</span><span class="sxs-lookup"><span data-stu-id="0e377-110">The router advertisement only has a nonzero router lifetime if there is a published default route.</span></span> <span data-ttu-id="0e377-111">Una ruta predeterminada es una ruta para el prefijo de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="0e377-111">A default route is a route for the zero-length prefix.</span></span>

<span data-ttu-id="0e377-112">Las rutas en vínculo publicadas dan como resultado opciones de información de prefijo en anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="0e377-112">Published on-link routes result in prefix information options in router advertisements.</span></span> <span data-ttu-id="0e377-113">Si el prefijo en vínculo tiene 64 bits, la opción de información de prefijo tiene el conjunto de bits L y un y los hosts que lo reciben configurarán las direcciones de forma autoconfigurada.</span><span class="sxs-lookup"><span data-stu-id="0e377-113">If the on-link prefix has 64 bits, the prefix information option has both the L and A bits set and hosts receiving it will autoconfigure addresses.</span></span>

<span data-ttu-id="0e377-114">Una interfaz que envía anuncios de enrutador también configurará automáticamente las direcciones para sí misma basándose en las opciones de información de prefijo que envía.</span><span class="sxs-lookup"><span data-stu-id="0e377-114">An interface that sends router advertisements will also autoconfigure addresses for itself based on the prefix information options that it sends.</span></span>

<span data-ttu-id="0e377-115">Se recomienda una duración no caducante finita en todas las rutas publicadas (por ejemplo, 30 minutos).</span><span class="sxs-lookup"><span data-stu-id="0e377-115">A finite nonaging lifetime on all published routes (for example, 30 minutes) is recommended.</span></span> <span data-ttu-id="0e377-116">Si decide retirar una ruta, puede cambiar la ruta para que tenga una duración de caducidad.</span><span class="sxs-lookup"><span data-stu-id="0e377-116">If you decide to retract a route, you can change the route to have an aging lifetime.</span></span> <span data-ttu-id="0e377-117">La ruta va a vencer en el transcurso de varios anuncios de enrutador y después desaparecerá del enrutador y de los hosts que reciban los anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="0e377-117">The route will age over the course of several router advertisements and then disappear from both the router and any hosts receiving the router advertisements.</span></span>

<span data-ttu-id="0e377-118">Las rutas que hospedan la búsqueda a través de anuncios de enrutador caducan y no se publican.</span><span class="sxs-lookup"><span data-stu-id="0e377-118">Routes that hosts find through router advertisements age and are not published.</span></span> <span data-ttu-id="0e377-119">Se trata también de la configuración de la antigüedad de los anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="0e377-119">Addresses autoconfigured from router advertisements age as well.</span></span>

 

 



