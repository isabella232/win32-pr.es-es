---
description: Describe las tareas que deben realizarse para crear un mensaje firmado.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Crear un mensaje firmado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277521"
---
# <a name="creating-a-signed-message"></a><span data-ttu-id="fc2bc-103">Crear un mensaje firmado</span><span class="sxs-lookup"><span data-stu-id="fc2bc-103">Creating a Signed Message</span></span>

<span data-ttu-id="fc2bc-104">En la ilustración siguiente se muestran las tareas que deben realizarse para crear un mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="fc2bc-104">The following illustration depicts the tasks that must be accomplished to create a signed message.</span></span> <span data-ttu-id="fc2bc-105">Los pasos se enumeran a continuación de la ilustración.</span><span class="sxs-lookup"><span data-stu-id="fc2bc-105">The steps are listed following the illustration.</span></span>

![firmar un mensaje](images/signdmsg.png)

<span data-ttu-id="fc2bc-107">**Para crear un mensaje firmado**</span><span class="sxs-lookup"><span data-stu-id="fc2bc-107">**To create a signed message**</span></span>

1.  <span data-ttu-id="fc2bc-108">Cree los datos (si es necesario) y obtenga un puntero a él.</span><span class="sxs-lookup"><span data-stu-id="fc2bc-108">Create the data (if necessary) and get a pointer to it.</span></span>
2.  <span data-ttu-id="fc2bc-109">Abra un [*almacén de certificados*](../secgloss/c-gly.md) que contenga el certificado del firmante.</span><span class="sxs-lookup"><span data-stu-id="fc2bc-109">Open a [*certificate store*](../secgloss/c-gly.md) that contains the signer's certificate.</span></span>
3.  <span data-ttu-id="fc2bc-110">Obtiene la [*clave privada*](../secgloss/p-gly.md) del certificado.</span><span class="sxs-lookup"><span data-stu-id="fc2bc-110">Get the [*private key*](../secgloss/p-gly.md) for the certificate.</span></span> <span data-ttu-id="fc2bc-111">Se debe establecer una propiedad en el certificado antes de utilizarla, para vincular un certificado a un [*CSP*](../secgloss/c-gly.md)determinado y, dentro de ese CSP, a una clave privada determinada.</span><span class="sxs-lookup"><span data-stu-id="fc2bc-111">A property must be set on the certificate before using it, to tie a certificate to a particular [*CSP*](../secgloss/c-gly.md), and, within that CSP, to a particular private key.</span></span> <span data-ttu-id="fc2bc-112">Debe establecerse una vez.</span><span class="sxs-lookup"><span data-stu-id="fc2bc-112">This needs to be set once.</span></span>
4.  <span data-ttu-id="fc2bc-113">Elija un algoritmo hash para la operación de resumen.</span><span class="sxs-lookup"><span data-stu-id="fc2bc-113">Choose a hashing algorithm for the digest operation.</span></span> <span data-ttu-id="fc2bc-114">Se recomienda seleccionar el algoritmo hash de una ubicación configurable que se puede actualizar posteriormente sin necesidad de realizar cambios en el código.</span><span class="sxs-lookup"><span data-stu-id="fc2bc-114">We recommend that the hashing algorithm be selected from a configurable location that can be subsequently updated without requiring changes to code.</span></span>
5.  <span data-ttu-id="fc2bc-115">Enviar los datos a través de la función de hash mediante el algoritmo hash, con lo que se crea un [*hash*](../secgloss/h-gly.md) (síntesis) de los datos.</span><span class="sxs-lookup"><span data-stu-id="fc2bc-115">Send the data through the hashing function by using the hashing algorithm, thus creating a [*hash*](../secgloss/h-gly.md) (digest) of the data.</span></span>
6.  <span data-ttu-id="fc2bc-116">Mediante la [*clave privada*](../secgloss/p-gly.md) obtenida a través de la propiedad en el certificado, Cifre el Resumen y cree la firma.</span><span class="sxs-lookup"><span data-stu-id="fc2bc-116">Using the [*private key*](../secgloss/p-gly.md) obtained through the property on the certificate, encrypt the digest, creating the signature.</span></span>
7.  <span data-ttu-id="fc2bc-117">Incluya lo siguiente en el mensaje firmado:</span><span class="sxs-lookup"><span data-stu-id="fc2bc-117">Include the following in the signed message:</span></span>

    -   <span data-ttu-id="fc2bc-118">Los datos firmados</span><span class="sxs-lookup"><span data-stu-id="fc2bc-118">The signed data</span></span>
    -   <span data-ttu-id="fc2bc-119">Algoritmo hash</span><span class="sxs-lookup"><span data-stu-id="fc2bc-119">The hash algorithm</span></span>
    -   <span data-ttu-id="fc2bc-120">La firma</span><span class="sxs-lookup"><span data-stu-id="fc2bc-120">The signature</span></span>
    -   <span data-ttu-id="fc2bc-121">El identificador del firmante (emisor de certificados y número de serie)</span><span class="sxs-lookup"><span data-stu-id="fc2bc-121">The signer identifier (certificate issuer and serial number)</span></span>
    -   <span data-ttu-id="fc2bc-122">El certificado del firmante (opcional)</span><span class="sxs-lookup"><span data-stu-id="fc2bc-122">The signer's certificate (optional)</span></span>

<span data-ttu-id="fc2bc-123">Para obtener un procedimiento detallado y un ejemplo, vea el [procedimiento para firmar datos](procedure-for-signing-data.md) y [el programa de ejemplo C: firmar un mensaje y comprobar la firma de un mensaje](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span><span class="sxs-lookup"><span data-stu-id="fc2bc-123">For a detailed procedure and example, see [Procedure for Signing Data](procedure-for-signing-data.md) and [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
