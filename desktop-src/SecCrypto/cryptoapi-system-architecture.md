---
description: Explica la arquitectura del sistema CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Arquitectura del sistema CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360227"
---
# <a name="cryptoapi-system-architecture"></a><span data-ttu-id="b70b1-103">Arquitectura del sistema CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="b70b1-103">CryptoAPI System Architecture</span></span>

<span data-ttu-id="b70b1-104">La arquitectura del sistema CryptoAPI se compone de cinco áreas funcionales principales:</span><span class="sxs-lookup"><span data-stu-id="b70b1-104">The CryptoAPI system architecture is composed of five major functional areas:</span></span>

-   [<span data-ttu-id="b70b1-105">Funciones criptográficas base</span><span class="sxs-lookup"><span data-stu-id="b70b1-105">Base Cryptographic Functions</span></span>](#base-cryptographic-functions)
-   [<span data-ttu-id="b70b1-106">Funciones de codificación y descodificación de certificados</span><span class="sxs-lookup"><span data-stu-id="b70b1-106">Certificate Encode/Decode Functions</span></span>](#certificate-encodedecode-functions)
-   [<span data-ttu-id="b70b1-107">Funciones del almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="b70b1-107">Certificate Store Functions</span></span>](#certificate-store-functions)
-   [<span data-ttu-id="b70b1-108">Funciones de mensaje simplificadas</span><span class="sxs-lookup"><span data-stu-id="b70b1-108">Simplified Message Functions</span></span>](#simplified-message-functions)
-   [<span data-ttu-id="b70b1-109">Funciones de mensajes de bajo nivel</span><span class="sxs-lookup"><span data-stu-id="b70b1-109">Low-level Message Functions</span></span>](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a><span data-ttu-id="b70b1-110">Funciones criptográficas base</span><span class="sxs-lookup"><span data-stu-id="b70b1-110">Base Cryptographic Functions</span></span>

-   <span data-ttu-id="b70b1-111">*Funciones de contexto* que se usan para conectarse a un CSP.</span><span class="sxs-lookup"><span data-stu-id="b70b1-111">*Context functions* used to connect to a CSP.</span></span> <span data-ttu-id="b70b1-112">Estas funciones permiten a las aplicaciones elegir un CSP específico por nombre o elegir un CSP específico que pueda proporcionar una clase de funcionalidad necesaria.</span><span class="sxs-lookup"><span data-stu-id="b70b1-112">These functions enable applications to choose a specific CSP by name or to choose a specific CSP that can provide a needed class of functionality.</span></span>
-   <span data-ttu-id="b70b1-113">[*Funciones de generación de claves*](../secgloss/k-gly.md) usadas para generar y almacenar [*claves criptográficas*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b70b1-113">[*Key generation functions*](../secgloss/k-gly.md) used to generate and store [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="b70b1-114">Se incluye compatibilidad completa para cambiar los [*modos de encadenamiento*](../secgloss/c-gly.md), los [*vectores de inicialización*](../secgloss/i-gly.md)y otras características de cifrado.</span><span class="sxs-lookup"><span data-stu-id="b70b1-114">Full support is included for changing [*chaining modes*](../secgloss/c-gly.md), [*initialization vectors*](../secgloss/i-gly.md), and other encryption features.</span></span> <span data-ttu-id="b70b1-115">Para obtener más información, consulte [generación de claves e intercambio de funciones](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b70b1-115">For more information, see [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>
-   <span data-ttu-id="b70b1-116">*Funciones de intercambio de claves* que se usan para intercambiar o transmitir claves.</span><span class="sxs-lookup"><span data-stu-id="b70b1-116">*Key exchange functions* used to exchange or transmit keys.</span></span> <span data-ttu-id="b70b1-117">Para obtener más información, consulte [almacenamiento de claves criptográficas y intercambio](cryptographic-key-storage-and-exchange.md) y [generación de claves y funciones de Exchange](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b70b1-117">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md) and [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>

## <a name="certificate-encodedecode-functions"></a><span data-ttu-id="b70b1-118">Funciones de codificación y descodificación de certificados</span><span class="sxs-lookup"><span data-stu-id="b70b1-118">Certificate Encode/Decode Functions</span></span>

-   <span data-ttu-id="b70b1-119">Funciones utilizadas para cifrar o descifrar datos.</span><span class="sxs-lookup"><span data-stu-id="b70b1-119">Functions used to encrypt or decrypt data.</span></span> <span data-ttu-id="b70b1-120">También se incluye compatibilidad con los datos de [*hash*](../secgloss/h-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b70b1-120">Support is also included for [*hashing*](../secgloss/h-gly.md) data.</span></span> <span data-ttu-id="b70b1-121">Para obtener más información, vea [funciones de cifrado y descifrado de datos](cryptography-functions.md) y [cifrado y](data-encryption-and-decryption.md)descifrado de datos.</span><span class="sxs-lookup"><span data-stu-id="b70b1-121">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md) and [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

## <a name="certificate-store-functions"></a><span data-ttu-id="b70b1-122">Funciones del almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="b70b1-122">Certificate Store Functions</span></span>

-   <span data-ttu-id="b70b1-123">Funciones utilizadas para administrar recopilaciones de certificados digitales.</span><span class="sxs-lookup"><span data-stu-id="b70b1-123">Functions used to manage collections of digital certificates.</span></span> <span data-ttu-id="b70b1-124">Para obtener más información, vea [certificados digitales](digital-certificates.md) y [funciones del almacén de certificados](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b70b1-124">For more information, see [Digital Certificates](digital-certificates.md) and [Certificate Store Functions](cryptography-functions.md).</span></span>

## <a name="simplified-message-functions"></a><span data-ttu-id="b70b1-125">Funciones de mensaje simplificadas</span><span class="sxs-lookup"><span data-stu-id="b70b1-125">Simplified Message Functions</span></span>

-   <span data-ttu-id="b70b1-126">Funciones utilizadas para cifrar y descifrar mensajes y datos.</span><span class="sxs-lookup"><span data-stu-id="b70b1-126">Functions used to encrypt and decrypt messages and data.</span></span>
-   <span data-ttu-id="b70b1-127">Funciones utilizadas para firmar mensajes y datos.</span><span class="sxs-lookup"><span data-stu-id="b70b1-127">Functions used to sign messages and data.</span></span>
-   <span data-ttu-id="b70b1-128">Funciones que se usan para comprobar la autenticidad de las firmas en los mensajes recibidos y los datos relacionados.</span><span class="sxs-lookup"><span data-stu-id="b70b1-128">Functions used to verify the authenticity of signatures on received messages and related data.</span></span>

<span data-ttu-id="b70b1-129">Para obtener más información, vea [mensajes simplificados](simplified-messages.md) y [funciones de mensaje simplificadas](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b70b1-129">For more information, see [Simplified Messages](simplified-messages.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

## <a name="low-level-message-functions"></a><span data-ttu-id="b70b1-130">Funciones de mensajes de bajo nivel</span><span class="sxs-lookup"><span data-stu-id="b70b1-130">Low-level Message Functions</span></span>

-   <span data-ttu-id="b70b1-131">Funciones utilizadas para realizar todas las tareas realizadas por las funciones de mensaje simplificadas.</span><span class="sxs-lookup"><span data-stu-id="b70b1-131">Functions used to perform all of the tasks performed by the simplified message functions.</span></span> <span data-ttu-id="b70b1-132">Las funciones de mensaje de bajo nivel proporcionan más flexibilidad que las funciones de mensaje simplificado, pero requieren más llamadas a funciones.</span><span class="sxs-lookup"><span data-stu-id="b70b1-132">The low-level message functions provide more flexibility than the simplified message functions but require more function calls.</span></span> <span data-ttu-id="b70b1-133">Para obtener más información, vea [mensajes de bajo nivel](low-level-messages.md) y [funciones de mensajes de bajo nivel](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b70b1-133">For more information, see [Low-level Messages](low-level-messages.md) and [Low-level Message Functions](cryptography-functions.md).</span></span>

![arquitectura de CryptoAPI](images/cryparch.png)

<span data-ttu-id="b70b1-135">Cada una de las áreas funcionales tiene una palabra clave en el nombre de función que indica su área funcional.</span><span class="sxs-lookup"><span data-stu-id="b70b1-135">Each of the functional areas has a key word in its function name that indicates its functional area.</span></span>



| <span data-ttu-id="b70b1-136">Área funcional</span><span class="sxs-lookup"><span data-stu-id="b70b1-136">Functional area</span></span>              | <span data-ttu-id="b70b1-137">Convención de nombre de función</span><span class="sxs-lookup"><span data-stu-id="b70b1-137">Function name convention</span></span> |
|------------------------------|--------------------------|
| <span data-ttu-id="b70b1-138">Funciones criptográficas base</span><span class="sxs-lookup"><span data-stu-id="b70b1-138">Base cryptographic functions</span></span> | <span data-ttu-id="b70b1-139">Codifica</span><span class="sxs-lookup"><span data-stu-id="b70b1-139">Crypt</span></span>                    |
| <span data-ttu-id="b70b1-140">Funciones de codificación y descodificación</span><span class="sxs-lookup"><span data-stu-id="b70b1-140">Encoding/decoding functions</span></span>  | <span data-ttu-id="b70b1-141">Codifica</span><span class="sxs-lookup"><span data-stu-id="b70b1-141">Crypt</span></span>                    |
| <span data-ttu-id="b70b1-142">Funciones del almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="b70b1-142">Certificate store functions</span></span>  | <span data-ttu-id="b70b1-143">Tienda</span><span class="sxs-lookup"><span data-stu-id="b70b1-143">Store</span></span>                    |
| <span data-ttu-id="b70b1-144">Funciones de mensaje simplificadas</span><span class="sxs-lookup"><span data-stu-id="b70b1-144">Simplified message functions</span></span> | <span data-ttu-id="b70b1-145">Message</span><span class="sxs-lookup"><span data-stu-id="b70b1-145">Message</span></span>                  |
| <span data-ttu-id="b70b1-146">Funciones de mensajes de bajo nivel</span><span class="sxs-lookup"><span data-stu-id="b70b1-146">Low-level message functions</span></span>  | <span data-ttu-id="b70b1-147">Msg</span><span class="sxs-lookup"><span data-stu-id="b70b1-147">Msg</span></span>                      |



 

<span data-ttu-id="b70b1-148">Las aplicaciones usan funciones en todas estas áreas.</span><span class="sxs-lookup"><span data-stu-id="b70b1-148">Applications use functions in all of these areas.</span></span> <span data-ttu-id="b70b1-149">Estas funciones, tomadas juntas, componen CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="b70b1-149">These functions, taken together, make up CryptoAPI.</span></span> <span data-ttu-id="b70b1-150">Las [*funciones criptográficas base*](../secgloss/b-gly.md) usan los CSP para los algoritmos criptográficos necesarios y para la generación y el almacenamiento seguro de [claves criptográficas](cryptographic-keys.md).</span><span class="sxs-lookup"><span data-stu-id="b70b1-150">The [*base cryptographic functions*](../secgloss/b-gly.md) use the CSPs for the necessary cryptographic algorithms and for the generation and secure storage of [cryptographic keys](cryptographic-keys.md).</span></span>

<span data-ttu-id="b70b1-151">Se usan dos tipos diferentes de claves criptográficas: [*las claves de sesión*](../secgloss/s-gly.md), que se usan para un solo cifrado y descifrado, y [*pares de claves pública y privada*](../secgloss/p-gly.md), que se usan de forma más permanente.</span><span class="sxs-lookup"><span data-stu-id="b70b1-151">Two different kinds of cryptographic keys are used: [*session keys*](../secgloss/s-gly.md), which are used for a single encryption/decryption, and [*public/private key pairs*](../secgloss/p-gly.md), which are used on a more permanent basis.</span></span>

> [!Note]  
> <span data-ttu-id="b70b1-152">Aunque una aplicación puede comunicarse directamente con cualquiera de las cinco áreas funcionales, no se puede comunicar directamente con un CSP.</span><span class="sxs-lookup"><span data-stu-id="b70b1-152">Although an application can communicate directly with any of the five functional areas, it cannot communicate directly with a CSP.</span></span> <span data-ttu-id="b70b1-153">Todas las comunicaciones de aplicación a CSP se producen a través de las [*funciones criptográficas base*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b70b1-153">All application-to-CSP communications occur through the [*base cryptographic functions*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="b70b1-154">Las funciones criptográficas base tienen un parámetro que especifica el CSP que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b70b1-154">Base cryptographic functions have a parameter that specifies which CSP to use.</span></span> <span data-ttu-id="b70b1-155">Este parámetro se puede establecer en **null** para seleccionar un CSP predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b70b1-155">This parameter can be set to **NULL** to select a default CSP.</span></span>

 

 

 
