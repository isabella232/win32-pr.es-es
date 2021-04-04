---
title: delete iplisten
description: Especifica una dirección IPv4 o IPv6 que se va a eliminar de la lista de escucha de IP.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- eliminar iplisten HTTP
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104076977"
---
# <a name="delete-iplisten"></a><span data-ttu-id="f3ca3-104">delete iplisten</span><span class="sxs-lookup"><span data-stu-id="f3ca3-104">delete iplisten</span></span>

<span data-ttu-id="f3ca3-105">Especifica una dirección IPv4 o IPv6 que se va a eliminar de la lista de escucha de IP.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-105">Specifies an IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="f3ca3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3ca3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3ca3-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ Address = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="f3ca3-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[address=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="f3ca3-108">Especifica la dirección IPv4 o IPv6 que se va a eliminar de la lista de escucha de IP.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-108">Specifies the IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3ca3-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3ca3-109">Remarks</span></span>

<span data-ttu-id="f3ca3-110">Elimina una dirección IP de la lista de escucha de IP.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-110">Deletes an IP address to the IP listen list.</span></span> <span data-ttu-id="f3ca3-111">No incluye el número de puerto.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-111">This does not include the port number.</span></span> <span data-ttu-id="f3ca3-112">La lista de escucha de IP se utiliza para establecer el ámbito de la lista de direcciones a las que se enlaza el servicio HTTP.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="f3ca3-113">"0.0.0.0" significa cualquier dirección IPv4 y "::" significa cualquier dirección IPv6.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="f3ca3-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f3ca3-114">Examples</span></span>

<span data-ttu-id="f3ca3-115">**eliminar dirección iplisten = fe80:: 1**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-115">**delete iplisten address=fe80::1**</span></span>

<span data-ttu-id="f3ca3-116">**Delete iplisten Address = pág**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-116">**delete iplisten address=1.1.1.1**</span></span>

<span data-ttu-id="f3ca3-117">**eliminar dirección iplisten = 0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-117">**delete iplisten address=0.0.0.0**</span></span>

<span data-ttu-id="f3ca3-118">**eliminar dirección iplisten =::**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-118">**delete iplisten address=::**</span></span>

 

 




