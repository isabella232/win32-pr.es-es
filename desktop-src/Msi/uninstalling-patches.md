---
description: A partir de Windows Installer 3,0, es posible desinstalar algunas revisiones de las aplicaciones.
ms.assetid: 11e995b7-30c7-4992-b436-3af289ac3966
title: Desinstalación de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9418704bdeeb5ccc57839cbe2416faa5692265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279481"
---
# <a name="uninstalling-patches"></a>Desinstalación de revisiones

A partir de Windows Installer 3,0, es posible desinstalar algunas revisiones de las aplicaciones. La revisión debe ser una [revisión](uninstallable-patches.md)que no se puede instalar. Cuando se usa una versión de Windows Installer anterior a la versión 3,0, la [eliminación de revisiones](removing-patches.md) requiere la desinstalación del producto patch y la reinstalación del producto sin aplicar la revisión.

**Windows Installer 2,0:** No compatible. Las revisiones aplicadas mediante una versión de Windows Installer anterior a Windows Installer 3,0 no se pueden desinstalar.

Al invocar una desinstalación de una revisión con cualquiera de los métodos siguientes, el instalador intenta quitar la revisión del primer producto visible para la aplicación o el usuario que solicita la desinstalación. El instalador busca los productos con revisión en el siguiente orden: por equipo administrado por usuario y por equipo sin administrar.

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a>Desinstalación de una revisión mediante MSIPATCHREMOVE en una línea de comandos

Puede desinstalar las revisiones de un comando mediante msiexec.exe y las opciones de la [línea de comandos](command-line-options.md). La siguiente línea de comandos de ejemplo quita una [revisión desinstalable](uninstallable-patches.md), example. MSP, de una aplicación example.msi, mediante la propiedad [**MSIPATCHREMOVE**](msipatchremove.md) y la opción de línea de comandos/i. Al usar/i, la aplicación revisada se puede identificar mediante la ruta de acceso al paquete de la aplicación (archivo. msi) o el [código de producto](product-codes.md)de la aplicación. En este ejemplo, el paquete de instalación de la aplicación se encuentra en " \\ \\ Server \\ share \\ Products \\ example \\example.msi" y la propiedad [**ProductCode**](productcode.md) de la aplicación es "{0C9840E7-7F0B-C648-10F0-4641926FE463}". El paquete de revisión se encuentra en " \\ \\ Server \\ share \\ Products example \\ \\ patches \\ example. MSP" y el GUID del código de revisión es "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".

**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a>Desinstalación de una revisión mediante las opciones de la línea de comandos estándar

A partir de la versión 3,0 de Windows Installer, puede usar las [Opciones de línea de comandos estándar](standard-installer-command-line-options.md) usadas por las actualizaciones del sistema operativo Microsoft Windows (update.exe) para desinstalar Windows Installer revisiones desde una línea de comandos.

La línea de comandos siguiente es el equivalente de línea de comandos estándar de la línea de comandos de Windows Installer que se usa para desinstalar una revisión mediante la propiedad [**MSIPATCHREMOVE**](msipatchremove.md) . La opción/Uninstall que se usa con la opción/Package denota la desinstalación de una revisión. Se puede hacer referencia a la revisión mediante la ruta de acceso completa a la revisión o mediante el GUID del código de la revisión.

**Msiexec/Package {0C9840E7-7F0B-C648-10F0-4641926FE463}/Uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/Passive**

> [!Note]  
> La opción/Passive estándar no es exactamente equivalente a la opción Windows Installer/QB.

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a>Desinstalación de una revisión mediante el método RemovePatches

Puede desinstalar las revisiones del script mediante la interfaz de [automatización](automation-interface.md)de Windows Installer. En el siguiente ejemplo de scripting se quita una [revisión desinstalable](uninstallable-patches.md), example. MSP, de una aplicación example.msi mediante el método [**RemovePatches**](installer-removepatches.md) del objeto [Installer](installer-object.md) . Cada revisión desinstalada se puede representar mediante la ruta de acceso completa al paquete de revisión o el GUID del código de la revisión. En este ejemplo, el paquete de instalación de la aplicación se encuentra en " \\ \\ Server \\ share \\ Products \\ example \\example.msi" y la propiedad [**ProductCode**](productcode.md) de la aplicación es "{0C9840E7-7F0B-C648-10F0-4641926FE463}". El paquete de revisión se encuentra en " \\ \\ Server \\ share \\ Products example \\ \\ patches \\ example. MSP" y el GUID del código de revisión es "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a>Desinstalación de una revisión mediante agregar o quitar programas

Con Windows XP, puede desinstalar revisiones mediante agregar o quitar programas.

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a>Desinstalación de una revisión mediante la función MsiRemovePatches

