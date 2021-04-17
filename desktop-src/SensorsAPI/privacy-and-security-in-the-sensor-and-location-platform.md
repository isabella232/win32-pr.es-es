---
description: El sensor de Windows y la plataforma de ubicación incluyen la configuración de privacidad para ayudar a proteger la información personal de los usuarios.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Privacidad y seguridad en el sensor de Windows y la plataforma de ubicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666370"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a><span data-ttu-id="1bc12-103">Privacidad y seguridad en el sensor de Windows y la plataforma de ubicación</span><span class="sxs-lookup"><span data-stu-id="1bc12-103">Privacy and Security in the Windows Sensor and Location Platform</span></span>

<span data-ttu-id="1bc12-104">El sensor de Windows y la plataforma de ubicación incluyen la configuración de privacidad para ayudar a proteger la información personal de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1bc12-104">The Windows Sensor and Location platform includes privacy settings to help protect users' personal information.</span></span>

<span data-ttu-id="1bc12-105">La plataforma ayuda a garantizar que los datos del sensor permanecen privados, cuando se requiere privacidad, de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="1bc12-105">The platform helps to ensure that sensor data remains private, when privacy is required, in the following ways:</span></span>

-   <span data-ttu-id="1bc12-106">De forma predeterminada, los sensores están desactivados.</span><span class="sxs-lookup"><span data-stu-id="1bc12-106">By default, sensors are off.</span></span> <span data-ttu-id="1bc12-107">Dado que el diseño de la plataforma presupone que cualquier sensor puede proporcionar datos personales, cada sensor está deshabilitado hasta que el usuario proporciona consentimiento explícito para acceder a los datos del sensor.</span><span class="sxs-lookup"><span data-stu-id="1bc12-107">Because the platform design presumes that any sensor can provide personal data, each sensor is disabled until the user provides explicit consent to access the sensor data.</span></span>
-   <span data-ttu-id="1bc12-108">Windows proporciona mensajes de divulgación y contenido de ayuda para el usuario.</span><span class="sxs-lookup"><span data-stu-id="1bc12-108">Windows provides disclosure messages and Help content for the user.</span></span> <span data-ttu-id="1bc12-109">Este contenido ayuda a los usuarios a entender cómo los sensores pueden afectar a la privacidad de sus datos personales y ayudan a los usuarios a tomar decisiones informadas.</span><span class="sxs-lookup"><span data-stu-id="1bc12-109">This content helps users understand how sensors can affect the privacy of their personal data and helps users make informed decisions.</span></span>
-   <span data-ttu-id="1bc12-110">El suministro de permisos para un sensor requiere derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="1bc12-110">Providing permission for a sensor requires administrator rights.</span></span>
-   <span data-ttu-id="1bc12-111">Cuando está habilitada, un dispositivo de sensor funciona para todos los programas que se ejecutan en una cuenta de usuario determinada (o para todas las cuentas de usuario).</span><span class="sxs-lookup"><span data-stu-id="1bc12-111">When it is enabled, a sensor device works for all programs running under a particular user account (or for all user accounts).</span></span> <span data-ttu-id="1bc12-112">Esto incluye a los usuarios y servicios no interactivos, como ASPNET o SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="1bc12-112">This includes noninteractive users and services, such as ASPNET or SYSTEM.</span></span> <span data-ttu-id="1bc12-113">Por ejemplo, si habilita un sensor GPS para su cuenta de usuario, solo los programas que se ejecutan en su cuenta de usuario tienen acceso al GPS.</span><span class="sxs-lookup"><span data-stu-id="1bc12-113">For example, if you enable a GPS sensor for your user account, only programs running under your user account have access to the GPS.</span></span> <span data-ttu-id="1bc12-114">Si habilita el GPS para todos los usuarios, cualquier programa que se ejecute en cualquier cuenta de usuario tendrá acceso al GPS.</span><span class="sxs-lookup"><span data-stu-id="1bc12-114">If you enable the GPS for all users, any program running under any user account has access to the GPS.</span></span>
-   <span data-ttu-id="1bc12-115">Los programas que utilizan sensores pueden llamar a un método para abrir un cuadro de diálogo de sistema que solicita a los usuarios que habiliten los dispositivos de sensor necesarios.</span><span class="sxs-lookup"><span data-stu-id="1bc12-115">Programs that use sensors can call a method to open a system dialog box that prompts users to enable needed sensor devices.</span></span> <span data-ttu-id="1bc12-116">Esta característica facilita a los desarrolladores y usuarios la seguridad de que los sensores funcionan cuando los programas los necesiten, a la vez que se mantiene el control del usuario de la divulgación de los datos del sensor.</span><span class="sxs-lookup"><span data-stu-id="1bc12-116">This feature makes it easy for developers and users to make sure that sensors work when programs need them, while maintaining user control of disclosure of sensor data.</span></span>
-   <span data-ttu-id="1bc12-117">Los controladores de sensor usan un objeto especial que procesa todas las solicitudes de e/s.</span><span class="sxs-lookup"><span data-stu-id="1bc12-117">Sensor drivers use a special object that processes all I/O requests.</span></span> <span data-ttu-id="1bc12-118">Este objeto garantiza que solo los programas que tienen permiso de usuario pueden tener acceso a los datos del sensor.</span><span class="sxs-lookup"><span data-stu-id="1bc12-118">This object makes sure that only programs that have user permission can access sensor data.</span></span>

 

 



