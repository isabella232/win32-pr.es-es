---
description: En esta sección se incluyen escenarios en los que se usan los procedimientos de CAPICOM.
ms.assetid: f886e04a-4ea7-4d24-a05f-3e08742fe134
title: Usar CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81b1a346b6186ead6544b7194259cc52ae2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543523"
---
# <a name="using-capicom"></a><span data-ttu-id="fdc17-103">Usar CAPICOM</span><span class="sxs-lookup"><span data-stu-id="fdc17-103">Using CAPICOM</span></span>

<span data-ttu-id="fdc17-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fdc17-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fdc17-105">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fdc17-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="fdc17-106">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="fdc17-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="fdc17-107">En esta sección se incluyen escenarios en los que se usan los procedimientos de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="fdc17-107">This section includes scenarios that use CAPICOM procedures.</span></span>

> [!Note]  
> <span data-ttu-id="fdc17-108">La creación de [*firmas digitales*](../secgloss/d-gly.md) y la desprotección de mensajes con CAPICOM se realiza mediante la criptografía de infraestructura de clave pública (PKI) y solo se puede hacer si el firmante o el usuario que descifra un mensaje con doble cifrado tiene acceso a un certificado con una clave privada asociada disponible.</span><span class="sxs-lookup"><span data-stu-id="fdc17-108">Creating [*digital signatures*](../secgloss/d-gly.md) and un-enveloping messages with CAPICOM is done using Public Key Infrastructure (PKI) cryptography and can only be done if the signer or user decrypting an enveloped message has access to a certificate with an available, associated private key.</span></span> <span data-ttu-id="fdc17-109">Para descifrar un mensaje con doble cifrado, debe haber un certificado con acceso a la clave privada en el almacén MY.</span><span class="sxs-lookup"><span data-stu-id="fdc17-109">To decrypt an enveloped message, a certificate with access to the private key must be in the MY store.</span></span>

 

<span data-ttu-id="fdc17-110">Los ejemplos y las discusiones de escenarios basados en tareas se han separado en las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="fdc17-110">Task-based scenarios discussions and examples have been separated into the following sections:</span></span>

-   [<span data-ttu-id="fdc17-111">Alternativas al uso de CAPICOM</span><span class="sxs-lookup"><span data-stu-id="fdc17-111">Alternatives to Using CAPICOM</span></span>](alternatives-to-using-capicom.md)
-   [<span data-ttu-id="fdc17-112">Preparación para usar CAPICOM</span><span class="sxs-lookup"><span data-stu-id="fdc17-112">Getting Ready to Use CAPICOM</span></span>](getting-ready-to-use-capicom.md)
-   [<span data-ttu-id="fdc17-113">Cifrar y descifrar datos</span><span class="sxs-lookup"><span data-stu-id="fdc17-113">Encrypting and Decrypting Data</span></span>](encrypting-and-decrypting-data.md)
-   [<span data-ttu-id="fdc17-114">Firmar datos y comprobar firmas digitales</span><span class="sxs-lookup"><span data-stu-id="fdc17-114">Signing Data and Verifying Digital Signatures</span></span>](signing-data-and-verifying-digital-signatures.md)
-   [<span data-ttu-id="fdc17-115">Uso de almacenes de certificados</span><span class="sxs-lookup"><span data-stu-id="fdc17-115">Using Certificate Stores</span></span>](using-certificate-stores.md)
-   [<span data-ttu-id="fdc17-116">Crear y recibir mensajes de datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="fdc17-116">Creating and Receiving Enveloped Data Messages</span></span>](creating-and-receiving-enveloped-data-messages-in-capicom.md)

 

 
