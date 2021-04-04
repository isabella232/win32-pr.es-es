---
description: El archivo DLL de filtro de contraseñas de Windows, Passfilt.dll, se ejecuta en el contexto de seguridad de la cuenta de sistema local y ayuda a filtrar contraseñas de cuentas locales o de dominio.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Instalación y registro de un archivo DLL de filtro de contraseñas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd911c1a527384e48a2ae4567f6d85862e184cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910062"
---
# <a name="installing-and-registering-a-password-filter-dll"></a><span data-ttu-id="8f2b6-103">Instalación y registro de un archivo DLL de filtro de contraseñas</span><span class="sxs-lookup"><span data-stu-id="8f2b6-103">Installing and Registering a Password Filter DLL</span></span>

<span data-ttu-id="8f2b6-104">Puede usar el filtro de contraseñas de Windows para filtrar contraseñas de cuentas locales o de dominio.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-104">You can use the Windows password filter to filter domain or local account passwords.</span></span> <span data-ttu-id="8f2b6-105">Para usar el filtro de contraseñas para las cuentas de dominio, instale y registre el archivo DLL en cada controlador de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-105">To use the password filter for domain accounts, install and register the DLL on each domain controller in the domain.</span></span>

<span data-ttu-id="8f2b6-106">Realice los pasos siguientes para instalar el filtro de contraseña.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-106">Perform the following steps to install your password filter.</span></span> <span data-ttu-id="8f2b6-107">Puede realizar estos pasos manualmente o puede escribir un instalador para realizar estos pasos.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-107">You can perform these steps manually, or you can write an installer to perform these steps.</span></span> <span data-ttu-id="8f2b6-108">Debe ser administrador o pertenecer al grupo de administradores para realizar estos pasos.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-108">You need to be an Administrator or belong to the Administrator Group to perform these steps.</span></span>

<span data-ttu-id="8f2b6-109">**Para instalar y registrar un archivo DLL de filtro de contraseñas de Windows**</span><span class="sxs-lookup"><span data-stu-id="8f2b6-109">**To install and register a Windows password filter DLL**</span></span>

1.  <span data-ttu-id="8f2b6-110">Copie el archivo DLL en el directorio de instalación de Windows en el controlador de dominio o en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-110">Copy the DLL to the Windows installation directory on the domain controller or local computer.</span></span> <span data-ttu-id="8f2b6-111">En las instalaciones estándar, la carpeta predeterminada es \\ Windows \\ system32.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-111">On standard installations, the default folder is \\Windows\\System32.</span></span> <span data-ttu-id="8f2b6-112">Asegúrese de crear un archivo DLL de filtro de contraseña de 32 bits para equipos de 32 bits y un archivo DLL de filtro de contraseñas de 64 bits para equipos de 64 bits y, a continuación, cópielos en la ubicación adecuada.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-112">Make sure that you create a 32-bit password filter DLL for 32-bit computers and a 64-bit password filter DLL for 64-bit computers, and then copy them to the appropriate location.</span></span>
2.  <span data-ttu-id="8f2b6-113">Para registrar el filtro de contraseña, actualice la siguiente clave del registro del sistema:</span><span class="sxs-lookup"><span data-stu-id="8f2b6-113">To register the password filter, update the following system registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    <span data-ttu-id="8f2b6-114">Si existe la subclave de **paquetes de notificación** , agregue el nombre de la dll a los datos de valor existentes.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-114">If the **Notification Packages** subkey exists, add the name of your DLL to the existing value data.</span></span> <span data-ttu-id="8f2b6-115">No sobrescriba los valores existentes y no incluya la extensión. dll.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-115">Do not overwrite the existing values, and do not include the .dll extension.</span></span>

    <span data-ttu-id="8f2b6-116">Si la subclave de los **paquetes de notificación** no existe, agréguela y especifique el nombre del archivo DLL para los datos del valor.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-116">If the **Notification Packages** subkey does not exist, add it, and then specify the name of the DLL for the value data.</span></span> <span data-ttu-id="8f2b6-117">No incluya la extensión. dll.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-117">Do not include the .dll extension.</span></span>

    <span data-ttu-id="8f2b6-118">La subclave de **paquetes de notificación** puede agregar varios paquetes.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-118">The **Notification Packages** subkey can add multiple packages.</span></span>

3.  <span data-ttu-id="8f2b6-119">Busque la configuración de complejidad de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-119">Find the password complexity setting.</span></span>

    <span data-ttu-id="8f2b6-120">En el panel de control, haga clic en **rendimiento y mantenimiento**, haga clic en **herramientas administrativas**, haga doble clic en **Directiva de seguridad local**, haga doble clic en **directivas de cuenta** y, a continuación, haga doble clic en **Directiva de contraseñas**.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-120">In Control Panel, click **Performance and Maintenance**, click **Administrative Tools**, double-click **Local Security Policy**, double-click **Account Policies**, and then double-click **Password Policy**.</span></span>

4.  <span data-ttu-id="8f2b6-121">Para aplicar el filtro de contraseña de Windows predeterminado y el filtro de contraseña personalizado, asegúrese de que la configuración de la Directiva las **contraseñas deben cumplir los requisitos de complejidad** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-121">To enforce both the default Windows password filter and the custom password filter, ensure that the **Passwords must meet complexity requirements** policy setting is enabled.</span></span> <span data-ttu-id="8f2b6-122">De lo contrario, deshabilite la configuración de directiva las **contraseñas deben cumplir los requisitos de complejidad** .</span><span class="sxs-lookup"><span data-stu-id="8f2b6-122">Otherwise, disable the **Passwords must meet complexity requirements** policy setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f2b6-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f2b6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f2b6-124">Consideraciones sobre la programación de filtros de contraseña</span><span class="sxs-lookup"><span data-stu-id="8f2b6-124">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="8f2b6-125">Aplicación segura de contraseñas y Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="8f2b6-125">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[<span data-ttu-id="8f2b6-126">Funciones de filtro de contraseñas</span><span class="sxs-lookup"><span data-stu-id="8f2b6-126">Password Filter Functions</span></span>](management-functions.md)
</dt> </dl>

 

 



