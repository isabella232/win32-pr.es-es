---
description: Explica los dos tipos de credenciales con las que funciona la API de administración de credenciales.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Tipos de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30968484b2cfc89b9238f624d9299fb75c72bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002133"
---
# <a name="kinds-of-credentials"></a><span data-ttu-id="9a899-103">Tipos de credenciales</span><span class="sxs-lookup"><span data-stu-id="9a899-103">Kinds of Credentials</span></span>

<span data-ttu-id="9a899-104">La API de administración de credenciales funciona con dos tipos de credenciales:</span><span class="sxs-lookup"><span data-stu-id="9a899-104">The Credentials Management API works with two kinds of credentials:</span></span>

-   [<span data-ttu-id="9a899-105">Credenciales de dominio</span><span class="sxs-lookup"><span data-stu-id="9a899-105">Domain Credentials</span></span>](#domain-credentials)
-   [<span data-ttu-id="9a899-106">Credenciales genéricas</span><span class="sxs-lookup"><span data-stu-id="9a899-106">Generic Credentials</span></span>](#generic-credentials)

## <a name="domain-credentials"></a><span data-ttu-id="9a899-107">Credenciales del dominio</span><span class="sxs-lookup"><span data-stu-id="9a899-107">Domain Credentials</span></span>

<span data-ttu-id="9a899-108">El sistema operativo usa las credenciales de dominio y las autentica la autoridad de seguridad local (LSA).</span><span class="sxs-lookup"><span data-stu-id="9a899-108">Domain credentials are used by the operating system and authenticated by the Local Security Authority (LSA).</span></span> <span data-ttu-id="9a899-109">Normalmente, las credenciales de dominio se establecen para un usuario cuando un paquete de seguridad registrado, como el protocolo Kerberos, autentica los datos de inicio de sesión proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9a899-109">Typically, domain credentials are established for a user when a registered security package, such as the Kerberos protocol, authenticates logon data that is provided by the user.</span></span> <span data-ttu-id="9a899-110">El sistema operativo almacena en caché las credenciales de inicio de sesión para que un inicio de sesión único proporcione al usuario acceso a muchos recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="9a899-110">The logon credentials are cached by the operating system so that a single sign-on gives the user access to many different resources.</span></span> <span data-ttu-id="9a899-111">Por ejemplo, las conexiones de red pueden producirse de forma transparente y el acceso a los objetos del sistema protegidos se puede conceder en función de las credenciales de dominio almacenadas en caché del usuario.</span><span class="sxs-lookup"><span data-stu-id="9a899-111">For example, network connections can occur transparently, and access to protected system objects can be granted based on the user's cached domain credentials.</span></span>

<span data-ttu-id="9a899-112">Las funciones de administración de credenciales proporcionan un mecanismo para que las aplicaciones pidan a un usuario las credenciales de dominio después de que el usuario inicie sesión y para que el sistema operativo autentique la información proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9a899-112">Credentials Management functions provide a mechanism for applications to prompt a user for domain credentials after the user logs on, and to have the operating system authenticate the information that is provided by the user.</span></span>

<span data-ttu-id="9a899-113">La parte secreta de las credenciales de dominio, la contraseña, está protegida por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9a899-113">The secret part of domain credentials, the password, is protected by the operating system.</span></span> <span data-ttu-id="9a899-114">Solo el código que se ejecuta en proceso con LSA puede leer y escribir credenciales de dominio.</span><span class="sxs-lookup"><span data-stu-id="9a899-114">Only code running in-process with the LSA can read and write domain credentials.</span></span> <span data-ttu-id="9a899-115">Las aplicaciones se limitan a escribir las credenciales de dominio.</span><span class="sxs-lookup"><span data-stu-id="9a899-115">Applications are limited to writing domain credentials.</span></span>

<span data-ttu-id="9a899-116">Windows admite el uso expandido de credenciales de tarjeta inteligente y certificado.</span><span class="sxs-lookup"><span data-stu-id="9a899-116">Windows supports expanded use of smart card and certificate credentials.</span></span> <span data-ttu-id="9a899-117">Para ayudar a garantizar la seguridad, la API de administración de credenciales nunca almacena el PIN de la tarjeta inteligente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="9a899-117">To help ensure security, the Credentials Management API never stores the smart card PIN on the computer.</span></span>

## <a name="generic-credentials"></a><span data-ttu-id="9a899-118">Credenciales genéricas</span><span class="sxs-lookup"><span data-stu-id="9a899-118">Generic Credentials</span></span>

<span data-ttu-id="9a899-119">Las credenciales genéricas las definen y autentican las aplicaciones que administran la autorización y la seguridad directamente en lugar de delegar estas tareas en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9a899-119">Generic credentials are defined and authenticated by applications that manage authorization and security directly instead of delegating these tasks to the operating system.</span></span> <span data-ttu-id="9a899-120">Por ejemplo, una aplicación puede requerir a los usuarios que escriban un nombre de usuario y una contraseña proporcionados por la aplicación o que generen un [*certificado*](../secgloss/c-gly.md) para tener acceso a un sitio Web.</span><span class="sxs-lookup"><span data-stu-id="9a899-120">For example, an application can require users to enter a user name and password provided by the application or to produce a [*certificate*](../secgloss/c-gly.md) to access a website.</span></span>

<span data-ttu-id="9a899-121">Las aplicaciones usan funciones de administración de credenciales para solicitar a los usuarios información de credenciales, genéricas y definidas por la aplicación, como el nombre de usuario, el certificado, la tarjeta inteligente o la contraseña.</span><span class="sxs-lookup"><span data-stu-id="9a899-121">Applications use Credentials Management functions to prompt users for application-defined, generic, credential information, such as user name, certificate, smart card, or password.</span></span> <span data-ttu-id="9a899-122">La información especificada por el usuario se devuelve a la aplicación para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="9a899-122">The information entered by the user is returned to the application for authentication.</span></span>

<span data-ttu-id="9a899-123">La administración de credenciales proporciona administración de caché personalizable y almacenamiento a largo plazo para las credenciales genéricas.</span><span class="sxs-lookup"><span data-stu-id="9a899-123">Credentials Management provides customizable cache management and long-term storage for generic credentials.</span></span> <span data-ttu-id="9a899-124">Los procesos de usuario pueden leer y escribir las credenciales genéricas.</span><span class="sxs-lookup"><span data-stu-id="9a899-124">Generic credentials can be read and written by user processes.</span></span>

 

 
