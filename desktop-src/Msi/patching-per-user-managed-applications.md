---
description: A partir de Windows Installer 3.0, es posible aplicar revisiones a una aplicación que se ha instalado en un contexto administrado por usuario después de que la revisión se haya registrado como con privilegios elevados.
ms.assetid: ebe5f447-9b74-48dc-8192-f2ac90dca490
title: Aplicación de revisiones para aplicaciones administradas por usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516af282dc7f149b86d03192303dc1b3da14416d1a6a22a4f3e716f641777500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979375"
---
# <a name="patching-per-user-managed-applications"></a>Aplicación de revisiones para aplicaciones administradas por usuario

A partir de Windows Installer 3.0, es posible aplicar revisiones a una aplicación que se ha instalado en un contexto administrado por usuario después de que la revisión se haya registrado como con privilegios elevados.

**Windows Installer 2.0:** No se admite. No se pueden aplicar revisiones a las aplicaciones instaladas en un contexto administrado por usuario mediante versiones de Windows Installer anteriores a Windows Installer 3.0.

Una aplicación se instala en el estado administrado por usuario en los casos siguientes.

-   La instalación por usuario de la aplicación se realizó mediante la implementación [y directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page).
-   La aplicación se anunció a un usuario especificado y se instaló mediante el método descrito en Advertising [a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).

Se requieren privilegios para instalar una aplicación en el contexto administrado por usuario. Por lo tanto, el instalador Windows las reinstalaciones o reparaciones del instalador de la aplicación mediante privilegios elevados. Esto significa que solo se pueden aplicar a la aplicación revisiones de orígenes de confianza.

A partir Windows Installer 3.0, puede aplicar una revisión a una aplicación administrada por usuario después de que la revisión se haya registrado como con privilegios elevados. Para registrar una revisión con privilegios elevados, use la función [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) o el método [**SourceListAddSource**](patch-sourcelistaddsource.md) del objeto [**Patch,**](patch-object.md) con privilegios elevados. Después de registrar la revisión, puede aplicar la revisión mediante las funciones [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o [**MsiApplyMultiplePatches,**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) los métodos [**ApplyPatch**](installer-applypatch.md) o [**ApplyMultiplePatches**](installer-applymultiplepatches.md) del objeto installer [**o**](installer-object.md)la opción de línea de comandos [/p](command-line-options.md).

> [!Note]
> Se puede registrar una revisión con privilegios elevados antes de instalar la aplicación. Cuando se ha registrado una revisión, permanece registrada hasta que se quita la última aplicación registrada para esta revisión.
> 
> Las revisiones que se han aplicado a una aplicación administrada por usuario no se pueden quitar sin quitar toda la aplicación. Los registros de revisión de una aplicación administrada por usuario se quitan al quitar la aplicación.

También puede usar este método para permitir que un usuario que no sea administrador pueda aplicar revisiones a una aplicación por máquina, o bien puede usar la aplicación de revisiones con privilegios mínimos que se describe en Revisión de control de cuentas de usuario [(UAC).](user-account-control--uac--patching.md)

## <a name="example-1"></a>Ejemplo 1

En el ejemplo de scripting siguiente se usa el [**método SourceListAddSource**](patch-sourcelistaddsource.md) para registrar un paquete de revisión ubicado en el servidor \\ \\ share products \\ \\ \\ \\ patches example.msp con privilegios elevados. Esa revisión está lista para aplicarse a un producto administrado por usuario.

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

En el ejemplo de código siguiente se usa la función [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para registrar un paquete de revisión ubicado en el servidor \\ \\ share products \\ \\ \\ patches \\ example.msp con privilegios elevados. Esa revisión está lista para aplicarse a un producto administrado por usuario.


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



 

 
