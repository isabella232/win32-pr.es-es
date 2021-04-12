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
# <a name="uninstalling-patches"></a><span data-ttu-id="6db4d-103">Desinstalación de revisiones</span><span class="sxs-lookup"><span data-stu-id="6db4d-103">Uninstalling Patches</span></span>

<span data-ttu-id="6db4d-104">A partir de Windows Installer 3,0, es posible desinstalar algunas revisiones de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6db4d-104">Beginning with Windows Installer 3.0, it is possible to uninstall some patches from applications.</span></span> <span data-ttu-id="6db4d-105">La revisión debe ser una [revisión](uninstallable-patches.md)que no se puede instalar.</span><span class="sxs-lookup"><span data-stu-id="6db4d-105">The patch must be an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="6db4d-106">Cuando se usa una versión de Windows Installer anterior a la versión 3,0, la [eliminación de revisiones](removing-patches.md) requiere la desinstalación del producto patch y la reinstalación del producto sin aplicar la revisión.</span><span class="sxs-lookup"><span data-stu-id="6db4d-106">When using a Windows Installer version less than version 3.0, [removing patches](removing-patches.md) requires uninstalling the patch product and reinstalling the product without applying the patch.</span></span>

<span data-ttu-id="6db4d-107">**Windows Installer 2,0:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="6db4d-107">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="6db4d-108">Las revisiones aplicadas mediante una versión de Windows Installer anterior a Windows Installer 3,0 no se pueden desinstalar.</span><span class="sxs-lookup"><span data-stu-id="6db4d-108">Patches applied using a version of Windows Installer that is earlier than Windows Installer 3.0 are not uninstallable.</span></span>

<span data-ttu-id="6db4d-109">Al invocar una desinstalación de una revisión con cualquiera de los métodos siguientes, el instalador intenta quitar la revisión del primer producto visible para la aplicación o el usuario que solicita la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="6db4d-109">When you invoke an uninstallation of a patch by any of the following methods, the installer attempts to remove the patch from the first product visible to the application or user requesting the uninstallation.</span></span> <span data-ttu-id="6db4d-110">El instalador busca los productos con revisión en el siguiente orden: por equipo administrado por usuario y por equipo sin administrar.</span><span class="sxs-lookup"><span data-stu-id="6db4d-110">The installer searches for patched products in the following order: per-user managed, per-user unmanaged, per-machine.</span></span>

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a><span data-ttu-id="6db4d-111">Desinstalación de una revisión mediante MSIPATCHREMOVE en una línea de comandos</span><span class="sxs-lookup"><span data-stu-id="6db4d-111">Uninstalling a patch using MSIPATCHREMOVE on a command line</span></span>

<span data-ttu-id="6db4d-112">Puede desinstalar las revisiones de un comando mediante msiexec.exe y las opciones de la [línea de comandos](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="6db4d-112">You can uninstall patches from a command by using msiexec.exe and the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="6db4d-113">La siguiente línea de comandos de ejemplo quita una [revisión desinstalable](uninstallable-patches.md), example. MSP, de una aplicación example.msi, mediante la propiedad [**MSIPATCHREMOVE**](msipatchremove.md) y la opción de línea de comandos/i.</span><span class="sxs-lookup"><span data-stu-id="6db4d-113">The following sample command line removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MSIPATCHREMOVE**](msipatchremove.md) property and the /i command line option.</span></span> <span data-ttu-id="6db4d-114">Al usar/i, la aplicación revisada se puede identificar mediante la ruta de acceso al paquete de la aplicación (archivo. msi) o el [código de producto](product-codes.md)de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6db4d-114">When using /i, the patched application can be identified by the path to the application's package (.msi file) or the application's [product code](product-codes.md).</span></span> <span data-ttu-id="6db4d-115">En este ejemplo, el paquete de instalación de la aplicación se encuentra en " \\ \\ Server \\ share \\ Products \\ example \\example.msi" y la propiedad [**ProductCode**](productcode.md) de la aplicación es "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="6db4d-115">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="6db4d-116">El paquete de revisión se encuentra en " \\ \\ Server \\ share \\ Products example \\ \\ patches \\ example. MSP" y el GUID del código de revisión es "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="6db4d-116">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>

