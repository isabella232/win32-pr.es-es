---
description: La autenticación es interactiva cuando se solicita al usuario que proporcione información de inicio de sesión. La autoridad de seguridad local (LSA) realiza una autenticación interactiva cuando un usuario inicia sesión a través de la interfaz de usuario GINA.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Autenticación interactiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361211"
---
# <a name="interactive-authentication"></a><span data-ttu-id="30539-104">Autenticación interactiva</span><span class="sxs-lookup"><span data-stu-id="30539-104">Interactive Authentication</span></span>

<span data-ttu-id="30539-105">La autenticación es interactiva cuando se solicita al usuario que proporcione información de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="30539-105">Authentication is interactive when a user is prompted to supply logon information.</span></span> <span data-ttu-id="30539-106">La [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) realiza una autenticación interactiva cuando un usuario inicia sesión a través de la interfaz de usuario [*Gina*](../secgloss/g-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="30539-106">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) performs an interactive authentication when a user logs on through the [*GINA*](../secgloss/g-gly.md) user interface.</span></span> <span data-ttu-id="30539-107">En la ilustración siguiente se muestran las partes de una autenticación interactiva típica.</span><span class="sxs-lookup"><span data-stu-id="30539-107">The following illustration shows the parts of a typical interactive authentication.</span></span>

![autenticación interactiva](images/lsaint3.png)

<span data-ttu-id="30539-109">Un usuario indica al sistema que comience la secuencia de inicio de sesión escribiendo la [*secuencia de atención de seguridad*](../secgloss/s-gly.md) (SAS) Ctrl + Alt + Supr.</span><span class="sxs-lookup"><span data-stu-id="30539-109">A user signals the system to begin the logon sequence by typing the CTRL+ALT+DEL [*secure attention sequence*](../secgloss/s-gly.md) (SAS).</span></span> <span data-ttu-id="30539-110">[*Winlogon*](../secgloss/w-gly.md) recibe la SAS y llama a Gina para mostrar una interfaz de usuario y obtener los datos de inicio de sesión del usuario, como un nombre de usuario y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="30539-110">[*Winlogon*](../secgloss/w-gly.md) receives the SAS and calls the GINA to display a user interface and obtain the user's logon data, such as a user name and password.</span></span>

<span data-ttu-id="30539-111">Después de obtener los datos de inicio de sesión, GINA llama a la función [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) para autenticar al usuario, especificando qué paquete de autenticación debe usarse para evaluar los datos de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="30539-111">After obtaining the logon data, the GINA calls the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) function to authenticate the user, specifying which authentication package must be used to evaluate the logon data.</span></span>

<span data-ttu-id="30539-112">LSA llama al paquete de autenticación especificado y le pasa los datos de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="30539-112">The LSA calls the specified authentication package and passes the logon data to it.</span></span> <span data-ttu-id="30539-113">El paquete de autenticación examina los datos y determina si la autenticación se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="30539-113">The authentication package examines the data and determines whether the authentication is successful.</span></span> <span data-ttu-id="30539-114">El resultado de la autenticación se devuelve a la LSA y de la LSA a GINA.</span><span class="sxs-lookup"><span data-stu-id="30539-114">The authentication result is returned to the LSA and from the LSA, to the GINA.</span></span>

<span data-ttu-id="30539-115">GINA muestra el éxito o el error de la autenticación al usuario y devuelve el resultado de la autenticación a Winlogon.</span><span class="sxs-lookup"><span data-stu-id="30539-115">The GINA displays the success or failure of the authentication to the user and returns the result of the authentication to Winlogon.</span></span> <span data-ttu-id="30539-116">Si la autenticación se realiza correctamente, se inicia la sesión de inicio de sesión del usuario y se guarda un conjunto de [*credenciales*](../secgloss/c-gly.md) de inicio de sesión para futuras referencias.</span><span class="sxs-lookup"><span data-stu-id="30539-116">If the authentication succeeds, the user's logon session begins and a set of logon [*credentials*](../secgloss/c-gly.md) are saved for future reference.</span></span>

> [!Note]  
> <span data-ttu-id="30539-117">En general, un desarrollador que escribe una GINA personalizada para aceptar datos de inicio de sesión especializados, como una [*tarjeta inteligente*](../secgloss/s-gly.md) o datos de análisis de retina, también debe escribir un paquete de autenticación responsable de procesar los datos y determinar su autenticidad.</span><span class="sxs-lookup"><span data-stu-id="30539-117">In general, a developer who writes a custom GINA to accept specialized logon data, such as a [*smart card*](../secgloss/s-gly.md) or retinal-scan data, must also write an authentication package responsible for processing that data and determining its authenticity.</span></span>

 

<span data-ttu-id="30539-118">Para obtener más información acerca de Winlogon y GINAs, consulte [Winlogon y Gina](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="30539-118">For more information about Winlogon and GINAs, see [Winlogon and GINA](winlogon-and-gina.md).</span></span> <span data-ttu-id="30539-119">Para obtener más información acerca de los paquetes de autenticación, vea [crear paquetes de seguridad personalizados](creating-custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="30539-119">For more information about authentication packages, see [Creating Custom Security Packages](creating-custom-security-packages.md).</span></span>

 

 
