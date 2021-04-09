---
description: El modelo de seguridad utilizado en el protocolo SMB de Microsoft es idéntico al utilizado por otras variantes de SMB y consta de dos niveles de seguridad&\# 8212; usuario y recurso compartido.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Autenticación de protocolo SMB de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907901"
---
# <a name="microsoft-smb-protocol-authentication"></a><span data-ttu-id="05414-103">Autenticación de protocolo SMB de Microsoft</span><span class="sxs-lookup"><span data-stu-id="05414-103">Microsoft SMB Protocol Authentication</span></span>

<span data-ttu-id="05414-104">El modelo de seguridad utilizado en el protocolo SMB de Microsoft es idéntico al usado por otras variantes de SMB y consta de dos niveles de seguridad: usuario y recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="05414-104">The security model used in Microsoft SMB Protocol is identical to the one used by other variants of SMB, and consists of two levels of security—user and share.</span></span> <span data-ttu-id="05414-105">Un recurso compartido es un archivo, un directorio o una impresora a los que pueden tener acceso los clientes del protocolo SMB de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05414-105">A share is a file, directory, or printer that can be accessed by Microsoft SMB Protocol clients.</span></span>

<span data-ttu-id="05414-106">La autenticación de nivel de usuario indica que el cliente que intenta tener acceso a un recurso compartido en un servidor debe proporcionar un nombre de usuario y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="05414-106">User-level authentication indicates that the client attempting to access a share on a server must provide a user name and password.</span></span> <span data-ttu-id="05414-107">Cuando se autentica, el usuario puede tener acceso a todos los recursos compartidos de un servidor no protegido también por seguridad de nivel de recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="05414-107">When authenticated, the user can then access all shares on a server not also protected by share-level security.</span></span> <span data-ttu-id="05414-108">Este nivel de seguridad permite a los administradores del sistema determinar específicamente qué usuarios y grupos pueden tener acceso a un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="05414-108">This security level allows system administrators to specifically determine which users and groups can access a share.</span></span>

<span data-ttu-id="05414-109">La autenticación de nivel de recurso compartido indica que el acceso a un recurso compartido solo está controlado por una contraseña asignada a ese recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="05414-109">Share-level authentication indicates that access to a share is controlled by a password assigned to that share only.</span></span> <span data-ttu-id="05414-110">A diferencia de la seguridad de nivel de usuario, este nivel de seguridad no requiere un nombre de usuario para la autenticación y no se establece ninguna identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="05414-110">Unlike user-level security, this security level does not require a user name for authentication and no user identity is established.</span></span>

<span data-ttu-id="05414-111">En ambos niveles de seguridad, la contraseña se cifra antes de enviarla al servidor.</span><span class="sxs-lookup"><span data-stu-id="05414-111">Under both of these security levels, the password is encrypted before it is sent to the server.</span></span> <span data-ttu-id="05414-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) y el cifrado antiguo de LAN Manager (LM) son compatibles con el protocolo SMB de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05414-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) and the older LAN Manager (LM) encryption are supported by Microsoft SMB Protocol.</span></span> <span data-ttu-id="05414-113">Ambos métodos de cifrado utilizan la autenticación de desafío-respuesta, donde el servidor envía al cliente una cadena aleatoria y el cliente devuelve una cadena de respuesta calculada que demuestra que el cliente tiene credenciales suficientes para el acceso.</span><span class="sxs-lookup"><span data-stu-id="05414-113">Both encryption methods use challenge-response authentication, where the server sends the client a random string and the client returns a computed response string that proves the client has sufficient credentials for access.</span></span>

 

 