Las aplicaciones pueden desinstalar las revisiones de otras aplicaciones mediante el uso de las [funciones de Windows Installer](installer-functions.md). En el ejemplo de código siguiente se quita una [revisión desinstalable](uninstallable-patches.md), example. MSP, de una aplicación example.msi, mediante la función [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) . Se puede hacer referencia a una revisión mediante la ruta de acceso completa al paquete de revisión o el GUID del código de la revisión. En este ejemplo, el paquete de instalación de la aplicación se encuentra en " \\ \\ Server \\ share \\ Products \\ example \\example.msi" y la propiedad [**ProductCode**](productcode.md) de la aplicación es "{0C9840E7-7F0B-C648-10F0-4641926FE463}". El paquete de revisión se encuentra en " \\ \\ Server \\ share \\ Products example \\ \\ patches \\ example. MSP" y el GUID del código de revisión es "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a>Desinstalación de una revisión de todas las aplicaciones que usan la función MsiRemovePatches

Una única revisión puede actualizar más de un producto en el equipo. Una aplicación puede utilizar [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para enumerar todos los productos del equipo y determinar si se ha aplicado una revisión a una instancia determinada del producto. A continuación, la aplicación puede desinstalar la revisión mediante [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa). Por ejemplo, una revisión única puede actualizar varios productos si la revisión actualiza un archivo en un componente compartido por varios productos y la revisión se distribuye para actualizar ambos productos.

En el ejemplo siguiente se muestra cómo una aplicación puede usar la Windows Installer para quitar una revisión de todas las aplicaciones que están disponibles para el usuario. No quita la revisión de las aplicaciones instaladas por usuario para otro usuario.


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 300
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>

#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

///////////////////////////////////////////////////////////////////
// RemovePatchFromAllVisibleapplications:
//
// Arguments:
//    wszPatchToRemove - GUID of patch to remove
//
///////////////////////////////////////////////////////////////////
//
UINT RemovePatchFromAllVisibleapplications(LPCWSTR wszPatchToRemove)
{
    if (!wszPatchToRemove)
        return ERROR_INVALID_PARAMETER;

    UINT uiStatus = ERROR_SUCCESS;
    DWORD dwIndex = 0;
    WCHAR wszapplicationCode[cchGUID+1] = {0};

    DWORD dwapplicationSearchContext = MSIINSTALLCONTEXT_ALL;
    MSIINSTALLCONTEXT dwInstallContext = MSIINSTALLCONTEXT_NONE;

    do
    {
        // Enumerate all visible applications in all contexts for the caller.
        // NULL for szUserSid defaults to using the caller's SID
        uiStatus = MsiEnumProductsEx(/*szapplicationCode*/NULL,
         /*szUserSid*/NULL,
         dwapplicationSearchContext,
         dwIndex,
         wszapplicationCode,
         &dwInstallContext,
         /*szSid*/NULL,
         /*pcchSid*/NULL);

        if (ERROR_SUCCESS == uiStatus)
        {
            // check to see if the provided patch is
            // registered for this application instance
            UINT uiPatchStatus = MsiGetPatchInfoEx(wszPatchToRemove,
             wszapplicationCode,
             /*szUserSid*/NULL,
             dwInstallContext,
             INSTALLPROPERTY_PATCHSTATE,
             NULL,
             NULL);

            if (ERROR_SUCCESS == uiPatchStatus)
            {
                // patch is registered to this application; remove patch
                wprintf(L"Removing patch %s from application %s...\n",
                 wszPatchToRemove, wszapplicationCode);
                                
                UINT uiRemoveStatus = MsiRemovePatches(
                 wszPatchToRemove,
                 wszapplicationCode,
                 INSTALLTYPE_SINGLE_INSTANCE,
                 L"");

                if (ERROR_SUCCESS != uiRemoveStatus)
                {
                    // This halts the enumeration and fails. Alternatively
                    // you could output an error and continue the
                    // enumeration
                     return ERROR_FUNCTION_FAILED;
                }
            }
            else if (ERROR_UNKNOWN_PATCH != uiPatchStatus)
            {
                // Some other error occurred during processing. This
                // halts the enumeration and fails. Alternatively you
                // could output an error and continue the enumeration
                 return ERROR_FUNCTION_FAILED;
            }
            // else patch was not applied to this application
            // (ERROR_UNKNOWN_PATCH returned)
        }

        dwIndex++;
    }
    while (uiStatus == ERROR_SUCCESS);

    if (ERROR_NO_MORE_ITEMS != uiStatus)
        return ERROR_FUNCTION_FAILED;

    return ERROR_SUCCESS;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuenciación de revisiones](sequencing-patches.md)
</dt> <dt>

[Quitar revisiones](removing-patches.md)
</dt> <dt>

[Revisiones desinstalables](uninstallable-patches.md)
</dt> <dt>

[Revisión de desinstalación de acciones personalizadas](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



