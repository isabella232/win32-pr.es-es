---
description: Una interfaz de usuario personalizada se puede incrustar en el paquete de Windows Installer.
ms.assetid: d037cd8d-9c88-4851-a9da-b2179f53cee6
title: Usar una interfaz de usuario incrustada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f187e50461cfe88adc9c2cabbf8dd8b88ca97a5a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104083613"
---
# <a name="using-an-embedded-ui"></a><span data-ttu-id="184a7-103">Usar una interfaz de usuario incrustada</span><span class="sxs-lookup"><span data-stu-id="184a7-103">Using an Embedded UI</span></span>

<span data-ttu-id="184a7-104">Una interfaz de usuario personalizada se puede incrustar en el paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="184a7-104">A custom user interface can be embedded within the Windows Installer package.</span></span>

<span data-ttu-id="184a7-105">El archivo DLL que contiene la interfaz de usuario personalizada y los archivos de recursos usados por la interfaz de usuario personalizada deben aparecer en la tabla [MsiEmbeddedUI](msiembeddedui-table.md) .</span><span class="sxs-lookup"><span data-stu-id="184a7-105">The DLL file containing the custom UI, and any resource files used by the custom UI, should be listed in the [MsiEmbeddedUI](msiembeddedui-table.md) table.</span></span> <span data-ttu-id="184a7-106">Por ejemplo, esta tabla MsiEmbeddedUI contiene una fila para el archivo DLL que contiene la interfaz de usuario incrustada y una fila para un archivo de mapa de bits que utiliza la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="184a7-106">For example, this MsiEmbeddedUI table contains a row for the DLL file containing the embedded UI and a row for a bitmap file used by the UI.</span></span>

| <span data-ttu-id="184a7-107">MsiEmbeddedUI</span><span class="sxs-lookup"><span data-stu-id="184a7-107">MsiEmbeddedUI</span></span> | <span data-ttu-id="184a7-108">FileName</span><span class="sxs-lookup"><span data-stu-id="184a7-108">FileName</span></span>    | <span data-ttu-id="184a7-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="184a7-109">Attributes</span></span> | <span data-ttu-id="184a7-110">MessageFilter</span><span class="sxs-lookup"><span data-stu-id="184a7-110">MessageFilter</span></span> | <span data-ttu-id="184a7-111">Datos</span><span class="sxs-lookup"><span data-stu-id="184a7-111">Data</span></span>            |
|---------------|-------------|------------|---------------|-----------------|
| <span data-ttu-id="184a7-112">EmbeddedUI</span><span class="sxs-lookup"><span data-stu-id="184a7-112">EmbeddedUI</span></span>    | <span data-ttu-id="184a7-113">embedui.dll</span><span class="sxs-lookup"><span data-stu-id="184a7-113">embedui.dll</span></span> | <span data-ttu-id="184a7-114">3</span><span class="sxs-lookup"><span data-stu-id="184a7-114">3</span></span>          | <span data-ttu-id="184a7-115">201359327</span><span class="sxs-lookup"><span data-stu-id="184a7-115">201359327</span></span>     | <span data-ttu-id="184a7-116">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="184a7-116">\[Binary Data\]</span></span> |
| <span data-ttu-id="184a7-117">CustomBitmap</span><span class="sxs-lookup"><span data-stu-id="184a7-117">CustomBitmap</span></span>  | <span data-ttu-id="184a7-118">custom.bmp</span><span class="sxs-lookup"><span data-stu-id="184a7-118">custom.bmp</span></span>  | <span data-ttu-id="184a7-119">0</span><span class="sxs-lookup"><span data-stu-id="184a7-119">0</span></span>          |               | <span data-ttu-id="184a7-120">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="184a7-120">\[Binary Data\]</span></span> |



 

<span data-ttu-id="184a7-121">El archivo DLL de la interfaz de usuario personalizada, en este ejemplo embedui.dll, debe exportar las funciones *InitializeEmbeddedUI*, *EmbeddedUIHandler* y *ShutdownEmbeddedUI* definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="184a7-121">The custom UI DLL, in this example embedui.dll, should export the user-defined *InitializeEmbeddedUI*, *EmbeddedUIHandler*, and *ShutdownEmbeddedUI* functions.</span></span> <span data-ttu-id="184a7-122">En el código de ejemplo siguiente se muestran estas funciones.</span><span class="sxs-lookup"><span data-stu-id="184a7-122">The following sample code illustrates these functions.</span></span>


