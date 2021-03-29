---
description: Cómo crear una conexión segura con Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Crear una conexión segura mediante Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335713a400804bc84fffa078496c53c9178e389b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814747"
---
# <a name="creating-a-secure-connection-using-schannel"></a><span data-ttu-id="d3c60-103">Crear una conexión segura mediante Schannel</span><span class="sxs-lookup"><span data-stu-id="d3c60-103">Creating a Secure Connection Using Schannel</span></span>

<span data-ttu-id="d3c60-104">El [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) de Schannel proporciona acceso a cuatro [*protocolos de seguridad*](/windows/desktop/SecGloss/s-gly):</span><span class="sxs-lookup"><span data-stu-id="d3c60-104">The Schannel [*security package*](/windows/desktop/SecGloss/s-gly) provides access to four [*security protocols*](/windows/desktop/SecGloss/s-gly):</span></span>

-   [<span data-ttu-id="d3c60-105">Seguridad de la capa de transporte (TLS 1,2)</span><span class="sxs-lookup"><span data-stu-id="d3c60-105">Transport Layer Security (TLS 1.2)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="d3c60-106">Seguridad de la capa de transporte (TLS 1,1)</span><span class="sxs-lookup"><span data-stu-id="d3c60-106">Transport Layer Security (TLS 1.1)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="d3c60-107">Seguridad de la capa de transporte (TLS 1,0)</span><span class="sxs-lookup"><span data-stu-id="d3c60-107">Transport Layer Security (TLS 1.0)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="d3c60-108">Capa de sockets seguros (SSL 3,0)</span><span class="sxs-lookup"><span data-stu-id="d3c60-108">Secure Sockets Layer (SSL 3.0)</span></span>](secure-sockets-layer-protocol.md)
-   [<span data-ttu-id="d3c60-109">Capa de sockets seguros (SSL 2,0)</span><span class="sxs-lookup"><span data-stu-id="d3c60-109">Secure Sockets Layer (SSL 2.0)</span></span>](secure-sockets-layer-protocol.md)

> [!Note]  
> <span data-ttu-id="d3c60-110">Los protocolos PCT y SSL 2,0 se han sustituido por el protocolo TLS y no se deben usar para el nuevo desarrollo.</span><span class="sxs-lookup"><span data-stu-id="d3c60-110">The PCT and SSL 2.0 protocols have been superseded by the TLS protocol and should not be used for new development.</span></span>

 

<span data-ttu-id="d3c60-111">**Para configurar una conexión segura entre un cliente y un servidor**</span><span class="sxs-lookup"><span data-stu-id="d3c60-111">**To set up a secure connection between a client and server**</span></span>

1.  <span data-ttu-id="d3c60-112">Obtener las credenciales de Schannel ([obtención de credenciales de Schannel](obtaining-schannel-credentials.md)).</span><span class="sxs-lookup"><span data-stu-id="d3c60-112">Obtain Schannel credentials ([Obtaining Schannel Credentials](obtaining-schannel-credentials.md)).</span></span>
2.  <span data-ttu-id="d3c60-113">Cree un contexto de seguridad de Schannel ([creando un contexto de seguridad de Schannel](creating-an-schannel-security-context.md)).</span><span class="sxs-lookup"><span data-stu-id="d3c60-113">Create an Schannel security context ([Creating an Schannel Security Context](creating-an-schannel-security-context.md)).</span></span>

<span data-ttu-id="d3c60-114">Una vez establecida una conexión, puede recuperar información sobre sus atributos.</span><span class="sxs-lookup"><span data-stu-id="d3c60-114">After a connection is established, you can retrieve information about its attributes.</span></span> <span data-ttu-id="d3c60-115">Para más información, consulte [obtención de información acerca de las conexiones Schannel](getting-information-about-schannel-connections.md).</span><span class="sxs-lookup"><span data-stu-id="d3c60-115">For details, see [Getting Information About Schannel Connections](getting-information-about-schannel-connections.md).</span></span>

<span data-ttu-id="d3c60-116">Si, después de establecer una conexión, los requisitos de seguridad de la aplicación cambian o se pierde la conexión, puede volver a negociar la conexión.</span><span class="sxs-lookup"><span data-stu-id="d3c60-116">If, after you have established a connection, the security requirements of your application change or the connection is lost, you can renegotiate the connection.</span></span> <span data-ttu-id="d3c60-117">Para obtener más información, consulte [renegociación de una conexión Schannel](renegotiating-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d3c60-117">For details, see [Renegotiating an Schannel Connection](renegotiating-an-schannel-connection.md).</span></span>

<span data-ttu-id="d3c60-118">Cuando haya terminado de usar una conexión Schannel, debe realizar la limpieza necesaria.</span><span class="sxs-lookup"><span data-stu-id="d3c60-118">When you have finished using an Schannel connection, you must perform the necessary cleanup.</span></span> <span data-ttu-id="d3c60-119">Para obtener más información, consulte [apagar una conexión Schannel](shutting-down-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d3c60-119">For details, see [Shutting Down an Schannel Connection](shutting-down-an-schannel-connection.md).</span></span>

<span data-ttu-id="d3c60-120">Para obtener información acerca de los ejemplos que se incluyen con el kit de desarrollo de software (SDK) de la plataforma que muestra el [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly)de Schannel, consulte los ejemplos de psdk con Schannel.</span><span class="sxs-lookup"><span data-stu-id="d3c60-120">For information about samples shipped with the Platform Software Development Kit (SDK) that demonstrate the Schannel [*security package*](/windows/desktop/SecGloss/s-gly), see the PSDK samples using Schannel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3c60-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3c60-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3c60-122">Especificar cifrados Schannel y niveles de cifrado</span><span class="sxs-lookup"><span data-stu-id="d3c60-122">Specifying Schannel Ciphers and Cipher Strengths</span></span>](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
