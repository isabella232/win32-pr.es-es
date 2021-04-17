---
description: A partir de Windows Installer 3,0, es posible aplicar revisiones a una aplicación que se ha instalado en un contexto administrado por el usuario después de haber registrado la revisión como con privilegios elevados.
ms.assetid: ebe5f447-9b74-48dc-8192-f2ac90dca490
title: Aplicación de revisiones para aplicaciones administradas por usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa6a19933e5c8ab409d510d980b8ed634a630e1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105670098"
---
# <a name="patching-per-user-managed-applications"></a><span data-ttu-id="c835f-103">Aplicación de revisiones para aplicaciones administradas por usuario</span><span class="sxs-lookup"><span data-stu-id="c835f-103">Patching Per-User Managed Applications</span></span>

<span data-ttu-id="c835f-104">A partir de Windows Installer 3,0, es posible aplicar revisiones a una aplicación que se ha instalado en un contexto administrado por el usuario después de haber registrado la revisión como con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="c835f-104">Beginning with Windows Installer 3.0, it is possible to apply patches to an application that has been installed in a per-user-managed context after the patch has been registered as having elevated privileges.</span></span>

<span data-ttu-id="c835f-105">**Windows Installer 2,0:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="c835f-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="c835f-106">No se pueden aplicar revisiones a las aplicaciones que se instalan en un contexto administrado por usuario con versiones de Windows Installer anteriores a Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="c835f-106">You cannot apply patches to applications that are installed in a per-user managed context using versions of Windows Installer earlier than Windows Installer 3.0.</span></span>

<span data-ttu-id="c835f-107">Una aplicación se instala en el estado administrado por el usuario en los casos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c835f-107">An application is installed in the per-user-managed state in the following cases.</span></span>

