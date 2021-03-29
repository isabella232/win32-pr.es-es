---
title: Llamadas de procedimiento remoto con RPC sobre HTTP
description: Los programas del explorador de Internet suelen emplear el protocolo de transporte de hipertexto (HTTP) como medio principal de examinar el World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- RPC llamada a procedimiento remoto, tareas, uso de RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993823"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a><span data-ttu-id="8ae0d-104">Llamadas de procedimiento remoto con RPC sobre HTTP</span><span class="sxs-lookup"><span data-stu-id="8ae0d-104">Remote Procedure Calls Using RPC over HTTP</span></span>

<span data-ttu-id="8ae0d-105">Los programas del explorador de Internet suelen emplear el protocolo de transporte de hipertexto (HTTP) como medio principal de examinar el World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="8ae0d-105">Internet browser programs commonly employ the Hypertext Transport Protocol (HTTP) as the primary means of browsing the World Wide Web.</span></span> <span data-ttu-id="8ae0d-106">HTTP, por lo tanto, ve un uso extensivo en la mayoría de los equipos de hoy en día.</span><span class="sxs-lookup"><span data-stu-id="8ae0d-106">HTTP, therefore, sees extensive usage on most computers today.</span></span> <span data-ttu-id="8ae0d-107">Microsoft ha extendido las capacidades de su servidor de Internet Information Server (IIS) para proporcionar servicios de llamada a procedimiento remoto mediante HTTP.</span><span class="sxs-lookup"><span data-stu-id="8ae0d-107">Microsoft has extended the capabilities of its Internet Information Server (IIS) to provide remote procedure call services using HTTP.</span></span>

<span data-ttu-id="8ae0d-108">La implementación de RPC a través de HTTP (RPC a través de HTTP) de Microsoft permite a los clientes RPC conectarse de forma segura y eficaz a través de Internet a programas de servidor RPC y ejecutar llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="8ae0d-108">The Microsoft RPC-over-HTTP implementation (RPC over HTTP) allows RPC clients to securely and efficiently connect across the Internet to RPC server programs and execute remote procedure calls.</span></span> <span data-ttu-id="8ae0d-109">Esto se consigue con la ayuda de un intermediario conocido como el proxy RPC a través de HTTP o simplemente el proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="8ae0d-109">This is accomplished with the help of an intermediary known as the RPC-over-HTTP Proxy, or simply the RPC Proxy.</span></span>

<span data-ttu-id="8ae0d-110">El proxy RPC se ejecuta en un equipo de IIS.</span><span class="sxs-lookup"><span data-stu-id="8ae0d-110">The RPC Proxy runs on an IIS computer.</span></span> <span data-ttu-id="8ae0d-111">Acepta solicitudes RPC procedentes de Internet, realiza comprobaciones de autenticación, validación y acceso en esas solicitudes, y si la solicitud supera todas las pruebas, el proxy RPC reenvía la solicitud al servidor RPC que realiza el procesamiento real.</span><span class="sxs-lookup"><span data-stu-id="8ae0d-111">It accepts RPC requests coming from the Internet, performs authentication, validation, and access checks on those requests, and if the request passes all tests, RPC Proxy forwards the request to the RPC server that performs the actual processing.</span></span> <span data-ttu-id="8ae0d-112">Con RPC a través de HTTP, el cliente RPC y el servidor no se comunican directamente; en su lugar, usan el proxy RPC como intermediario.</span><span class="sxs-lookup"><span data-stu-id="8ae0d-112">With RPC over HTTP the RPC client and server do not communicate directly; rather, they use the RPC Proxy as intermediary.</span></span> <span data-ttu-id="8ae0d-113">Este modelo se eligió por muchas razones.</span><span class="sxs-lookup"><span data-stu-id="8ae0d-113">This model was chosen for many reasons.</span></span> <span data-ttu-id="8ae0d-114">Para obtener más información, vea [seguridad de RPC a través de http](rpc-over-http-security.md).</span><span class="sxs-lookup"><span data-stu-id="8ae0d-114">For more information, see [RPC over HTTP Security](rpc-over-http-security.md).</span></span>

<span data-ttu-id="8ae0d-115">En esta sección se proporciona información general sobre RPC a través de HTTP en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="8ae0d-115">This section provides an overview of RPC over HTTP in the following topics:</span></span>

-   [<span data-ttu-id="8ae0d-116">Usar HTTP como transporte RPC</span><span class="sxs-lookup"><span data-stu-id="8ae0d-116">Using HTTP as an RPC Transport</span></span>](using-http-as-an-rpc-transport.md)
-   [<span data-ttu-id="8ae0d-117">Seguridad de RPC a través de HTTP</span><span class="sxs-lookup"><span data-stu-id="8ae0d-117">RPC over HTTP Security</span></span>](rpc-over-http-security.md)
-   [<span data-ttu-id="8ae0d-118">Requisitos del sistema e interoperabilidad de RPC a través de HTTP</span><span class="sxs-lookup"><span data-stu-id="8ae0d-118">System Requirements and Interoperability for RPC over HTTP</span></span>](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [<span data-ttu-id="8ae0d-119">Configuración de equipos para RPC a través de HTTP</span><span class="sxs-lookup"><span data-stu-id="8ae0d-119">Configuring Computers for RPC over HTTP</span></span>](configuring-computers-for-rpc-over-http.md)
-   [<span data-ttu-id="8ae0d-120">Recomendaciones de implementación de RPC sobre HTTP</span><span class="sxs-lookup"><span data-stu-id="8ae0d-120">RPC over HTTP Deployment Recommendations</span></span>](rpc-over-http-deployment-recommendations.md)

<span data-ttu-id="8ae0d-121">Para obtener información sobre escenarios de RPC a través de HTTP de gran volumen, consulte [equilibrio de carga de Microsoft RPC](rpc-load-balancing.md).</span><span class="sxs-lookup"><span data-stu-id="8ae0d-121">For information regarding high volume RPC over HTTP scenarios, please see [Microsoft RPC Load Balancing](rpc-load-balancing.md).</span></span>

 

 




