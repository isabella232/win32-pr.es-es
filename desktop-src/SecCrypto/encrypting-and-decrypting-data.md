---
description: Cuando un documento o texto debe tener privacidad protegida por un solo usuario o cuando el documento se va a compartir entre un pequeño grupo de personas que tienen acceso a la misma contraseña secreta, se puede realizar un cifrado o descifrado simple.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Cifrar y descifrar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002592"
---
# <a name="encrypting-and-decrypting-data"></a><span data-ttu-id="c1acf-103">Cifrar y descifrar datos</span><span class="sxs-lookup"><span data-stu-id="c1acf-103">Encrypting and Decrypting Data</span></span>

<span data-ttu-id="c1acf-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c1acf-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c1acf-105">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c1acf-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="c1acf-106">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="c1acf-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="c1acf-107">Cuando un documento o texto debe tener privacidad protegida por un solo usuario o cuando el documento se va a compartir entre un pequeño grupo de personas que tienen acceso a la misma contraseña secreta, se puede realizar un cifrado o descifrado simple.</span><span class="sxs-lookup"><span data-stu-id="c1acf-107">When a document or text needs to have privacy protected by a single user or when the document is to be shared among a small group of people who all have access to the same secret password, simple encryption/decryption can be done.</span></span> <span data-ttu-id="c1acf-108">CAPICOM no admite el tipo de \# contenido de PKCS 7 EncryptedData, pero usa una estructura ASN no estándar para EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="c1acf-108">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a non-standard ASN structure for EncryptedData.</span></span> <span data-ttu-id="c1acf-109">Por lo tanto, solo CAPICOM puede descifrar un objeto EncryptedData de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="c1acf-109">Therefore, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

<span data-ttu-id="c1acf-110">En las secciones siguientes se muestran ejemplos de tareas de cifrado y descifrado:</span><span class="sxs-lookup"><span data-stu-id="c1acf-110">The following sections show examples for encryption and decryption tasks:</span></span>

-   [<span data-ttu-id="c1acf-111">Cifrado de un mensaje en CAPICOM</span><span class="sxs-lookup"><span data-stu-id="c1acf-111">Encrypting a Message in CAPICOM</span></span>](encrypting-a-message-in-capicom.md)
-   [<span data-ttu-id="c1acf-112">Descifrado de un mensaje en CAPICOM</span><span class="sxs-lookup"><span data-stu-id="c1acf-112">Decrypting a Message in CAPICOM</span></span>](decrypting-a-message-in-capicom.md)

 

 