<span data-ttu-id="6db4d-117">**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**</span><span class="sxs-lookup"><span data-stu-id="6db4d-117">**Msiexec /I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE={EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /qb**</span></span>

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a><span data-ttu-id="6db4d-118">Desinstalación de una revisión mediante las opciones de la línea de comandos estándar</span><span class="sxs-lookup"><span data-stu-id="6db4d-118">Uninstalling a patch using the standard command line options</span></span>

<span data-ttu-id="6db4d-119">A partir de la versión 3,0 de Windows Installer, puede usar las [Opciones de línea de comandos estándar](standard-installer-command-line-options.md) usadas por las actualizaciones del sistema operativo Microsoft Windows (update.exe) para desinstalar Windows Installer revisiones desde una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="6db4d-119">Beginning with Windows Installer version 3.0, you can use the [standard command line options](standard-installer-command-line-options.md) used by Microsoft Windows Operating System Updates (update.exe) to uninstall Windows Installer patches from a command line.</span></span>

<span data-ttu-id="6db4d-120">La línea de comandos siguiente es el equivalente de línea de comandos estándar de la línea de comandos de Windows Installer que se usa para desinstalar una revisión mediante la propiedad [**MSIPATCHREMOVE**](msipatchremove.md) .</span><span class="sxs-lookup"><span data-stu-id="6db4d-120">The following command line is the standard command line equivalent of the Windows Installer command line used to uninstall a patch using the [**MSIPATCHREMOVE**](msipatchremove.md) property.</span></span> <span data-ttu-id="6db4d-121">La opción/Uninstall que se usa con la opción/Package denota la desinstalación de una revisión.</span><span class="sxs-lookup"><span data-stu-id="6db4d-121">The /uninstall option used with the /package option denotes the uninstallation of a patch.</span></span> <span data-ttu-id="6db4d-122">Se puede hacer referencia a la revisión mediante la ruta de acceso completa a la revisión o mediante el GUID del código de la revisión.</span><span class="sxs-lookup"><span data-stu-id="6db4d-122">The patch can be referenced by the full path to the patch or by the patch code GUID.</span></span>

<span data-ttu-id="6db4d-123">**Msiexec/Package {0C9840E7-7F0B-C648-10F0-4641926FE463}/Uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/Passive**</span><span class="sxs-lookup"><span data-stu-id="6db4d-123">**Msiexec /package {0C9840E7-7F0B-C648-10F0-4641926FE463} /uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /passive**</span></span>

> [!Note]  
> <span data-ttu-id="6db4d-124">La opción/Passive estándar no es exactamente equivalente a la opción Windows Installer/QB.</span><span class="sxs-lookup"><span data-stu-id="6db4d-124">The /passive standard option is not an exact equivalent of the Windows Installer /qb option.</span></span>

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a><span data-ttu-id="6db4d-125">Desinstalación de una revisión mediante el método RemovePatches</span><span class="sxs-lookup"><span data-stu-id="6db4d-125">Uninstalling a patch using the RemovePatches method</span></span>

<span data-ttu-id="6db4d-126">Puede desinstalar las revisiones del script mediante la interfaz de [automatización](automation-interface.md)de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6db4d-126">You can uninstall patches from script by using the Windows Installer [Automation Interface](automation-interface.md).</span></span> <span data-ttu-id="6db4d-127">En el siguiente ejemplo de scripting se quita una [revisión desinstalable](uninstallable-patches.md), example. MSP, de una aplicación example.msi mediante el método [**RemovePatches**](installer-removepatches.md) del objeto [Installer](installer-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6db4d-127">The following scripting sample removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object.</span></span> <span data-ttu-id="6db4d-128">Cada revisión desinstalada se puede representar mediante la ruta de acceso completa al paquete de revisión o el GUID del código de la revisión.</span><span class="sxs-lookup"><span data-stu-id="6db4d-128">Each patch being uninstalled can be represented by either the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="6db4d-129">En este ejemplo, el paquete de instalación de la aplicación se encuentra en " \\ \\ Server \\ share \\ Products \\ example \\example.msi" y la propiedad [**ProductCode**](productcode.md) de la aplicación es "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="6db4d-129">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="6db4d-130">El paquete de revisión se encuentra en " \\ \\ Server \\ share \\ Products example \\ \\ patches \\ example. MSP" y el GUID del código de revisión es "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="6db4d-130">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a><span data-ttu-id="6db4d-131">Desinstalación de una revisión mediante agregar o quitar programas</span><span class="sxs-lookup"><span data-stu-id="6db4d-131">Uninstalling a patch using Add/Remove Programs</span></span>

<span data-ttu-id="6db4d-132">Con Windows XP, puede desinstalar revisiones mediante agregar o quitar programas.</span><span class="sxs-lookup"><span data-stu-id="6db4d-132">With Windows XP, you can uninstall patches using Add/Remove programs.</span></span>

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a><span data-ttu-id="6db4d-133">Desinstalación de una revisión mediante la función MsiRemovePatches</span><span class="sxs-lookup"><span data-stu-id="6db4d-133">Uninstalling a patch using the MsiRemovePatches function</span></span>

<span data-ttu-id="6db4d-134">Las aplicaciones pueden desinstalar las revisiones de otras aplicaciones mediante el uso de las [funciones de Windows Installer](installer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6db4d-134">Your applications can uninstall patches from other applications by using the [Windows Installer Functions](installer-functions.md).</span></span> <span data-ttu-id="6db4d-135">En el ejemplo de código siguiente se quita una [revisión desinstalable](uninstallable-patches.md), example. MSP, de una aplicación example.msi, mediante la función [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) .</span><span class="sxs-lookup"><span data-stu-id="6db4d-135">The following code example removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function.</span></span> <span data-ttu-id="6db4d-136">Se puede hacer referencia a una revisión mediante la ruta de acceso completa al paquete de revisión o el GUID del código de la revisión.</span><span class="sxs-lookup"><span data-stu-id="6db4d-136">A patch can be referenced by the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="6db4d-137">En este ejemplo, el paquete de instalación de la aplicación se encuentra en " \\ \\ Server \\ share \\ Products \\ example \\example.msi" y la propiedad [**ProductCode**](productcode.md) de la aplicación es "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="6db4d-137">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="6db4d-138">El paquete de revisión se encuentra en " \\ \\ Server \\ share \\ Products example \\ \\ patches \\ example. MSP" y el GUID del código de revisión es "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="6db4d-138">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a><span data-ttu-id="6db4d-139">Desinstalación de una revisión de todas las aplicaciones que usan la función MsiRemovePatches</span><span class="sxs-lookup"><span data-stu-id="6db4d-139">Uninstalling a patch from all applications using MsiRemovePatches function</span></span>

<span data-ttu-id="6db4d-140">Una única revisión puede actualizar más de un producto en el equipo.</span><span class="sxs-lookup"><span data-stu-id="6db4d-140">A single patch can update more than one product on the computer.</span></span> <span data-ttu-id="6db4d-141">Una aplicación puede utilizar [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para enumerar todos los productos del equipo y determinar si se ha aplicado una revisión a una instancia determinada del producto.</span><span class="sxs-lookup"><span data-stu-id="6db4d-141">An application can use [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) to enumerate all the products on the computer and determine whether a patch has been applied to a particular instance of the product.</span></span> <span data-ttu-id="6db4d-142">A continuación, la aplicación puede desinstalar la revisión mediante [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span><span class="sxs-lookup"><span data-stu-id="6db4d-142">The application can then uninstall the patch using [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span> <span data-ttu-id="6db4d-143">Por ejemplo, una revisión única puede actualizar varios productos si la revisión actualiza un archivo en un componente compartido por varios productos y la revisión se distribuye para actualizar ambos productos.</span><span class="sxs-lookup"><span data-stu-id="6db4d-143">For example, a single patch can update multiple products if the patch updates a file in a component that is shared by multiple products and the patch is distributed to update both products.</span></span>

<span data-ttu-id="6db4d-144">En el ejemplo siguiente se muestra cómo una aplicación puede usar la Windows Installer para quitar una revisión de todas las aplicaciones que están disponibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="6db4d-144">The following example demonstrates how an application can use the Windows Installer to remove a patch from all applications that are available to the user.</span></span> <span data-ttu-id="6db4d-145">No quita la revisión de las aplicaciones instaladas por usuario para otro usuario.</span><span class="sxs-lookup"><span data-stu-id="6db4d-145">It does not remove the patch from applications installed per-user for another user.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6db4d-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6db4d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6db4d-147">Secuenciación de revisiones</span><span class="sxs-lookup"><span data-stu-id="6db4d-147">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="6db4d-148">Quitar revisiones</span><span class="sxs-lookup"><span data-stu-id="6db4d-148">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="6db4d-149">Revisiones desinstalables</span><span class="sxs-lookup"><span data-stu-id="6db4d-149">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="6db4d-150">Revisión de desinstalación de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="6db4d-150">Patch Uninstall Custom Actions</span></span>](patch-uninstall-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="6db4d-151">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="6db4d-151">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="6db4d-152">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="6db4d-152">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="6db4d-153">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="6db4d-153">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="6db4d-154">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="6db4d-154">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



