---
description: Para ayudar a mantener la seguridad de una instalación de software, siga estas instrucciones al crear una Windows Installer acción personalizada.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Directrices para proteger las acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119c045833b165222756702244cf65bb2225a8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277555"
---
# <a name="guidelines-for-securing-custom-actions"></a><span data-ttu-id="8f7b7-103">Directrices para proteger las acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="8f7b7-103">Guidelines for Securing Custom Actions</span></span>

<span data-ttu-id="8f7b7-104">El cumplimiento de las siguientes directrices al crear un paquete de Windows Installer con acciones personalizadas ayuda a mantener un entorno seguro durante la instalación:</span><span class="sxs-lookup"><span data-stu-id="8f7b7-104">Adherence to the following guidelines when authoring a Windows Installer package with custom actions helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="8f7b7-105">Proteja los archivos adicionales escritos por la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-105">Secure any additional files written by your custom action.</span></span>
-   <span data-ttu-id="8f7b7-106">Compruebe la longitud del búfer y la validez de todos los datos leídos por la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-106">Check buffer lengths and validity of all data read by your custom action.</span></span> <span data-ttu-id="8f7b7-107">Esto incluye propiedades que pueden proporcionar datos a la acción personalizada, especialmente las que usan propiedades públicas proporcionadas por un usuario.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-107">This includes properties that may supply data to your custom action, particularly those that use public properties provided by a user.</span></span>
-   <span data-ttu-id="8f7b7-108">No confíe en archivos dll externos que no sean de confianza para el sistema en todas las plataformas en las que el paquete de instalación está diseñado para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-108">Do not rely on external DLLs that are not trusted by the system on all platforms on which your installation package is intended to run.</span></span>
-   <span data-ttu-id="8f7b7-109">Considere detenidamente si desea usar acciones personalizadas que usen privilegios [*elevados*](e-gly.md) o suplantación.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-109">Carefully consider whether to use custom actions that use [*elevated*](e-gly.md) privileges or impersonation.</span></span> <span data-ttu-id="8f7b7-110">Acciones personalizadas como "abrir una dirección URL después de completarse la instalación", "iniciar el software después de completarse la instalación" o "iniciar el archivo Léame una vez completada la instalación" no suele requerir privilegios elevados para funcionar.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-110">Custom actions such as “open a URL after installation is completed,” “launch the software after installation is complete,” or “launch ReadMe after installation is complete” would not usually require elevated privileges to function.</span></span> <span data-ttu-id="8f7b7-111">Si la acción personalizada se debe ejecutar con privilegios *elevados* , asegúrese de que el código de acción personalizada se protege contra las saturaciones del búfer y la carga involuntaria de código no seguro.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-111">If your custom action must run with *elevated* privileges, be sure that the custom action code guards against buffer overruns and inadvertent loading of unsafe code.</span></span> <span data-ttu-id="8f7b7-112">Tenga en cuenta que durante la fase de ejecución de la instalación, el instalador pasa información a un proceso con privilegios *elevados* y ejecuta el script.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-112">Note that during the execution phase of the installation, the installer passes information to a process with *elevated* privileges and runs the script.</span></span> <span data-ttu-id="8f7b7-113">Cualquier acción personalizada que se ejecute durante la fase de ejecución puede ejecutarse con privilegios *elevados* .</span><span class="sxs-lookup"><span data-stu-id="8f7b7-113">Any custom actions that run during the execution phase may run with *elevated* privileges.</span></span>
-   <span data-ttu-id="8f7b7-114">Recopile toda la información proporcionada por el usuario durante la secuencia de IU.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-114">Gather all information provided by the user during the UI sequence.</span></span> <span data-ttu-id="8f7b7-115">No solicite al usuario ninguna información que no se pueda establecer mediante una propiedad pública.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-115">Do not prompt the user for any information that can't be set using a public property.</span></span>
-   <span data-ttu-id="8f7b7-116">Si la acción personalizada de script expande propiedades, tome precauciones para asegurarse de que la acción personalizada está protegida contra la posibilidad de que se produzca la inyección de script.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-116">If your script custom action expands properties, take precautions that the custom action is secured against the possibility of script injection.</span></span> <span data-ttu-id="8f7b7-117">El script puede estar registrado en texto no cifrado.</span><span class="sxs-lookup"><span data-stu-id="8f7b7-117">Script may be logged in clear text.</span></span>

<span data-ttu-id="8f7b7-118">Vea también [seguridad de la acción personalizada](custom-action-security.md).</span><span class="sxs-lookup"><span data-stu-id="8f7b7-118">See also [Custom Action Security](custom-action-security.md).</span></span>

 

 



