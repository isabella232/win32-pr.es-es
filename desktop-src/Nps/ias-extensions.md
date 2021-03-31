---
title: Extensiones de servidor de directivas de redes
description: La API de extensiones de NPS permite a los desarrolladores de software escribir archivos dll de extensión que se pueden usar para la autenticación, la autorización y las cuentas. La API de extensiones de NPS es compatible con el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995482"
---
# <a name="network-policy-server-extensions"></a><span data-ttu-id="ffad9-104">Extensiones de servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="ffad9-104">Network Policy Server Extensions</span></span>

> [!Note]  
> <span data-ttu-id="ffad9-105">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ffad9-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="ffad9-106">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="ffad9-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="ffad9-107">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="ffad9-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="ffad9-108">La API de extensiones de NPS permite a los desarrolladores de software escribir archivos dll de extensión que se pueden usar para la autenticación, la autorización y las cuentas.</span><span class="sxs-lookup"><span data-stu-id="ffad9-108">The NPS Extensions API enables software developers to write extension DLLs that can be used for authentication, authorization, and accounting.</span></span> <span data-ttu-id="ffad9-109">La API de extensiones de NPS es compatible con el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="ffad9-109">NPS Extensions API supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span>

<span data-ttu-id="ffad9-110">Los archivos dll de extensión que se implementan mediante la API de extensiones de NPS pueden proporcionar control de sesión y contabilidad mejorados.</span><span class="sxs-lookup"><span data-stu-id="ffad9-110">The extension DLLs implemented using the NPS Extensions API can provide enhanced session control and accounting.</span></span> <span data-ttu-id="ffad9-111">Estos archivos DLL se pueden usar para escenarios como el control del número de sesiones de red de usuario final, el uso de un servidor de estado y la conexión a bases de datos de autenticación de dominio y servicios de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ffad9-111">These DLLs can be used for scenarios such as controlling the number of end-user network sessions, using a state server, and connecting to domain authentication databases and Active Directory services.</span></span> <span data-ttu-id="ffad9-112">Los archivos dll de extensión pueden expandir las autorizaciones de acceso remoto proporcionadas por NPS agregando sus propias autorizaciones al enviar una respuesta de aceptación de nuevo a un cliente de autenticación.</span><span class="sxs-lookup"><span data-stu-id="ffad9-112">The extension DLLs can expand the remote access authorizations provided by NPS by adding their own authorizations when sending an Accept response back to an authenticating client.</span></span>

<span data-ttu-id="ffad9-113">La API de extensiones de NPS es aplicable en cualquier entorno informático en el que pueda mejorar la eficacia para autenticar a los usuarios de acceso telefónico a través de un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="ffad9-113">NPS Extensions API is applicable in any computing environment where it would improve efficiency to authenticate dial-in users through a remote server.</span></span> <span data-ttu-id="ffad9-114">Esta tecnología es especialmente útil para los proveedores de servicios de Internet (ISP).</span><span class="sxs-lookup"><span data-stu-id="ffad9-114">This technology is especially useful for Internet Service Providers (ISPs).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ffad9-115">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ffad9-115">In This Section</span></span>

[<span data-ttu-id="ffad9-116">Información general</span><span class="sxs-lookup"><span data-stu-id="ffad9-116">Overview</span></span>](/windows/desktop/Nps/ias-about-internet-authentication-service)

<span data-ttu-id="ffad9-117">Información general sobre RADIUS y la API de extensiones de NPS.</span><span class="sxs-lookup"><span data-stu-id="ffad9-117">General information about RADIUS and the NPS Extensions API.</span></span>

[<span data-ttu-id="ffad9-118">Utilizan</span><span class="sxs-lookup"><span data-stu-id="ffad9-118">Using</span></span>](/windows/desktop/Nps/ias-using-internet-authentication-service)

<span data-ttu-id="ffad9-119">Código de ejemplo que muestra cómo usar la API de extensiones de NPS.</span><span class="sxs-lookup"><span data-stu-id="ffad9-119">Sample code that demonstrates how to use the NPS Extensions API.</span></span>

[<span data-ttu-id="ffad9-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="ffad9-120">Reference</span></span>](/windows/desktop/Nps/ias-internet-authentication-service-reference)

<span data-ttu-id="ffad9-121">Documentación de tipos enumerados, funciones y estructuras que componen la API de extensiones de NPS.</span><span class="sxs-lookup"><span data-stu-id="ffad9-121">Documentation of enumerated types, functions, and structures that compose the NPS Extensions API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffad9-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffad9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffad9-123">Servidor de directivas de redes (servicio de autenticación de Internet)</span><span class="sxs-lookup"><span data-stu-id="ffad9-123">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="ffad9-124">Protocolo de autenticación extensible (EAP)</span><span class="sxs-lookup"><span data-stu-id="ffad9-124">Extensible Authentication Protocol (EAP)</span></span>](../eap/eap-start-page.md)
</dt> </dl>

 

 