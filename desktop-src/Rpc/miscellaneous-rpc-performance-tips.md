---
title: Sugerencias de rendimiento de RPC varias
description: En esta sección se describen varias sugerencias de rendimiento para desarrollar servidores RPC de alto rendimiento. En esta sección se proporcionan muchas sugerencias que hacen referencia al cliente RPC. Desarrollar correctamente un cliente RPC permite que el servidor RPC realice menos trabajo.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075355"
---
# <a name="miscellaneous-rpc-performance-tips"></a><span data-ttu-id="c77ad-105">Sugerencias de rendimiento de RPC varias</span><span class="sxs-lookup"><span data-stu-id="c77ad-105">Miscellaneous RPC Performance Tips</span></span>

<span data-ttu-id="c77ad-106">En esta sección se describen varias sugerencias de rendimiento para desarrollar servidores RPC de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c77ad-106">This section discusses miscellaneous performance tips for developing high performance RPC servers.</span></span> <span data-ttu-id="c77ad-107">En esta sección se proporcionan muchas sugerencias que hacen referencia al cliente RPC.</span><span class="sxs-lookup"><span data-stu-id="c77ad-107">This section provides many tips that refer to the RPC client.</span></span> <span data-ttu-id="c77ad-108">Desarrollar correctamente un cliente RPC permite que el servidor RPC realice menos trabajo.</span><span class="sxs-lookup"><span data-stu-id="c77ad-108">Developing an RPC client properly enables the RPC server to perform less work.</span></span>

## <a name="use-kerberos"></a><span data-ttu-id="c77ad-109">Usar Kerberos</span><span class="sxs-lookup"><span data-stu-id="c77ad-109">Use Kerberos</span></span>

<span data-ttu-id="c77ad-110">Si se usa la seguridad, use Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c77ad-110">If security is used, use Kerberos.</span></span> <span data-ttu-id="c77ad-111">En el lado del servidor, Kerberos no requiere acceso al KDC.</span><span class="sxs-lookup"><span data-stu-id="c77ad-111">On the server side, Kerberos does not require access to the KDC.</span></span> <span data-ttu-id="c77ad-112">Esto mueve la carga de trabajo del servidor al cliente, lo que proporciona servidores de mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c77ad-112">This moves the workload from the server to the client, which provides better performing servers.</span></span>

## <a name="use-static-identity-tracking"></a><span data-ttu-id="c77ad-113">Usar seguimiento de identidad estático</span><span class="sxs-lookup"><span data-stu-id="c77ad-113">Use Static Identity Tracking</span></span>

<span data-ttu-id="c77ad-114">Si se usa la seguridad, intente usar el seguimiento de identidad estático.</span><span class="sxs-lookup"><span data-stu-id="c77ad-114">If security is used, try to use static identity tracking.</span></span> <span data-ttu-id="c77ad-115">El seguimiento de identidades estáticas es más barato en términos de uso de recursos que el seguimiento de identidad dinámica.</span><span class="sxs-lookup"><span data-stu-id="c77ad-115">Static identity tracking is cheaper in terms of resource usage than dynamic identity tracking.</span></span> <span data-ttu-id="c77ad-116">Si la identidad del cliente cambia y el servidor no debe ser consciente del cambio, use el seguimiento dinámico en lugar de crear un identificador de enlace diferente para cada identidad.</span><span class="sxs-lookup"><span data-stu-id="c77ad-116">If the client identity changes, and the server should not be aware of the change, use dynamic tracking instead of creating a different binding handle for each identity.</span></span> <span data-ttu-id="c77ad-117">Pero si la identidad es la misma, asegúrese de que RPC tenga en cuenta este hecho para evitar que RPC realice comprobaciones de la identidad modificada cada vez.</span><span class="sxs-lookup"><span data-stu-id="c77ad-117">But if the identity is the same, ensure RPC is aware of that fact to avoid having RPC make checks for changed identity every time.</span></span>

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a><span data-ttu-id="c77ad-118">Usar la función RpcGetAuthorizationContextForClient</span><span class="sxs-lookup"><span data-stu-id="c77ad-118">Use the RpcGetAuthorizationContextForClient Function</span></span>

<span data-ttu-id="c77ad-119">Si necesita comprobar el acceso en Windows XP, utilice la función [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) .</span><span class="sxs-lookup"><span data-stu-id="c77ad-119">If you need to check access in Windows XP, use the [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) function.</span></span> <span data-ttu-id="c77ad-120">Los contextos de authz resultantes permiten comprobaciones de acceso muy rápidas, que se almacenan en caché eficazmente en el tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="c77ad-120">The resulting Authz contexts enables very fast access checks, which are efficiently cached by the RPC run time.</span></span>

## <a name="do-not-modify-the-token-unless-necessary"></a><span data-ttu-id="c77ad-121">No modifique el token a menos que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c77ad-121">Do Not Modify the Token Unless Necessary</span></span>

<span data-ttu-id="c77ad-122">Si se utiliza el seguimiento de identidad dinámica, no modifique el token de subproceso o proceso a menos que sea absolutamente necesario.</span><span class="sxs-lookup"><span data-stu-id="c77ad-122">If dynamic identity tracking is used, do not modify the thread/process token unless absolutely necessary.</span></span> <span data-ttu-id="c77ad-123">Aunque se modifique a la configuración que tenía anteriormente, el token a menudo es lo suficientemente diferente para el sistema de seguridad para desencadenar el establecimiento de un nuevo contexto de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c77ad-123">Even if it is modified to settings it previously had, the token often is sufficiently different to the security system to trigger the establishment of a new security context.</span></span>

## <a name="consider-mixed-mode-serialization-for-context-handles"></a><span data-ttu-id="c77ad-124">Considerar la serialización en modo mixto para los identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="c77ad-124">Consider Mixed Mode Serialization for Context Handles</span></span>

<span data-ttu-id="c77ad-125">El modo de serialización predeterminado para el identificador de contexto es en serie (exclusivo).</span><span class="sxs-lookup"><span data-stu-id="c77ad-125">The default serialization mode for context handle is serialized (exclusive).</span></span> <span data-ttu-id="c77ad-126">Considere la posibilidad de realizar todas las llamadas que no modifiquen el estado del identificador de contexto en el modo de serialización compartida.</span><span class="sxs-lookup"><span data-stu-id="c77ad-126">Consider making all calls that do not modify the state of the context handle in shared serialization mode.</span></span> <span data-ttu-id="c77ad-127">Vea [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c77ad-127">See [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) for more information.</span></span>

 

 




