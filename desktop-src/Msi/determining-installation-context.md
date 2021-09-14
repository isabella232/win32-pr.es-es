---
description: Una aplicación puede llamar a las funciones MsiEnumProducts o MsiEnumProductsEx para enumerar los productos instalados o anunciados en el sistema.
ms.assetid: 162bda20-0c62-4eac-8c1f-fd107e42c528
title: Determinar el contexto de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24367e2367f845dfef2e4947a32d9dec84d644cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158594"
---
# <a name="determining-installation-context"></a>Determinar el contexto de instalación

Una aplicación puede llamar a las funciones [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) o [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para enumerar los productos instalados o anunciados en el sistema. Esta función puede enumerar todos los productos instalados en el contexto de instalación [por máquina](installation-context.md). Puede enumerar los productos instalados en el contexto por usuario para el usuario actual. La aplicación puede recuperar información sobre el contexto de estos productos mediante una llamada a las funciones [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) [**o MsiGetProductInfo.**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

El Windows puede instalar productos para que se ejecuten con privilegios elevados (sistema) para usuarios que no son administradores. Esto requiere el permiso de un usuario administrador. Un producto que se instala con privilegios elevados se denomina "administrado". Se administran todos los productos instalados por máquina. Los productos instalados por usuario solo se administran si un agente del sistema local realiza un anuncio al suplantar a un usuario. Este es el método utilizado por la implementación de software a través [directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page). Las aplicaciones por usuario instaladas mientras se [establecen las directivas AlwaysInstallElevated](alwaysinstallelevated.md) no se consideran administradas. Mediante una [**llamada a MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda), una aplicación puede comprobar si se administra un producto determinado.

En el ejemplo siguiente se muestra cómo una aplicación determina el contexto mediante [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa), [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)y [**MsiIsProductEneo.**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 200
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>
#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

UINT DetermineContextForAllProducts()
{
    WCHAR wszProductCode[cchGUID+1] = {0};
    WCHAR wszAssignmentType[10] = {0};
    DWORD cchAssignmentType = 
            sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
    DWORD dwIndex = 0;

    DWORD cchProductName = MAX_PATH;
    WCHAR* lpProductName = new WCHAR[cchProductName];
    if (!lpProductName)
    {
        return ERROR_OUTOFMEMORY;
    }

    UINT uiStatus = ERROR_SUCCESS;

    // enumerate all visible products
    do
    {
        uiStatus = MsiEnumProducts(dwIndex,
                          wszProductCode);
        if (ERROR_SUCCESS == uiStatus)
        {
            cchAssignmentType = 
                sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
            BOOL fPerMachine = FALSE;
            BOOL fManaged = FALSE;

            // Determine assignment type of product
            // This indicates whether the product
            // instance is per-user or per-machine
            if (ERROR_SUCCESS == 
                MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_ASSIGNMENTTYPE,wszAssignmentType,&cchAssignmentType))
            {
                if (L'1' == wszAssignmentType[0])
                    fPerMachine = TRUE;
            }
            else
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // determine the "managed" status of the product.
            // If fManaged is TRUE, product is installed managed
            // and runs with elevated privileges.
            // If fManaged is FALSE, product installation operations
            // run as the user.
            if (ERROR_SUCCESS != MsiIsProductElevated(wszProductCode,
                                         &fManaged))
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // obtain the user friendly name of the product
            UINT uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            if (ERROR_MORE_DATA == uiReturn)
            {
                // try again, but with a larger product name buffer
                delete [] lpProductName;

                // returned character count does not include
                // terminating NULL
                ++cchProductName;

                lpProductName = new WCHAR[cchProductName];
                if (!lpProductName)
                {
                    uiStatus = ERROR_OUTOFMEMORY;
                    break;
                }

                uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            }

            if (ERROR_SUCCESS != uiReturn)
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // output information
            wprintf(L" Product %s:\n", lpProductName);
            wprintf(L"\t%s\n", wszProductCode);
                        wprintf(L"\tInstalled %s %s\n", 
                fPerMachine ? L"per-machine" : L"per-user",
                fManaged ? L"managed" : L"non-managed");
        }
        dwIndex++;
    }
    while (ERROR_SUCCESS == uiStatus);

    if (lpProductName)
    {
        delete [] lpProductName;
        lpProductName = NULL;
    }

    return (ERROR_NO_MORE_ITEMS == uiStatus) ? ERROR_SUCCESS : uiStatus;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> <dt>

[**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
</dt> <dt>

[**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)
</dt> <dt>

[Instalación de un paquete con privilegios elevados para un usuario que no es administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
</dt> <dt>

[Anuncio de Per-User aplicación que se va a instalar con privilegios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
</dt> <dt>

[Contexto de instalación](installation-context.md)
</dt> </dl>

 

 
