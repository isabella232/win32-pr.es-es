---
description: Explica el procedimiento utilizado para almacenar una clave de sesión.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Almacenar una clave de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687592"
---
# <a name="storing-a-session-key"></a><span data-ttu-id="1dd2c-103">Almacenar una clave de sesión</span><span class="sxs-lookup"><span data-stu-id="1dd2c-103">Storing a Session Key</span></span>

> [!Note]  
> <span data-ttu-id="1dd2c-104">En esta sección se da por supuesto que los usuarios disponen de un conjunto de [*pares de claves pública y privada*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1dd2c-104">This section assumes that users possess a set of [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="1dd2c-105">Puede encontrar instrucciones y un ejemplo para crear pares de claves en [el programa C de ejemplo: crear un contenedor de claves y generar claves](example-c-program-creating-a-key-container-and-generating-keys.md).</span><span class="sxs-lookup"><span data-stu-id="1dd2c-105">Instructions and an example for creating key pairs can be found in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span>

 

<span data-ttu-id="1dd2c-106">**Para almacenar una clave de sesión**</span><span class="sxs-lookup"><span data-stu-id="1dd2c-106">**To store a session key**</span></span>

1.  <span data-ttu-id="1dd2c-107">Cree un [*BLOB de clave*](../secgloss/k-gly.md) simple mediante la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) .</span><span class="sxs-lookup"><span data-stu-id="1dd2c-107">Create a simple [*key BLOB*](../secgloss/k-gly.md) by using the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function.</span></span> <span data-ttu-id="1dd2c-108">Esto transferirá la clave de sesión del CSP al espacio de memoria de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-108">This will transfer the session key from the CSP to an application's memory space.</span></span> <span data-ttu-id="1dd2c-109">Especifique que se use una clave pública de Exchange para firmar el BLOB de clave.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-109">Specify that an exchange public key be used to sign the key BLOB.</span></span>
2.  <span data-ttu-id="1dd2c-110">Almacene el BLOB de clave firmado en el disco.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-110">Store the signed key BLOB to disk.</span></span> <span data-ttu-id="1dd2c-111">Se supone que todos los discos no son seguros.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-111">It is assumed that all disks are nonsecure.</span></span>
3.  <span data-ttu-id="1dd2c-112">Cuando se necesite la clave, lea el BLOB de la clave desde el disco.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-112">When the key is needed, read the key BLOB from disk.</span></span>
4.  <span data-ttu-id="1dd2c-113">Vuelva a importar el BLOB de la clave en el CSP mediante la función [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="1dd2c-113">Import the key BLOB back into the CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span>

<span data-ttu-id="1dd2c-114">Para obtener un ejemplo de cómo crear una [*clave de sesión*](../secgloss/s-gly.md) y exportar esa clave a un [*BLOB de clave simple*](../secgloss/s-gly.md) que se puede escribir en un archivo de disco, vea el [ejemplo C programa: exportar una clave de sesión](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="1dd2c-114">For an example of creating a [*session key*](../secgloss/s-gly.md) and exporting that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

<span data-ttu-id="1dd2c-115">Este procedimiento solo proporciona una seguridad mínima.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-115">This procedure provides only minimal security.</span></span> <span data-ttu-id="1dd2c-116">Si la clave de sesión almacenada se va a usar para cifrar los datos en una fecha posterior, el procedimiento anterior no proporciona la seguridad adecuada.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-116">If the stored session key will be used to encrypt data at a later date, the preceding procedure does not provide adequate security.</span></span>

<span data-ttu-id="1dd2c-117">Para proporcionar mayor seguridad, firme el BLOB de clave con una clave privada de Exchange antes de que se almacene en el disco.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-117">To provide greater security, sign the key BLOB with an exchange private key before it is stored to disk.</span></span> <span data-ttu-id="1dd2c-118">Cuando el BLOB de clave se lee después del disco, se puede validar su firma para asegurarse de que el BLOB de clave está intacto.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-118">When the key BLOB is later read from disk, its signature can be validated to ensure that the key BLOB is intact.</span></span>

<span data-ttu-id="1dd2c-119">Si el BLOB de clave no está firmado, cualquier usuario con acceso al disco u otro medio donde se almacena la clave puede crear una nueva clave de sesión.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-119">If the key BLOB is not signed, anyone with access to the disk or other media where the key is stored can create a new session key.</span></span>

<span data-ttu-id="1dd2c-120">La nueva clave de sesión puede cifrarse con la [*clave de intercambio*](../secgloss/e-gly.md)de [*claves públicas*](../secgloss/p-gly.md) del usuario original, y esta nueva clave se puede sustituir por la original.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-120">The new session key can be encrypted with the original user's [*public key*](../secgloss/p-gly.md) [*exchange key*](../secgloss/e-gly.md), and this new key can be substituted for the original.</span></span> <span data-ttu-id="1dd2c-121">Si el usuario usaba sin saberlo la clave de sesión sustituida para cifrar archivos y mensajes, el individuo que creó la clave sustitutivo podría descifrarlos fácilmente.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-121">If the user unknowingly used the substituted session key to encrypt files and messages, the individual who created the substitute key could easily decrypt them.</span></span>

<span data-ttu-id="1dd2c-122">Las firmas digitales se describen en detalle en [hashes y firmas digitales](hashes-and-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="1dd2c-122">Digital signatures are discussed in detail in [Hashes and Digital Signatures](hashes-and-digital-signatures.md).</span></span>

 

 
