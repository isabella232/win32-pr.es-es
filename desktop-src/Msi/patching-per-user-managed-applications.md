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
# <a name="patching-per-user-managed-applications"></a>Aplicación de revisiones para aplicaciones administradas por usuario

A partir de Windows Installer 3,0, es posible aplicar revisiones a una aplicación que se ha instalado en un contexto administrado por el usuario después de haber registrado la revisión como con privilegios elevados.

**Windows Installer 2,0:** No compatible. No se pueden aplicar revisiones a las aplicaciones que se instalan en un contexto administrado por usuario con versiones de Windows Installer anteriores a Windows Installer 3,0.

Una aplicación se instala en el estado administrado por el usuario en los casos siguientes.

-   La instalación por usuario de la aplicación se realizó con la implementación y el [Directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page).
-   La aplicación se ha anunciado a un usuario especificado y se ha instalado mediante el método descrito en el apartado [anunciar una aplicación Per-User que se va a instalar con privilegios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).

Se requieren privilegios para instalar una aplicación en el contexto administrado por el usuario; por lo tanto, el instalador también realiza Windows Installer futuras reinstalaciones o reparaciones de la aplicación con privilegios elevados. Esto significa que solo se pueden aplicar a la aplicación revisiones de orígenes de confianza.

A partir de Windows Installer 3,0, puede aplicar una revisión a una aplicación administrada por usuario después de haber registrado la revisión como con privilegios elevados. Para registrar una revisión como con privilegios elevados, use la función [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) o el método [**SourceListAddSource**](patch-sourcelistaddsource.md) del objeto [**patch**](patch-object.md) , con privilegios elevados. Después de registrar la revisión, puede aplicar la revisión mediante las funciones [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , [**ApplyPatch**](installer-applypatch.md) o [**ApplyMultiplePatches**](installer-applymultiplepatches.md) del [**objeto Installer**](installer-object.md)o la [opción de línea de comandos](command-line-options.md)/p.

> [!Note]
> Se puede registrar una revisión como con privilegios elevados antes de instalar la aplicación. Cuando se ha registrado una revisión, permanece registrada hasta que se quita la última aplicación registrada para esta revisión.
> 
> Las revisiones que se han aplicado a una aplicación administrada por usuario no se pueden quitar sin quitar toda la aplicación. Los registros de revisiones para una aplicación administrada por usuario se quitan en la eliminación de la aplicación.

También puede usar este método para permitir que un usuario no administrador aplique revisiones a una aplicación por equipo, o bien puede usar la aplicación de revisiones con privilegios mínimos descritas en la aplicación de [revisiones de control de cuentas de usuario (UAC)](user-account-control--uac--patching.md).

## <a name="example-1"></a>Ejemplo 1

En el siguiente ejemplo de scripting se usa el método [**SourceListAddSource**](patch-sourcelistaddsource.md) para registrar un paquete de revisión ubicado en \\ \\ Server \\ share \\ Products \\ \\ example. MSP como con privilegios elevados. Esa revisión está lista para aplicarse a un producto administrado por usuario.

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

## <a name="example-2"></a>Ejemplo 2

En el ejemplo de código siguiente se usa la función [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para registrar un paquete de revisión ubicado en \\ \\ Server \\ share \\ Products \\ \\ example. MSP como con privilegios elevados. Esa revisión está lista para aplicarse a un producto administrado por usuario.


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



 

 
