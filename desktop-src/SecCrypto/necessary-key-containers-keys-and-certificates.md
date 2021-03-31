---
description: Los programas de ejemplo de las secciones siguientes realizan operaciones que requieren que los pares de claves pública y privada estén disponibles para el cifrado y descifrado de archivos, mensajes y firmas.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Contenedores de claves, claves y certificados necesarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817643"
---
# <a name="necessary-key-containers-keys-and-certificates"></a><span data-ttu-id="fb769-103">Contenedores de claves, claves y certificados necesarios</span><span class="sxs-lookup"><span data-stu-id="fb769-103">Necessary Key Containers, Keys, and Certificates</span></span>

<span data-ttu-id="fb769-104">Los programas de ejemplo de las secciones siguientes realizan operaciones que requieren que los [*pares de claves pública y privada*](../secgloss/p-gly.md) estén disponibles para el cifrado y descifrado de archivos, mensajes y firmas.</span><span class="sxs-lookup"><span data-stu-id="fb769-104">Example programs in the following sections perform operations that require [*public/private key pairs*](../secgloss/p-gly.md) to be available for encrypting and decrypting files, messages, and signatures.</span></span> <span data-ttu-id="fb769-105">Muchos de estos programas se compilarán, vincularán y ejecutarán pero producirán errores en tiempo de ejecución sin la existencia de [*contenedores de claves*](../secgloss/k-gly.md), claves, [*almacenes de certificados*](../secgloss/c-gly.md)y certificados adecuados en esos almacenes.</span><span class="sxs-lookup"><span data-stu-id="fb769-105">Many of these programs will compile, link, and run but fail at run time without the existence of proper [*key containers*](../secgloss/k-gly.md), keys, [*certificate stores*](../secgloss/c-gly.md), and certificates in those stores.</span></span>

<span data-ttu-id="fb769-106">Además, algunos de los certificados del almacén MY deben tener algunas de sus propiedades extendidas establecidas.</span><span class="sxs-lookup"><span data-stu-id="fb769-106">In addition, some of the certificates in the MY store must have some of their extended properties set.</span></span>

<span data-ttu-id="fb769-107">La creación del contenedor de claves predeterminado necesario puede realizarse mediante la ejecución del programa en el [ejemplo C programa: creación de un contenedor de claves y generación de claves](example-c-program-creating-a-key-container-and-generating-keys.md).</span><span class="sxs-lookup"><span data-stu-id="fb769-107">Creating the needed default key container can be done by running the program in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span> <span data-ttu-id="fb769-108">Tenga en cuenta que la creación de un contenedor de claves no genera automáticamente pares de claves pública y privada.</span><span class="sxs-lookup"><span data-stu-id="fb769-108">Note that the creation of a key container does not automatically generate public/private key pairs.</span></span> <span data-ttu-id="fb769-109">Sin embargo, el programa de ejemplo crea el contenedor de claves y genera los pares de claves pública y privada.</span><span class="sxs-lookup"><span data-stu-id="fb769-109">The example program, however, both creates the key container and generates the public/private key pairs.</span></span>

<span data-ttu-id="fb769-110">Una vez generados los pares de claves pública y privada, los certificados de prueba que usan esas claves se pueden obtener de una [*entidad de certificación*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="fb769-110">After public/private key pairs have been generated, test certificates using those keys can be obtained from a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="fb769-111">Algunos de los programas suponen que existen certificados con nombres de asunto específicos en mi almacén del sistema.</span><span class="sxs-lookup"><span data-stu-id="fb769-111">Several of the programs assume that certificates with specific subject names exist in the MY system store.</span></span> <span data-ttu-id="fb769-112">En concreto, varios programas buscan certificados con los nombres de asunto "certificado de prueba completa" y "Hortense".</span><span class="sxs-lookup"><span data-stu-id="fb769-112">In particular, several programs look for certificates with the subject names "Full Test Cert" and "Hortense."</span></span> <span data-ttu-id="fb769-113">Los nombres de asunto de los certificados se pueden cambiar en el código para que coincidan con los nombres de asunto de los certificados que existen en el almacén de certificados MY.</span><span class="sxs-lookup"><span data-stu-id="fb769-113">The subject names for the certificates may be changed in the code to match the subject names of certificates that exist in the MY certificate store.</span></span>

<span data-ttu-id="fb769-114">Ejecutar el programa de ejemplo del [programa C de ejemplo: si se enumeran los certificados de un almacén](example-c-program-listing-the-certificates-in-a-store.md) , se mostrarán todos los certificados de un almacén y todas las propiedades extendidas que se establezcan en esos certificados.</span><span class="sxs-lookup"><span data-stu-id="fb769-114">Running the example program in [Example C Program: Listing the Certificates in a Store](example-c-program-listing-the-certificates-in-a-store.md) will display all of the certificates in a store and all of the extended properties that are set on those certificates.</span></span>

 

 
