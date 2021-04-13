---
description: Una aplicación que utiliza una entidad de seguridad para almacenar las claves de sesión suele seguir estos pasos.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Almacenar claves de sesión mediante una entidad de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360744"
---
# <a name="storing-session-keys-using-a-backup-authority"></a><span data-ttu-id="4bd53-103">Almacenar claves de sesión mediante una entidad de seguridad</span><span class="sxs-lookup"><span data-stu-id="4bd53-103">Storing Session Keys Using a Backup Authority</span></span>

<span data-ttu-id="4bd53-104">Una aplicación que utiliza una [*entidad de seguridad*](../secgloss/b-gly.md) para almacenar las claves de sesión suele seguir estos pasos.</span><span class="sxs-lookup"><span data-stu-id="4bd53-104">An application using a [*backup authority*](../secgloss/b-gly.md) to store session keys typically follows these steps.</span></span>

<span data-ttu-id="4bd53-105">**Para usar una autoridad de copia de seguridad**</span><span class="sxs-lookup"><span data-stu-id="4bd53-105">**To use a backup authority**</span></span>

1.  <span data-ttu-id="4bd53-106">Cifre el archivo como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="4bd53-106">Encrypt the file as usual.</span></span>
2.  <span data-ttu-id="4bd53-107">Exporte la [*clave de sesión*](../secgloss/s-gly.md) usada para cifrar el archivo en un [*BLOB de clave simple*](../secgloss/s-gly.md), especificando que su propia [*clave pública de intercambio de claves*](../secgloss/k-gly.md) se usará para cifrar el BLOB de clave.</span><span class="sxs-lookup"><span data-stu-id="4bd53-107">Export the [*session key*](../secgloss/s-gly.md) used to encrypt the file into a [*simple key BLOB*](../secgloss/s-gly.md), specifying that your own [*key exchange public key*](../secgloss/k-gly.md) be used to encrypt the key BLOB.</span></span> <span data-ttu-id="4bd53-108">Almacene este BLOB de clave con el archivo cifrado.</span><span class="sxs-lookup"><span data-stu-id="4bd53-108">Store this key BLOB with the encrypted file.</span></span>
3.  <span data-ttu-id="4bd53-109">Vuelva a exportar la clave de sesión, esta vez especificando que se utilizará la clave pública de la entidad de copia de seguridad para cifrar el BLOB de clave.</span><span class="sxs-lookup"><span data-stu-id="4bd53-109">Export the session key again, this time specifying that the backup authority's public key be used to encrypt the key BLOB.</span></span> <span data-ttu-id="4bd53-110">Envíe este BLOB de clave a la entidad de seguridad, junto con la descripción de la clave, el número de serie, etc.</span><span class="sxs-lookup"><span data-stu-id="4bd53-110">Send this key BLOB to the backup authority, along with the key's description, serial number, and so on.</span></span>

<span data-ttu-id="4bd53-111">Si se pierde un [*par de claves*](../secgloss/k-gly.md) , las claves se pueden recuperar de la [*entidad de seguridad*](../secgloss/b-gly.md) si se puede establecer la identidad del propietario de las claves.</span><span class="sxs-lookup"><span data-stu-id="4bd53-111">If a [*key pair*](../secgloss/k-gly.md) is lost, the keys can be retrieved from the [*backup authority*](../secgloss/b-gly.md) if the identity of the keys' owner can be established.</span></span> <span data-ttu-id="4bd53-112">El procedimiento para establecer la identidad viene determinado por la Directiva de la entidad de seguridad concreta y no implica CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="4bd53-112">The procedure for establishing identity is determined by the policy of the particular backup authority and does not involve CryptoAPI.</span></span>

<span data-ttu-id="4bd53-113">Para el código necesario para crear una clave de sesión y exportar esa clave a un [*BLOB de clave simple*](../secgloss/s-gly.md) que se puede escribir en un archivo de disco, vea el [ejemplo C programa: exportar una clave de sesión](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="4bd53-113">For the code needed to create a session key and export that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

 

 
