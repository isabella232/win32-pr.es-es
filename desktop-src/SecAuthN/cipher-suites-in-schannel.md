---
description: Un conjunto de cifrado es un conjunto de algoritmos criptográficos.
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: Conjuntos de cifrado en TLS/SSL (Schannel SSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa8b47aed266c49ac306adfd2aef78af269a39
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105653131"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a><span data-ttu-id="31d82-103">Conjuntos de cifrado en TLS/SSL (Schannel SSP)</span><span class="sxs-lookup"><span data-stu-id="31d82-103">Cipher Suites in TLS/SSL (Schannel SSP)</span></span>

<span data-ttu-id="31d82-104">Un conjunto de cifrado es un conjunto de algoritmos criptográficos.</span><span class="sxs-lookup"><span data-stu-id="31d82-104">A cipher suite is a set of cryptographic algorithms.</span></span> <span data-ttu-id="31d82-105">La implementación de Schannel SSP de los protocolos TLS/SSL usa algoritmos de un conjunto de cifrado para crear claves y cifrar la información.</span><span class="sxs-lookup"><span data-stu-id="31d82-105">The schannel SSP implementation of the TLS/SSL protocols use algorithms from a cipher suite to create keys and encrypt information.</span></span> <span data-ttu-id="31d82-106">Un conjunto de cifrado especifica un algoritmo para cada una de las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="31d82-106">A cipher suite specifies one algorithm for each of the following tasks:</span></span>

-   <span data-ttu-id="31d82-107">Intercambio de claves</span><span class="sxs-lookup"><span data-stu-id="31d82-107">Key exchange</span></span>
-   <span data-ttu-id="31d82-108">Cifrado masivo</span><span class="sxs-lookup"><span data-stu-id="31d82-108">Bulk encryption</span></span>
-   <span data-ttu-id="31d82-109">Autenticación de mensajes</span><span class="sxs-lookup"><span data-stu-id="31d82-109">Message authentication</span></span>

<span data-ttu-id="31d82-110">Los [*algoritmos de intercambio de claves*](/windows/desktop/SecGloss/k-gly) protegen la información necesaria para crear claves compartidas.</span><span class="sxs-lookup"><span data-stu-id="31d82-110">[*Key exchange algorithms*](/windows/desktop/SecGloss/k-gly) protect information required to create shared keys.</span></span> <span data-ttu-id="31d82-111">Estos algoritmos son asimétricos ([*algoritmos de clave pública*](/windows/desktop/SecGloss/p-gly)) y funcionan bien para cantidades de datos relativamente pequeñas.</span><span class="sxs-lookup"><span data-stu-id="31d82-111">These algorithms are asymmetric ([*public key algorithms*](/windows/desktop/SecGloss/p-gly)) and perform well for relatively small amounts of data.</span></span>

<span data-ttu-id="31d82-112">Los algoritmos de cifrado masivo cifran los mensajes intercambiados entre clientes y servidores.</span><span class="sxs-lookup"><span data-stu-id="31d82-112">Bulk encryption algorithms encrypt messages exchanged between clients and servers.</span></span> <span data-ttu-id="31d82-113">Estos algoritmos son [*simétricos*](/windows/desktop/SecGloss/s-gly) y funcionan bien para grandes cantidades de datos.</span><span class="sxs-lookup"><span data-stu-id="31d82-113">These algorithms are [*symmetric*](/windows/desktop/SecGloss/s-gly) and perform well for large amounts of data.</span></span>

<span data-ttu-id="31d82-114">Los algoritmos de [autenticación de mensajes](message-authentication-codes-in-schannel.md) generan [*hashes*](/windows/desktop/SecGloss/h-gly) de mensajes y firmas que garantizan la [*integridad*](/windows/desktop/SecGloss/i-gly) de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="31d82-114">[Message authentication](message-authentication-codes-in-schannel.md) algorithms generate message [*hashes*](/windows/desktop/SecGloss/h-gly) and signatures that ensure the [*integrity*](/windows/desktop/SecGloss/i-gly) of a message.</span></span>

<span data-ttu-id="31d82-115">Los desarrolladores especifican estos elementos mediante tipos de datos de [**\_ identificador de alg**](/windows/desktop/SecCrypto/alg-id) .</span><span class="sxs-lookup"><span data-stu-id="31d82-115">Developers specify these elements by using [**ALG\_ID**](/windows/desktop/SecCrypto/alg-id) data types.</span></span> <span data-ttu-id="31d82-116">Para obtener más información, consulte [especificar cifrados Schannel y intensidades de cifrado](specifying-schannel-ciphers-and-cipher-strengths.md).</span><span class="sxs-lookup"><span data-stu-id="31d82-116">For more information, see [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).</span></span>

<span data-ttu-id="31d82-117">En versiones anteriores de Windows, los conjuntos de cifrado TLS y las curvas elípticas se configuraban mediante una sola cadena:</span><span class="sxs-lookup"><span data-stu-id="31d82-117">In earlier versions of Windows, TLS cipher suites and elliptical curves were configured by using a single string:</span></span>

![Diagrama que muestra una sola cadena para un conjunto de cifrado.](images/tls-cipher-suite.png)

<span data-ttu-id="31d82-119">Las distintas versiones de Windows admiten diferentes conjuntos de cifrado TLS y orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="31d82-119">Different Windows versions support different TLS cipher suites and priority order.</span></span> <span data-ttu-id="31d82-120">Vea la versión de Windows correspondiente para el orden predeterminado en el que los elige el proveedor de Microsoft Schannel.</span><span class="sxs-lookup"><span data-stu-id="31d82-120">See the corresponding Windows version for the default order in which they are chosen by the Microsoft Schannel Provider.</span></span>

<span data-ttu-id="31d82-121">**Windows Server 2022:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md)</span><span class="sxs-lookup"><span data-stu-id="31d82-121">**Windows Server 2022:** For information about supported cipher suites, see [TLS Cipher Suites in Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md)</span></span>

