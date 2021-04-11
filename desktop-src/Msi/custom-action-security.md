---
description: De forma predeterminada, el instalador ejecuta acciones personalizadas con privilegios de usuario para limitar el acceso de las acciones personalizadas al sistema.
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: Seguridad de la acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7d36e0e5c6cecc61730144fb7efdeed63ba0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361551"
---
# <a name="custom-action-security"></a><span data-ttu-id="78333-103">Seguridad de la acción personalizada</span><span class="sxs-lookup"><span data-stu-id="78333-103">Custom Action Security</span></span>

<span data-ttu-id="78333-104">De forma predeterminada, el instalador ejecuta acciones personalizadas con privilegios de usuario para limitar el acceso de las acciones personalizadas al sistema.</span><span class="sxs-lookup"><span data-stu-id="78333-104">The installer runs custom actions with user privileges by default in order to limit the access of custom actions to the system.</span></span> <span data-ttu-id="78333-105">El instalador puede ejecutar acciones personalizadas con privilegios elevados si se instala una aplicación administrada o si se ha especificado la Directiva del sistema para privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="78333-105">The installer may run custom actions with elevated privileges if a managed application is being installed or if the system policy has been specified for elevated privileges.</span></span>

<span data-ttu-id="78333-106">Debe usar la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) y **msidbCustomActionTypeHideTarget** para evitar el registro de información confidencial utilizada por la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="78333-106">You should use the [**MsiHiddenProperties**](msihiddenproperties.md) property and **msidbCustomActionTypeHideTarget** to prevent logging of sensitive information used by the custom action.</span></span> <span data-ttu-id="78333-107">Para obtener más información sobre **MsidbCustomActionTypeHideTarget** , consulte la [opción de destino oculto de acción personalizada](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="78333-107">For more information about **msidbCustomActionTypeHideTarget** see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

<span data-ttu-id="78333-108">Desactive la propiedad CustomActionData después de establecerla para asegurarse de que los datos confidenciales ya no estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="78333-108">Clear the CustomActionData property after setting it to ensure that sensitive data is no longer available.</span></span> <span data-ttu-id="78333-109">El código de ejemplo siguiente es un fragmento de código usado por una acción personalizada de DLL inmediata que está configurando datos para su uso por una acción personalizada diferida llamada "MyDeferredCA":</span><span class="sxs-lookup"><span data-stu-id="78333-109">Example code below is a snippet used by an immediate DLL custom action that is setting up data for use by a deferred custom action called "MyDeferredCA":</span></span>


```C++
#include <windows.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall MyImmediateCA(MSIHANDLE hInstall)
{
    // set up information for deferred custom action called MyDeferredCA
    const TCHAR szValue[] = TEXT("data");
    UINT uiStat = ERROR_INSTALL_FAILURE;
    if (ERROR_SUCCESS == MsiSetProperty(hInstall, TEXT("MyDeferredCA"), szValue))
    {
        uiStat = MsiDoAction(hInstall, TEXT("MyDeferredCA"));

        // clear CustomActionData property
        if (ERROR_SUCCESS != MsiSetProperty(hInstall, TEXT("MyDeferredCA"), TEXT("")))
            return ERROR_INSTALL_FAILURE;
    }

    return (uiStat == ERROR_SUCCESS) ? uiStat : ERROR_INSTALL_FAILURE;    
}
```



<span data-ttu-id="78333-110">Tenga en cuenta que solo [las acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md) pueden usar el atributo **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="78333-110">Note that only [deferred execution custom actions](deferred-execution-custom-actions.md) can use the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="78333-111">Para obtener más información, consulte [acción personalizada In-Script opciones de ejecución](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="78333-111">For more information see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="78333-112">Si no se establece el bit **msidbCustomActionTypeNoImpersonate** para una acción personalizada, el instalador ejecuta la acción personalizada con privilegios de nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="78333-112">If the **msidbCustomActionTypeNoImpersonate** bit is not set for a custom action, the installer runs the custom action with user-level privileges.</span></span> <span data-ttu-id="78333-113">Para obtener más información, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="78333-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="78333-114">Si se establece el bit **msidbCustomActionTypeNoImpersonate** y se instala una aplicación administrada con permisos de administrador, el instalador puede ejecutar la acción personalizada con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="78333-114">If the **msidbCustomActionTypeNoImpersonate** bit is set and a managed application is being installed with administrator permission, the installer may run the custom action with elevated privileges.</span></span> <span data-ttu-id="78333-115">Sin embargo, si un usuario intenta instalar la aplicación administrada sin permiso de administrador, el instalador ejecuta la aplicación con privilegios de nivel de usuario independientemente de si **msidbCustomActionTypeNoImpersonate** está establecido.</span><span class="sxs-lookup"><span data-stu-id="78333-115">However, if a user attempts to install the managed application without administrator permission, the installer runs the application with user level privileges regardless of whether **msidbCustomActionTypeNoImpersonate** is set.</span></span>

<span data-ttu-id="78333-116">Tenga en cuenta que una acción personalizada se puede ejecutar con privilegios del sistema aunque no se haya establecido el bit **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="78333-116">Note that a custom action may run with system privileges even when the **msidbCustomActionTypeNoImpersonate** bit is not set.</span></span> <span data-ttu-id="78333-117">Esto sucede si un administrador instala la aplicación para todos los usuarios de un servidor que ejecuta el servicio de rol de Terminal Server mediante Windows 2000 y la acción no está marcada con **msidbCustomActionTypeTSAware**.</span><span class="sxs-lookup"><span data-stu-id="78333-117">This occurs if an administrator installs the application for all users on a server running the Terminal Server role service using Windows 2000 and the action is not marked with **msidbCustomActionTypeTSAware**.</span></span> <span data-ttu-id="78333-118">Una acción personalizada también puede ejecutarse con privilegios del sistema si la instalación se invoca cuando no hay ningún contexto de usuario.</span><span class="sxs-lookup"><span data-stu-id="78333-118">A custom action may also run with system privileges if the installation is invoked when there is no user context.</span></span> <span data-ttu-id="78333-119">Por ejemplo, si no hay ningún usuario que haya iniciado sesión actualmente durante una instalación invocada por la implementación de la aplicación 2000 de Windows.</span><span class="sxs-lookup"><span data-stu-id="78333-119">For example, if there is no currently logged-on user during an installation invoked by Windows 2000 Application Deployment.</span></span>

<span data-ttu-id="78333-120">Al crear sus propias acciones personalizadas, debe crear siempre la acción personalizada mediante métodos seguros.</span><span class="sxs-lookup"><span data-stu-id="78333-120">When creating your own custom actions, you should always author the custom action using secure methods.</span></span> <span data-ttu-id="78333-121">Para obtener más información, consulte [directrices para proteger las acciones personalizadas](guidelines-for-securing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="78333-121">For more information, see [Guidelines for Securing Custom Actions](guidelines-for-securing-custom-actions.md).</span></span>

 

 



