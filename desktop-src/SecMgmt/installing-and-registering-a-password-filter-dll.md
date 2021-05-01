---
description: El archivo DLL de filtro de contraseña de Windows, Passfilt.dll, se ejecuta en el contexto de seguridad de la cuenta del sistema local y le ayuda a filtrar las contraseñas de dominio o de cuenta local.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Instalación y registro de un archivo DLL de filtro de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2e9f93630dc6bdaa5dbcc7e665a6b1cebff0e
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327170"
---
# <a name="installing-and-registering-a-password-filter-dll"></a><span data-ttu-id="aeee4-103">Instalación y registro de un archivo DLL de filtro de contraseña</span><span class="sxs-lookup"><span data-stu-id="aeee4-103">Installing and Registering a Password Filter DLL</span></span>

<span data-ttu-id="aeee4-104">Puede usar el filtro de contraseñas de Windows para filtrar las contraseñas de dominio o de cuenta local.</span><span class="sxs-lookup"><span data-stu-id="aeee4-104">You can use the Windows password filter to filter domain or local account passwords.</span></span> <span data-ttu-id="aeee4-105">Para usar el filtro de contraseña para las cuentas de dominio, instale y registre el archivo DLL en cada controlador de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="aeee4-105">To use the password filter for domain accounts, install and register the DLL on each domain controller in the domain.</span></span>

<span data-ttu-id="aeee4-106">Realice los pasos siguientes para instalar el filtro de contraseña.</span><span class="sxs-lookup"><span data-stu-id="aeee4-106">Perform the following steps to install your password filter.</span></span> <span data-ttu-id="aeee4-107">Puede realizar estos pasos manualmente o escribir un instalador para realizar estos pasos.</span><span class="sxs-lookup"><span data-stu-id="aeee4-107">You can perform these steps manually, or you can write an installer to perform these steps.</span></span> <span data-ttu-id="aeee4-108">Debe ser administrador o pertenecer al grupo de administradores para realizar estos pasos.</span><span class="sxs-lookup"><span data-stu-id="aeee4-108">You need to be an Administrator or belong to the Administrator Group to perform these steps.</span></span>

<span data-ttu-id="aeee4-109">**Para instalar y registrar un archivo DLL de filtro de contraseña de Windows**</span><span class="sxs-lookup"><span data-stu-id="aeee4-109">**To install and register a Windows password filter DLL**</span></span>

1.  <span data-ttu-id="aeee4-110">Copie el archivo DLL en el directorio de instalación de Windows en el controlador de dominio o en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="aeee4-110">Copy the DLL to the Windows installation directory on the domain controller or local computer.</span></span> <span data-ttu-id="aeee4-111">En instalaciones estándar, la carpeta predeterminada es \\ Windows \\ System32.</span><span class="sxs-lookup"><span data-stu-id="aeee4-111">On standard installations, the default folder is \\Windows\\System32.</span></span> <span data-ttu-id="aeee4-112">Asegúrese de crear un archivo DLL de filtro de contraseña de 32 bits para equipos de 32 bits y un archivo DLL de filtro de contraseña de 64 bits para equipos de 64 bits y, a continuación, cópielos en la ubicación adecuada.</span><span class="sxs-lookup"><span data-stu-id="aeee4-112">Make sure that you create a 32-bit password filter DLL for 32-bit computers and a 64-bit password filter DLL for 64-bit computers, and then copy them to the appropriate location.</span></span>
2.  <span data-ttu-id="aeee4-113">Para registrar el filtro de contraseña, actualice la siguiente clave del Registro del sistema:</span><span class="sxs-lookup"><span data-stu-id="aeee4-113">To register the password filter, update the following system registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    <span data-ttu-id="aeee4-114">Si el **valor Paquetes de** notificación *REG_MULTI_SZ* tipo existe, agregue el nombre del archivo DLL a los datos de valor existentes.</span><span class="sxs-lookup"><span data-stu-id="aeee4-114">If the **Notification Packages** value of type *REG_MULTI_SZ* exists, add the name of your DLL to the existing value data.</span></span> <span data-ttu-id="aeee4-115">No sobrescriba los valores existentes y no incluya la extensión .dll.</span><span class="sxs-lookup"><span data-stu-id="aeee4-115">Do not overwrite the existing values, and do not include the .dll extension.</span></span>

    <span data-ttu-id="aeee4-116">Si el **valor Paquetes** de notificación no existe, cándalo, asíézcale el tipo REG_MULTI_SZ y, *a* continuación, especifique el nombre del archivo DLL para los datos de valor.</span><span class="sxs-lookup"><span data-stu-id="aeee4-116">If the **Notification Packages** value does not exist, create it, give it the *REG_MULTI_SZ* type and then specify the name of the DLL for the value data.</span></span> <span data-ttu-id="aeee4-117">No incluya la extensión .dll.</span><span class="sxs-lookup"><span data-stu-id="aeee4-117">Do not include the .dll extension.</span></span>

    <span data-ttu-id="aeee4-118">El **valor Paquetes de** notificación puede agregar varios paquetes.</span><span class="sxs-lookup"><span data-stu-id="aeee4-118">The **Notification Packages** value can add multiple packages.</span></span>

3.  <span data-ttu-id="aeee4-119">Busque la configuración de complejidad de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="aeee4-119">Find the password complexity setting.</span></span>

    <span data-ttu-id="aeee4-120">En Panel de control, haga clic en Rendimiento y mantenimiento, herramientas **administrativas,** haga doble clic en Directiva de seguridad **local,** haga doble clic en Directivas de cuentay, a continuación, haga doble clic en **Directiva de contraseña.** </span><span class="sxs-lookup"><span data-stu-id="aeee4-120">In Control Panel, click **Performance and Maintenance**, click **Administrative Tools**, double-click **Local Security Policy**, double-click **Account Policies**, and then double-click **Password Policy**.</span></span>

4.  <span data-ttu-id="aeee4-121">Para aplicar el filtro predeterminado de contraseñas de Windows y el filtro de contraseña personalizado, asegúrese de que la configuración de directiva Contraseñas debe cumplir **los** requisitos de complejidad está habilitada.</span><span class="sxs-lookup"><span data-stu-id="aeee4-121">To enforce both the default Windows password filter and the custom password filter, ensure that the **Passwords must meet complexity requirements** policy setting is enabled.</span></span> <span data-ttu-id="aeee4-122">De lo contrario, deshabilite **la configuración de directiva Contraseñas debe cumplir los requisitos** de complejidad.</span><span class="sxs-lookup"><span data-stu-id="aeee4-122">Otherwise, disable the **Passwords must meet complexity requirements** policy setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aeee4-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aeee4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aeee4-124">Consideraciones de programación del filtro de contraseñas</span><span class="sxs-lookup"><span data-stu-id="aeee4-124">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="aeee4-125">Aplicación de contraseñas seguras y Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="aeee4-125">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[<span data-ttu-id="aeee4-126">Funciones de filtro de contraseña</span><span class="sxs-lookup"><span data-stu-id="aeee4-126">Password Filter Functions</span></span>](management-functions.md)
</dt> </dl>

 

 



