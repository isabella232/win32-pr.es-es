---
description: Explica las diferencias entre SSP/APs y SSP.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APs frente a SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002599"
---
# <a name="sspaps-vs-ssps"></a><span data-ttu-id="9837a-103">SSP/APs frente a SSP</span><span class="sxs-lookup"><span data-stu-id="9837a-103">SSP/APs vs. SSPs</span></span>

<span data-ttu-id="9837a-104">Los [*paquetes de seguridad*](../secgloss/s-gly.md) se implementan en uno de los siguientes tipos de bibliotecas de vínculos dinámicos (dll):</span><span class="sxs-lookup"><span data-stu-id="9837a-104">[*Security packages*](../secgloss/s-gly.md) are deployed in one of the following types of dynamic-link libraries (DLLs):</span></span>

-   [<span data-ttu-id="9837a-105">SSP/APs</span><span class="sxs-lookup"><span data-stu-id="9837a-105">SSP/APs</span></span>](#sspaps-vs-ssps)
-   [<span data-ttu-id="9837a-106">SSP</span><span class="sxs-lookup"><span data-stu-id="9837a-106">SSPs</span></span>](#sspaps-vs-ssps)

<span data-ttu-id="9837a-107">El hecho de que un paquete de seguridad esté en un proveedor de soporte técnico de seguridad/[*paquete de autenticación*](../secgloss/a-gly.md) (SSP/AP) o un archivo dll de proveedor de [*compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) esté determinado por los tipos de servicios de seguridad que proporciona y por la medida en la que se requiere la integración con la [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA).</span><span class="sxs-lookup"><span data-stu-id="9837a-107">Whether a security package is in a security support provider/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) or a [*security support provider*](../secgloss/s-gly.md) (SSP) DLL is determined by the types of security services it provides and the extent to which it requires integration with the [*Local Security Authority*](../secgloss/l-gly.md) (LSA).</span></span> <span data-ttu-id="9837a-108">Estas diferencias también determinan la API implementada en un paquete de seguridad personalizado.</span><span class="sxs-lookup"><span data-stu-id="9837a-108">These differences also determine the API implemented in a custom security package.</span></span>

## <a name="sspaps"></a><span data-ttu-id="9837a-109">SSP/APs</span><span class="sxs-lookup"><span data-stu-id="9837a-109">SSP/APs</span></span>

<span data-ttu-id="9837a-110">Un SSP/AP es un archivo DLL que contiene uno o varios [*paquetes de seguridad*](../secgloss/s-gly.md) y puede funcionar como SSP para aplicaciones cliente/servidor y como un paquete de [autenticación](authentication-packages.md) para aplicaciones de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="9837a-110">An SSP/AP is a DLL that contains one or more [*Security packages*](../secgloss/s-gly.md) and can function as an SSP for client/server applications and as an [authentication package](authentication-packages.md) for logon applications.</span></span> <span data-ttu-id="9837a-111">Para funcionar en ambos roles, SSP/APs se cargan en el espacio de proceso de LSA al iniciar el sistema y se pueden cargar también en procesos de aplicación cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="9837a-111">To function in both of these roles, SSP/APs are loaded into the LSA process space at system startup and can be loaded into client/server application processes as well.</span></span>

<span data-ttu-id="9837a-112">Los paquetes de seguridad SSP/AP personalizados deben implementar las [funciones implementadas por SSP/APS en modo de usuario](authentication-functions.md)y [las funciones implementadas por SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="9837a-112">Custom SSP/AP security packages must implement both the [Functions Implemented by User-mode SSP/APs](authentication-functions.md), and [Functions Implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="9837a-113">Estas implementaciones de función pueden hacer uso de las funciones de compatibilidad de LSA para ofrecer características de seguridad avanzadas, como la creación de tokens, la compatibilidad con [*credenciales adicionales*](../secgloss/s-gly.md) y la autenticación de paso a través.</span><span class="sxs-lookup"><span data-stu-id="9837a-113">These function implementations can make use of LSA support functions to offer advanced security features such as token creation, [*supplemental credentials*](../secgloss/s-gly.md) support, and pass-through authentication.</span></span>

<span data-ttu-id="9837a-114">Si un paquete de seguridad SSP/AP personalizado proporciona toda la gama de funciones de [*integridad*](../secgloss/i-gly.md) y privacidad de los mensajes, también implementará las [funciones implementadas por SSP/APS en modo de usuario](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="9837a-114">If a custom SSP/AP security package provides the full range of message [*integrity*](../secgloss/i-gly.md) and privacy functions, it will also implement the [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span>

## <a name="ssps"></a><span data-ttu-id="9837a-115">SSP</span><span class="sxs-lookup"><span data-stu-id="9837a-115">SSPs</span></span>

<span data-ttu-id="9837a-116">Un SSP es un archivo DLL que contiene uno o varios paquetes de seguridad que proporcionan servicios de autenticación, integridad de mensajes y cifrado de mensajes a las aplicaciones cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="9837a-116">An SSP is a DLL that contains one or more security packages that provide authenticated connection, message integrity, and message encryption services to client/server applications.</span></span> <span data-ttu-id="9837a-117">Los SSP implementan funciones de la [interfaz del proveedor de compatibilidad para seguridad](sspi.md) (SSPI).</span><span class="sxs-lookup"><span data-stu-id="9837a-117">SSPs implement [Security Support Provider Interface](sspi.md) (SSPI) functions.</span></span> <span data-ttu-id="9837a-118">Las aplicaciones pueden tener acceso a los paquetes de seguridad de un SSP llamando directamente a las funciones SSPI.</span><span class="sxs-lookup"><span data-stu-id="9837a-118">Applications can access the security packages in an SSP by calling the SSPI functions directly.</span></span> <span data-ttu-id="9837a-119">Los SSP se cargan en los procesos de cliente y servidor; no están integradas con la LSA.</span><span class="sxs-lookup"><span data-stu-id="9837a-119">SSPs are loaded into the client and server processes; they are not integrated with the LSA.</span></span>

 

 
