---
title: Información general sobre la arquitectura SSPI
description: SSPI es una interfaz de software.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078098"
---
# <a name="sspi-architectural-overview"></a><span data-ttu-id="a6961-103">Información general sobre la arquitectura SSPI</span><span class="sxs-lookup"><span data-stu-id="a6961-103">SSPI Architectural Overview</span></span>

<span data-ttu-id="a6961-104">SSPI es una interfaz de software.</span><span class="sxs-lookup"><span data-stu-id="a6961-104">SSPI is a software interface.</span></span> <span data-ttu-id="a6961-105">Las bibliotecas de programación distribuidas, como RPC, pueden usarlas para las comunicaciones autenticadas.</span><span class="sxs-lookup"><span data-stu-id="a6961-105">Distributed programming libraries such as RPC can use it for authenticated communications.</span></span> <span data-ttu-id="a6961-106">Uno o varios módulos de software proporcionan las capacidades de autenticación reales.</span><span class="sxs-lookup"><span data-stu-id="a6961-106">One or more software modules provide the actual authentication capabilities.</span></span> <span data-ttu-id="a6961-107">Cada módulo, denominado proveedor de compatibilidad para seguridad (SSP), se implementa como una biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="a6961-107">Each module, called a security support provider (SSP), is implemented as a dynamic link library (DLL).</span></span> <span data-ttu-id="a6961-108">Un SSP proporciona uno o varios paquetes de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a6961-108">An SSP provides one or more security packages.</span></span>

<span data-ttu-id="a6961-109">Hay disponible una variedad de SSP y paquetes.</span><span class="sxs-lookup"><span data-stu-id="a6961-109">A variety of SSPs and packages are available.</span></span> <span data-ttu-id="a6961-110">Windows incluye el paquete de seguridad de NTLM y el paquete de seguridad del protocolo Kerberos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a6961-110">Windows ships with the NTLM security package and the Microsoft Kerberos protocol security package.</span></span> <span data-ttu-id="a6961-111">Además, puede optar por instalar el paquete de seguridad de capa de sockets seguros (SSL) o cualquier otro SSP compatible con SSPI.</span><span class="sxs-lookup"><span data-stu-id="a6961-111">In addition, you may choose to install the Secure Socket Layer (SSL) security package, or any other SSPI-compatible SSP.</span></span>

<span data-ttu-id="a6961-112">El uso de SSPI garantiza que, independientemente del SSP que seleccione, la aplicación tenga acceso a las características de autenticación de forma uniforme.</span><span class="sxs-lookup"><span data-stu-id="a6961-112">Using SSPI ensures that no matter which SSP you select, your application accesses the authentication features in a uniform manner.</span></span> <span data-ttu-id="a6961-113">Esta capacidad proporciona a la aplicación una mayor independencia de la implementación de la red que estaba disponible en el pasado.</span><span class="sxs-lookup"><span data-stu-id="a6961-113">This capability provides your application greater independence from the implementation of the network than was available in the past.</span></span>

<span data-ttu-id="a6961-114">Las aplicaciones distribuidas se comunican a través de la interfaz RPC.</span><span class="sxs-lookup"><span data-stu-id="a6961-114">Distributed applications communicate through the RPC interface.</span></span> <span data-ttu-id="a6961-115">El software RPC, a su vez, obtiene acceso a las características de autenticación de un SSP a través de la SSPI.</span><span class="sxs-lookup"><span data-stu-id="a6961-115">The RPC software in turn, accesses the authentication features of an SSP through the SSPI.</span></span>

<span data-ttu-id="a6961-116">Para obtener más información, vea [SSPI](/windows/desktop/SecAuthN/sspi).</span><span class="sxs-lookup"><span data-stu-id="a6961-116">For more information, see [SSPI](/windows/desktop/SecAuthN/sspi).</span></span>

 

 