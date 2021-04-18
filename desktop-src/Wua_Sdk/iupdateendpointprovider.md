---
description: Contiene el método utilizado para obtener un punto de conexión que se utiliza para conectarse a un servicio.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Interfaz IUpdateEndpointProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 81e9481f5233fac05e7fa7bdf3afa53c4c55513a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715277"
---
# <a name="iupdateendpointprovider-interface"></a><span data-ttu-id="54adc-103">Interfaz IUpdateEndpointProvider</span><span class="sxs-lookup"><span data-stu-id="54adc-103">IUpdateEndpointProvider interface</span></span>

<span data-ttu-id="54adc-104">Contiene el método utilizado para obtener un punto de conexión que se utiliza para conectarse a un servicio.</span><span class="sxs-lookup"><span data-stu-id="54adc-104">Contains the method used to get an endpoint that is used to connect to a service.</span></span> <span data-ttu-id="54adc-105">Esta interfaz se implementa al escribir un proveedor de extremos.</span><span class="sxs-lookup"><span data-stu-id="54adc-105">This interface is implemented when writing an endpoint provider.</span></span>

## <a name="members"></a><span data-ttu-id="54adc-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="54adc-106">Members</span></span>

<span data-ttu-id="54adc-107">La interfaz **IUpdateEndpointProvider** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="54adc-107">The **IUpdateEndpointProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="54adc-108">**IUpdateEndpointProvider** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="54adc-108">**IUpdateEndpointProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="54adc-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="54adc-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="54adc-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="54adc-110">Methods</span></span>

<span data-ttu-id="54adc-111">La interfaz **IUpdateEndpointProvider** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="54adc-111">The **IUpdateEndpointProvider** interface has these methods.</span></span>



| <span data-ttu-id="54adc-112">Método</span><span class="sxs-lookup"><span data-stu-id="54adc-112">Method</span></span>                                                                       | <span data-ttu-id="54adc-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="54adc-113">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="54adc-114">**GetServiceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="54adc-114">**GetServiceEndpoint**</span></span>](iupdateendpointauthprovider-getserviceendpoint.md) | <span data-ttu-id="54adc-115">Solicita un extremo que se utiliza para conectarse a un servicio.</span><span class="sxs-lookup"><span data-stu-id="54adc-115">Requests an endpoint that is used to connect to a service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54adc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54adc-116">Remarks</span></span>

<span data-ttu-id="54adc-117">WUA llama al método [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) para iniciar el proceso de negociación.</span><span class="sxs-lookup"><span data-stu-id="54adc-117">WUA calls the [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) method to start the negotiation process.</span></span> <span data-ttu-id="54adc-118">Cuando se realiza la llamada, WUA pasa los tipos de token registrados y la implementación de esta interfaz devuelve los tipos de token que prefiere usar.</span><span class="sxs-lookup"><span data-stu-id="54adc-118">When the call is made, WUA passes in the registered token types, and the implementation of this interface returns the token types that it prefers to use.</span></span>

 

 
