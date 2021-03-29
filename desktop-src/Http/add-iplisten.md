---
title: add iplisten
description: Especifica una dirección IPv4 o IPv6 que se va a agregar a la lista de escucha de IP.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- Agregar iplisten HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6090d3044be134035edb5f1f42a9790859d0301d
ms.sourcegitcommit: 243954e695c6ab5372b2935b095c3cd0b1202e16
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2020
ms.locfileid: "103994999"
---
# <a name="add-iplisten"></a><span data-ttu-id="63b81-104">add iplisten</span><span class="sxs-lookup"><span data-stu-id="63b81-104">add iplisten</span></span>

<span data-ttu-id="63b81-105">Especifica una dirección IPv4 o IPv6 que se va a agregar a la lista de escucha de IP.</span><span class="sxs-lookup"><span data-stu-id="63b81-105">Specifies an IPv4 or IPv6 address to be added to the IP listen list.</span></span>

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="63b81-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63b81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63b81-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ IPAddress = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="63b81-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="63b81-108">Especifica la dirección IPv4 o IPv6 que se va a agregar a la lista de escucha de IP.</span><span class="sxs-lookup"><span data-stu-id="63b81-108">Specifies the IPv4 or IPv6 address to be added to the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63b81-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63b81-109">Remarks</span></span>

<span data-ttu-id="63b81-110">Agrega una nueva dirección IP a la lista de escucha de IP.</span><span class="sxs-lookup"><span data-stu-id="63b81-110">Adds a new IP address to the IP listen list.</span></span> <span data-ttu-id="63b81-111">No incluye el número de puerto.</span><span class="sxs-lookup"><span data-stu-id="63b81-111">This does not include the port number.</span></span> <span data-ttu-id="63b81-112">La lista de escucha de IP se utiliza para establecer el ámbito de la lista de direcciones a las que se enlaza el servicio HTTP.</span><span class="sxs-lookup"><span data-stu-id="63b81-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="63b81-113">"0.0.0.0" significa cualquier dirección IPv4 y "::" significa cualquier dirección IPv6.</span><span class="sxs-lookup"><span data-stu-id="63b81-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="63b81-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="63b81-114">Examples</span></span>

<span data-ttu-id="63b81-115">**add iplisten ipaddress=fe80::1**</span><span class="sxs-lookup"><span data-stu-id="63b81-115">**add iplisten ipaddress=fe80::1**</span></span>

<span data-ttu-id="63b81-116">**add iplisten ipaddress=1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="63b81-116">**add iplisten ipaddress=1.1.1.1**</span></span>

<span data-ttu-id="63b81-117">**add iplisten ipaddress=0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="63b81-117">**add iplisten ipaddress=0.0.0.0**</span></span>

<span data-ttu-id="63b81-118">**add iplisten ipaddress=::**</span><span class="sxs-lookup"><span data-stu-id="63b81-118">**add iplisten ipaddress=::**</span></span>

 

 