```C++
#include <stdio.h>
#include <stdlib.h>
#include <windows.h>
#include <msi.h>
#include <msiquery.h>
#include <Aclapi.h>
#include <strsafe.h>
#pragma comment(lib, "msi.lib")

#define cchGUID 38

int __stdcall InitializeEmbeddedUI(MSIHANDLE hInstall, 
        LPCWSTR szResourcePath, LPDWORD pdwInternalUILevel)
{
    // The hInstall handle is only valid within this function and 
     // can be used to get or set properties. The handle 
    // does not need to be explicitly closed.

    WCHAR szProductCode[cchGUID+1];
    DWORD cchProductCode = ARRAYSIZE(szProductCode);
    UINT uiStat =  MsiGetProperty(hInstall, L"ProductCode",
             szProductCode, &cchProductCode);
    UNREFERENCED_PARAMETER(szResourcePath);

    if (ERROR_SUCCESS != uiStat)
    {
        // The installation should fail.
        return ERROR_INSTALL_FAILURE;
    }

    WCHAR* szReinstall = NULL;
    DWORD cchReinstall = 0;
    uiStat = MsiGetProperty(hInstall, TEXT("REINSTALL"),  
            szReinstall, &cchReinstall);
    if (ERROR_MORE_DATA == uiStat)
    {
        ++cchProductCode; // Add 1 for terminating null character.
        szReinstall = new WCHAR[cchReinstall];
        if (szReinstall)
        {
        uiStat = MsiGetProperty(hInstall, L"REINSTALL", 
                szReinstall, &cchReinstall);
        }
    }
    if (ERROR_SUCCESS != uiStat)
    {
        if (szReinstall != NULL) 
            delete [] szReinstall;
        // This installation should fail.
        return ERROR_INSTALL_FAILURE;
    }

    if (INSTALLSTATE_DEFAULT != MsiQueryProductState(szProductCode))
    {
        if (INSTALLUILEVEL_BASIC == *pdwInternalUILevel)
        {
            // Insert the custom UI used by basic installation here.
        }
        else
        {
            // Insert the custom UI used by full installation here.
        }
    }
    else if (szReinstall && szReinstall[0])
    {
        // Reinstall the UI sequence.
    }
    else
    {
        // This is a maintenance installation. Remove the UI sequence.

        MsiSetProperty(hInstall, TEXT("REMOVE"), TEXT("ALL"));
    }

    if (szProductCode)
        delete [] szReinstall;

    // Setting the internal UI level to none specifies that 
    // no authored UI should run.
    *pdwInternalUILevel = INSTALLUILEVEL_NONE;
    return 0;
}

DWORD __stdcall ShutdownEmbeddedUI()
{
    // ShutdownEmbeddedUI is optional. It can allow the embedded UI 
    // to perform any cleanup. After this call, the embedded UI   
    // should not receive any additional callbacks.
    return 0;
}


INT __stdcall EmbeddedUIHandler(UINT iMessageType, MSIHANDLE hRecord)
{
    // This function is similar to the MsiSetExternalUIRecord callback.
    INSTALLMESSAGE mt;
    UINT uiFlags;
    UNREFERENCED_PARAMETER(hRecord);

    mt = (INSTALLMESSAGE) (0xFF000000 & (UINT) iMessageType);
    uiFlags = 0x00FFFFFF & iMessageType;

    switch (mt)
    {
    case INSTALLMESSAGE_FATALEXIT:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ERROR:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_WARNING:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_FILESINUSE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_RESOLVESOURCE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_USER:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_INFO:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_OUTOFDISKSPACE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ACTIONSTART:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ACTIONDATA:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_PROGRESS:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_SHOWDIALOG:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_COMMONDATA:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_INSTALLSTART:
        {
            // This message is sent when the Install begins.
            // Record contains the ProductName and ProductCode
            return IDOK;
        }
    case INSTALLMESSAGE_INSTALLEND:
        {
            // This message is sent when the Install ends.
            // Record contains the ProductName and ProductCode 
            // and return value of the installation.
            return IDOK;
        }

    default:
        {
            return 0;
        }
    }
}
```



 

 



