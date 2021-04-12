---
description: El modelo de interfaz del proveedor de compatibilidad para seguridad (SSPI) proporciona una única interfaz para una aplicación de transporte de cliente/servidor mediante los diversos paquetes de seguridad disponibles en un equipo o una red.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Procedimientos utilizados con la mayoría de los protocolos y paquetes de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541163"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a><span data-ttu-id="6c549-103">Procedimientos utilizados con la mayoría de los protocolos y paquetes de seguridad</span><span class="sxs-lookup"><span data-stu-id="6c549-103">Procedures Used with Most Security Packages and Protocols</span></span>

<span data-ttu-id="6c549-104">El modelo de [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) proporciona una única interfaz para una aplicación de transporte de cliente/servidor mediante los diversos paquetes de [*seguridad*](../secgloss/s-gly.md) disponibles en un equipo o una red.</span><span class="sxs-lookup"><span data-stu-id="6c549-104">The [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) model provides a single interface for a client/server transport application using the various [*security packages*](../secgloss/s-gly.md) available on a computer or network.</span></span> <span data-ttu-id="6c549-105">SSPI permite a una aplicación usar un paquete de seguridad sin tratar con los [*protocolos de seguridad*](../secgloss/s-gly.md) subyacentes del paquete.</span><span class="sxs-lookup"><span data-stu-id="6c549-105">SSPI allows an application to use a security package without dealing with the underlying [*security protocols*](../secgloss/s-gly.md) of the package.</span></span> <span data-ttu-id="6c549-106">Al mismo tiempo, SSPI también permite que las aplicaciones sofisticadas con reconocimiento de la seguridad aprovechen las capacidades avanzadas de los paquetes de seguridad específicos.</span><span class="sxs-lookup"><span data-stu-id="6c549-106">At the same time, SSPI also allows sophisticated, security-aware applications to take advantage of the advanced capabilities of specific security packages.</span></span>

<span data-ttu-id="6c549-107">Las aplicaciones inicializan SSPI mediante los pasos siguientes para proteger una conexión de red para la mayoría de los paquetes de seguridad:</span><span class="sxs-lookup"><span data-stu-id="6c549-107">Applications initialize SSPI using the following steps to secure a network connection for most security packages:</span></span>

-   [<span data-ttu-id="6c549-108">Usar SecBufferDesc y SecBuffer</span><span class="sxs-lookup"><span data-stu-id="6c549-108">Using SecBufferDesc and SecBuffer</span></span>](using-secbufferdesc-and-secbuffer.md)
-   [<span data-ttu-id="6c549-109">Inicializando SSPI</span><span class="sxs-lookup"><span data-stu-id="6c549-109">Initializing SSPI</span></span>](initializing-sspi.md)
-   [<span data-ttu-id="6c549-110">Establecer una conexión segura con la autenticación</span><span class="sxs-lookup"><span data-stu-id="6c549-110">Establishing a Secure Connection with Authentication</span></span>](establishing-a-secure-connection-with-authentication.md)
-   [<span data-ttu-id="6c549-111">Garantizar la integridad de la comunicación durante el intercambio de mensajes</span><span class="sxs-lookup"><span data-stu-id="6c549-111">Ensuring Communication Integrity During Message Exchange</span></span>](ensuring-communication-integrity-during-message-exchange.md)
-   [<span data-ttu-id="6c549-112">Finalizar una sesión SSPI</span><span class="sxs-lookup"><span data-stu-id="6c549-112">Ending an SSPI Session</span></span>](ending-an-sspi-session.md)

 

 
