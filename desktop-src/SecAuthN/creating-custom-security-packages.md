---
description: Explica cómo crear un paquete de seguridad personalizado.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Crear paquetes de seguridad personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2136775d18e9d33f59d1b1f44fd817b3f3271ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910634"
---
# <a name="creating-custom-security-packages"></a><span data-ttu-id="46eec-103">Crear paquetes de seguridad personalizados</span><span class="sxs-lookup"><span data-stu-id="46eec-103">Creating Custom Security Packages</span></span>

## <a name="ssp-security-packages"></a><span data-ttu-id="46eec-104">Paquetes de seguridad de SSP</span><span class="sxs-lookup"><span data-stu-id="46eec-104">SSP Security Packages</span></span>

<span data-ttu-id="46eec-105">Si un paquete de seguridad del proveedor de compatibilidad para seguridad (SSP) personalizado se utiliza exclusivamente para la compatibilidad con la seguridad de cliente/servidor, puede implementar la [interfaz del proveedor de compatibilidad para seguridad](sspi.md)de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="46eec-105">If a custom security support provider (SSP) security package will be used exclusively for client/server security support it can implement the Microsoft [Security Support Provider Interface](sspi.md).</span></span>

<span data-ttu-id="46eec-106">El ejemplo de SampSSP que se incluye con el kit de desarrollo de software (SDK) de plataforma contiene un ejemplo de implementación de paquete de seguridad de SSP.</span><span class="sxs-lookup"><span data-stu-id="46eec-106">The SampSSP sample shipped with the Platform Software Development Kit (SDK) contains a sample SSP security package implementation.</span></span>

## <a name="sspap-security-packages"></a><span data-ttu-id="46eec-107">Paquetes de seguridad SSP/AP</span><span class="sxs-lookup"><span data-stu-id="46eec-107">SSP/AP Security Packages</span></span>

<span data-ttu-id="46eec-108">Los paquetes de autenticación del [*proveedor de soporte de seguridad*](/windows/desktop/SecGloss/s-gly)personalizados / [](/windows/desktop/SecGloss/a-gly) (SSP/APS) contienen paquetes de seguridad que funcionan como paquetes de autenticación (APS) y proveedores de compatibilidad para seguridad (SSP).</span><span class="sxs-lookup"><span data-stu-id="46eec-108">Custom [*security support provider*](/windows/desktop/SecGloss/s-gly)/[*authentication packages*](/windows/desktop/SecGloss/a-gly) (SSP/APs) contain security packages that function as authentication packages (APs) and security support providers (SSPs).</span></span> <span data-ttu-id="46eec-109">Estos paquetes implementan API independientes para admitir cada rol.</span><span class="sxs-lookup"><span data-stu-id="46eec-109">These packages implement separate APIs to support each role.</span></span>

<span data-ttu-id="46eec-110">Dado que funciona como un AP, un [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) SSP/AP personalizado debe proporcionar implementaciones para todas las [funciones implementadas por los paquetes de autenticación](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="46eec-110">Because it functions as an AP, a custom SSP/AP [*security package*](/windows/desktop/SecGloss/s-gly) must provide implementations for all of the [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="46eec-111">Para proporcionar compatibilidad con la seguridad integrada, un paquete personalizado de seguridad SSP/AP debe proporcionar implementaciones para las [funciones implementadas por SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="46eec-111">To provide integrated security support, a custom SSP/AP security package must provide implementations for the [Functions implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="46eec-112">[Las funciones de LSA llamadas por SSP/APS](authentication-functions.md) describen las funciones de soporte técnico disponibles para los desarrolladores de SSP/AP que desean interactuar con la LSA.</span><span class="sxs-lookup"><span data-stu-id="46eec-112">[LSA Functions Called by SSP/APs](authentication-functions.md) describes the support functions available to the SSP/AP developers that want to interact with the LSA.</span></span>

<span data-ttu-id="46eec-113">Los paquetes de seguridad SSP/AP, para que se ejecuten como AP y SSP, pueden ejecutarse como parte del sistema operativo y como parte de una aplicación de usuario.</span><span class="sxs-lookup"><span data-stu-id="46eec-113">SSP/AP security packages, in order to perform as both an AP and an SSP, may execute as part of the operating system and as part of a user application.</span></span> <span data-ttu-id="46eec-114">Estos dos modos de ejecución se conocen como modo LSA y modo usuario, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="46eec-114">These two modes of execution are known as LSA mode and user mode, respectively.</span></span> <span data-ttu-id="46eec-115">Para obtener más información sobre los paquetes de seguridad personalizados en el modo LSA, vea [inicialización del modo LSA](lsa-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="46eec-115">For details about custom security packages in LSA mode see [LSA Mode Initialization](lsa-mode-initialization.md).</span></span> <span data-ttu-id="46eec-116">Para obtener más información sobre el modo de usuario, consulte [inicialización del modo de usuario](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="46eec-116">For details about user mode, see [User Mode Initialization](user-mode-initialization.md).</span></span>

<span data-ttu-id="46eec-117">Si un paquete de seguridad SSP/AP personalizado ofrece servicios para aplicaciones cliente/servidor, debe proporcionar implementaciones para las funciones descritas en [funciones implementadas por SSP/APS en modo de usuario](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="46eec-117">If a custom SSP/AP security package offers services for client/server applications it should provide implementations for the functions described in [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="46eec-118">[Las funciones de LSA llamadas por SSP/APS en modo de usuario](authentication-functions.md) describen las funciones de soporte técnico disponibles para un SSP/AP que se ejecutan en un proceso de cliente o servidor.</span><span class="sxs-lookup"><span data-stu-id="46eec-118">[LSA Functions Called By User-mode SSP/APs](authentication-functions.md) describes the support functions available to an SSP/AP executing in a client or server process.</span></span>

<span data-ttu-id="46eec-119">Para obtener información acerca del registro de un archivo DLL SSP/AP, consulte [registro de dll de SSP/AP](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="46eec-119">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46eec-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="46eec-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46eec-121">Restricciones en relación con el registro y la instalación de un paquete de seguridad</span><span class="sxs-lookup"><span data-stu-id="46eec-121">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