-   <span data-ttu-id="c835f-108">La instalación por usuario de la aplicación se realizó con la implementación y el [Directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span><span class="sxs-lookup"><span data-stu-id="c835f-108">The per-user installation of the application was performed using deployment and [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span></span>
-   <span data-ttu-id="c835f-109">La aplicación se ha anunciado a un usuario especificado y se ha instalado mediante el método descrito en el apartado [anunciar una aplicación Per-User que se va a instalar con privilegios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="c835f-109">The application was advertised to a specified user and installed by the method described in [Advertising a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span></span>

<span data-ttu-id="c835f-110">Se requieren privilegios para instalar una aplicación en el contexto administrado por el usuario; por lo tanto, el instalador también realiza Windows Installer futuras reinstalaciones o reparaciones de la aplicación con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="c835f-110">Privileges are required to install an application in the per-user-managed context; therefore, future Windows Installer reinstallations or repairs of the application are also performed by the installer using elevated privileges.</span></span> <span data-ttu-id="c835f-111">Esto significa que solo se pueden aplicar a la aplicación revisiones de orígenes de confianza.</span><span class="sxs-lookup"><span data-stu-id="c835f-111">This means that only patches from trusted sources can be applied to the application.</span></span>

<span data-ttu-id="c835f-112">A partir de Windows Installer 3,0, puede aplicar una revisión a una aplicación administrada por usuario después de haber registrado la revisión como con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="c835f-112">Beginning with Windows Installer 3.0, you can apply a patch to a per-user managed application after the patch has been registered as having elevated privileges.</span></span> <span data-ttu-id="c835f-113">Para registrar una revisión como con privilegios elevados, use la función [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) o el método [**SourceListAddSource**](patch-sourcelistaddsource.md) del objeto [**patch**](patch-object.md) , con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="c835f-113">To register a patch as having elevated privileges, use the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function or the [**SourceListAddSource**](patch-sourcelistaddsource.md) method of the [**Patch**](patch-object.md) object, with elevated privileges.</span></span> <span data-ttu-id="c835f-114">Después de registrar la revisión, puede aplicar la revisión mediante las funciones [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , [**ApplyPatch**](installer-applypatch.md) o [**ApplyMultiplePatches**](installer-applymultiplepatches.md) del [**objeto Installer**](installer-object.md)o la [opción de línea de comandos](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="c835f-114">After registering the patch, you can apply the patch using the [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) functions, [**ApplyPatch**](installer-applypatch.md) or [**ApplyMultiplePatches**](installer-applymultiplepatches.md) methods of the [**Installer Object**](installer-object.md), or the /p [command-line option](command-line-options.md).</span></span>

> [!Note]
> <span data-ttu-id="c835f-115">Se puede registrar una revisión como con privilegios elevados antes de instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c835f-115">A patch can be registered as having elevated privileges before the application is installed.</span></span> <span data-ttu-id="c835f-116">Cuando se ha registrado una revisión, permanece registrada hasta que se quita la última aplicación registrada para esta revisión.</span><span class="sxs-lookup"><span data-stu-id="c835f-116">When a patch has been registered, it remains registered until the last registered application for this patch is removed.</span></span>
> 
> <span data-ttu-id="c835f-117">Las revisiones que se han aplicado a una aplicación administrada por usuario no se pueden quitar sin quitar toda la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c835f-117">Patches that have been applied to a per-user managed application cannot be removed without removing the entire application.</span></span> <span data-ttu-id="c835f-118">Los registros de revisiones para una aplicación administrada por usuario se quitan en la eliminación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c835f-118">The patch registrations for a per-user managed application are removed on the removal of the application.</span></span>

<span data-ttu-id="c835f-119">También puede usar este método para permitir que un usuario no administrador aplique revisiones a una aplicación por equipo, o bien puede usar la aplicación de revisiones con privilegios mínimos descritas en la aplicación de [revisiones de control de cuentas de usuario (UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="c835f-119">You can also use this method to enable a non-administrator to patch a per-machine application, or you can use least-privilege patching described in [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

## <a name="example-1"></a><span data-ttu-id="c835f-120">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="c835f-120">Example 1</span></span>

<span data-ttu-id="c835f-121">En el siguiente ejemplo de scripting se usa el método [**SourceListAddSource**](patch-sourcelistaddsource.md) para registrar un paquete de revisión ubicado en \\ \\ Server \\ share \\ Products \\ \\ example. MSP como con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="c835f-121">The following scripting sample uses the [**SourceListAddSource**](patch-sourcelistaddsource.md) method to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="c835f-122">Esa revisión está lista para aplicarse a un producto administrado por usuario.</span><span class="sxs-lookup"><span data-stu-id="c835f-122">That patch is then ready to be applied to a per-user managed product.</span></span>

``` syntax
const msiInstallContextUserManaged = 1
const msiInstallSourceTypeNetwork = 1

const PatchCode = "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}"
const UserSid = "S-X-X-XX-XXXXXXXXX-XXXXXXXXX-XXXXXXXXX-XXXXXXX"
const PatchPath = "\\server\share\products\patches\"
const PatchPackageName = "example.msp"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

Set patch = installer.Patch(PatchCode, "", UserSid, msiInstallContextUserManaged)

patch.SourceListAddSource msiInstallSourceTypeNetwork, PatchPath, 0

patch.SourceListInfo("PackageName") = PatchPackageName
```

## <a name="example-2"></a><span data-ttu-id="c835f-123">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="c835f-123">Example 2</span></span>

<span data-ttu-id="c835f-124">En el ejemplo de código siguiente se usa la función [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para registrar un paquete de revisión ubicado en \\ \\ Server \\ share \\ Products \\ \\ example. MSP como con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="c835f-124">The following code sample uses the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="c835f-125">Esa revisión está lista para aplicarse a un producto administrado por usuario.</span><span class="sxs-lookup"><span data-stu-id="c835f-125">That patch is then ready to be applied to a per-user managed product.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif    // UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI
#endif    // _WIN32_MSI

#include <windows.h>
#include <msi.h>


/////////////////////////////////////////////////////////////////
// RegisterElevatedPatch
//
// Purpose: register a patch elevated from a network location
//
// Arguments:
//    wszPatchCode <entity type="ndash"/> GUID of patch to be registered
//    wszUserSid   - String SID that specifies the user account
//    wszPatchPath <entity type="ndash"/> Network location of patch
//    wszPatchPackageName <entity type="ndash"/> Package name of patch
//
/////////////////////////////////////////////////////////////////
UINT RegisterElevatedPatch(LPCWSTR wszPatchCode, 
LPCWSTR wszUserSid, 
LPCWSTR wszPatchPath, 
LPCWSTR wszPatchPackageName)
{
// wszUserSid can be NULL
// when wszUserSid is NULL, register patch for current user
// current user must be administrator
if (!wszPatchCode || !wszPatchPath || !wszPatchPackageName)
    return ERROR_INVALID_PARAMETER;

UINT uiReturn = ERROR_SUCCESS;

uiReturn = MsiSourceListAddSourceEx(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szSource*/ wszPatchPath,
/*dwIndex*/ 0);
if (ERROR_SUCCESS == uiReturn)
{
uiReturn = MsiSourceListSetInfo(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szProperty*/ L"PackageName",
/*szValue*/ wszPatchPackageName);
if (ERROR_SUCCESS != uiReturn)
{
// Function call failed, return error code
    return uiReturn;
}
}
else
{
// Function call failed, return error code
    return uiReturn;
}

return ERROR_SUCCESS;
}


```



 

 
