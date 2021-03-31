---
title: Usar la seguridad de Transport-Level en el cliente
description: El cliente especifica el modo en que el servidor suplanta al cliente cuando el cliente establece el enlace de cadenas.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- RPC llamada a procedimiento remoto, tareas, uso de la seguridad de nivel de transporte en el cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995551"
---
# <a name="using-transport-level-security-on-the-client"></a><span data-ttu-id="c080f-104">Usar la seguridad de Transport-Level en el cliente</span><span class="sxs-lookup"><span data-stu-id="c080f-104">Using Transport-Level Security on the Client</span></span>

<span data-ttu-id="c080f-105">El cliente especifica el modo en que el servidor suplanta al cliente cuando el cliente establece el enlace de cadenas.</span><span class="sxs-lookup"><span data-stu-id="c080f-105">The client specifies how the server impersonates the client when the client establishes the string binding.</span></span> <span data-ttu-id="c080f-106">Esta información de QOS se proporciona como una opción de extremo en el enlace de cadenas.</span><span class="sxs-lookup"><span data-stu-id="c080f-106">This QOS information is provided as an endpoint option in the string binding.</span></span> <span data-ttu-id="c080f-107">El cliente puede especificar el nivel de suplantación, seguimiento dinámico o estático y la marca de solo efectivo.</span><span class="sxs-lookup"><span data-stu-id="c080f-107">The client can specify the level of impersonation, dynamic or static tracking, and the effective-only flag.</span></span>

<span data-ttu-id="c080f-108">**Para proporcionar información de calidad de servicio para el servidor**</span><span class="sxs-lookup"><span data-stu-id="c080f-108">**To supply quality-of-service information for the server**</span></span>

1.  <span data-ttu-id="c080f-109">El cliente llama a [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) para crear las cadenas de componentes, incluidas las opciones de punto de conexión, en el contexto de enlace de cadena correcto.</span><span class="sxs-lookup"><span data-stu-id="c080f-109">The client calls [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) to create the component strings, including endpoint options, in the correct string-binding context.</span></span>
2.  <span data-ttu-id="c080f-110">El cliente llama a [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obtener un nuevo identificador de enlace y aplicar la información de calidad de servicio para el cliente.</span><span class="sxs-lookup"><span data-stu-id="c080f-110">The client calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain a new binding handle and to apply the quality-of-service information for the client.</span></span>
3.  <span data-ttu-id="c080f-111">El cliente realiza llamadas a procedimientos remotos mediante el identificador.</span><span class="sxs-lookup"><span data-stu-id="c080f-111">The client makes remote procedure calls using the handle.</span></span>

<span data-ttu-id="c080f-112">Microsoft RPC solo admite características de seguridad de Windows en [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) y [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="c080f-112">Microsoft RPC supports Windows security features only on [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) and [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="c080f-113">Se omiten las opciones de seguridad para otros transportes.</span><span class="sxs-lookup"><span data-stu-id="c080f-113">Security options for other transports are ignored.</span></span>

<span data-ttu-id="c080f-114">El cliente puede asociar los siguientes parámetros de seguridad al enlace para el transporte de canalización con nombre [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) o [**ncalrpc**](/windows/desktop/Midl/ncalrpc):</span><span class="sxs-lookup"><span data-stu-id="c080f-114">The client can associate the following security parameters to the binding for the named-pipe transport [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) or [**ncalrpc**](/windows/desktop/Midl/ncalrpc):</span></span>

-   <span data-ttu-id="c080f-115">Identificación, suplantación o anónima.</span><span class="sxs-lookup"><span data-stu-id="c080f-115">Identification, Impersonation, or Anonymous.</span></span> <span data-ttu-id="c080f-116">Especifica el tipo de seguridad que se usa.</span><span class="sxs-lookup"><span data-stu-id="c080f-116">Specifies the type of security used.</span></span> <span data-ttu-id="c080f-117">El valor predeterminado es la suplantación.</span><span class="sxs-lookup"><span data-stu-id="c080f-117">The default is Impersonation.</span></span>
-   <span data-ttu-id="c080f-118">Dinámica o estática.</span><span class="sxs-lookup"><span data-stu-id="c080f-118">Dynamic or Static.</span></span> <span data-ttu-id="c080f-119">Determina si la información de seguridad asociada a un subproceso es una copia de la información de seguridad creada en el momento en que se realiza la llamada a procedimiento remoto (estática) o un puntero a la información de seguridad (dinámica).</span><span class="sxs-lookup"><span data-stu-id="c080f-119">Determines whether security information associated with a thread is a copy of the security information created at the time the remote procedure call is made (static) or a pointer to the security information (dynamic).</span></span>

    <span data-ttu-id="c080f-120">La información de seguridad estática no cambia.</span><span class="sxs-lookup"><span data-stu-id="c080f-120">Static security information does not change.</span></span> <span data-ttu-id="c080f-121">La configuración dinámica refleja la configuración de seguridad actual, incluidos los cambios realizados después de realizar la llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="c080f-121">The dynamic setting reflects the current security settings, including changes made after the remote procedure call is made.</span></span> <span data-ttu-id="c080f-122">En el caso de [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), el valor predeterminado para las conexiones remotas de canalización con nombre es estático, para las conexiones de canalización con nombre local, el valor predeterminado es dinámico.</span><span class="sxs-lookup"><span data-stu-id="c080f-122">For [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), the default for remote named pipe connections is static, for local named pipe connections the default is dynamic.</span></span>

-   <span data-ttu-id="c080f-123">**True** o **false**.</span><span class="sxs-lookup"><span data-stu-id="c080f-123">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="c080f-124">Especifica el valor de la marca de solo efectivo.</span><span class="sxs-lookup"><span data-stu-id="c080f-124">Specifies the value of the effective-only flag.</span></span> <span data-ttu-id="c080f-125">Un valor de **true** indica que solo los privilegios de token establecidos en on en el momento de la llamada son efectivos.</span><span class="sxs-lookup"><span data-stu-id="c080f-125">A value of **TRUE** indicates that only token privileges set to on at the time of the call are effective.</span></span> <span data-ttu-id="c080f-126">Un valor de **false** indica que todos los privilegios están disponibles y que la aplicación puede modificarlos.</span><span class="sxs-lookup"><span data-stu-id="c080f-126">A value of **FALSE** indicates that all privileges are available and that the application can modify them.</span></span>

<span data-ttu-id="c080f-127">Cualquier combinación de estas opciones se puede asignar al enlace, tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c080f-127">Any combination of these settings can be assigned to the binding, as shown in the following example:</span></span>

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

<span data-ttu-id="c080f-128">La configuración predeterminada de los parámetros de seguridad varía según el protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="c080f-128">Default security-parameter settings vary according to the transport protocol.</span></span>

<span data-ttu-id="c080f-129">Para obtener más información sobre la sintaxis de las opciones del punto de conexión, vea [punto de conexión](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="c080f-129">For additional information about the syntax of the endpoint options, see [endpoint](/windows/desktop/Midl/endpoint).</span></span>

 

 