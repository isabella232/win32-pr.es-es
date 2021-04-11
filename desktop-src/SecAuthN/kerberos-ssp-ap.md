---
description: El paquete de autenticación de Kerberos se usa al iniciar sesión en una red; los inicios de sesión locales se controlan mediante MSV1 \_ 0.
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: SSP/SSP de Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082773"
---
# <a name="kerberos-sspap"></a><span data-ttu-id="904e5-103">SSP/SSP de Kerberos</span><span class="sxs-lookup"><span data-stu-id="904e5-103">Kerberos SSP/AP</span></span>

<span data-ttu-id="904e5-104">El paquete de autenticación de [*Kerberos*](../secgloss/k-gly.md) se usa al iniciar sesión en una red; los inicios de sesión locales se controlan mediante MSV1 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="904e5-104">The [*Kerberos*](../secgloss/k-gly.md) authentication package is used when logging on to a network; local logons are handled by MSV1\_0.</span></span>

<span data-ttu-id="904e5-105">Cuando un usuario inicia sesión con una cuenta de red, de forma predeterminada, Kerberos intenta conectarse al [*centro de distribución de claves*](../secgloss/k-gly.md) de Kerberos (KDC) en el controlador de dominio y obtener un vale de concesión de vales (TGT) mediante los datos de inicio de sesión proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="904e5-105">When a user logs on using a network account, by default, Kerberos attempts to connect to the Kerberos [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) on the domain controller and obtain a ticket granting ticket (TGT) by using the logon data supplied by the user.</span></span>

<span data-ttu-id="904e5-106">Si un KDC de Kerberos no está disponible, Windows usa MSV1 \_ 0 y la autenticación de paso a través como se describe en el [paquete de \_ autenticación MSV1 0](msv1-0-authentication-package.md).</span><span class="sxs-lookup"><span data-stu-id="904e5-106">If a Kerberos KDC is not available, Windows uses MSV1\_0 and pass-through authentication as described in [MSV1\_0 Authentication Package](msv1-0-authentication-package.md).</span></span>

<span data-ttu-id="904e5-107">El paquete de autenticación Kerberos admite la versión 5, revisión 6 del protocolo Kerberos.</span><span class="sxs-lookup"><span data-stu-id="904e5-107">The Kerberos authentication package supports version 5, revision 6 of the Kerberos protocol.</span></span> <span data-ttu-id="904e5-108">Este protocolo se basa en el [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt)de Internet.</span><span class="sxs-lookup"><span data-stu-id="904e5-108">This protocol is based on Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).</span></span> <span data-ttu-id="904e5-109">Para obtener más información, vea el sitio web de IETF:</span><span class="sxs-lookup"><span data-stu-id="904e5-109">For more information, see the IETF website:</span></span>

[https://www.ietf.org](https://www.ietf.org/)

<span data-ttu-id="904e5-110">Para obtener más información acerca de Kerberos, consulte [Microsoft Kerberos](microsoft-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="904e5-110">For more information about Kerberos, see [Microsoft Kerberos](microsoft-kerberos.md).</span></span>

## <a name="kerberos-credential-formats"></a><span data-ttu-id="904e5-111">Formatos de credenciales de Kerberos</span><span class="sxs-lookup"><span data-stu-id="904e5-111">Kerberos Credential Formats</span></span>

<span data-ttu-id="904e5-112">Las [*credenciales*](../secgloss/c-gly.md) de usuario asignadas por el paquete de autenticación Kerberos después de un intento de inicio de sesión correcto son un vale y una clave de cifrado temporal, a menudo denominada [*clave de sesión*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="904e5-112">The user [*credentials*](../secgloss/c-gly.md) assigned by the Kerberos authentication package after a successful logon attempt are a ticket and a temporary encryption key, often called a [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="904e5-113">El vale contiene una copia cifrada de las credenciales del cliente y la clave de sesión.</span><span class="sxs-lookup"><span data-stu-id="904e5-113">The ticket contains both an encrypted copy of the client's credentials and the session key.</span></span>

 

 