<span data-ttu-id="31d82-122">**Windows 10, versión 1903:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows 10 V1903](tls-cipher-suites-in-windows-10-v1903.md)</span><span class="sxs-lookup"><span data-stu-id="31d82-122">**Windows 10, version 1903:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)</span></span>

<span data-ttu-id="31d82-123">**Windows 10, versión 1809:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)</span><span class="sxs-lookup"><span data-stu-id="31d82-123">**Windows 10, version 1809:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)</span></span>

<span data-ttu-id="31d82-124">**Windows 10, versión 1803:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)</span><span class="sxs-lookup"><span data-stu-id="31d82-124">**Windows 10, version 1803:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)</span></span>

<span data-ttu-id="31d82-125">**Windows 10, versión 1709:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)</span><span class="sxs-lookup"><span data-stu-id="31d82-125">**Windows 10, version 1709:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)</span></span>

<span data-ttu-id="31d82-126">**Windows 10, versión 1703:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)</span><span class="sxs-lookup"><span data-stu-id="31d82-126">**Windows 10, version 1703:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)</span></span>

<span data-ttu-id="31d82-127">**Windows Server 2016 y Windows 10, versión 1607:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)</span><span class="sxs-lookup"><span data-stu-id="31d82-127">**Windows Server 2016 and Windows 10, version 1607:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)</span></span>

<span data-ttu-id="31d82-128">**Windows 10, versión 1511:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)</span><span class="sxs-lookup"><span data-stu-id="31d82-128">**Windows 10, version 1511:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)</span></span>

<span data-ttu-id="31d82-129">**Windows 10, versión 1507:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)</span><span class="sxs-lookup"><span data-stu-id="31d82-129">**Windows 10, version 1507:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)</span></span>

<span data-ttu-id="31d82-130">**Windows Server 2012 R2 y Windows 8.1:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows 8.1](tls-cipher-suites-in-windows-8-1.md)</span><span class="sxs-lookup"><span data-stu-id="31d82-130">**Windows Server 2012 R2 and Windows 8.1:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 8.1](tls-cipher-suites-in-windows-8-1.md)</span></span>

<span data-ttu-id="31d82-131">**Windows Server 2012 y Windows 8:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows 8](tls-cipher-suites-in-windows-8.md) .</span><span class="sxs-lookup"><span data-stu-id="31d82-131">**Windows Server 2012 and Windows 8:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 8](tls-cipher-suites-in-windows-8.md)</span></span>

<span data-ttu-id="31d82-132">**Windows Server 2008 R2 y Windows 7:** Para obtener información sobre los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows 7](tls-cipher-suites-in-windows-7.md) .</span><span class="sxs-lookup"><span data-stu-id="31d82-132">**Windows Server 2008 R2 and Windows 7:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 7](tls-cipher-suites-in-windows-7.md)</span></span>

<span data-ttu-id="31d82-133">**Windows Server 2008 y Windows Vista:** Para obtener información acerca de los conjuntos de cifrado compatibles, consulte [conjuntos de cifrado TLS en Windows Vista](schannel-cipher-suites-in-windows-vista.md) .</span><span class="sxs-lookup"><span data-stu-id="31d82-133">**Windows Server 2008 and Windows Vista:** For information about supported cipher suites, see [TLS Cipher Suites in Windows Vista](schannel-cipher-suites-in-windows-vista.md)</span></span>

<span data-ttu-id="31d82-134">**Windows Server 2003 y Windows XP:** Para obtener información acerca de los conjuntos de cifrado compatibles, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="31d82-134">**Windows Server 2003 and Windows XP:** For information about supported cipher suites, see the following topics.</span></span>

| <span data-ttu-id="31d82-135">Tema</span><span class="sxs-lookup"><span data-stu-id="31d82-135">Topic</span></span>                                                                         | <span data-ttu-id="31d82-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="31d82-136">Description</span></span>                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31d82-137">Conjuntos de cifrado TLS</span><span class="sxs-lookup"><span data-stu-id="31d82-137">TLS Cipher Suites</span></span>](tls-cipher-suites.md)<br/>                         | <span data-ttu-id="31d82-138">Información sobre los conjuntos de cifrado disponibles con el protocolo TLS en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31d82-138">Information about the cipher suites available with the TLS protocol in Windows Server 2003 and Windows XP.</span></span><br/>              |
| [<span data-ttu-id="31d82-139">Protocolo Capa de sockets seguros</span><span class="sxs-lookup"><span data-stu-id="31d82-139">Secure Sockets Layer Protocol</span></span>](secure-sockets-layer-protocol.md)<br/> | <span data-ttu-id="31d82-140">Información general sobre SSL 2,0 y 3,0, incluidos los conjuntos de cifrado disponibles en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31d82-140">General information about SSL 2.0 and 3.0, including the available cipher suites in Windows Server 2003 and Windows XP.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="31d82-141">Antes de Windows 10, las cadenas de conjunto de cifrado se anexaban con la curva elíptica para determinar la prioridad de la curva.</span><span class="sxs-lookup"><span data-stu-id="31d82-141">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="31d82-142">Windows 10 admite un valor de orden de prioridad de curva elíptica, por lo que el sufijo de curva elíptica no es necesario y se reemplaza por el nuevo orden de prioridad de curva elíptica, cuando se proporciona, para permitir que las organizaciones usen la Directiva de grupo para configurar diferentes versiones de Windows con los mismos conjuntos de cifrado.</span><span class="sxs-lookup"><span data-stu-id="31d82-142">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>

 

